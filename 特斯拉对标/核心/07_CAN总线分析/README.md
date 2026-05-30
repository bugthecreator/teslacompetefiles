# 07_CAN总线分析

**与防夹算法的相关性：⭐⭐⭐⭐ (协议级别数据)**

## 文件清单

| 文件 | 大小 | 类型 | 内容说明 | 防夹相关性 |
|------|------|------|---------|-----------|
| opendbc_master.zip | 1.3MB | ✅ ZIP | commaai/opendbc 完整仓库。包含 Tesla 及其他车型的 CAN DBC 文件、Python解析工具、信号定义。 | ⭐⭐⭐⭐ 高度相关 |
| opendbc_opendbc-master_opendbc_dbc_tesla_can.dbc | 53KB | ✅ TEXT | **Tesla CAN 总线定义文件**。定义了所有公开的 CAN 消息和信号，包括：DOOR_STATE_*(车门状态)、BODY_R1(车身消息)、GTW_* (网关信号)等。约900行定义。 | ⭐⭐⭐⭐⭐ 核心 |
| opendbc_opendbc-master_opendbc_dbc_tesla_model3_party.dbc | 33KB | ✅ TEXT | Model 3 第三方接入 CAN 定义（comma.ai openpilot 使用的消息）。含 APS 自动驾驶相关信号。 | ⭐⭐ 弱相关 |
| opendbc_opendbc-master_opendbc_dbc_tesla_model3_vehicle.dbc | 24KB | ✅ TEXT | Model 3 车辆内部 CAN 定义。含 VCLEFT_doorStatus、VCRIGHT_doorStatus、VCFRONT_lighting 等车身控制信号。 | ⭐⭐⭐ 参考 |
| opendbc_opendbc-master_opendbc_dbc_tesla_powertrain.dbc | 7.5KB | ✅ TEXT | 动力总成 CAN 定义。含电机扭矩、转速信号，与防夹算法中的电机控制有关。 | ⭐⭐ 弱相关 |

## 关键信号（与防夹相关）
从 tesla_can.dbc 中提取：
```
CAN ID 792: 通用状态消息
  DOOR_STATE_FL     - 左前门状态 (0=关, 1=开, 2=初始化中)
  DOOR_STATE_FR     - 右前门状态
  DOOR_STATE_RL     - 左后门状态
  DOOR_STATE_RR     - 右后门状态
  DOOR_STATE_FrontTrunk - 前备箱状态

CAN ID 643: BODY_R1 - 车身控制器消息
  包含车身控制系统状态

CAN ID 259/258: VCLEFT/VCRIGHT_doorStatus - 车门控制器
  包含门把手拉动状态、行李厢锁闩状态等
```

## 说明
这些 DBC 文件来自 comma.ai 的 openpilot 开源项目。它们只定义了 CAN 总线上的信号，**不包含 LIN 总线上的车窗电机控制信号**（特斯拉使用 LIN 总线与门模块通信，窗控算法在 LIN 侧运行）。但通过这些 CAN 信号可以理解特斯拉车身控制的整体架构。
