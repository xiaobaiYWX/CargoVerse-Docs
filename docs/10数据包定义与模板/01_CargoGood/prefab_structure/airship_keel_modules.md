# 飞艇龙骨模块

状态：正式 CargoGood 定义；数据同步批次 2026-09-10。数值为首轮基线，后续按实际航运测试校准。

## 定义

| 项目 | 内容 |
| --- | --- |
| 资源 ID | `cargoverse:prefab_structure/airship_keel_modules` |
| JSON 文件 | `src/main/resources/data/cargoverse/cargo_goods/prefab_structure/airship_keel_modules.json` |
| Schema 版本 | 1 |
| CargoClass | `prefab_structure` |
| 显示名称 | 飞艇龙骨模块 |
| UI 图标 | `cargoverse:textures/gui/cargo_goods/prefab_structure/airship_keel_modules.png`（32×32 RGBA PNG） |
| 科技等级 | 3 |
| 标签 | `ingredient.prefab_structure.airship_keel_modules` |
| 结算单位 | `cargoverse:void_byte` |

## 数值

| 项目 | 数值 | 单位 |
| --- | ---: | --- |
| 单位质量 | 10 | Kpg/t |
| 单位基础价值 | 1040 | VB/t |
| 单位许可证经验 | 2 | exp/t |
| 单位繁荣经验 | 1 | exp/t |
| 基础完整度 | 100 | 点 |

## 运输要求

无。

## 内容定位与投放

AUI 结构制造→飞艇建造与大修节点；标准化船体骨架；常规

- 设计来源：[A03 飞艇总装与航修港](<../../07_贸易点/factory/aviation/飞艇总装与航修港.md>)；主要去处：[S02 远航货运枢纽](<../../07_贸易点/market/logistics/远航货运枢纽.md>)。按[资源表版贸易点设计](<../../07_贸易点/设计总览.md>)投放，贸易点与资源表已同步数据包，自然结构待补。
- 本轮采用持续周转：来源初始 1 t、容量 3 t、日补 1 t；主要买方初始 0、容量 3 t、日耗 0.75 t、满库停止收购。已同步资源表，自然结构待补。
- 基础估值沿用已评审目录的参考值；质量按物流定位区分，经验按科技层级分档，不按货价线性增长。
- 货物专属标签仅匹配本货物；资源表、商店或制造台需要其他候选货物时应显式列出。

[返回 CargoGood 目录](../README.md)

图标采用统一像素风格的独立实物轮廓，由内置 image_gen 生成并导出为 32×32；透明底、最近邻缩放，无文字标签。
