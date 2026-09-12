# 液压执行缸

状态：正式 CargoGood 定义；数据同步批次 2026-09-10。数值为首轮基线，后续按实际航运测试校准。

## 定义

| 项目 | 内容 |
| --- | --- |
| 资源 ID | `cargoverse:mechanical_parts/hydraulic_cylinders` |
| JSON 文件 | `src/main/resources/data/cargoverse/cargo_goods/mechanical_parts/hydraulic_cylinders.json` |
| Schema 版本 | 1 |
| CargoClass | `mechanical_parts` |
| 显示名称 | 液压执行缸 |
| UI 图标 | `cargoverse:textures/gui/cargo_goods/mechanical_parts/hydraulic_cylinders.png`（32×32 RGBA PNG） |
| 科技等级 | 3 |
| 标签 | `ingredient.mechanical_parts.hydraulic_cylinders` |
| 结算单位 | `cargoverse:void_byte` |

## 数值

| 项目 | 数值 | 单位 |
| --- | ---: | --- |
| 单位质量 | 3 | Kpg/t |
| 单位基础价值 | 680 | VB/t |
| 单位许可证经验 | 2 | exp/t |
| 单位繁荣经验 | 1 | exp/t |
| 基础完整度 | 100 | 点 |

## 运输要求

无。

## 内容定位与投放

液压部件厂→装卸、采矿设备；功能总成；常规

- 设计来源：[A02 通用机电装备厂](<../../07_贸易点/factory/machinery/通用机电装备厂.md>)；主要去处：[D03 重工材料与矿机厂](<../../07_贸易点/factory/heavy/重工材料与矿机厂.md>)。按[资源表版贸易点设计](<../../07_贸易点/设计总览.md>)投放，贸易点与资源表已同步数据包，自然结构待补。
- 本轮采用持续周转：来源初始 2 t、容量 6 t、日补 2 t；主要买方初始 0、容量 6 t、日耗 2 t、满库停止收购。已同步资源表，自然结构待补。
- 基础估值沿用已评审目录的参考值；质量按物流定位区分，经验按科技层级分档，不按货价线性增长。
- 货物专属标签仅匹配本货物；资源表、商店或制造台需要其他候选货物时应显式列出。

[返回 CargoGood 目录](../README.md)

图标采用统一像素风格的独立实物轮廓，由内置 image_gen 生成并导出为 32×32；透明底、最近邻缩放，无文字标签。
