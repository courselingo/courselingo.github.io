# CourseLingo 组织主页 · org-site

CourseLingo 的**组织主页**（GitHub Pages 站点）：列出哪些课程已完成、哪些在施工、哪些已规划，
以及每一门的**授权状态**。这是项目的正门。

非官方 · 社区项目，与任何院校均无隶属关系。

## 构建

零配置文件之外没有依赖，只需要 Python：

```powershell
$py = "C:\Users\keriko\.dsh\dsh-runtimes\dsh-primary-runtime\dependencies\python\python.exe"

# 构建（严格模式：任何 warning 都算失败 —— 本站要求 0 warning）
& $py -m mkdocs build --strict -f "D:\Vibe_Workspace\courselingo\org-site\mkdocs.yml"

# 本地预览
& $py -m mkdocs serve -f "D:\Vibe_Workspace\courselingo\org-site\mkdocs.yml"
```

产物在 `site/`（已在 `.gitignore` 中忽略）。

**关于构建输出里那条 Material 横幅**：MkDocs Material 9.7.x 启动时会打印一段
「Warning from the Material for MkDocs team」（讲 MkDocs 2.0 的破坏性变更）。
那是主题自己打印的**提示**，不是 MkDocs 的 warning，**不影响 `--strict` 的判定**（退出码仍为 0）。
想让它消失，构建前设环境变量 `NO_MKDOCS_2_WARNING=1` 即可。

依赖见 [`requirements.txt`](requirements.txt)：`mkdocs-material`；
**建议同时安装 `jieba`** —— Material 用它对中文分词，装了之后站内搜索对中文的命中率明显更好。
没装也能正常构建，只是中文检索退化为整串匹配。

## 结构

```
org-site/
├── mkdocs.yml              MkDocs Material 配置（language: zh、明暗主题切换、本地搜索）
├── requirements.txt        mkdocs-material（+ jieba 建议项）
├── .github/workflows/
│   └── pages.yml           构建并部署到 GitHub Pages（--strict 把关）
└── docs/
    ├── index.md            首页：hero + 课程状态总表（已完成 / 施工中 / 已规划 / 明确不做）
    ├── courses.md          课程：逐课程进度与授权记录
    ├── how-we-work.md      我们怎么做：授权闸门 → 术语表冻结 → 逐讲产出 → 机检 → 人工复核
    ├── licensing.md        授权说明：逐课程逐材料的条款、证据 URL 与访问日期
    ├── stylesheets/extra.css
    └── assets/             品牌资源（logo.png / logo-square.png / favicon.png / favicon-32.png）
```

`nav` 为：**首页 / 课程 / 我们怎么做 / 授权说明**。

## 部署到 GitHub Pages

本目录被设计成**自带完整仓库内容**：整个 `org-site/` 即仓库根。
在 GitHub 上新建组织仓库（例如 `courselingo/courselingo.github.io`，
这样站点落在 <https://courselingo.github.io/>），把本目录内容推到 `main` 分支，
`.github/workflows/pages.yml` 会自动构建并部署。

若站点落在子路径（如 `https://courselingo.github.io/org-site/`），
把 `mkdocs.yml` 的 `site_url` 改成对应地址即可。

## 事实来源（不要在这儿发明授权结论）

本站所有授权结论都来自平台仓库的核实记录，改动前请先核对原文：

| 文档 | 内容 |
| --- | --- |
| [course-catalog.md](https://github.com/courselingo/courselingo/blob/main/docs/course-catalog.md) | 逐课程授权结论 + 逐字原文引用（核实日期 2026-09-28） |
| [content-policy.md](https://github.com/courselingo/courselingo/blob/main/docs/content-policy.md) | 授权、署名与内容边界（含退出码 3 的拒绝执行） |
| [prior-art.md](https://github.com/courselingo/courselingo/blob/main/docs/prior-art.md) | 已有的 6.824 中文翻译及其**无许可**状态 |
| [brand.md](https://github.com/courselingo/courselingo/blob/main/docs/brand.md) | 命名、口号、语气、logo 用法（深色底必须垫白色底片） |

## Logo 用法（重要）

`logo.png` 是**透明底**版本，为**浅色背景**设计：主蓝在白底对比度 8.4:1，
在深色底仅 2.2:1。所以页头与抽屉导航里都用 `stylesheets/extra.css` 给它垫一张**白色小底片**。
不得与任何学校校徽、课程 Logo 混用或组合。
