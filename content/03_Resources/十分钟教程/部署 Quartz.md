---
date created: 2025-07-11T18:58:04+08:00
date modified: 2025-07-20T17:14:25+08:00
tags:
  - 软件设置
---

## Official Guide

Quartz requires **at least [Node](https://nodejs.org/) v22** and `npm` v10.9.2 to function correctly. Ensure you have this installed on your machine before continuing.

Then, in your terminal of choice, enter the following commands line by line:

```sh
git clone https://github.com/jackyzha0/quartz.git
cd quartz
npm i
npx quartz create
```

This will guide you through initializing your Quartz with content. Once you’ve done so, see how to:

1. [Writing content](https://quartz.jzhao.xyz/authoring-content) in Quartz
2. [Configure](https://quartz.jzhao.xyz/configuration) Quartz’s behaviour
3. Change Quartz’s [layout](https://quartz.jzhao.xyz/layout)
4. [Build and preview](https://quartz.jzhao.xyz/build) Quartz
5. Sync your changes with [GitHub](https://quartz.jzhao.xyz/setting-up-your-GitHub-repository)
6. [Host](https://quartz.jzhao.xyz/hosting) Quartz online

If you prefer instructions in a video format you can try following Nicole van der Hoeven’s [video guide on how to set up Quartz!](https://www.youtube.com/watch?v=6s6DT1yN4dw&t=227s)

关键点：**网络通畅**！！！

---

## Basic Custom Settings

基础设置都在 quartz.config.ts 中 

### 修改字体和名称

```ts
pageTitle: "DCBJ",  // line 11
body: "Noto Serif SC",  // line 27
```

### iOS 添加到桌面后的图标、全屏

图片的存放位置都在 quartz/static 下

- quartz-static 里的==图标==，要保持名称与原来一致
- 添加到 iOS 桌面自动生成图标代码、==全屏==显示

在 quartz/components/head.tsx 中添加 `apple-touch-icon` 以便在 iOS 设备上显示自定义图标。将其添加到 `<head>` 标签内的其他 `<link>` 元素旁边

在 `const iconPath = joinSegments(baseDir, "static/icon.png")` 下一行添加：

```ts
const appleIconPath = joinSegments(baseDir, "static/apple-touch-icon.png")
```

在 `<link rel="icon" href={iconPath} />` 下一行添加：

```ts
 <link rel="apple-touch-icon" href={appleIconPath} />
```

在 ` <meta name="generator" content="Quartz" />` 之后添加：

```ts
<meta name="apple-mobile-web-app-capable" content="yes" />
<meta name="apple-mobile-web-app-status-bar-style" content="black-translucent" />
<meta name="apple-mobile-web-app-title" content={title} />
```

### ==页脚==内容在 layout.ts footer 部分

```ts
links: {
  GitHub: "https://github.com/PrideWood",
  "douban": "https://www.douban.com/people/PW2018",
  "bilibili": "https://space.bilibili.com/28065777",
```

### 更改 ==index 显示的标题==，在 yaml 中写入

```yaml
---
title: Welcome to DCBJ
description: 分享我的学习笔记与探索
publish: true
---
```

- 更改字体颜色也在 quartz.config.ts 中，不过要搞清楚 color 下面各种颜色的命名分别对应哪部分文字，需要在 quartz-styles-base.scss 中搞清楚，可以在初期进行测试，如果已经部署好了不要轻易改变

### 添加 svg 图片到 404 页面中

在 [undraw](https://undraw.co/search) 中找到心仪的图片并下载，重命名（如“404-illustration.svg”）后存放在 quartz/static 文件夹中

找到 quartz/components/pages/404.tsx，在 `<h1>404</h1>` 下添加

```tsx
  <img
	src="static/404-illustration.svg"
	alt="Not found illustration"
	style={{
	  maxWidth: "200px",
	  width: "100%",
	  margin: "2rem 0",
	  display: "block"
	}}
  />
```