# 课程

本页是**课程清单与授权记录**：哪几门做完了、哪几门在施工、哪几门已规划，以及每一门的授权状态**如实**写在这里。

- 核实方法：逐页抓取原始 HTML，逐字留证；抓取到的原始页面留档在平台仓库 `docs/_fetch/`。
- 核实日期：**2026-09-28**（含同日二次核实）。
- 判定原则：**条款未核实 = 不发布**；「未声明许可」按**保留所有权利**处理。

!!! warning "两条必须记住的坑"
    1. **「没有声明许可」≠「可以自由使用」**，而**「主页有 CC 徽章」≠「整站都能随便用」**。
    2. **核实的对象必须是「我们实际要用的那份文件」**，而不是课程入口页 —— 6.824 主页有徽章、
       我们依赖的讲义文件 `notes/l01.txt` 却没有任何声明，就是这一条漏掉的结果。

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

## 已规划

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

### MIT OpenCourseWare

| 项 | 内容 |
| --- | --- |
| 官方入口 | <https://ocw.mit.edu/> · 条款 <https://ocw.mit.edu/terms/> |
| 许可 | 🟡 **CC BY-NC-SA 4.0** |
| 改编 | ✅ "Adapt — remix, transform, and build upon the material" |
| 商用 | ❌ "Noncommercial — You may not use the material for commercial purposes."（MIT 的解释：衍生作品同样不得商用） |
| 相同方式共享 | ✅ "If you remix, transform, or build upon the material, you must distribute your contributions under the same license as the original." |

**判读**：这是唯一明确允许改编的目标来源，代价是两条**传染性**约束 ——
不能商用，且我们的产出必须以 CC BY-NC-SA 4.0 发布。
因此**不能把 OCW 材料与 6.824 的材料混进同一个授权边界**（一课程一仓库正是为此）。

### CMU 15-445 · 数据库系统

| 项 | 内容 |
| --- | --- |
| 官方入口 | <https://15445.courses.cs.cmu.edu/> |
| 许可 | 🔴 **未声明 = 保留所有权利**（主页与 `spring2024/`、`fall2023/`、`spring2023/`、`syllabus`、`faq` 均无任何授权标注） |
| 状态 | **已规划 / 待核实** —— 先按保留所有权利处理 |

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

## 一页看完的状态与授权

| 课程 | 状态 | 授权状态（诚实结论） | 逐字稿 / 原文对照 |
| --- | --- | --- | --- |
| MIT 6.824 / 6.5840 | **施工中**（3 讲 + 2 篇导读已发布） | ⚠️ **未确认**：CC BY 3.0 US 徽章只在主页；讲义 `notes/l01.txt` 无任何声明 | ⛔ 不产出 |
| MIT 6.1810 / 6.S081 | **已规划** | ⚠️ 已取证页面为 CC BY 3.0 US；**讲义未单独取证 ⇒ 未确认**；xv6 教材 MIT | ⛔ 未解锁 |
| MIT OpenCourseWare | **已规划** | 🟡 CC BY-NC-SA 4.0（禁商用 + SA 传染） | 🟡 须同协议发布 |
| CMU 15-445 | **已规划 / 待核实** | 🔴 未声明许可 = 保留所有权利 | ⛔ 不可做 |
| Stanford CS 144 | **待核实** | ⚠️ 站点未声明；实验 README 自订「公开可读但禁发解答」 | ⛔ 不可做 |
| UC Berkeley CS 61A | **明确不做** | 🔴 保留所有权利（© Regents of the University of California） | ⛔ 不可做 |

!!! tip "全课程的共同红线"
    **作业 / Lab 解答一律不翻译、不公开**（6.824、6.S081、CS 61A、CS 144 都有明文要求）。
    需要更细的逐材料记录，见[授权说明](licensing.md)与平台仓库
    [`docs/course-catalog.md`](https://github.com/courselingo/courselingo/blob/main/docs/course-catalog.md)。
