# AUI Atlas 标准干货柜 S 型


[天穹联合工业](<../README.md>) → [Atlas 标准干货柜](<README.md>) → S 型

面向跨行业基础运输，提供广泛的干货兼容性、可靠耐久与标准化维护。

## 定义

| 项目 | 内容 |
| --- | --- |
| 完整型号 | `AUI-Atlas-SD-S` |
| 资源 ID | `cargoverse:aui/atlas_sd_s` |
| 定义文件 | [atlas_sd_s.json](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/aui/atlas_sd_s.json>) |
| 制造商 | 天穹联合工业 / Aether Union Industries（`cargoverse:aui`） |
| 系列全称 | Atlas 标准干货柜 |
| 尺寸等级 | S |
| 调度点 | 1 |
| 结算单位 | `cargoverse:void_byte` |
| 标签 | `series.aui.atlas` |

## 结构模板

**正式模板已提供。** 当前引用：`cargoverse:cargo/aui/atlas/aui_atlas_sd_s`。结构文件存在，尚未在本轮重新验证游戏内碰撞、接口与实际质量。

[当前 NBT 文件](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/aui/atlas/aui_atlas_sd_s.nbt>) · [缺失模板总表](<../../缺失结构模板.md>)

## 数值

| 指标 | 定义基础值 | 默认实际值（含厂商通用倍率） |
| --- | --- | --- |
| 容量（t） | 10 | 11 |
| 空柜目标质量（Kpg） | 20 | 20 |
| 最大耐久 | 100 | 100 |

天穹联合工业：容量 ×1.1，空重与耐久不变。 指定货物容量按所有适用倍率相乘后一次向下取整，不能先取整默认容量再乘专项倍率。目标空重仍受结构中非货柜方块质量下限约束。

## CargoClass 兼容

| 分类 | CargoClass | 当前 CargoGood 数 |
| --- | --- | --- |
| 农业产品 | `agriculture` | 5 |
| 原始资源 | `raw_resource` | 4 |
| 半成品资源 | `processed_resource` | 4 |
| 精加工资源 | `refined_resource` | 4 |
| 机械零件 | `mechanical_parts` | 5 |
| 建筑材料 | `construction_material` | 4 |
| 日常通用补给 | `general_supplies` | 4 |
| 工具器械 | `tools_equipment` | 4 |

仅允许上表分类，`none` 与其他未列出分类均不可装载。同一允许分类下的货物均可选择，但不能混装不同 CargoGood。

## 防护与运输要求

消除：无。

设计缺陷：无。未被消除的货物运输要求继续生效；所有型号保留 `time_limit`。御寒不代表恒温冷藏，防潮不代表抗腐蚀。

## 制造与投放

| 项目 | v2 实体材料设计 |
| --- | --- |
| 加工费 | 80 VB |
| 实体材料 | 铁锭 ×16、橡木木板 ×8、玻璃 ×4、红石 ×2 |
| 最低许可证 | S |
| 最低繁荣等级 | 0 |
| 材料最少占格 | 4 格，按每种物品 64 堆叠 |
| 当前配方状态 | 默认测试点已实装；新增站点目录待接入 |

正式提供节点：[标准建材装配港](<../../../07_贸易点/factory/标准建材装配港/货柜制造台定义.md>)（仅抽中工坊时）、[通用机电装备厂](<../../../07_贸易点/factory/通用机电装备厂/货柜制造台定义.md>)（固定中心）。同型号跨站使用同一配方与加工费。材料来自玩家随身物品栏，不扣贸易点库存；正常占用 1 调度点，基础领取另行处理。

[统一配方与定价依据](<../../../08_货柜制造台/制造配方与投放总表.md>)。当前 Atlas S 材料、80 VB 与繁荣 0 均保持实装值。

## 当前 JSON

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/aui/atlas/aui_atlas_sd_s",
  "manufacturer": "cargoverse:aui",
  "display_name": "AUI Atlas 标准干货柜 S 型",
  "description": "§lAUI Atlas 标准干货柜 S 型\n§r§7面向跨行业基础运输，提供广泛的干货兼容性、可靠耐久与标准化维护。\n§r§l制造商：天穹联合工业 / Aether Union Industries\n§r§l系列：Atlas 标准干货柜",
  "size_class": "S",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 1,
  "capacity": 10,
  "empty_mass": 20,
  "max_durability": 100,
  "allowed_cargo_classes": [
    "agriculture",
    "raw_resource",
    "processed_resource",
    "refined_resource",
    "mechanical_parts",
    "construction_material",
    "general_supplies",
    "tools_equipment"
  ],
  "special_designs": [],
  "design_defects": [],
  "tags": [
    "series.aui.atlas"
  ]
}
```

## 基础运输权益

本型号同时作为天穹联合工业的[初始基础货柜](<../../../05_基础货柜/aui_basic.md>)。注册终端领取的基础资产占 **0 调度点**；普通购买／制造的同型号仍占 1 点。型号 JSON 中的 `dispatch_points` 保持普通版本成本，豁免依据资产标记。
