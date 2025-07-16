---
date created: 2025-07-16T09:32:28+08:00
date modified: 2025-07-16T09:33:17+08:00
tags:
  - 软件设置
---
# 💡 Windows 技巧：让任何软件开机自启

很多人每天开机第一件事就是点开好几个常用软件。  
其实，Windows 自带的==任务计划程序==就能帮你自动打开：

## 🚀 设置步骤（以 Obsidian 为例）

1. 打开【任务计划程序】（Win+S 搜索即可）；

![step1.png](https://img.dacnote.cn/images/202507/step1.png)

2. 点击【创建任务】；

![step2.png](https://img.dacnote.cn/images/202507/step2.png)

3. 【常规】页：
	- 任务名任意（如“启动 Obsidian”）
	- 勾选【使用最高权限运行】

![step3.png](https://img.dacnote.cn/images/202507/step3.png)

4. 【触发器】页：
	- 新建触发器 → 设置为“登录时”启动；
	- 推荐：设置“延迟 5 秒”启动，更丝滑；

![step4.png](https://img.dacnote.cn/images/202507/step4.png)

![step5.png](https://img.dacnote.cn/images/202507/step5.png)

5. 【操作】页：
   - 新建操作 → 浏览选择你的 `.exe` 文件路径；

![step6.png](https://img.dacnote.cn/images/202507/step6.png)

![step7.png](https://img.dacnote.cn/images/202507/step7.png)

保存后，开机即自动执行，无需手动操作！

## 🧹 取消方法

不想用了？只需：

- 打开【任务计划程序】；
- 找到任务 → 右键【禁用】或【删除】。

## 🧠 Tips

- 几乎所有你常用的软件都可以使用此方法；
- 想顺序启动多个程序？设置多个任务，错开几秒启动更加流畅；
- 截图步骤⑦中下拉列表中最小值为 30 秒，设置其他值则需要输入数字和单位；
- 找不到软件路径，右键点击桌面上软件的快捷方式 - 打开文件所在的位置。

快去动手试一试吧，遇到问题求助一下 AI。
