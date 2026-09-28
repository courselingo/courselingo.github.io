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

**选课由两个已取证的输入相乘得出：「社区需求」来自 [CS 自学指南](https://github.com/pkuflyingpig/cs-self-learning)（75,894 stars，MIT License）的收录与分类，
「我们能发布什么」来自逐条授权核验。** 两者分开记账 —— 「有社区推荐」是需求依据，**不是**授权依据。

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

### 第一梯队 · 授权已核实，建议紧接着做

下表的共同点是 **A 级来源**：许可**已核实允许衍生**，所以我们能做真正的**翻译**（译文 + 双语原文对照），
而不是只能自己写讲解 —— 这就是我们与「B 站搬运」的根本差异。需求信号全部来自 CS 自学指南的收录、分类与难度标注。

| 课程 | 授权状态（已核实） | 我们因此能发布 | 为什么排在前面 |
| --- | --- | --- | --- |
| **UC Berkeley CS168 · 计算机网络** | 🟢 **CC BY-SA 4.0**（在线教材 `textbook.cs168.io` 带 `rel="license"` 与 by-sa 链接）。⚠️ 课程站本身**未声明**任何许可 | **译文 + 双语原文对照，且可商用**（无 NC）；须署名，并以 CC BY-SA 4.0 发布衍生作品 | 全场**唯一没有 NC 约束**的一项：商业化路径（会员、付费专栏）在 BY-SA 下不受阻；中文完全空白 |
| **MIT 6.006 · 算法导论** | 🟡 **CC BY-NC-SA 4.0**，课程页与 lecture-notes 子页**都**带 CC 链接 | **译文 + 双语原文对照**；须署名、禁商用，产出必须以 CC BY-NC-SA 4.0 发布（SA 传染） | 受众最大（算法入门），许可链条最干净：**课程页与讲义页双重取证**，没有 6.824 那种「徽章只在主页」的缺口 |
| **CMU 15-442 / 15-642 · Machine Learning Systems** | 🟡 **CC BY-NC 4.0，无 SA** —— 依据是网站**源码仓库根目录**的 `LICENSE` | **译文 + 双语原文对照**；须署名、禁商用，但**不传染**：我们的产出不必被拖成 CC | 最热方向 × 无 SA（不污染我们的发布协议）× 与已上线的 6.824 分布式能力直接衔接 |
| **ETH Zurich DDCA → Computer Architecture · 体系结构** | 🟡 **CC BY-NC-SA 4.0**，在 `start` / `lectures` / `schedule` **三页一致**（许可核到材料页，而不是只核入口页） | **译文 + 双语原文对照**，范围限 wiki 托管内容；须署名、禁商用、同协议发布。⚠️ 同页的 **YouTube 视频不做**（平台条款），客座讲者材料逐件复核 | 中文空白 × 系统纵深；两门成链（DDCA 是 CA 的先修） |
| **（备选）UCSD CSE 234 · ML Systems / LLM Systems** | 🟢 **MIT License**（最宽松）—— 依据是 `hao-ai-lab/cse234-w25` 仓库根目录的 `LICENSE` | **译文 + 双语原文对照，可商用**（无 NC、无 SA） | 与 15-442 同属机器学习系统，为避免同期双开而列为**第一顺位备选**；一旦 NC 约束影响商业化，立即顶上 |

!!! note "为什么「备选」也写进第一梯队"
    CSE 234 的许可比上面四门都宽松。它不排进正式名单**不是许可问题**，而是与 15-442 同分类、
    同期双开不划算 —— 这是**排期判断**，不是授权判断，两者不能混着说。

### 已规划 / 仅讲解（B 级与待核实）

这几门的需求同样成立，但**许可不允许译文**：要么未声明 = 保留所有权利，要么讲义层面的授权尚未取证。

| 课程 | 授权状态（诚实结论） | 因此我们怎么做 |
| --- | --- | --- |
| **MIT 6.1810 / 6.S081（xv6 操作系统）** | 🟢 主页与 `6.S081/2023/general.html` 带 **CC BY 3.0 US** 徽章；配套 xv6 教材为 **MIT License**。⚠️ **但讲义文件未单独取证** ⇒ 讲义的覆盖范围同样 **未确认** | 就已取证页面而言可商用、可翻译、无 ShareAlike；**逐字稿路线未解锁**，动手前逐材料再核一遍 |
| **CMU 15-445 · 数据库系统** | 🔴 **未声明许可 = 保留所有权利**（主页与多份 syllabus 均无任何授权标注） | 只发布我们自己独立撰写的**原创讲解**，不逐字稿、不做原文对照、不转载课件 |
| **Stanford CS 144 · 计算机网络** | ⚠️ **混合**：站点无声明；实验 README 自订条款「公开可读，但任何人不得公开发布解答」 | 未授予明确的商用与衍生权，翻译其课件应视为**需要先取得授权** |

> MIT OpenCourseWare 的 **CC BY-NC-SA 4.0** 不是单独一门「课」，而是第一梯队 **6.006 / 6.046J** 的授权依据：
> 允许改编，但**禁止商用**且 **SA 会传染** —— 采用它的讲次必须整仓按 CC BY-NC-SA 4.0 发布（一课程一仓库正是为此）。

### 明确不做

| 课程 | 为什么不做 |
| --- | --- |
| **UC Berkeley CS 61A** | 🔴 **未声明开放许可 = 保留所有权利**。页面原文：`Copyright ©2026, Regents of the University of California and respective authors.` 版权归加州大学校董会，未授予改编或再发布的权利。课程另有明文要求 `Do not post your solutions publicly during or after the semester.` —— 作业与 Lab 解答**永久排除**。**我们的选择是拒绝，而不是先发了再说。** |
| **UC Berkeley CS162 · 操作系统** | ⛔ **真正的 C 级拒绝，全站不做（连原创讲解也不做）**。`/policies/` 原文：`Under no circumstances are students permitted to upload course materials online or distribute these materials`。课程明确说了不要传播 ⇒ 我们不做，这是比法律底线更保守的**政策性选择**；将来要动的正确路径是先取得讲师书面授权 |
| **MIT 6.1600** | ⛔ **有 CC 徽章却不能翻译的典型**。notes 仓库是 **CC BY-NC-ND 4.0** —— **ND = 禁止衍生作品，翻译即衍生作品 ⇒ 翻译被明文禁止**。它提醒我们：「带 CC 标」不等于「能翻译」，**必须看后缀** |

> 完整拒绝清单（Princeton Algorithms「All rights reserved」、CS:APP 与 Kurose & Ross 的商业教材、
> KAIST CS420 无 `LICENSE`）见[课程页](courses.md)的「明确不做」一节。

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

!!! note "核验口径：只看页面会漏掉一整类许可"
    GitHub Pages 类的课程站，许可**写在源码仓库根目录的 `LICENSE` 里，页面上一个字都没有**。
    只抓页面会 **100% 漏掉**这一类：CMU 15-442（CC BY-NC 4.0）与 UCSD CSE 234（MIT License）
    这两条结论都是**翻开仓库**才取到的。所以我们的核验对象始终是「**我们实际要用的那份文件**」，
    再到它所在的仓库里找许可 —— **两步都做，缺一步就不算取证。**

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
[`docs/course-selection.md`](https://github.com/courselingo/courselingo/blob/main/docs/course-selection.md)（**本轮选课决策记录：需求 × 授权，含逐字证据**）·
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
