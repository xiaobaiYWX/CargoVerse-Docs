# HRI Explorer 科考样本舱 L 型

[地平线研究院](<../README.md>) → [Explorer 科考样本舱](<README.md>) → L 型

恢复原有尺寸与结构模板，容量和空重按当前系列的 1∶2∶4∶7∶12 阶梯补回，耐久、分类许可与防护沿用当前系列。

## 定义

| 项目 | 内容 |
| --- | --- |
| 完整型号 | `HRI-Explorer-SI-L` |
| 资源 ID | `cargoverse:hri/explorer_si_l` |
| 定义文件 | [explorer_si_l.json](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/hri/explorer_si_l.json>) |
| 制造商 | 地平线研究院 |
| 系列全称 | Explorer 科考样本舱 |
| 尺寸等级 | L |
| 调度点 | 4 |
| 结算单位 | `cargoverse:void_byte` |
| 标签 | `series.hri.explorer` |

## 结构模板

**正式模板已提供。** 当前引用：`cargoverse:cargo/hri/explorer/hri_explorer_si_l`。

[当前 NBT 文件](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/hri/explorer/hri_explorer_si_l.nbt>) · [模板接入状态](<../../缺失结构模板.md>)

## 数值

| 指标 | 定义基础值 | 默认实际值（含厂商通用倍率） |
| --- | --- | --- |
| 容量（t） | 32 | 25 |
| 空柜目标质量（Kpg） | 96 | 105.6 |
| 最大耐久 | 125 | 162.5 |

实际容量包含厂商通用倍率并向下取整；专项货物倍率另行计算。空重仍受模板中非货柜方块质量下限约束。

## CargoClass 兼容

`research_sample`、`tools_equipment`、`medical_supply`、`special_resource`。仅允许上述分类，不支持 none；同一货柜不可混装不同 CargoGood。

## 防护与运输要求

消除：易碎、防潮、避光。`cargoverse:fragile`、`cargoverse:moisture_proof`、`cargoverse:light_sensitive`

设计缺陷：无。所有货物的原有 time_limit 继续生效；御寒不代表恒温冷藏。

## 制造与投放

| 项目 | 规划 |
| --- | --- |
| 加工费 VB | 720 |
| 最低许可证 | L |
| 最低繁荣等级 | 3 |
| 节点类型 | 科考前哨、样本交接站 |
| 当前配方 | 待编制材料配方与投放；定义已注册 |

## 当前 JSON

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/hri/explorer/hri_explorer_si_l",
  "manufacturer": "cargoverse:hri",
  "display_name": "HRI Explorer 科考样本舱 L 型",
  "description": "§lHRI Explorer 科考样本舱 L 型\n§r§7面向科考样本和采样器材往返，通过缓冲、防潮与遮光设计保护研究物资。\n§r§l制造商：地平线研究院 / Horizon Research Institute\n§r§l系列：Explorer 科考样本舱",
  "size_class": "L",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 4,
  "capacity": 32,
  "empty_mass": 96,
  "max_durability": 125,
  "allowed_cargo_classes": [
    "research_sample",
    "tools_equipment",
    "medical_supply",
    "special_resource"
  ],
  "special_designs": [
    "cargoverse:fragile",
    "cargoverse:moisture_proof",
    "cargoverse:light_sensitive"
  ],
  "design_defects": [],
  "tags": [
    "series.hri.explorer"
  ]
}
```
