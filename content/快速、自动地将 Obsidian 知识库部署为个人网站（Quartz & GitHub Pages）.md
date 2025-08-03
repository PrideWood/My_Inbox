---
title: 快速、自动地将 Obsidian 知识库部署为个人网站（Quartz & GitHub Pages）
source: https://mp.weixin.qq.com/s/msmzz543xzfkEyVPG0UWww
tags:
  - 公众号文章
  - 教程
date created: Saturday, August 2nd 2025, 3:27:17 pm
date modified: Sunday, August 3rd 2025, 11:26:16 pm
---
Original 晓浩 *2025 年 07 月 30 日 21:50*

## Obsidian 是一个强大的双链笔记和知识管理工具，许多人使用它来构建自己的“数字花园”或“第二大脑”。当你想将这些知识分享出来时，一个优雅、快速且自动化的发布流程就显得至关重要。

本文将向您介绍一种 **现代且高效的自动化部署方案** ：使用 Quartz 将您的 Obsidian 知识库变为一个美观的静态网站，并借助 GitHub Actions 实现全自动化部署。此方案的核心优势在于 **将您的内容仓库（Obsidian Vault）与网站框架（Quartz）完全隔离** ，并使用 GitHub Pages 推荐的 `GitHub Actions` 作为部署源。

### 核心优势：为何选择此方法？

本方案是对传统插件发布流程（ `obsidian-enveloppe` 或 `digitalgarden` 插件）的一次彻底升级，旨在解决其 **手动操作繁琐** 和 **速度缓慢** 的痛点。

- **全自动发布** ：您只需在 Obsidian 中完成写作并通过 `Obsidian Git` 自动同步。后续所有构建和部署流程均由 GitHub Actions 自动完成，真正实现“写完即走”。并且无需额外安装插件。
- **极致的速度** ：部署在 GitHub 的高速服务器上进行。一个 1GB 的大型知识库，整体构建流程也仅需 4-5 分钟，远胜于本地手动操作十几分钟的漫长等待。
- **稳定可靠** ：告别缓慢且易出错的本地文件差异比对。每次部署都是一次全新的、干净的构建，确保了结果的一致性。
- **位置无关** ：只要能将笔记推送到 GitHub，无论在何处、用何设备，都能更新您的网站。

## 准备工作 (Prerequisites)

在开始之前，您只需要准备好：

- **一个与 GitHub 同步的 Obsidian 知识库** ：您需要已经使用 `Obsidian Git` 插件将您的 Vault 同步到一个 GitHub 仓库（内容仓库），该仓库可以是私有的。
- **一个 GitHub 账户** ：用于托管网站代码和运行自动化流程。

## 第一步：创建 Quartz 网站仓库

1. 访问 Quartz 的官方 GitHub 模板：https://github.com/jackyzha0/quartz/generate
2. 填写您的仓库名称（例如 `my-digital-garden` ），并设置为 **Public (公开)** 。
3. 点击 “Create repository from template”。
4. 将这个新的 **网站仓库 (Site Repo)** 克隆到您的本地电脑。

```
git clone https://github.com/YOUR_USERNAME/my-digital-garden.git
cd my-digital-garden
```

## 第二步：使用 Personal Access Token (PAT) 设置安全访问

我们将创建一个具有严格限制的 PAT，授权网站仓库读取您的私有内容仓库。

1. **生成 Fine-grained PAT**
	在 GitHub `Settings` \> `Developer settings` \> `Personal access tokens` \> `Fine-grained tokens` 页面，点击 `Generate new token` 。
2. **配置 Token**
- **Token name** ： `QUARTZ_CONTENT_ACCESS` 。
	- **Expiration** ：建议 `90 days` 。
	- **Repository access** ：选择 `Only select repositories` ，然后 **只选择您的内容仓库 (Content Repo)** 。
	- **Permissions** ：在 `Repository permissions` 下，找到 `Contents` 并设置为 `Read-only` 。
	- 点击 `Generate token` 。
4. **立即复制生成的 Token！** 它只会出现一次。
5. **在网站仓库中添加 Token 作为 Secret**
- 打开您的 **网站仓库** 的 GitHub 页面，进入 `Settings` \> `Security` \> `Secrets and variables` \> `Actions` 。
	- 点击 `New repository secret` ， **Name** 设为 `ACCESS_TOKEN` ， **Secret** 粘贴您刚刚复制的 PAT。

## 第三步：配置 GitHub Actions 工作流

这是自动化流程的核心。我们将配置工作流来检出内容、清理不必要的文件、构建并部署网站。

1. 在您本地的 **网站仓库** 中，用以下内容 **完全替换**`.github/workflows/deploy.yml` 文件。 （由于微信公众号的排版，下面代码的缩进可能有问题，请自行调整；或从此处下载 https://gist.github.com/h4rvey-g/08b05f94ae94e225b474364322e10ff4 ）
2. **请务必将 `YOUR_USERNAME/YOUR_CONTENT_REPO` 替换为您自己的 GitHub 用户名和内容仓库名称。**
3. **保存文件，然后将这些更改提交并推送到您的 GitHub 网站仓库。**

```
name: Deploy Quartz to GitHub Pages

on:
    schedule:
    # 每6小时运行一次，可以根据需要调整
        - cron:'0 */6 * * *'
    push:
        branches:
      # 当推送到这个分支时触发
            - v4
    workflow_dispatch:# 允许在 GitHub Actions 页面手动触发

permissions:
    contents: read
    pages: write
    id-token: write

concurrency:
    group: "pages"
    cancel-in-progress: true

jobs:
    build:
        runs-on: ubuntu-22.04
        steps:
          - name: Checkout Site Repo
            uses: actions/checkout@v4
            with:
              fetch-depth: 0

          - name: Checkout Content Repo
            uses: actions/checkout@v4
            with:
             repository: YOUR_USERNAME/YOUR_CONTENT_REPO# <-- 修改这里
              token: ${{secrets.ACCESS_TOKEN}}
              path: content

          - name: Clean up content directory
            run: |
              rm -rf content/.git
              rm -rf content/.obsidian
              # 根据需要添加更多要清理的文件/文件夹
              find content -name ".DS_Store" -delete

          - name: Setup Node.js
            uses: actions/setup-node@v4
            with:
              node-version:20
              cache:'npm'

          - name: Install dependencies
            run: npm ci

          - name: Build Quartz
            run: npx quartz build

          - name: Upload Pages Artifact
            uses: actions/upload-pages-artifact@v3
            with:
              path: ./public

# 部署作业：负责将构建好的构件部署到 GitHub Pages
    deploy:
        needs: build
    
        environment:
          name: github-pages
          url: ${{steps.deployment.outputs.page_url}}
      
        runs-on: ubuntu-latest
        steps:
          - name: Deploy to GitHub Pages
            id: deployment
            uses: actions/deploy-pages@v4
```

## 第四步：激活 GitHub Pages 并配置域名

1. 在您的 **网站仓库** 的 GitHub 页面，进入 `Settings` \> `Pages` 。
2. 在 `Build and deployment` 部分，将 `Source` **选择为 `GitHub Actions`** 。
3. 可配置自定义域名。

## 总结

恭喜！您已成功建立一个采用现代 GitHub Pages 部署方案的全自动化个人知识网站。现在，您的工作流程被简化到了极致：

1. **在 Obsidian 中写作和修改笔记。**
2. **使用 Obsidian Git 插件提交并推送到您的私有内容仓库。**
3. **GitHub Actions 会在几分钟内自动为您完成网站的更新和部署。**

这个架构不仅实现了内容与形式的分离，还采用了 GitHub 官方推荐的部署方式，并提供了极致的速度和便利性，让您可以完全专注于知识的创作与分享。

![Image](https://mp.weixin.qq.com/s/www.w3.org/2000/svg'%20xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg%20stroke='none'%20stroke-width='1'%20fill='none'%20fill-rule='evenodd'%20fill-opacity='0'%3E%3Cg%20transform='translate(-249.000000,%20-126.000000)'%20fill='%23FFFFFF'%3E%3Crect%20x='249'%20y='126'%20width='1'%20height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)
