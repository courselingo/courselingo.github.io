# 课程

本页是**课程清单与授权记录**：哪几门做完了、哪几门在施工、哪几门已规划，以及每一门的授权状态**如实**写在这里。

- 核实方法：逐页抓取原始 HTML，逐字留证；抓取到的原始页面留档在平台仓库 `docs/_fetch/`。
- 核实日期：**2026-09-28**（含同日二次核实）。
- 判定原则：**条款未核实 = 不发布**；「未声明许可」按**保留所有权利**处理。
- 选课依据：需求信号（CS 自学指南的收录、分类与难度标注）× 授权等级 × 中文空白程度；
  完整决策记录与逐条证据见平台仓库
  [`docs/course-selection.md`](https://github.com/courselingo/courselingo/blob/main/docs/course-selection.md)。

!!! warning "三条必须记住的坑"
    1. **「没有声明许可」≠「可以自由使用」**，而**「主页有 CC 徽章」≠「整站都能随便用」**。
    2. **核实的对象必须是「我们实际要用的那份文件」**，而不是课程入口页 —— 6.824 主页有徽章、
       我们依赖的讲义文件 `notes/l01.txt` 却没有任何声明，就是这一条漏掉的结果。
    3. **许可可能压根不在页面上**：GitHub Pages 类课程站把许可写在**源码仓库根目录的 `LICENSE`** 里，
       页面一个字都没有 —— 只抓页面会 100% 漏掉。CMU 15-442 与 UCSD CSE 234 两门课的许可结论
       都是**翻开仓库**才拿到的。另需警惕：**「带 CC 标」不等于「能翻译」，ND 后缀明文禁止翻译。**

## 已完成

目前**没有任何一门课程整体完成**。已发布的材料如下（均已通过授权闸门、机检与人工复核）。

| 课程 | 已发布 | 形式 | 授权状态 |
| --- | --- | --- | --- |
| MIT 6.824 / 6.5840 · 分布式系统 | 3 讲：Introduction、RPC and Threads、GFS | 原创中文讲解 | ⚠️ 讲义授权 **未确认** |
| MIT 6.824 / 6.5840 · 分布式系统 | 2 篇论文导读：MapReduce、Raft | 原创导读（非翻译） | ⚠️ 论文授权 **未确认**（逐篇登记，见下） |

## 施工中

### MIT 6.824 / 6.5840 · 分布式系统（MIT · 6.5840 / 6.824）

| 项 | 内容 |
| --- | --- |
| 官方入口 | <https://pdos.csail.mit.edu/6.824/> |
| 状态 | **施工中** —— 3 讲 + 2 篇论文导读已发布，后续讲次持续产出 |
| 许可 | ⚠️ **CC BY 3.0 US，但只出现在主页**；讲义 `notes/l01.txt` **无任何声明** ⇒ 讲义授权 **`未确认`** |
| 讲义授权 | **`未确认`** —— `rel="license"` 0、CC 链接 0、版权声明 0 |
| 我们的做法 | 只发布**原创讲解**（讲概念，不复制原文表达）；**不产出逐字稿，不做双语原文对照，不转载课件** |

**主页的授权证据（逐字原文，也是全站唯一一处）：**

```html
<a rel="license" href="https://creativecommons.org/licenses/by/3.0/us/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/3.0/us/88x31.png" /></a>
```

**逐页实测计数**（这是我们判断覆盖范围的依据）：

| URL | `rel="license"` | CC 链接 | 版权声明 |
| --- | --- | --- | --- |
| `https://pdos.csail.mit.edu/6.824/` | **1** | 1 | 0 |
| `https://pdos.csail.mit.edu/6.824/schedule.html` | 0 | 0 | 0 |
| `https://pdos.csail.mit.edu/6.824/labs/lab-mr.html` | 0 | 0 | 0 |
| `https://pdos.csail.mit.edu/6.824/general.html` | 0 | 0 | 0 |
| **`https://pdos.csail.mit.edu/6.824/notes/l01.txt`**（我们实际依据的文件） | **0** | **0** | **0** |

**判读**：`CC BY 3.0 US` 的**许可文本**本身很宽松（无 NC、无 SA、无 ND），
但**它写在哪里、覆盖什么**是另一回事。徽章只覆盖主页，讲义那份文件没有任何许可依据
⇒ 按「无声明 = 保留所有权利」处理 ⇒ **逐字稿翻译与双语原文对照一律不产出**。

**另有与 CC 平行的课程条款**（来源 <https://pdos.csail.mit.edu/6.824/labs/collab.html>，逐字引用）：

> "Please do not publish your code or make it available to current or future 6.5840 students."

⇒ **Lab 代码与作业答案永久排除**。这既是授权问题，也是学术诚信问题。

**论文部分逐篇登记**（`papers.toml`，不用课程级布尔）：

| 论文 | 授权状态 | 产出形态 |
| --- | --- | --- |
| MapReduce: Simplified Data Processing on Large Clusters | ⚠️ 未确认（无声明） | 原创导读 |
| The Google File System | ⚠️ 已记录条款：ACM 标准声明 —— **再发布需事先专门许可** | 原创导读 |
| In Search of an Understandable Consensus Algorithm（Raft） | ⚠️ 未确认（无声明） | 原创导读 |
| ZooKeeper / Chain Replication | 待核实 | 尚未产出 |

论文的 `redistribution` 一律为 `unknown`，因此论文页**只有导读，没有译文**。

## 第一梯队 · 授权已核实，建议紧接着做

**入选条件（三条同时满足）**：① 授权已核实为 **A 级**（许可允许衍生 ⇒ 能做**真正的翻译**，这是与 B 站搬运的核心差异）；
② 需求由 CS 自学指南的收录与难度标注证实；③ 中文空白或中文资源明显不足。

### UC Berkeley CS168 · 计算机网络

| 项 | 内容 |
| --- | --- |
| 官方入口 | <https://sp25.cs168.io/> · 在线教材 <https://textbook.cs168.io/> |
| 许可 | 🟢 **CC BY-SA 4.0（仅教材）** —— **本轮唯一无 NC、可商用的课程级开放许可** |
| 证据 URL | <https://textbook.cs168.io/>（教材 License 段，带 `rel="license"` 与 by-sa 徽章） |
| 证据（逐字） | `This work is licensed under a Creative Commons Attribution-ShareAlike 4.0 International License.` |
| 我们能发布 | ✅ **译文 + 双语原文对照，可商用**；义务 = 署名 + 以 CC BY-SA 4.0 发布衍生作品（SA 传染，但**无 NC**） |
| ⚠️ 范围限定 | **课程站 `sp25.cs168.io` 未声明任何许可**（主页与 `/policies/` 均 0 命中；`license` 的命中全是图标库注释）⇒ 课程站讲义与项目按 **B 级**：只做讲解。教材与课程站是**两套授权** |

### MIT 6.006 · 算法导论（数据结构与算法）

| 项 | 内容 |
| --- | --- |
| 官方入口 | <https://ocw.mit.edu/courses/6-006-introduction-to-algorithms-fall-2011/> |
| 许可 | 🟡 **CC BY-NC-SA 4.0**，**课程页与讲义子页双重出现** |
| 证据 URL | <https://ocw.mit.edu/courses/6-006-introduction-to-algorithms-fall-2011/pages/lecture-notes/> |
| 证据（逐字） | `"license": "https://creativecommons.org/licenses/by-nc-sa/4.0/"` |
| 我们能发布 | ✅ **译文 + 双语原文对照**；义务 = **署名 + 非商业 + 相同方式共享**（产出必须以 CC BY-NC-SA 4.0 发布） |
| ⚠️ 逐件复核 | OCW 材料可能夹带**被明确排除在 CC 之外**的第三方内容（6.828 页面即有 `All rights reserved. This content is excluded from our Creative Commons license.` 的标注）⇒ **配图一律逐件复核，不直接搬运** |

### CMU 15-442 / 15-642 · Machine Learning Systems

| 项 | 内容 |
| --- | --- |
| 官方入口 | <https://mlsyscourse.org/schedule> |
| 许可 | 🟡 **CC BY-NC 4.0（无 SA）** |
| 证据 URL | <https://raw.githubusercontent.com/mlsyscourse/mlsyscourse.github.io/main/LICENSE>（**网站源码仓库根目录**，页面上没有） |
| 证据（逐字） | `Attribution-NonCommercial 4.0 International` |
| 我们能发布 | ✅ **译文 + 双语原文对照**；义务 = **署名 + 非商业**；**无 SA ⇒ 不传染**，我们的产出不必被拖成 CC |
| ⚠️ 范围限定 | `LICENSE` 位于**网站仓库**，覆盖网站托管的内容；**作业在 `mlsyscourse/assignment*` 三个独立仓库，尚未核实** ⇒ 作业按 B 级 / 不产出处理 |

### ETH Zurich DDCA → Computer Architecture · 体系结构

| 项 | 内容 |
| --- | --- |
| 官方入口 | <https://safari.ethz.ch/digitaltechnik/spring2023/>（DDCA） · <https://safari.ethz.ch/architecture/fall2022/doku.php?id=schedule>（CA） |
| 许可 | 🟡 **CC BY-NC-SA 4.0**，在 `start` / `lectures` / `schedule` **三页一致** |
| 证据（逐字） | `Except where otherwise noted, content on this wiki is licensed under the following license:` + `CC Attribution-Noncommercial-Share Alike 4.0 International` |
| 我们能发布 | ✅ **译文 + 双语原文对照 + wiki 托管文件**（`lib/exe/fetch.php?media=…`）；义务 = **署名 + 非商业 + 相同方式共享** |
| ⛔ 明确不做 | **YouTube 视频**（CA 排期页有 43 个链接）：视频受**平台条款**约束，不转载、不做字幕翻译 |
| ⚠️ 逐件复核 | 「Except where otherwise noted」不是空话：wiki 上有**客座/第三方讲者材料**，不能默认继承 wiki 许可 |

### （备选）UCSD CSE 234 · ML Systems / LLM Systems

| 项 | 内容 |
| --- | --- |
| 官方入口 | <https://hao-ai-lab.github.io/cse234-w25/> |
| 许可 | 🟢 **MIT License**（本轮**最宽松**的一项：无 NC、无 SA、可商用） |
| 证据 URL | <https://raw.githubusercontent.com/hao-ai-lab/cse234-w25/main/LICENSE>（仓库根目录） |
| 证据（逐字） | `MIT License … The website is adapted from UC Berkeley Data Science 8` |
| 我们能发布 | ✅ **译文 + 双语原文对照，可商用** |
| 为什么是备选 | 与 15-442 **同分类**，避免同期双开；**这是排期判断，不是授权判断** —— 一旦 NC 约束影响商业化，立即顶上 |
| ⚠️ 待核实 | 作业材料是否托管在同一仓库（若在，则随 MIT）；`LICENSE` 中的 "Copyright (c) 2024 DSC 204A" 与 CSE 234 的对应关系 |

## 已规划 / 仅讲解（B 级）

> 这一档的课**需求成立，但许可不允许译文**：未声明 = 保留所有权利。我们只发布**原创讲解**，
> 不产出逐字稿，不做双语原文对照，不转载课件。

### MIT 6.1810 / 6.S081 · 操作系统工程（xv6）

| 项 | 内容 |
| --- | --- |
| 官方入口 | <https://pdos.csail.mit.edu/6.1810/> · <https://pdos.csail.mit.edu/6.S081/2023/general.html> |
| 许可 | 🟢 **CC BY 3.0 US**（与 6.824 同一徽章、同一 `href`；出现在主页与 `6.S081/2023/general.html`） |
| 讲义授权 | ⚠️ **`未确认`** —— **其讲义文件未单独取证**（沿用 6.824 的教训）⇒ **逐字稿路线同样未解锁** |
| 配套教材 | `xv6-riscv` / `xv6-book` / `xv6-public` 均为 **MIT License** |
| 我们的做法 | 动手前逐材料重新核实；在取得讲义自身的许可依据之前，只做原创讲解 |

课程自订条款（逐字，见 6.S081 general 页）：

> "Do not post your lab or homework solutions on publicly accessible web sites (such as GitHub) or file spaces (such as your Athena Public directory)."

### MIT OpenCourseWare（6.006 / 6.046J 的授权依据）

| 项 | 内容 |
| --- | --- |
| 官方入口 | <https://ocw.mit.edu/> · 条款 <https://ocw.mit.edu/terms/> |
| 许可 | 🟡 **CC BY-NC-SA 4.0** |
| 改编 | ✅ "Adapt — remix, transform, and build upon the material" |
| 商用 | ❌ "Noncommercial — You may not use the material for commercial purposes."（MIT 的解释：衍生作品同样不得商用） |
| 相同方式共享 | ✅ "If you remix, transform, or build upon the material, you must distribute your contributions under the same license as the original." |

**判读**：OCW 是明确允许改编的来源，代价是两条**传染性**约束 —— 不能商用，且我们的产出必须以 CC BY-NC-SA 4.0 发布。
**第一梯队 6.006 与 6.046J 就落在这一档**（也可以通过课程页 `rel="license"` 逐页复制到讲义页，见上）。
因此**不能把 OCW 材料与 6.824 的材料混进同一个授权边界**（一课程一仓库正是为此）。

### CMU 15-445 · 数据库系统

| 项 | 内容 |
| --- | --- |
| 官方入口 | <https://15445.courses.cs.cmu.edu/> |
| 许可 | 🔴 **未声明 = 保留所有权利**（主页与 `spring2024/`、`fall2023/`、`spring2023/`、`syllabus`、`faq` 均无任何授权标注） |
| 状态 | **B 级：只做原创讲解** —— 先按保留所有权利处理，不逐字稿、不做原文对照、不转载课件 |

唯一相关的文本是学术诚信条款，不是授权：

> "Any violation of this policy is cheating. The minimum penalty for cheating (including plagiarism) will be a zero grade for the whole assignment"

### Stanford CS 144 · 计算机网络

| 项 | 内容 |
| --- | --- |
| 官方入口 | <https://cs144.github.io/> |
| 站点许可 | ⚠️ **未声明** |
| 实验代码许可 | ⚠️ **自订条款**（非标准开源许可，写在仓库 README 而非 `LICENSE`） |

站点逐字引用：

> "Please don't post source code to lab solutions."

实验代码授权（<https://raw.githubusercontent.com/CS144/imp/master/README.md>）：

> "These labs are open to the public under the (friendly, but also mandatory) condition that to preserve their value as a teaching tool, solutions not be posted publicly by anybody."

`.../CS144/imp/master/LICENSE` 与 `.../cs144.github.io/master/LICENSE` **均为 HTTP 404**（没有独立许可证文件）。

**判读**：只授予「公开可读」，**未明确授予商业使用或衍生权**；且**解答不得公开**。
⇒ 待核实，翻译其课件应视为需要先取得授权。

## 明确不做

### UC Berkeley CS 61A · 计算机程序的构造与解释

| 项 | 内容 |
| --- | --- |
| 官方入口 | <https://cs61a.org/>（302 → `/fa26/`） |
| 许可 | 🔴 **无任何许可声明 = 保留所有权利** |
| 原文引用 | "Copyright ©2026, Regents of the University of California and respective authors." |
| 出现位置 | 首页、`/fa26/syllabus/`、`/fa26/articles/contact/` 页脚 |
| 我们的决定 | **不做。** 拒绝，而不是先发了再说 |

**判读**：版权归加州大学校董会，未授予改编或再发布的权利。

- ⛔ 逐字稿翻译 / 字幕翻译：**不可做**
- ⛔ 转载课件 PDF：**不可做**
- ⛔ 作业与 Lab 解答：**永久排除**（站点明文：`Do not post your solutions publicly during or after the semester.`）

> 细节提醒：页面里那 4 处 "License" 字样**全部是站点模板自带的图标库许可注释**
> （`Feather. MIT License`、`Bootstrap Icons. MIT License`），与课程内容无关 —— 别被命中数误导。

!!! note "教材的许可管不到课程"
    同一门课的教材 [Composing Programs](https://composingprograms.com/3ed/)（3ed）是
    **CC BY-NC-SA 4.0**（"This work is licensed under a Creative Commons
    Attribution-NonCommercial-ShareAlike 4.0 International License"），**可改编但禁商用 + SA**。
    这与 CS 61A 课程站是**两套授权**：教材开放 ≠ 课程幻灯片 / 作业开放。

### UC Berkeley CS162 · 操作系统

| 项 | 内容 |
| --- | --- |
| 官方入口 | <https://cs162.org/> · 条款 <https://cs162.org/policies/> |
| 许可 | ⛔ **课程明确禁止传播** → 我们的 **C 级：拒绝执行** |
| 原文引用 | `Under no circumstances are students permitted to upload course materials online or distribute these materials` |
| 我们的决定 | **全站不做，连原创讲解也不做** |

**判读**：这是本轮唯一的**真正 C 级拒绝**。保留一条中间结论，不要简化：
该条款措辞面向**选课学生**，严格讲约束的是学生而非第三方；但本项目 [授权说明](licensing.md) 的既定立场是
「课程明确说了不要传播 ⇒ 我们不做」，这是**比法律底线更保守的政策性选择**。
⇒ 将来若要动 CS162，正确路径是**先取得讲师/院系书面授权**，而不是先发布。

### MIT 6.1600 · 有 CC 徽章却不能翻译

| 项 | 内容 |
| --- | --- |
| 许可 | ⛔ **CC BY-NC-ND 4.0**（notes 仓库，既有结论） |
| 我们的决定 | **翻译路线被明文禁止** |

**判读**：这是开放许可里**最反直觉**的一类 —— **ND = NoDerivatives（禁止衍生作品），而翻译就是衍生作品**
⇒ 带 CC 徽章的讲义，翻译被**明文禁止**。
**教训：「带 CC 标」不等于「能翻译」，必须看后缀。** 6.006（BY-NC-SA）能做译文，6.1600（BY-NC-ND）不能，
差别只在最后两位字母 —— 这也是我们逐页留证、不做记忆推断的原因。

### 其余明确不做（沿用既有结论）

| 课程 | 结论 | 依据 |
| --- | --- | --- |
| **Princeton · Algorithms 4th ed.（Algo）** | ⛔ 不做 | 站点明文 `All rights reserved.` |
| **CS:APP / CMU 15-213** | ⛔ 不做翻译 | 商业教材（页脚 `Copyright © 2015,` Pearson），站点无 CC；且社区已有 B 站中文讲解 ⇒ 差异化也不成立 |
| **Kurose & Ross《计算机网络：自顶向下方法》** | ⛔ 不做 | 商业教材：`Copyright © 2010-2025 J.F. Kurose, K.W. Ross` |
| **KAIST CS420 · Compiler Design** | ⛔ 不做翻译 | 两个分支均**无 `LICENSE`** ⇒ 保留所有权利（只能写「无 LICENSE」，**不能**写成「作者拒绝授权」）；替代路径：编译原理走 MIT OCW 6.035（CC BY-NC-SA 4.0，已核实） |
| **全部课程的 Lab / 作业解答** | ⛔ **永久排除（硬规则）** | 6.824、6.S081、CS 144、CS 61A、Nand2Tetris 五处**各自**都有禁发解答的条款 —— 著作权与学术诚信的双重风险 |

## 一页看完的状态与授权

| 课程 | 状态 | 授权状态（诚实结论） | 逐字稿 / 原文对照 |
| --- | --- | --- | --- |
| MIT 6.824 / 6.5840 | **施工中**（3 讲 + 2 篇导读已发布） | ⚠️ **未确认**：CC BY 3.0 US 徽章只在主页；讲义 `notes/l01.txt` 无任何声明 | ⛔ 不产出 |
| UC Berkeley CS168 | **第一梯队（P0）** | 🟢 **CC BY-SA 4.0**（教材，无 NC）；⚠️ 课程站未声明 | ✅ 译文 + 对照，**可商用**；课程站按 B 级 |
| MIT 6.006 | **第一梯队（P0）** | 🟡 CC BY-NC-SA 4.0（课程页 + 讲义页双重） | ✅ 译文 + 对照，须同协议发布 |
| CMU 15-442 / 15-642 | **第一梯队（P0）** | 🟡 CC BY-NC 4.0，无 SA（仓库根 `LICENSE`） | ✅ 译文 + 对照，不传染；作业待核实 |
| ETH DDCA → CA | **第一梯队（P0）** | 🟡 CC BY-NC-SA 4.0（wiki 三页一致） | ✅ 译文 + 对照（限 wiki 内容）；⛔ YouTube 不做 |
| UCSD CSE 234 | **第一梯队 · 备选** | 🟢 **MIT License**（最宽松，可商用） | ✅ 译文 + 对照；作业待核实 |
| MIT 6.1810 / 6.S081 | **已规划** | ⚠️ 已取证页面为 CC BY 3.0 US；**讲义未单独取证 ⇒ 未确认**；xv6 教材 MIT | ⛔ 未解锁 |
| MIT OpenCourseWare | **授权范式**（6.006 / 6.046J 的依据） | 🟡 CC BY-NC-SA 4.0（禁商用 + SA 传染） | 🟡 须同协议发布 |
| CMU 15-445 | **已规划 / 仅讲解** | 🔴 未声明许可 = 保留所有权利 | ⛔ 不可做 |
| Stanford CS 144 | **待核实 / 仅讲解** | ⚠️ 站点未声明；实验 README 自订「公开可读但禁发解答」 | ⛔ 不可做 |
| UC Berkeley CS 61A | **明确不做** | 🔴 保留所有权利（© Regents of the University of California） | ⛔ 不可做 |
| UC Berkeley CS162 | **明确不做（C 级）** | ⛔ 明文禁止传播课程材料 | ⛔ 不可做 |
| MIT 6.1600 | **明确不做** | ⛔ **CC BY-NC-ND 4.0**：ND 明文禁止翻译 | ⛔ 不可做 |

!!! tip "全课程的共同红线"
    **作业 / Lab 解答一律不翻译、不公开**（6.824、6.S081、CS 61A、CS 144 都有明文要求）。
    需要更细的逐材料记录，见[授权说明](licensing.md)与平台仓库
    [`docs/course-catalog.md`](https://github.com/courselingo/courselingo/blob/main/docs/course-catalog.md)；
    本轮选课的完整决策记录（需求 × 授权 × 差异化）见
    [`docs/course-selection.md`](https://github.com/courselingo/courselingo/blob/main/docs/course-selection.md)。
