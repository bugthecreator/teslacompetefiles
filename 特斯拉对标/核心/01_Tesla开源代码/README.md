# 01_Tesla开源代码

**与防夹算法的相关性：⭐⭐ (搜索脚本和结果页面)**

## 文件清单

| 文件 | 大小 | 类型 | 内容说明 | 防夹相关性 |
|------|------|------|---------|-----------|
| github.com_teslamotors.html | 290KB | ✅ HTML | Tesla GitHub 组织主页（https://github.com/teslamotors）的 HTML 缓存。列出 Tesla 的所有公开仓库。**不含源码**。 | ⭐ 弱相关 |
| tesla_all_repos.json | 390KB | ✅ JSON | Tesla GitHub 上所有仓库的 API 返回数据。可查阅 Tesla 有哪些公开仓库。**未见直接含防夹代码的仓库**。 | ⭐ 弱相关 |
| comprehensive_search.py | 12.5KB | ✅ PY | 综合搜索脚本——搜索 GitHub 仓库、GPL 源码、代码片段中与 Tesla 防夹相关的内容。**这是搜索工具，不是结果**。 | ⭐⭐ 工具脚本 |
| search_*.py (4 files) | ~2KB each | ✅ PY | GitHub/各平台搜索脚本，分别搜索不同关键词。**尚未找到 Tesla GPL 源码**（Tesla 已不再提供公开 GPL 下载）。 | ⭐⭐ 工具脚本 |

### github_search/ 子目录
| 文件 | 大小 | 类型 | 内容说明 | 防夹相关性 |
|------|------|------|---------|-----------|
| *web.html (9 files) | ~98KB each | ✅ HTML | DuckDuckGo 搜索结果页面。每个文件对应一个关键词的搜索结果（如"model3 window hall sensor"、"ANTI_PINCH Tesla"等）。**这些是搜索引擎结果页，不是实际内容**。仅保存了约10个关键词的搜索结果快照。 | ⭐ 仅索引 |

## 说明
真正的 Tesla GPL 源代码曾可从 tesla.com/legal/opensource 下载（tesla-2024.x-gpl-code.zip），但截至2026年5月该页面已403禁止访问。包含车窗/LIN总线驱动的内核代码可能曾存在于这些 GPL 包中，但目前已无法获取。
