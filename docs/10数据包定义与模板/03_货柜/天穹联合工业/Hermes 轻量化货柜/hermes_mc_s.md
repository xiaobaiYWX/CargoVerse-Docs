# AUI Hermes 轻量化货柜 S 型

[天穹联合工业](<../README.md>) → [Hermes 轻量化货柜](<README.md>) → S 型

该系列恢复原尺寸、基础数值与分类许可；制造费用尚未重新定稿。

## 定义

| 项目 | 内容 |
| --- | --- |
| 完整型号 | `AUI-Hermes-MC-S` |
| 资源 ID | `cargoverse:aui/hermes_mc_s` |
| 定义文件 | [hermes_mc_s.json](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/aui/hermes_mc_s.json>) |
| 制造商 | 天穹联合工业 |
| 系列全称 | Hermes 轻量化货柜 |
| 尺寸等级 | S |
| 调度点 | 1 |
| 结算单位 | `cargoverse:void_byte` |
| 标签 | `series.aui.hermes` |

## 结构模板

**正式模板已提供。** 当前引用：`cargoverse:cargo/aui/hermes/aui_hermes_mc_s`。

[当前 NBT 文件](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/aui/hermes/aui_hermes_mc_s.nbt>) · [模板接入状态](<../../缺失结构模板.md>)

## 数值

| 指标 | 定义基础值 | 默认实际值（含厂商通用倍率） |
| --- | --- | --- |
| 容量（t） | 10 | 11 |
| 空柜目标质量（Kpg） | 22 | 22 |
| 最大耐久 | 70 | 70 |

实际容量包含厂商通用倍率并向下取整；专项货物倍率另行计算。空重仍受模板中非货柜方块质量下限约束。

## CargoClass 兼容

`agriculture`、`raw_resource`、`processed_resource`、`weapon_armor`、`mechanical_parts`、`electronics`、`general_supplies`、`medical_supply`、`valuables`、`research_sample`。仅允许上述分类，不支持 none；同一货柜不可混装不同 CargoGood。

## 防护与运输要求

消除：无。

设计缺陷：无。所有货物的原有 time_limit 继续生效；御寒不代表恒温冷藏。

## 制造与投放

| 项目 | 规划 |
| --- | --- |
| 加工费 VB | 待设计 |
| 最低许可证 | S |
| 最低繁荣等级 | 1 |
| 节点类型 | 通用物流与短途交接站 |
| 当前配方 | 待编制材料配方与投放；定义已注册 |

## 当前 JSON

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/aui/hermes/aui_hermes_mc_s",
  "manufacturer": "cargoverse:aui",
  "display_name": "AUI Hermes 轻量化货柜 S 型",
  "description": "§lAUI Hermes 轻量化货柜 S 型\n§r§7保留原有轻型物流产品线，以较低耐久承运多类短途干货。\n§r§l制造商：天穹联合工业\n§r§l系列：Hermes 轻量化货柜",
  "size_class": "S",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 1,
  "capacity": 10,
  "empty_mass": 22,
  "max_durability": 70,
  "allowed_cargo_classes": [
    "agriculture",
    "raw_resource",
    "processed_resource",
    "weapon_armor",
    "mechanical_parts",
    "electronics",
    "general_supplies",
    "medical_supply",
    "valuables",
    "research_sample"
  ],
  "special_designs": [],
  "design_defects": [],
  "tags": [
    "series.aui.hermes"
  ]
}
```
