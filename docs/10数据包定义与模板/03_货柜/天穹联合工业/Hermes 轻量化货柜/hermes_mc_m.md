# AUI Hermes 轻量化货柜 M 型

> 分类同步说明（2026-10-20）：本页兼容类别已更新为十四类方案。其他型号/投放规划可能保留历史设计，完整运行时定义以项目 JSON 为准；本轮不重平衡容量、质量或制造价格。


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
| 容量（个） | 110 | 110 |
| 空柜目标质量（Kpg） | 44 | 44 |

未配置 CargoClass 容量修正，所有允许分类均使用基础容量。

容量、空重、防护与缺陷均由本货柜型号直接定义；未列出的允许分类使用基础容量。指定分类容量在最终乘算后一次向下取整。目标空重仍受结构中非货柜方块质量下限约束。

## CargoClass 兼容

| 分类 | CargoClass |
| --- | --- |
| 农业物资 | `agriculture` |
| 食品与食材 | `food` |
| 原料资源 | `raw_resource` |
| 加工材料 | `processed_resource` |
| 工具与装备 | `tools_equipment` |
| 机械零件 | `mechanical_parts` |
| 红石与控制 | `electronics` |
| 通用物资 | `general_supplies` |
| 化工与药剂 | `chemical_material` |
| 物流与仓储 | `logistics_equipment` |

仅允许上述类别，不支持 none；一柜只装一种精确物品变体。首批物品标签与运输参数已配置；未覆盖物品使用默认运输规则，不代表全部物品已经归类或平衡。

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
    "food",
    "raw_resource",
    "processed_resource",
    "tools_equipment",
    "mechanical_parts",
    "electronics",
    "general_supplies",
    "chemical_material",
    "logistics_equipment"
  ],
  "special_designs": [],
  "design_defects": [],
  "tags": [
    "series.aui.hermes"
  ]
}
```
