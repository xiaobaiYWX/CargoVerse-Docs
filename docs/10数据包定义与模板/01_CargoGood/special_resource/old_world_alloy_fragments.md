# 旧世合金残片

状态：正式 CargoGood 定义；数据同步批次 2026-09-10。数值为首轮基线，后续按实际航运测试校准。

## 定义

| 项目 | 内容 |
| --- | --- |
| 资源 ID | `cargoverse:special_resource/old_world_alloy_fragments` |
| JSON 文件 | `src/main/resources/data/cargoverse/cargo_goods/special_resource/old_world_alloy_fragments.json` |
| Schema 版本 | 1 |
| CargoClass | `special_resource` |
| 显示名称 | 旧世合金残片 |
| UI 图标 | `cargoverse:textures/gui/cargo_goods/special_resource/old_world_alloy_fragments.png`（32×32 RGBA PNG） |
| 科技等级 | 4 |
| 标签 | `ingredient.special_resource.old_world_alloy_fragments` |
| 结算单位 | `cargoverse:void_byte` |

## 数值

| 项目 | 数值 | 单位 |
| --- | ---: | --- |
| 单位质量 | 5 | Kpg/t |
| 单位基础价值 | 4000 | VB/t |
| 单位许可证经验 | 3 | exp/t |
| 单位繁荣经验 | 1.5 | exp/t |
| 基础完整度 | 100 | 点 |

## 运输要求

无。

## 内容定位与投放

REX 遗迹渠道→专门材料修复；可利用但尚不可复制的材料遗存，限量发现；常规

- 设计来源：[R01 遗民打捞交换所](<../../07_贸易点/resource/salvage/遗民打捞交换所.md>)；主要去处：[A02 通用机电装备厂](<../../07_贸易点/factory/machinery/通用机电装备厂.md>)。按[资源表版贸易点设计](<../../07_贸易点/设计总览.md>)投放，贸易点与资源表已同步数据包，自然结构待补。
- 本轮采用有限批次：来源初始 1 t、容量 1 t、日补 0；主要买方初始 0、容量 1 t、日耗 0、满库停止收购。已同步资源表，自然结构待补。
- 基础估值沿用已评审目录的参考值；质量按物流定位区分，经验按科技层级分档，不按货价线性增长。
- 货物专属标签仅匹配本货物；资源表、商店或制造台需要其他候选货物时应显式列出。

[返回 CargoGood 目录](../README.md)

图标采用统一像素风格的独立实物轮廓，由内置 image_gen 生成并导出为 32×32；透明底、最近邻缩放，无文字标签。
