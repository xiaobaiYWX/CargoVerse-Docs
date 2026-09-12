# 周界警戒系统

状态：正式 CargoGood 定义；数据同步批次 2026-09-10。数值为首轮基线，后续按实际航运测试校准。

## 定义

| 项目 | 内容 |
| --- | --- |
| 资源 ID | `cargoverse:electronics/perimeter_security_systems` |
| JSON 文件 | `src/main/resources/data/cargoverse/cargo_goods/electronics/perimeter_security_systems.json` |
| Schema 版本 | 1 |
| CargoClass | `electronics` |
| 显示名称 | 周界警戒系统 |
| UI 图标 | `cargoverse:textures/gui/cargo_goods/electronics/perimeter_security_systems.png`（32×32 RGBA PNG） |
| 科技等级 | 3 |
| 标签 | `ingredient.electronics.perimeter_security_systems` |
| 结算单位 | `cargoverse:void_byte` |

## 数值

| 项目 | 数值 | 单位 |
| --- | ---: | --- |
| 单位质量 | 1 | Kpg/t |
| 单位基础价值 | 710 | VB/t |
| 单位许可证经验 | 2 | exp/t |
| 单位繁荣经验 | 1 | exp/t |
| 基础完整度 | 100 | 点 |

## 运输要求

| 词条 ID | 参数 |
| --- | --- |
| `cargoverse:moisture_proof` | `damage_per_second` = 0.5 |

## 内容定位与投放

BDS 安全系统集成→工业设施与重要航线据点；传感、通信与警戒控制成套交付；防潮

- 设计来源：[B02 安防设施集成厂](<../../07_贸易点/factory/security/安防设施集成厂.md>)；主要去处：[B03 边境驻防补给港](<../../07_贸易点/market/defense/边境驻防补给港.md>)。按[资源表版贸易点设计](<../../07_贸易点/设计总览.md>)投放，贸易点与资源表已同步数据包，自然结构待补。
- 本轮采用持续周转：来源初始 2 t、容量 6 t、日补 2 t；主要买方初始 0、容量 3 t、日耗 1 t、满库停止收购。已同步资源表，自然结构待补。
- 基础估值沿用已评审目录的参考值；质量按物流定位区分，经验按科技层级分档，不按货价线性增长。
- 货物专属标签仅匹配本货物；资源表、商店或制造台需要其他候选货物时应显式列出。

[返回 CargoGood 目录](../README.md)

图标采用统一像素风格的独立实物轮廓，由内置 image_gen 生成并导出为 32×32；透明底、最近邻缩放，无文字标签。
