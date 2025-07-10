## 🪴 Get Started

Quartz requires **at least [Node](https://nodejs.org/) v22** and `npm` v10.9.2 to function correctly. Ensure you have this installed on your machine before continuing.

Then, in your terminal of choice, enter the following commands line by line:

```
git clone https://github.com/jackyzha0/quartz.gitcd quartznpm inpx quartz create
```

This will guide you through initializing your Quartz with content. Once you’ve done so, see how to:

1. [Writing content](https://quartz.jzhao.xyz/authoring-content) in Quartz
2. [Configure](https://quartz.jzhao.xyz/configuration) Quartz’s behaviour
3. Change Quartz’s [layout](https://quartz.jzhao.xyz/layout)
4. [Build and preview](https://quartz.jzhao.xyz/build) Quartz
5. Sync your changes with [GitHub](https://quartz.jzhao.xyz/setting-up-your-GitHub-repository)
6. [Host](https://quartz.jzhao.xyz/hosting) Quartz online

If you prefer instructions in a video format you can try following Nicole van der Hoeven’s [video guide on how to set up Quartz!](https://www.youtube.com/watch?v=6s6DT1yN4dw&t=227s)



# 一级标题



## 二级标题



### 三级标题



| 第一列 | 第二列 | 第三列 |
| ------ | ------ | ------ |
| 1      | 2      | 3      |



这是公式
$$ρ=\frac{m}{V}$$



这是Callout

> [!note] 正分数指数幂
> 给定正数 $a$ 和正整数 $m,n（n>1,且m,n互素)$，若存在唯一的正数 $b$，使得 $b^n=a^m$，则称 $b\ 为\ a\ 的\frac{m}{n}次幂$，记作 $b=a^{\frac{m}{n}}$



下面是mermaid

```mermaid
graph LR
A[直线与直线平行]
B[直线与平面平行]
C[平面与平面平行]

A --判定--> B
B --性质--> A
B --判定--> C
C --> B
C --性质--> A
```