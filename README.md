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

### Git与GitHub进阶：大厂工作流与CI/CD实践

在掌握了Git的基础操作和GitHub的初步使用后，我们来看看在大型科技公司（通常称为“大厂”）中，这些工具是如何深度融入日常开发流程的，以及如何通过CI/CD和GitHub Actions提升开发效率和软件质量。

#### 大厂日常Git工作流

在大型科技公司（通常称为“大厂”）中，Git 是日常开发的核心工具。以下是一些常见的使用场景和实践：

*   **分支策略 (Branching Strategy):**
    *   **Gitflow Workflow:** 这是一个相对复杂但功能完善的分支模型，包含 `master` (或 `main`)、`develop`、`feature/*`、`release/*` 和 `hotfix/*` 等分支。`feature` 分支用于开发新功能，`develop` 是集成分支，`release` 用于准备发布，`master` 代表生产环境的稳定代码，`hotfix` 用于快速修复生产问题。这种模式适合有明确版本发布周期的项目。
    *   **Trunk-Based Development (TBD):** 开发者直接在主干分支（通常是 `main` 或 `master`）上进行小批量、频繁的提交。为了避免破坏主干，通常会结合特性开关（Feature Flags/Toggles）和强大的自动化测试。这种模式有利于持续集成和快速交付。
    *   **GitHub Flow:** 一个更简单的模型，`main` 分支始终是可部署的。开发新功能时，从 `main` 创建 `feature` 分支，完成后通过 Pull Request (PR) 合并回 `main`。合并后立即部署。

*   **代码评审 (Code Review):**
    *   所有代码变更（尤其是合并到 `develop` 或 `main` 分支的）都必须经过代码评审。
    *   通过 Pull Requests (PRs) 或 Merge Requests (MRs) 进行。团队成员会检查代码的正确性、可读性、性能、安全性以及是否符合编码规范。
    *   评审者会提出修改建议，开发者根据反馈修改代码，直到获得批准。

*   **提交规范 (Commit Message Conventions):**
    *   清晰、规范的 Commit Message 至关重要。常见的规范有 Conventional Commits。
    *   一个好的 Commit Message 通常包括一个简短的摘要（类型 + 主题），以及可选的详细描述和关联的 Issue ID。例如: `feat: add user login functionality` 或 `fix: resolve issue with cart calculation (closes #123)`.
    *   这有助于理解代码变更历史、自动化生成 CHANGELOG，以及更容易地进行代码回溯。

*   **版本控制与协作:**
    *   Git 使得多人协作开发更为高效。开发者可以在本地独立工作，然后通过 `push` 和 `pull` (或 `fetch` + `merge`/`rebase`) 与远程仓库同步代码。
    *   解决合并冲突 (Merge Conflicts) 是常见操作，需要仔细处理以确保代码的正确性。
    *   `git rebase -i` (交互式变基) 常用于在合并前整理提交历史，使其更线性、清晰。

*   **保持代码质量:**
    *   除了代码评审，还会结合自动化工具，如静态代码分析 (Linters)、单元测试、集成测试等，确保在代码合并前发现潜在问题。
    *   这些检查通常会在 CI (Continuous Integration) 流水线中自动执行。

#### CI/CD 与 GitHub Actions

#### 什么是 CI/CD?

CI/CD 是持续集成 (Continuous Integration) 和持续交付/持续部署 (Continuous Delivery/Continuous Deployment) 的简称。这是一套在应用开发阶段引入自动化来频繁向客户交付应用的方法。

*   **持续集成 (CI):** 开发人员会定期将其代码变更合并到中央代码仓库中，之后自动化构建和测试流程会自动运行。CI 的主要目标是更快地发现并解决缺陷，提高软件质量，并缩短验证和发布新软件更新所需的时间。
*   **持续交付 (CD):** 在 CI 的基础上，将所有代码更改在构建和测试通过后，自动发布到测试环境或预生产环境。这意味着除了自动化测试外，你还拥有一个自动化的发布流程，可以在任何时候点击一个按钮来部署你的应用。
*   **持续部署 (CD):** 这是 CD 的下一步。每一次通过所有自动化测试的代码变更都会自动部署到生产环境。这种方式可以极大地加速反馈循环，并让客户更快地享受到新功能。

#### CI/CD 的存在意义

*   **自动化流程:** 减少手动操作，从而降低人为错误的风险。
*   **更快的反馈:** 开发者可以快速得到关于代码变更的反馈，及时发现和修复问题。
*   **提高代码质量:** 自动化的测试和构建确保了代码在集成和部署前的质量。
*   **加速交付:** 更频繁、更可靠地发布新功能和修复。
*   **降低风险:** 小批量、频繁的发布比一次性发布大量变更的风险更小。

#### GitHub Actions 入门

GitHub Actions 是 GitHub 内置的一个强大的 CI/CD 工具。它允许你在 GitHub 仓库中自动化、自定义和执行软件开发工作流程。你可以创建工作流程 (workflows) 来构建、测试、打包、发布或部署任何项目。

工作流程由一个或多个作业 (jobs) 组成，而作业又由一系列按顺序执行的步骤 (steps) 组成。步骤可以运行命令（如 `npm install`）或运行一个 action（预构建的脚本或自定义代码）。

工作流程通常定义在仓库的 `.github/workflows` 目录下的 YAML 文件中。

**一个简单的 GitHub Actions 工作流示例:**

假设你有一个 Node.js 项目，并希望在每次推送到 `main` 分支或创建 Pull Request 时运行测试。你可以创建一个名为 `ci.yml` 的文件，内容如下：

```yaml
# .github/workflows/ci.yml

name: Node.js CI

on:
  push:
    branches: [ main ]
  pull_request:
    branches: [ main ]

jobs:
  build:
    runs-on: ubuntu-latest # 指定运行环境

    strategy:
      matrix:
        node-version: [18.x, 20.x] # 可以测试多个 Node.js 版本

    steps:
    - name: Checkout repository # 第一步：检出代码
      uses: actions/checkout@v3

    - name: Use Node.js ${{ matrix.node-version }} # 第二步：设置 Node.js 环境
      uses: actions/setup-node@v3
      with:
        node-version: ${{ matrix.node-version }}
        cache: 'npm' # 可选：缓存 npm 依赖

    - name: Install dependencies # 第三步：安装依赖
      run: npm ci

    - name: Run tests # 第四步：运行测试
      run: npm test
```

**解释:**

*   `name: Node.js CI`: 工作流程的名称。
*   `on`: 定义触发工作流程的事件。这里是当有代码推送到 `main` 分支，或者有 Pull Request 指向 `main` 分支时触发。
*   `jobs`: 定义工作流程中的作业。
    *   `build`: 作业的 ID。
    *   `runs-on: ubuntu-latest`: 指定作业运行在最新版的 Ubuntu 虚拟机上。
    *   `strategy.matrix.node-version`: 定义一个构建矩阵，使得该作业会在 Node.js 18.x 和 20.x 两个版本下分别运行。
    *   `steps`: 定义作业中的步骤。
        *   `uses: actions/checkout@v3`: 使用官方的 `checkout` action 来获取仓库代码。
        *   `uses: actions/setup-node@v3`: 使用官方的 `setup-node` action 来安装指定版本的 Node.js。
        *   `run: npm ci`: 执行命令安装项目依赖（`npm ci` 通常比 `npm install` 更快且更适合 CI 环境）。
        *   `run: npm test`: 执行命令运行测试。

当满足 `on` 中定义的条件时，GitHub Actions 会自动执行这个工作流程。你可以在仓库的 "Actions" 标签页查看工作流程的运行状态和日志。

GitHub Actions 不仅仅局限于 CI/CD，还可以用于自动化各种任务，例如：

*   自动给 Issue 打标签。
*   在有新的 Release 时发布到包管理器。
*   定时运行脚本（例如，每天检查依赖更新）。
*   部署静态网站到 GitHub Pages。

通过学习和使用 GitHub Actions，你可以极大地提升开发效率和项目质量。

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