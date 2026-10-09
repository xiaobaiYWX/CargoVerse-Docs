# 工业棉布

状态：正式 CargoGood 定义；整数数值批次 2026-10-02。计量口径见[整数数值基线](<../整数数值基线.md>)，后续按实际航运测试校准。

## 定义

| 项目 | 内容 |
| --- | --- |
| 资源 ID | `cargoverse:processed_resource/industrial_cotton_cloth` |
| JSON 文件 | `src/main/resources/data/cargoverse/cargo_goods/processed_resource/industrial_cotton_cloth.json` |
| Schema 版本 | 1 |
| CargoClass | `processed_resource` |
| 显示名称 | 工业棉布 |
| UI 图标 | `cargoverse:textures/gui/cargo_goods/processed_resource/industrial_cotton_cloth.png`（32×32 RGBA PNG） |
| 科技等级 | 2 |
| 标签 | `ingredient.processed_resource.industrial_cotton_cloth`、`textile_input` |
| 结算单位 | `cargoverse:void_byte` |

## 数值

| 项目 | 数值 | 单位 |
| --- | ---: | --- |
| 单位质量 | 1 | Kpg/t |
| 单位基础价值 | 38 | VB/t |
| 单位许可证经验 | 6 | exp/t |
| 单位繁荣经验 | 3 | exp/t |
| 基础完整度 | 200 | 点 |

## 运输要求

| 词条 ID | 参数 |
| --- | --- |
| `cargoverse:moisture_proof` | `damage_per_second` = 1 |

## 内容定位与投放

棉包纺织→补给、医疗、防护器材；防潮

- 设计来源：[V01 梯田农林站](<../../07_贸易点/resource/梯田农林站/00_总体说明.md>)；主要去处：[S01 云港民生集配站](<../../07_贸易点/market/云港民生集配站/00_总体说明.md>)。按[资源表版贸易点设计](<../../07_贸易点/设计总览.md>)投放，贸易点与资源表已同步数据包，自然结构已接入。
- 当前主要来源采用持续周转：初始 400 t、容量 800 t、日补 200 t；主要买方长期不限额收购。按[数量与运力基线](<../数量与运力基线.md>)配置，t 表示货物数量而非吨。
- 基础估值沿用现值；质量按物流定位取整数，经验按科技层级使用整数计分，完整度与损耗等比调整；详见[整数数值基线](<../整数数值基线.md>)。
- 货物专属标签仅匹配本货物；资源表、商店或制造台需要其他候选货物时应显式列出。

[返回 CargoGood 目录](../README.md)

图标采用统一像素风格的独立实物轮廓，由内置 image_gen 生成并导出为 32×32；透明底、最近邻缩放，无文字标签。
