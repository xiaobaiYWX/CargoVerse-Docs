# AUI Nomad 拓殖工程柜 X 型

[天穹联合工业](<../README.md>) → [Nomad 拓殖工程柜](<README.md>) → X 型

恢复原有尺寸与结构模板，容量和空重按当前系列的 1∶2∶4∶7∶12 阶梯补回，耐久、分类许可与防护沿用当前系列。

## 定义

| 项目 | 内容 |
| --- | --- |
| 完整型号 | `AUI-Nomad-HD-X` |
| 资源 ID | `cargoverse:aui/nomad_hd_x` |
| 定义文件 | [nomad_hd_x.json](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/aui/nomad_hd_x.json>) |
| 制造商 | 天穹联合工业 |
| 系列全称 | Nomad 拓殖工程柜 |
| 尺寸等级 | X |
| 调度点 | 6 |
| 结算单位 | `cargoverse:void_byte` |
| 标签 | `series.aui.nomad` |

## 结构模板

**正式模板已提供。** 当前引用：`cargoverse:cargo/aui/nomad/aui_nomad_hd_x`。

[当前 NBT 文件](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/aui/nomad/aui_nomad_hd_x.nbt>) · [模板接入状态](<../../缺失结构模板.md>)

## 数值

| 指标 | 定义基础值 | 默认实际值（含厂商通用倍率） |
| --- | --- | --- |
| 容量（t） | 56 | 61 |
| 空柜目标质量（Kpg） | 196 | 196 |
| 最大耐久 | 160 | 160 |

实际容量包含厂商通用倍率并向下取整；专项货物倍率另行计算。空重仍受模板中非货柜方块质量下限约束。

## CargoClass 兼容

`prefab_structure`、`construction_material`、`machinery`、`general_supplies`。仅允许上述分类，不支持 none；同一货柜不可混装不同 CargoGood。

## 防护与运输要求

消除：易碎、防潮、勿倒置。`cargoverse:fragile`、`cargoverse:moisture_proof`、`cargoverse:keep_upright`

设计缺陷：无。所有货物的原有 time_limit 继续生效；御寒不代表恒温冷藏。

## 制造与投放

| 项目 | 规划 |
| --- | --- |
| 加工费 VB | 980 |
| 最低许可证 | X |
| 最低繁荣等级 | 4 |
| 节点类型 | 拓殖营地、工程集散站 |
| 当前配方 | 待编制材料配方与投放；定义已注册 |

## 当前 JSON

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/aui/nomad/aui_nomad_hd_x",
  "manufacturer": "cargoverse:aui",
  "display_name": "AUI Nomad 拓殖工程柜 X 型",
  "description": "§lAUI Nomad 拓殖工程柜 X 型\n§r§7承运拓殖设施、工程建材与部署物资，采用缓冲、防潮与固定设计，适合中小型工程交付。\n§r§l制造商：天穹联合工业 / Aether Union Industries\n§r§l系列：Nomad 拓殖工程柜",
  "size_class": "X",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 6,
  "capacity": 56,
  "empty_mass": 196,
  "max_durability": 160,
  "allowed_cargo_classes": [
    "prefab_structure",
    "construction_material",
    "machinery",
    "general_supplies"
  ],
  "special_designs": [
    "cargoverse:fragile",
    "cargoverse:moisture_proof",
    "cargoverse:keep_upright"
  ],
  "design_defects": [],
  "tags": [
    "series.aui.nomad"
  ]
}
```
