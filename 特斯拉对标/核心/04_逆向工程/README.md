# 04_逆向工程

**与防夹算法的相关性：⭐⭐⭐⭐⭐ (最有价值的实际用户反馈)**

## 文件清单

| 文件 | 大小 | 类型 | 内容说明 | 防夹相关性 |
|------|------|------|---------|-----------|
| reddit_power_windows_FMVSS118_recall.json | 133KB | ✅ JSON | **核心数据**。Reddit 讨论帖 "Tesla Power Windows May Pinch / FMVSS 118 Recall" 的完整 JSON。包含 100+ 条评论，讨论了：① NHTSA 要求 Tesla OTA 修复自动反转系统；② 车窗防夹的原理（电流/力检测）；③ 校准方法（按住开关30秒）；④ 双层玻璃导致的误触发问题。 | ⭐⭐⭐⭐⭐ 核心 |
| reddit_power_windows_FMVSS118_recall.txt | 11KB | ✅ TXT | 上述JSON的纯文本提取，可直接阅读 | ⭐⭐⭐⭐⭐ 核心 |
| reddit_window_issue.json | 76KB | ✅ JSON | Reddit 讨论帖 "Weird window issue" 完整 JSON。含车主讨论车窗上下反复（误触发防夹）的原因分析：颠簸路面、窗膜、导轨灰尘、电机老化等。多位车主反映与车速、颠簸有关，证实是**力/电流阈值检测型防夹**。 | ⭐⭐⭐⭐⭐ 核心 |
| reddit_window_issue.txt | 5KB | ✅ TXT | 上述JSON的纯文本提取 | ⭐⭐⭐⭐⭐ 核心 |
| reddit_ModelY_anti_pinch.json | 13KB | ✅ JSON | Reddit 讨论帖 "Does Model Y have anti pinch sensor technology?" 完整 JSON。讨论小孩手指被夹住的事件，分析特斯拉防夹系统的灵敏度问题。有评论指出"小孩手指软组织难以与橡胶密封条区分"——**直接揭示了力检测型防夹的局限性**。 | ⭐⭐⭐⭐⭐ 核心 |
| reddit_ModelY_anti_pinch.txt | 0.7KB | ✅ TXT | 上述JSON的纯文本提取 | ⭐⭐⭐⭐⭐ 核心 |
| www.reddit.com_r_*_does.html | 8.3KB | ✅ HTML | Reddit HTML页面（3个），需要JavaScript验证才能查看。**无法直接阅读**。已保存JSON版本作为替代。 | ⭐⭐ 仅备份 |

## 价值说明
这些 Reddit 数据是**实车用户反馈**，直接反映了特斯拉防夹算法的实际表现：
1. ✅ 确认使用**电流/力检测**方式（评论区多处证实）
2. ✅ 确认OTA可调防夹参数（22V-085更新）
3. ✅ 揭示**误触发模式**（颠簸/窗膜/灰尘）
4. ✅ 揭示**校准方法**（开关保持30s自学习）
5. ✅ 揭示**灵敏度局限**（细软手指难检测）
