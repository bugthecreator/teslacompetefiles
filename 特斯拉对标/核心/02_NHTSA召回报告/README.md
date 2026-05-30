# 02_NHTSA召回报告

**与防夹算法的相关性：⭐⭐⭐⭐⭐ (官方安全缺陷报告，最权威)**

## 状态
⚠️ **当前只有 Google 缓存页面（无实际召回数据）。**

NHTSA (National Highway Traffic Safety Administration) 服务器拦截了所有自动化下载请求。
Google 缓存也无法获取到实际内容。

## 已知的关联召回

### 1. 22V-085 — 前备箱防夹召回 (2022年2月)
- **影响**: 1,097,000 辆
- **车型**: Model 3 (2017-2022), Model Y (2020-2022), Model S (2021-2022), Model X (2021-2022)
- **问题**: 电动前备箱关闭时防夹检测不充分
- **修复**: OTA 固件更新，增强防夹校准
- **来源**: Reddit + 新闻报导确认

### 2. 未编号 — 车窗自动反转系统OTA更新 (2022年11月)
- **问题**: FMVSS 118 合规性问题，自动车窗反转系统校准不足
- **修复**: OTA 固件更新 "enhances the calibration of the vehicle's automatic window reversal system behavior"
- **来源**: Reddit r/teslamotors 讨论帖 (已保存在04_逆向工程)

## 如需获取原始PDF
需要手动访问 https://www.nhtsa.gov/vehicle/2022/TESLA/MODEL-3/4DR/SDN
然后点击"Recalls"标签查找。
