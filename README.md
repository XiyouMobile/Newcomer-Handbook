# Newcomer-Handbook
新人手册

首先欢迎大家加入3G实验室, 希望我们能够帮助你接触到更大, 更广阔的世界! 大家一定一定要记住一点, 你的身份Tag不代表你能做什么
你可以做Web, 可以做Server, 可以做Android, 可以做IOS, Everything else.

一定要尝试一些跨领域的内容, Web的可以看看怎么做服务端, 怎么设计数据库, 怎么做Trace, 怎么做部署;
Server的可以看看怎么做CSS, 怎么设计一个复杂的页面结构, 怎么优化产品的打开速度性能;
学习Linux, 学习Database, 学习渲染, 都是能做的.
等等.

你还可以怀揣梦想, 你可以考研, 可以刷绩点申请海外名校, MIT, Standford, UCB, Harvard, Oxford(想要读海外硕博要提前准备)

更大一点的, 你可以去硅谷, 中关村创业;

一定要相信自己能行.

<div style="font: 16px">学好英语！多读英语文献</div>

---

鸡汤结束

实验室的相关信息默认大家已经在飞书文档里面看过了，这里主要是给大家一些要求以及前几周的一些小要求.

首先建议大家先通读以下文档，对于以后的学习有很好的帮助

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

### 学习 git
主要学习本地版本控制, 包括 add commit reset 这些基本的操作

#### 尝试开始使用Github

虽然能够知道这个网站并注册了账号, 但是你可能并不清楚Github到底是用来干什么的, 可以认为是你在进入大厂工作前能接触到的最先进的程序员协作平台, 涵盖了基本日常工作的每一部分.

1. 代码托管
2. 流水线布置, 执行
3. 流水线执行结果托管
4. 项目追踪(Github Project, Github ISSUE, Github Pull Request), 文档(Github Wiki, Github Readme)
...

~有些大厂的代码及流水线基建甚至可能不如Github~

那怎么开始使用Github呢?

要从你自己的需求开始, 比如说, 我想要自己部署一个自己的网站. 

如果是Web组的, 可以去了解什么是Github.io域名, 然后开是看什么是Astro, 什么是Next.JS, 什么是React...

如果是Server的, 可以开始看看有什么Self Host, 然后会接触到什么是Docker, 什么是服务, 什么是Go, 什么是数据库...

...

然后可以开始探索其他内容, 逛Github就像逛街, 在Marker里找一个Topic一个个的看下去, 看大家都在做什么, 用什么, 玩什么.

OK, 到这一步你就自己能学会怎么用Github了, 至于Github Action等其他的附属内容, 便只是后续自己用的内容.

重要的是培养一个认知.

## 第二周: AI 时代, 我可以怎么办

大家应该都已经听说过Claude, OpenAI, QWEN, DeepSeek一类的AI, 可能有少数人用过WindSurf或者Github Copilot, 可能再少点会用过Cursor 再少点用过 Claude Code, 更少的用过Jules.

那这些都跟Agent, AI等理念相关, 这些是什么呢? 我们怎么去拥抱变化呢? 我们再也不会手写代码了吗?

### 尝试用AI

显然, 重要的第一步是, 要有自己的需求, 这是一个产出过剩的社会, 如果没有自己的需求, 很容易陷入迷茫, 可以先从简单的帮助自己再到帮助他人再到从中挣钱.

然后, 很显然, 第二步是想办法尝试一下上述所有的这些内容, 结合自己的需求体会一下他们能够帮你干什么, 比如说上述中的自己搭建一个网站, 部署到Github IO上, 整个操作都可以让QWEN进行指导.
(能用上OpenAI或者Claude会更好)

从中去尝试如何跟LLM交涉

### 学会用AI

在手动尝试了QWEN给出的内容之后, 现在可以尝试现在做好的Agent, Devin, WindSurf, Cursor都可以, 有钱了直接用Claude Code Max也可以(有门槛).

尝试的只给一个基础目标与限制, 根据需求, 比如说, 想要将实验的官网换成Shadcn, 后端架构进行调整, 添加可行的流水线配置, 从Windows切换到Fedora等.

去理解AI的每一步输出以及回馈是怎么做的, 尝试不同的Prompt, 给出更细节的要求.

### 与AI一起工作

在了解了现在的AI Agent的工作方式之后, 可以开始尝试与之前直接开始写代码完全不同的工作方式, 第一步是规划整体的架构, 该怎么写代码, 什么东西要写到什么地方, 该如何进行测试, 该怎么进行测试.

# 需要一直做的事情

认识更具有经验与认知的人, 学习他们的认知培养和思维方式, 当前可以先听一些博客: 硅谷101, 科技早知道, 代码之外, JaneStree, JumpTrading.

# 一些有意思的寻找目前新的技术栈或者海外工作的方式

## Vite, Vitest, OXC 等知名开源项目的官方网站上看Sponsor都是谁

## GitHub Sponsors

## 硅谷有贵人