# Newcomer-Handbook
新人手册

首先欢迎大家加入实验室

实验室的相关信息默认大家已经在飞书文档里面看过了，这里主要是给大家一些要求以及前几周的一些小要求

首先建议大家先通读以下文档，对于以后的学习有很好的帮助

然后是一些小建议：<div style="font: 16px">学好英语！多读英语文献</div>

https://github.com/XiyouMobile/tutorial-basics-for-tech/blob/master/General.md


## 第一周

### 安装并学习使用命令行工具
- windows 下建议使用 fluent terminal + powerShell 或者 wsl
- linux
    + 终端模拟器推荐有:Kitty, WezTerm
    + Shell 推荐有 fish (开箱即用), elvish(适合处理批量任务), NuShell(类似于elvish, 更适合写数据处理)
    + Terminal Session Manager 可以使用 TMUX （历史悠久）,  Zellij （Modern 易用）, 可以根据个人爱好选择
- mac 推荐 iterm2 (Kitty, WezTerm 支持 MacOS)
    + 适用 Linux 的教程都部分适用于 MacOS, 主要不兼容点有 GNU 和 BSD 系工具的不同和 MacOS 没有自带的包管理器导致的安装包命令的不同
    + 包管理器有多种选项, 可以用 homebrew 或者 NixOS 的 NixShell, 两者区别很大, 且打包的目的不同, 可以自己选择

### 学习使用命令行工具（主要针对 linux/mac 系统）

1. 终端上的输入输出: Unix 下用户态程序都有的文件描述符有哪些, 都有什么用；管道是什么, 怎么使用；程序退出的数字代表什么；
2. 使用 Terminal 在文件夹中跳转, 如何操作文件, 怎么组合使用命令来将命令的输出变成文件
3. 环境变量都是什么, 怎么修改, 如何进入 shell 时设置好变量信息, 常用的环境变量有哪些
4. Modern Unix: 如何快速的在文件夹下搜索某个文件的内容：rg(基于文本匹配), ast-grep(基于AST匹配), 如何快速的在文件夹下找到某个文件, 如何编写脚本批量更改多个文件的内容。
5. 尝试租凭服务器搭建自己的网站: Self-Host: Nginx, Hexo, SaaS: Vercel, Cloudflare Pages, AWS

### 有能力的前提下尽可能安装双系统 windows/linux

计算机专业是能够使用纯 Linux 环境, 但是最好能有一个 Windows 的机器来帮助你写报告, 或者不嫌麻烦可以用 Google Docs, Office 365, LaTex(Typst)

## 第二周

### 学习 git
主要学习本地版本控制, 包括 add commit reset 这些基本的操作

### 尝试将代码推送到 github
- 推送至自己的仓库
- 联系组长添加为团队 member 并向团队仓库推送

