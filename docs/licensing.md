# 授权说明

这一页是本站最重要的页面。授权风险是这个项目最大的敌人 —— 比翻译质量更能决定生死。

## 三条原则

1. **条款未核实 = 不发布。** 拿不到许可依据，就按**保留所有权利**处理。
2. **核实对象必须是「我们实际要用的那份文件」**，不是课程入口页。
3. **「找到许可」不等于「许可覆盖那份文件」。** 覆盖范围未确立时，同样按未核实处理。

!!! warning "两个我们实际踩过的坑"
    **坑一：只看过滤掉标签后的纯文本，会 100% 漏掉 CC 徽章。**
    6.824 主页的授权写在页脚的**图片徽章**里（`rel="license"`），徽章没有可见文字，
    纯文本抽取会得到「命中 0」，从而误判成「无许可」。

    **坑二：找到徽章之后，还必须确认它覆盖哪份文件。**
    我们曾由「主页有徽章」推出「讲义可以翻译」——
    二次核实补查了**我们实际依据的讲义文件** `notes/l01.txt`：
    `rel="license"` / CC 链接 / 版权声明 **均为 0** ⇒ **讲义授权 `未确认`**，
    该推论**已被原文否定并撤回**。

## 逐课程 · 逐材料的授权记录

核实方法：逐页抓取原始 HTML（本机 DNS 为 fake-IP，统一走 SOCKS5 代理），逐字留证；
原始页面留档在平台仓库 `docs/_fetch/`。**核实日期：2026-09-28**。

!!! info "先说清楚 6.824 的结论"
    **6.824 不是「无授权」** —— 主页的 CC BY 3.0 US 徽章真实存在。
    但它是**主页范围的许可**，不是整站许可：徽章**全站只出现一次**，
    而我们实际依据的讲义文件**没有任何声明**。所以结论是「**讲义那份文件没有许可依据**」，
    不是「6.824 无许可」。这两句话不一样，前一句才是准确的。

### MIT 6.824 / 6.5840 · 分布式系统

| 材料 | 许可条款 | 来源 URL | 访问日期 | 允许商用 | 允许衍生 | 有 SA |
| --- | --- | --- | --- | --- | --- | --- |
| **主页** | CC BY 3.0 US（徽章仅此一处） | <https://pdos.csail.mit.edu/6.824/> | 2026-09-28 | ✅（就主页而言） | ✅（就主页而言） | ❌ |
| **讲义 `notes/l01.txt`** | **无任何声明 → `未确认`（默认保留所有权利）** | <https://pdos.csail.mit.edu/6.824/notes/l01.txt> | 2026-09-28 | ⚠️ 未确认 | ⚠️ 未确认 | ⚠️ 未确认 |
| 幻灯片 | ⚠️ 未单独取证（与讲义同处理 = `未确认`） | — | 2026-09-28 | ⚠️ 未确认 | ⚠️ 未确认 | ⚠️ 未确认 |
| Lab 代码 | 课程条款**禁止公开** | <https://pdos.csail.mit.edu/6.824/labs/collab.html> | 2026-09-28 | — | — | — |
| golabs 发行包 | ⚠️ 未核实（`g.csail.mit.edu` 实测不可达，GitHub 上无对应仓库） | `git://g.csail.mit.edu/6.5840-golabs-2026` | 2026-09-28 | ⚠️ | ⚠️ | ⚠️ |
| 视频（2020 及更早） | YouTube 平台条款（页面只嵌 `youtube.com/embed/...`） | <http://nil.csail.mit.edu/6.824/2020/video/1.html> | 2026-09-28 | ⚠️ | ⚠️ | ⚠️ |

主页的授权证据（逐字原文 HTML，也是全站唯一一处）：

```html
<a rel="license" href="https://creativecommons.org/licenses/by/3.0/us/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/3.0/us/88x31.png" /></a>
```

逐页计数（判断覆盖范围的依据）：

| URL | 大小 | `rel="license"` | CC 链接 | 版权声明 |
| --- | --- | --- | --- | --- |
| `/6.824/` | 3995 B | **1** | 1 | 0 |
| `/6.824/schedule.html` | 17414 B | 0 | 0 | 0 |
| `/6.824/labs/lab-mr.html` | 15394 B | 0 | 0 | 0 |
| `/6.824/general.html` | 8065 B | 0 | 0 | 0 |
| **`/6.824/notes/l01.txt`** | 10886 B | **0** | **0** | **0** |

**对我们的含义**：`CC BY 3.0 US` 的许可文本宽松（无 NC、无 SA、无 ND），
但它**覆盖哪里**才是关键。讲义没有许可依据 ⇒

- ⛔ **不产出逐字稿翻译**（翻译是衍生作品，会复制原作全部表达）；
- ⛔ **不做双语原文对照**（本质是逐字稿的并排呈现，走同一道闸门）；
- ⛔ **不转载原始课件**；
- ✅ **只发布我们自己的原创讲解** —— 讲概念、不复制原文表达。**这是 6.824 当前唯一路线。**
- ⛔ **Lab 代码与作业答案永久排除** —— 课程明文要求不得公开。

### MIT 6.1810 / 6.S081 · 操作系统工程

| 材料 | 许可条款 | 来源 URL | 访问日期 | 允许商用 | 允许衍生 | 有 SA |
| --- | --- | --- | --- | --- | --- | --- |
| 主页 / 讲座页 | CC BY 3.0 US | <https://pdos.csail.mit.edu/6.1810/> | 2026-09-28 | ✅（就主页而言） | ✅（就主页而言） | ❌ |
| **讲义文件** | ⚠️ **未单独取证 → `未确认`**（沿用 6.824 的教训） | — | 2026-09-28 | ⚠️ 未确认 | ⚠️ 未确认 | ⚠️ 未确认 |
| xv6 源码 / 教材 | **MIT License** | <https://raw.githubusercontent.com/mit-pdos/xv6-riscv/riscv/LICENSE> | 2026-09-28 | ✅ | ✅ | ❌ |

**对我们的含义**：就已取证的页面而言可商用、可翻译、无 SA，
但**讲义文件的覆盖范围未确立** ⇒ **逐字稿路线未解锁**；动手前必须逐材料重新核实。

### MIT OpenCourseWare

| 材料 | 许可条款 | 来源 URL | 访问日期 | 允许商用 | 允许衍生 | 有 SA |
| --- | --- | --- | --- | --- | --- | --- |
| 课程材料 | **CC BY-NC-SA 4.0** | <https://ocw.mit.edu/terms/> | 2026-09-28 | ❌ | ✅ | ✅ |

逐字条款：

> "Adapt — remix, transform, and build upon the material"
>
> "Noncommercial — You may not use the material for commercial purposes."
>
> "Share Alike — If you remix, transform, or build upon the material, you must distribute your contributions under the same license as the original."

MIT 对「非商业」的解释（逐字）：

> "Non-commercial use means that users may not sell, profit from, or commercialize OCW materials or **works derived from** them."

**对我们的含义**：唯一明确允许改编的来源，代价是两条**传染性**约束 ——
**不得商用**，且产出**必须以 CC BY-NC-SA 4.0 发布**。
⇒ 不能把 OCW 材料与 6.824 的材料混在同一个授权边界里（所以**一课程一仓库**是授权上的必要设计）。

### Composing Programs（CS 61A 教材，3ed）

| 材料 | 许可条款 | 来源 URL | 访问日期 | 允许商用 | 允许衍生 | 有 SA |
| --- | --- | --- | --- | --- | --- | --- |
| 教材 | **CC BY-NC-SA 4.0** | <https://composingprograms.com/3ed/> | 2026-09-28 | ❌ | ✅ | ✅ |

> "This work is licensed under a Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License (CC BY-NC-SA 4.0)."

**注意**：现行第三版是 **4.0**（旧版文案曾写 3.0，站点现已 302 到 `/3ed/`）。
教材开放 **≠** 课程开放 —— 它与 CS 61A 课程站是两套授权。

### UC Berkeley CS 61A

| 材料 | 许可条款 | 来源 URL | 访问日期 | 允许商用 | 允许衍生 | 有 SA |
| --- | --- | --- | --- | --- | --- | --- |
| 课件 / 作业 / 视频 | **未声明 → 保留所有权利** | <https://cs61a.org/fa26/> | 2026-09-28 | ❌ | ❌ | — |

页面原文（页脚）：

> "Copyright ©2026, Regents of the University of California and respective authors."

作业条款原文：

> "Do not post your solutions publicly during or after the semester."

**我们的决定：不做。** 版权归加州大学校董会，未授予改编或再发布的权利。
我们**选择拒绝，而不是先发了再说** —— 同一条线索下，教材的 CC BY-NC-SA 4.0 也**不能**给课程内容开口子。

### CMU 15-445

| 材料 | 许可条款 | 来源 URL | 访问日期 | 允许商用 | 允许衍生 | 有 SA |
| --- | --- | --- | --- | --- | --- | --- |
| 课件 | **未声明 → 保留所有权利** | <https://15445.courses.cs.cmu.edu/> | 2026-09-28 | ❌ | ❌ | — |

核实范围：主页 + `/spring2024/`、`/fall2023/`、`/spring2023/` + `syllabus.html` + `faq.html`。
**全部页面无任何许可标注**（无 Creative Commons、无 `rel="license"`、无授权措辞）。
唯一相关文本是学术诚信条款，不是授权。

**对我们的含义**：已规划 / 待核实；先按保留所有权利处理 —— 只做原创讲解，不逐字稿、不转载课件。

### Stanford CS 144

| 材料 | 许可条款 | 来源 URL | 访问日期 | 允许商用 | 允许衍生 | 有 SA |
| --- | --- | --- | --- | --- | --- | --- |
| 站点 | **未声明** | <https://cs144.github.io/> | 2026-09-28 | ❌ | ❌ | — |
| 实验代码 | **自订：公开可读但禁发解答** | <https://raw.githubusercontent.com/CS144/imp/master/README.md> | 2026-09-28 | ⚠️ 未授予 | ⚠️ 未授予 | — |

站点原文：

> "Please don't post source code to lab solutions."

实验代码条款原文（写在 README，**不是** `LICENSE` 文件）：

> "These labs are open to the public under the (friendly, but also mandatory) condition that to preserve their value as a teaching tool, solutions not be posted publicly by anybody."

`.../CS144/imp/master/LICENSE` 与 `.../cs144.github.io/master/LICENSE` 均为 **HTTP 404**。

**对我们的含义**：待核实 —— 只授予「公开可读」，**未明确授予商业使用或衍生权**；
翻译其课件应视为**需要先取得授权**。

## 一律不产出的内容

| 做法 | 我们的处理 |
| --- | --- |
| 完整讲座逐字稿的翻译 | ⛔ 不产出（6.824 讲义 `未确认`） |
| 视频字幕的翻译 | ⛔ 不产出 |
| 官方作业 / Lab 题面与答案的翻译 | ⛔ **永久排除**（著作权 + 学术诚信双重风险） |
| 原始课件（PDF / PPT / 视频）的转载 | ⛔ 一律**只链接官方来源**，不转载 |
| 我们自己撰写的概念讲解 | ✅ 可做（讲概念，不复制原文表达） |
| 术语表、学习路径、原创配图 | ✅ 可做 |

## ⛔ 拒绝执行是怎么落地的

课程明确不允许传播时，在 `course.toml` 里写：

```toml
[license]
redistribution = "forbidden"        # 课程明确不允许传播
evidence_url = "https://.../terms"  # 依据
```

于是：

- `validate.py` → **退出码 3**，打印明确理由，不再跑其余校验；
- `build.py` → **退出码 3**，**不产出任何站点**；
- CI 里 `build` 依赖 `validate` → **部署不会发生**。

**为什么用独立的退出码 3**：让人一眼区分「内容写错了」（`1`，改改就好）与
「这件事我们不做」（`3`，改内容没用）。
**为什么连原创讲解也拦**：法律上独立撰写的概念讲解通常安全，
但课程既然明确说了不要传播，本项目**选择不做** —— 这是比法律底线更保守的**政策性选择**。

## 我们自己的授权

| 对象 | 协议 |
| --- | --- |
| 代码（平台工具、构建脚本、校验脚本） | **MIT** |
| 我们的原创内容（讲解、导读、术语表、配图） | **CC BY 4.0**（允许商用与改编，只需署名） |
| 上游课程材料（讲义、幻灯片、视频、作业） | **一律不转载、不再分发**；版权归原作者与院校所有 |

**但课程规定优先 —— 这是硬规则。** 我们自己的宽松协议只覆盖原创部分：

| 上游条款 | 我们怎么做 |
| --- | --- |
| CC BY 类（6.824 主页、6.1810 已取证页面） | 就**已覆盖的材料**而言，产出可用 CC BY 4.0，但**必须保留上游署名**。⚠️ 6.824 的徽章只在主页，讲义无声明 ⇒ 讲义不得据此发布逐字稿或原文对照 |
| CC BY-NC-SA 类（OCW、Composing Programs） | 产出**必须**同样以 CC BY-NC-SA 发布，且**不得商用** |
| 未声明 / 保留所有权利（6.824 讲义、CS 61A、15-445、CS 144 站点） | 只发布我们自己独立撰写的讲解；逐字稿与原文对照不产出 |
| **明确不允许传播** | ⛔ **拒绝执行**（退出码 3） |

## 下线机制

任何内容一旦被指出超出授权范围：

1. **立即下线**（不回退讨论、不等核实结论）；
2. 在对应仓库开 issue 记录决策；
3. 复盘该课程的授权判断是否有系统性偏差。

**宁可错杀，不可拖延。**

## 非官方声明

CourseLingo 是**非官方 · 社区项目**，与 MIT、UC Berkeley、CMU、Stanford 等任何院校
**均无隶属关系**，不使用其校徽或课程 Logo，也不暗示任何官方背书与合作关系。

## 证据在哪里

| 文档 | 内容 |
| --- | --- |
| [`docs/course-catalog.md`](https://github.com/courselingo/courselingo/blob/main/docs/course-catalog.md) | 逐课程授权结论与逐字原文引用 |
| [`docs/licensing-research-log.md`](https://github.com/courselingo/courselingo/blob/main/docs/licensing-research-log.md) | 核实过程与取证记录 |
| [`docs/content-policy.md`](https://github.com/courselingo/courselingo/blob/main/docs/content-policy.md) | 授权、署名与内容边界的完整规则 |
| [`docs/prior-art.md`](https://github.com/courselingo/courselingo/blob/main/docs/prior-art.md) | 同类中文翻译项目的许可状态 |
| [`docs/_fetch/`](https://github.com/courselingo/courselingo/tree/main/docs/_fetch) | 抓取到的原始页面留证 |
