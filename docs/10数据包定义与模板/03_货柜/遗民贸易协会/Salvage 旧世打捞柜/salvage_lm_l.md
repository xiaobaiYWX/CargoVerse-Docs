# REX Salvage 旧世打捞柜 L 型

[遗民贸易协会](<../README.md>) → [Salvage 旧世打捞柜](<README.md>) → L 型

恢复原有尺寸与结构模板，容量和空重按当前系列的 1∶2∶4∶7∶12 阶梯补回，耐久、分类许可与防护沿用当前系列。

## 定义

| 项目 | 内容 |
| --- | --- |
| 完整型号 | `REX-Salvage-LM-L` |
| 资源 ID | `cargoverse:rex/salvage_lm_l` |
| 定义文件 | [salvage_lm_l.json](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/rex/salvage_lm_l.json>) |
| 制造商 | 遗民贸易协会 |
| 系列全称 | Salvage 旧世打捞柜 |
| 尺寸等级 | L |
| 调度点 | 4 |
| 结算单位 | `cargoverse:void_byte` |
| 标签 | `series.rex.salvage` |

## 结构模板

**正式模板已提供。** 当前引用：`cargoverse:cargo/rex/salvage/rex_salvage_lm_l`。

[当前 NBT 文件](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/rex/salvage/rex_salvage_lm_l.nbt>) · [模板接入状态](<../../缺失结构模板.md>)

## 数值

| 指标 | 定义基础值 | 默认实际值（含厂商通用倍率） |
| --- | --- | --- |
| 容量（t） | 36 | 36 |
| 空柜目标质量（Kpg） | 88 | 88 |
| 最大耐久 | 80 | 80 |

实际容量包含厂商通用倍率并向下取整；专项货物倍率另行计算。空重仍受模板中非货柜方块质量下限约束。

## CargoClass 兼容

`valuables`、`special_resource`、`research_sample`、`electronics`、`anomalous_cargo`。仅允许上述分类，不支持 none；同一货柜不可混装不同 CargoGood。

## 防护与运输要求

消除：易碎。`cargoverse:fragile`

设计缺陷：无。所有货物的原有 time_limit 继续生效；御寒不代表恒温冷藏。

## 制造与投放

| 项目 | 规划 |
| --- | --- |
| 加工费 VB | 280 |
| 最低许可证 | L |
| 最低繁荣等级 | 3 |
| 节点类型 | 遗民交换所、旧世打捞交接点 |
| 当前配方 | 待编制材料配方与投放；定义已注册 |

## 当前 JSON

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/rex/salvage/rex_salvage_lm_l",
  "manufacturer": "cargoverse:rex",
  "display_name": "REX Salvage 旧世打捞柜 L 型",
  "description": "§lREX Salvage 旧世打捞柜 L 型\n§r§7由遗民贸易协会筛选翻修的旧世打捞柜，提供基础缓冲，以较低成本承运遗物和特殊材料。\n§r§l制造商：遗民贸易协会 / Remnant Exchange\n§r§l系列：Salvage 旧世打捞柜",
  "size_class": "L",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 4,
  "capacity": 36,
  "empty_mass": 88,
  "max_durability": 80,
  "allowed_cargo_classes": [
    "valuables",
    "special_resource",
    "research_sample",
    "electronics",
    "anomalous_cargo"
  ],
  "special_designs": [
    "cargoverse:fragile"
  ],
  "design_defects": [],
  "tags": [
    "series.rex.salvage"
  ]
}
```
