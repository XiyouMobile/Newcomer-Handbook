# Newcomer-Handbook
新人手册

首先欢迎大家加入3G实验室, 希望我们能够帮助你接触到更大, 更广阔的世界! 大家一定一定要记住一点, 你的身份Tag不代表你能做什么
你可以做Web, 可以做Server, 可以做Android, 可以做IOS, Everything else.

一定要尝试一些跨领域的内容, Web的可以看看怎么做服务端, 怎么设计数据库, 怎么做Trace, 怎么做部署;
Server的可以看看怎么做CSS, 怎么设计一个复杂的页面结构, 怎么优化产品的打开速度性能;
学习Linux, 学习Database, 学习渲染, 都是能做的.
等等.

你还可以怀揣梦想, 你可以考研, 可以刷绩点申请海外名校, MIT, Stanford, UCB, Harvard, Oxford(想要读海外硕博要提前准备)

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

### Git与GitHub进阶：所谓大厂搬砖姿势与“懒人必备”CI/CD

行了行了，Git基础命令 `add commit push` 你已经玩溜了，GitHub账号也注册了，是不是感觉已经可以指点江山，拳打南山敬老院，脚踢北海幼儿园了？少年，图样图森破啊！在大厂里，Git和GitHub可不仅仅是代码备份工具，那是咱程序员的“瑞士军刀”和“社交平台”（雾）。想知道硅谷码农们是怎么用Git协同“搬砖”，以及如何让机器替你干那些重复的脏活累活吗？来，老司机带你发车！

#### 大厂Git骚操作：优雅地和队友“同床异梦”

在Google、Meta这种“宇宙厂”，几百上千号人同时开发一个项目是家常便饭。这时候，你要是还只会 `git push origin master`，那你离被“优化”也就不远了。

*   **分支策略 (Branching Strategy) - 你走你的阳关道，我过我的独木桥，最后还得殊途同归:**
    *   **Gitflow Workflow:** 想象一下，`master` (或 `main`) 分支是已经上线的、闪闪发光的正式版产品，轻易不敢动。`develop` 分支是大家合并代码的“大本营”，新功能都在这里集结。你要开发个新功能？从 `develop` 拉个 `feature/你的功能名` 分支，自己捣鼓去吧，不影响别人。功能好了，再合并回 `develop`。要发版了？从 `develop` 拉个 `release/版本号` 分支，专门修复Bug、准备上线。万一线上版本出了紧急Bug？赶紧从 `master` 拉个 `hotfix/救火队员` 分支修复，然后合并回 `master` 和 `develop`。是不是听着就头大？别怕，这套流程虽然复杂，但条理清晰，适合有严格版本发布周期的项目。
    *   **Trunk-Based Development (TBD) - 天天上线，主打一个“快”:** 简单粗暴，大部分人都直接在主干 (`main` 或 `master`) 上干活。提交要小而频繁，而且必须有**特性开关 (Feature Flags)** 兜底——新功能先藏起来，等稳定了再放出来给用户看。这种玩法对自动化测试要求极高，不然分分钟玩崩。但好处是集成快，交付快，很受推崇“敏捷”的公司喜欢。
    *   **GitHub Flow - 轻量级选手，小步快跑:** `main` 分支永远是“可部署”的状态。想加新功能？从 `main` 拉个 `feature` 分支。写完了，提个 Pull Request (PR)，让大佬们瞅瞅，没问题就合并回 `main`，然后“一键部署”。简单直接，很多中小型项目或者追求快速迭代的团队都爱用。

*   **代码评审 (Code Review) - “线上裸奔”前的最后一道防线:**
    *   你的代码写得再牛，也得让别人瞅瞅。在大厂，几乎所有代码（尤其要合并到主分支的）都得经过至少一个同事的“法眼”。
    *   一般通过 Pull Request (PR) 或 Merge Request (MR) 进行。你的队友会像玩“大家来找茬”一样，检查你的代码逻辑、可读性、性能、安全性，以及有没有遵守团队的“黑话”（编码规范）。
    *   别怕被喷，大佬们都是为了你好（顺便秀一下自己的存在感）。虚心接受，认真修改，直到你的PR被打上“Approved”标签，你就可以长舒一口气了。

*   **提交规范 (Commit Message Conventions) - 让你的“犯罪记录”清晰可查:**
    *   `git commit -m "update"` 这种提交信息，在大厂是要被拉出来“祭天”的。Commit Message是你留给后人（包括几个月后的你自己）的“时光胶囊”，必须言简意赅，信息量大。
    *   推荐使用 **Conventional Commits** 规范，格式一般是 `类型(范围): 简短描述`，比如 `feat(login): add multi-factor authentication` (新功能：登录模块增加两步验证) 或者 `fix(cart): prevent negative quantity in shopping cart (closes #123)` (修复Bug：购物车模块阻止商品数量为负，并关闭了123号问题单)。
    *   这样做的好处多多：一眼就知道这次提交干了啥，方便追溯历史，还能自动生成项目更新日志 (CHANGELOG)。是不是很酷？

*   **版本控制与协作 - 优雅地“合并”与“变基”:**
    *   `git pull` 和 `git push` 只是基本操作。当多个人修改了同一个文件的同一部分，就会产生“合并冲突 (Merge Conflicts)”。别慌，这是Git在提醒你：“老铁，你俩想到一块儿去了，快商量下听谁的！”手动解决冲突，然后 `git add` 再 `git commit` 就行。
    *   `git rebase -i` (交互式变基) 是个神仙命令，可以在你把本地分支推送到远程前，把你的提交历史“梳理”得干干净净、漂漂亮亮，强迫症患者福音。不过，**千万别对已经推送到公共分支的代码进行 `rebase`**，否则你的队友会提刀来见你。

*   **保持代码质量 - “机器人”比你更懂代码:**
    *   除了靠人眼评审，大厂还会用一堆自动化工具来保证代码质量，比如用 Linters (代码风格检查器) 规范格式，用单元测试、集成测试验证功能。这些检查通常会在你提交PR后，由 CI (持续集成) 系统自动跑起来。要是挂了，你的PR页面上会亮起红灯，那就乖乖回去改Bug吧。

#### CI/CD 与 GitHub Actions - 让机器替你“996”

每次写完代码，都要手动编译、测试、打包、部署？太Low了！在讲究效率的今天，这些重复性工作必须交给机器。这就是 CI/CD 大显身手的时候了。

##### 什么是 CI/CD？听着高大上，其实就是“自动化一条龙”

*   **CI (Continuous Integration - 持续集成):** 想象一下，你和你的队友们都在疯狂写代码。每当有人把代码推到共享仓库（比如 `develop` 分支），CI系统就会自动把最新的代码拉下来，编译构建，然后跑一遍自动化测试。如果一切OK，绿灯行；如果挂了，红灯警告，赶紧修复。**核心思想：早发现，早治疗。** 避免了等到项目快上线了，才发现一堆代码合并不了，或者各种隐藏Bug集中爆发的“惊喜”。

*   **CD (Continuous Delivery/Deployment - 持续交付/持续部署):**
    *   **持续交付 (Continuous Delivery):** 在CI的基础上更进一步。当代码通过了所有自动化测试后，系统会自动把它部署到一个类似“预发布”或“测试”的环境。这意味着，你的产品随时都是“可发布”状态，只差最后一步人工确认，就能推给真实用户。
    *   **持续部署 (Continuous Deployment):** 最激进的玩法。只要代码通过了所有测试，就**直接、自动**部署到生产环境，用户马上就能用到最新的功能。听起来是不是很刺激？这对自动化测试的覆盖率和可靠性要求极高，一般只有对自己团队和流程非常有信心的公司才敢这么玩。

##### CI/CD 的存在意义？简单说，就是“多快好省”还“稳”

*   **自动化大法好:** 机器干活，又快又准，还不用发工资，不像某些人类同事，改个Bug能引入仨新的。
*   **快速反馈，早死早超生:** 代码一提交，几分钟就知道有没有问题。Bug越早发现，修复成本越低。
*   **质量杠杠滴:** 自动化测试覆盖，每次提交都测一遍，想引入低级错误都难。
*   **交付快到飞起:** 以前可能几周甚至几个月才发一个版本，现在一天发几十次都洒洒水啦。用户开心，老板也开心。
*   **妈妈再也不用担心我上线出事故了:** 小步快跑，每次只更新一点点，就算出问题，影响范围也小，回滚也快。

##### GitHub Actions 入门 - GitHub “全家桶”里的免费CI/CD神器

GitHub Actions 是 GitHub 自带的CI/CD工具，免费（大部分情况下够用），而且跟GitHub仓库无缝集成，配置起来也相对简单。你可以在你的仓库里定义一些工作流程 (workflows)，比如当代码 `push` 或者有人提 `Pull Request` 的时候，自动执行编译、测试、部署等操作。

工作流程写在项目根目录下的 `.github/workflows` 文件夹里，用的是 YAML 格式。

**举个栗子：Node.js 项目自动测试**

假设你的Node.js项目用 `npm test` 跑测试，你想在每次往 `main` 分支 `push` 代码，或者有人往 `main` 分支提PR的时候，自动跑一遍测试。可以这样写一个 `ci.yml`：

```yaml
# .github/workflows/ci.yml

name: Node.js CI # 工作流叫啥名，你说了算

on: # 啥时候触发？
  push: # 当有代码push的时候
    branches: [ main ] # 并且是push到main分支
  pull_request: # 或者当有Pull Request的时候
    branches: [ main ] # 并且是针对main分支的PR

jobs: # 要干哪些活？
  build: # 第一个活，叫build（你也可以叫别的）
    runs-on: ubuntu-latest # 用啥系统跑？最新的Ubuntu虚拟机，安排！

    strategy: # 跑测试的策略
      matrix: # 可以定义一个矩阵，跑多个版本
        node-version: [18.x, 20.x] # 比如在Node.js 18和20版本下都跑一遍

    steps: # 具体步骤
    - name: Checkout repository # 第一步：先把代码从仓库拉下来
      uses: actions/checkout@v3 # 用官方的checkout动作，版本号是v3

    - name: Use Node.js ${{ matrix.node-version }} # 第二步：安装指定版本的Node.js
      uses: actions/setup-node@v3 # 用官方的setup-node动作
      with: # 带上参数
        node-version: ${{ matrix.node-version }} # Node版本用上面矩阵里定义的
        cache: 'npm' # 顺便把npm的依赖缓存一下，下次跑得快

    - name: Install dependencies # 第三步：装依赖
      run: npm ci # 用npm ci装，比npm install更稳，CI环境推荐

    - name: Run tests # 第四步：跑测试！
      run: npm test # 执行你的测试命令
```

**解读一下上面的“咒语”:**

*   `name`: 工作流的名字，显示在GitHub Actions页面上。
*   `on`: 触发条件。这里是 `push` 到 `main` 分支，或者有 `pull_request` 到 `main` 分支时触发。
*   `jobs`: 工作流可以包含一个或多个“作业”。
    *   `build`: 这个作业的名字（ID）。
    *   `runs-on`: 指定作业运行在什么环境，`ubuntu-latest` 就是最新的Ubuntu。GitHub还提供Windows和macOS环境。
    *   `strategy.matrix.node-version`: 定义了一个“构建矩阵”。这段代码会让整个作业在Node.js 18.x和20.x两个版本下各跑一次。想支持更多版本？往列表里加就行。
    *   `steps`: 作业里的一系列步骤，按顺序执行。
        *   `uses: actions/checkout@v3`: `uses` 关键字表示使用一个别人写好的“动作”(Action)。`actions/checkout@v3` 是官方提供的，用来把你的仓库代码下载到虚拟机里。
        *   `uses: actions/setup-node@v3`: 官方的安装Node.js的动作。`with` 用来传递参数。
        *   `run: npm ci`: `run` 关键字表示直接执行一个shell命令。
        *   `run: npm test`: 执行测试命令。

只要你把这个文件放到 `.github/workflows/ci.yml`，每次满足触发条件，GitHub就会自动帮你跑这些步骤。你可以在仓库的 "Actions" 标签页看到执行情况，成功了是绿色对勾，失败了是红色叉叉，点进去还能看详细日志。

GitHub Actions 的能耐远不止这些，比如：

*   自动给新提的 Issue 打上标签。
*   项目发新版 (Release) 的时候，自动打包并发布到 npm。
*   每天定时跑个脚本，检查一下依赖库有没有安全漏洞。
*   如果你写的是静态网站，可以自动部署到 GitHub Pages。

总之，拥抱 GitHub Actions，让重复劳动见鬼去吧！把时间花在更有创造性的事情上，比如...呃...刷知乎？（手动狗头）

好了，关于大厂Git玩法和CI/CD的“黑话”就先科普到这。赶紧动手试试，把你的项目也武装起来吧！记住，工具是死的，人是活的，怎么用才能最大化摸鱼...啊不，是提升效率，就看你的悟性了！

## 第二周: AI 时代, 我可以怎么办

大家应该都已经听说过Claude, OpenAI, QWEN, DeepSeek一类的AI, 可能有少数人用过WindSurf或者Github Copilot, 可能再少点会用过Cursor 再少点用过 Claude Code, 更少的用过Jules.

那这些都跟Agent, AI等理念相关, 这些是什么呢? 我们怎么去拥抱变化呢? 我们再也不会手写代码了吗?

### 尝试用AI

显然, 重要的第一步是, 要有自己的需求, 这是一个产出过剩的社会, 如果没有自己的需求, 很容易陷入迷茫, 可以先从简单的帮助自己再到帮助他人再到从中挣钱.

然后, 很显然, 第二步是想办法尝试一下上述所有的这些内容, 结合自己的需求体会一下他们能够帮你干什么, 比如说上述中的自己搭建一个网站, 部署到Github IO上, 整个操作都可以让QWEN进行指导.
(能用上OpenAI或者Claude会更好)

从中去尝试如何跟LLM交涉.

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

硅谷的门槛最高的拉到投资的途径是: 同学.

你在Stanford读了个夜校, 你旁边坐了一位Zoom的二号员工, 你跟他关系比较好, 后来你想创业, 他给你介绍了一个熟人, 你跟这个熟人聊了聊, 当天你就拿到了200万美金的投资.

然后你做了一个月, 感觉IDEA不太行, 回头再找了熟人, 他说没关系, 你可以再试试, 又给你打了200万美金.

---
(For details on the website setup and local development, see [DEV_GUIDE.md](./DEV_GUIDE.md).)