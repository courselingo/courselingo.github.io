# CourseLingo · 译课 AI

**AI-powered translation & explanation for classic CS courses.**

### 让经典 CS 课程，跨语言也能学懂。

CourseLingo（课语 AI）用 AI 把经典计算机科学课程翻译并**讲解**成中文：先冻结课程术语表，再逐讲产出可溯源的原创讲解，目标是让中文读者**真正学懂**，而不是勉强读完。

<p class="cl-actions">
<a class="md-button md-button--primary" href="https://github.com/courselingo/courselingo">平台主仓库 · courselingo/courselingo</a>
<a class="md-button" href="courses.md">课程状态总表</a>
</p>

!!! warning "非官方 · 社区项目"
    CourseLingo 是社区项目，与 MIT、UC Berkeley、CMU、Stanford 等**任何院校均无隶属关系**，
    不使用其校徽或课程 Logo，也不暗示任何官方背书。文中出现的课程名称均为**描述性引用**，
    版权归原作者与院校所有。

## 课程状态总表 {#course-status}

下表每一行都附**已核实的授权状态**（核实日期 **2026-09-28**，逐字原文引用与取证记录见[授权说明](licensing.md)）。
凡是授权未核实的，我们就不做那道工序 —— 这不是免责声明，是构建流水线里的硬闸门。

### 已完成

目前**还没有任何一门课程整体完成**。这里的「已完成」指的是已经通过授权闸门、机检与人工复核并发布的材料。

| 课程 | 已完成的内容 | 授权状态 |
| --- | --- | --- |
| MIT 6.824 / 6.5840 · 分布式系统 | 3 讲（Introduction、RPC and Threads、GFS）+ 2 篇论文导读（MapReduce、Raft） | ⚠️ **未确认**（讲义层面）—— 见下方「施工中」 |

### 施工中

| 课程 | 进度 | 授权状态（诚实结论） | 因此我们怎么做 |
| --- | --- | --- | --- |
| **MIT 6.824 / 6.5840 · 分布式系统** | 3 讲 + 2 篇论文导读已发布，后续讲次继续产出 | ⚠️ **未确认**。CC BY 3.0 US 徽章**只出现在课程主页**（`pdos.csail.mit.edu/6.824/`，全站唯一一处 `rel="license"`）；我们实际依据的讲义文件 `notes/l01.txt` **许可标注 0、CC 链接 0、版权声明 0** | 讲义按「未确认 = 默认保留所有权利」处理：**只发布原创讲解，不产出逐字稿，不做双语原文对照**，也不转载原始课件 |

!!! note "为什么 6.824 是「未确认」而不是「已授权」"
    徽章确实存在，所以 6.824 **不是**「无授权」；但徽章的覆盖范围**从未被取证**，
    而我们实际要用的那份讲义文件上**没有任何声明**。核到实际使用的文件，结论就是「未确认」。

### 已规划

| 课程 | 授权状态（2026-09-28 核实） | 对我们的含义 |
| --- | --- | --- |
| **MIT 6.1810 / 6.S081（xv6 操作系统）** | 🟢 主页与 `6.S081/2023/general.html` 带 **CC BY 3.0 US** 徽章；配套 xv6 教材为 **MIT License**。⚠️ **但讲义文件未单独取证** ⇒ 讲义的覆盖范围同样 **未确认** | 就已取证页面而言可商用、可翻译、无 ShareAlike；**逐字稿路线未解锁**，动手前逐材料再核一遍 |
| **MIT OpenCourseWare 课程** | 🟡 **CC BY-NC-SA 4.0**：允许改编，但**禁止商用**且**相同方式共享（SA）会传染** | 可以做，但产出必须同样以 CC BY-NC-SA 4.0 发布、且不得商用 —— 这是授权边界，不是偏好 |
| **CMU 15-445 · 数据库系统** | 🔴 **未声明许可 = 保留所有权利**（主页与多份 syllabus 均无任何授权标注） | 已规划/待核实：只发布我们自己独立撰写的讲解，不逐字稿、不转载课件 |
| **Stanford CS 144 · 计算机网络** | ⚠️ **混合**：站点无声明；实验 README 自订条款「公开可读，但任何人不得公开发布解答」 | 待核实：未授予明确的商用与衍生权，翻译其课件应视为**需要先取得授权** |

### 明确不做

| 课程 | 为什么不做 |
| --- | --- |
| **UC Berkeley CS 61A** | 🔴 **未声明开放许可 = 保留所有权利**。页面原文：`Copyright ©2026, Regents of the University of California and respective authors.` 版权归加州大学校董会，未授予改编或再发布的权利。课程另有明文要求 `Do not post your solutions publicly during or after the semester.` —— 作业与 Lab 解答**永久排除**。**我们的选择是拒绝，而不是先发了再说。** |

!!! note "教材开放 ≠ 课程开放"
    CS 61A 的教材 Composing Programs（3ed）本身是 **CC BY-NC-SA 4.0**（可改编、禁商用、SA）。
    但课程站是保留所有权利 —— 教材的许可**管不到**课程的幻灯片与作业，
    所以我们不会用它给课程内容开口子。

## 我们怎么做

五道关，顺序不能换（[完整说明](how-we-work.md)）：

1. **授权闸门** —— 授权未核实就不放行。闸门不通过时 `validate.py` 与 `build.py` 都以**退出码 3** 拒绝，**不产出任何站点**。
2. **术语表先冻结** —— 核心概念全篇同译，术语表先行、翻译跟随。
3. **逐讲产出** —— 讲概念、讲动机、讲推导，而不是复制原文表达。
4. **机检** —— 内容（授权与转载探测）、配图、文风各有一道自动检查。
5. **人工复核** —— 机器拦不住译文，最后一步必须由人看。

内容本身是**纯 Markdown**，站点渲染是**可替换的**：同一批 Markdown 既能用 MkDocs Material 渲染，也能被平台自带的零依赖构建脚本渲染，还能直接喂给 AI Agent。**换渲染器不需要改内容。**

## 一篇诚实的说明：6.824 的中文翻译已经存在

所以我们**不能**靠「第一个中文版」立足。存在的版本包括：

| 项目 | 形态 | 覆盖 | 许可 |
| --- | --- | --- | --- |
| mit-public-courses-cn-translatio / mit6-824 | GitBook | Lecture 01/03/04/06–12（约 10 讲） | **无** |
| huihongxiao/MIT6.824 | GitHub 源码仓（上面 GitBook 的源） | 同上 | **无**（仓库无 LICENSE） |

他们**没有许可**。其中一份 README 的原话是：

> 此次翻译纯属个人爱好，**如果涉及到任何版权行为，请联系我，我将删除内容**。

那不是一份许可，而是一份「可能侵权、欢迎来函即删」的免责声明；GitBook 侧的文档里「版权 / 许可 / license / CC / ©」出现 **0 次**。他们翻译的是视频讲课内容，而视频的权利状态正是我们核实过的**未确认**项。

**三条结论：**

1. 我们不能从他们那里拷贝任何文本 —— 无许可 = 保留全部权利。
2. 我们走的是另一条路：**授权未确认，就不做全文翻译**；6.824 现行只发布原创讲解。
3. 这条判断在代码里有对应实现：讲义授权未核实 ⇒ `output_mode = "transcript"` 被 `validate.py` 以**退出码 1** 拒绝，`build_site.py` **不注入**双语原文对照块。

证据与核实记录都在平台仓库里，可自行查证：
[`docs/prior-art.md`](https://github.com/courselingo/courselingo/blob/main/docs/prior-art.md) ·
[`docs/course-catalog.md`](https://github.com/courselingo/courselingo/blob/main/docs/course-catalog.md) ·
[`docs/licensing-research-log.md`](https://github.com/courselingo/courselingo/blob/main/docs/licensing-research-log.md) ·
[`docs/content-policy.md`](https://github.com/courselingo/courselingo/blob/main/docs/content-policy.md)

## 授权

| 对象 | 协议 |
| --- | --- |
| 代码（平台工具、构建脚本、校验脚本） | **MIT** |
| 我们的原创内容（讲解、导读、术语表、配图） | **CC BY 4.0** |
| 上游课程材料（讲义、幻灯片、视频、作业） | **一律不转载、不再分发**；版权归原作者与院校所有 |

**课程规定优先。** 我们自己的协议只覆盖原创部分；当课程或论文的条款更严格时（例如 MIT OCW 的 CC BY-NC-SA 4.0），**以其条款为准**。

任何内容一旦被指出超出授权范围，我们会**立即下线**，不等核实结论 —— 完整规则见[授权说明](licensing.md)。
