# AUI Hermes 轻量化货柜 M 型


[天穹联合工业](<../README.md>) → [Hermes 轻量化货柜](<README.md>) → M 型

该系列恢复原尺寸、基础数值与分类许可；实体材料与加工费已重新设计，见下方制造与投放。

## 定义

| 项目 | 内容 |
| --- | --- |
| 完整型号 | `AUI-Hermes-MC-M` |
| 资源 ID | `cargoverse:aui/hermes_mc_m` |
| 定义文件 | [hermes_mc_m.json](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/aui/hermes_mc_m.json>) |
| 制造商 | 天穹联合工业 |
| 系列全称 | Hermes 轻量化货柜 |
| 尺寸等级 | M |
| 调度点 | 2 |
| 结算单位 | `cargoverse:void_byte` |
| 标签 | `series.aui.hermes` |

## 结构模板

**正式模板已提供。** 当前引用：`cargoverse:cargo/aui/hermes/aui_hermes_mc_m`。

[当前 NBT 文件](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/aui/hermes/aui_hermes_mc_m.nbt>) · [模板接入状态](<../../缺失结构模板.md>)

## 数值

| 指标 | 定义基础值 | 实际值 |
| --- | ---: | ---: |
| 容量（t） | 110 | 110 |
| 空柜目标质量（Kpg） | 44 | 44 |

未配置 CargoClass 容量修正，所有允许分类均使用基础容量。

容量、空重、防护与缺陷均由本货柜型号直接定义；未列出的允许分类使用基础容量。指定分类容量在最终乘算后一次向下取整。目标空重仍受结构中非货柜方块质量下限约束。

## CargoClass 兼容

`agriculture`、`raw_resource`、`processed_resource`、`weapon_armor`、`mechanical_parts`、`electronics`、`general_supplies`、`medical_supply`、`valuables`、`research_sample`。仅允许上述分类，不支持 none；同一货柜不可混装不同 CargoGood。

## 防护与运输要求

消除：无。

设计缺陷：无。所有货物的原有 time_limit 继续生效；御寒不代表恒温冷藏。

## 制造与投放

| 项目 | v2 实体材料设计 |
| --- | --- |
| 加工费 | 200 VB |
| 实体材料 | 铁锭 ×20、铜锭 ×16、白色羊毛 ×8、红石 ×4 |
| 最低许可证 | M |
| 最低繁荣等级 | 1 |
| 材料最少占格 | 4 格，按每种物品 64 堆叠 |
| 当前配方状态 | 配方设计完成，尚未写入运行时制造定义 |

正式提供节点：[A02 通用机电装备厂](<../../../07_贸易点/factory/通用机电装备厂/定义设计/01_货柜制造台定义.md>)（固定专业工坊）、[A03 飞艇总装与航修港](<../../../07_贸易点/factory/飞艇总装与航修港/定义设计/01_货柜制造台定义.md>)（固定配套制造台）。同型号跨站使用同一实体配方、加工费和门槛；玩家背包供料，不扣贸易点库存。普通资产按当前型号占用调度点，基础领取独立处理。

[统一配方与定价依据](<../../../08_货柜制造台/制造配方与投放总表.md>)。数值为首轮设计目标，尚未完成实机平衡。

## 当前 JSON

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/aui/hermes/aui_hermes_mc_m",
  "manufacturer": "cargoverse:aui",
  "display_name": "AUI Hermes 轻量化货柜 M 型",
  "description": "§lAUI Hermes 轻量化货柜 M 型\n§r§7保留原有轻型物流产品线，以轻量结构承运多类短途干货。\n§r§l制造商：天穹联合工业\n§r§l系列：Hermes 轻量化货柜",
  "size_class": "M",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 2,
  "capacity": 110,
  "empty_mass": 44,
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
