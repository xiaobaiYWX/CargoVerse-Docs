# VBS Harvest 农鲜周转柜 S 型

[绿洲农业联盟](<../README.md>) → [Harvest 农鲜周转柜](<README.md>) → S 型

面向农鲜供应链的周转货柜，提供防潮保护，并发挥绿洲农业联盟的农业装载专长。

## 定义

| 项目 | 内容 |
| --- | --- |
| 完整型号 | `VBS-Harvest-LM-S` |
| 资源 ID | `cargoverse:vbs/harvest_lm_s` |
| 定义文件 | [harvest_lm_s.json](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/vbs/harvest_lm_s.json>) |
| 制造商 | 绿洲农业联盟 / Verdant BioSystems（`cargoverse:vbs`） |
| 系列全称 | Harvest 农鲜周转柜 |
| 尺寸等级 | S |
| 调度点 | 1 |
| 结算单位 | `cargoverse:void_byte` |
| 标签 | `series.vbs.harvest` |

## 结构模板

**正式模板已接入。** 当前引用：`cargoverse:cargo/vbs/harvest/vbs_harvest_lm_s`。

包络尺寸（X × Y × Z）：**6 × 4 × 6** 方块；体积 144 方块³。

模板中的连接部件：`simulated:rope_connector` ×4。已校验压缩 NBT、尺寸、方块位置与调色板索引；游戏内连接、碰撞和实际质量尚未重新实测。

[当前 NBT 文件](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/vbs/harvest/vbs_harvest_lm_s.nbt>) · [模板接入与缺失清单](<../../缺失结构模板.md>)

## 数值

| 指标 | 定义基础值 | 默认实际值（含厂商通用倍率） |
| --- | --- | --- |
| 容量（t） | 12 | 12 |
| 空柜目标质量（Kpg） | 24 | 24 |
| 最大耐久 | 85 | 85 |

绿洲农业联盟：当前 5 种农业货物与 4 种活体货物容量 ×1.25；水产与研究样本不享受该专项倍率。实际装载仍须满足本柜的分类许可。 指定货物容量按所有适用倍率相乘后一次向下取整，不能先取整默认容量再乘专项倍率。目标空重仍受结构中非货柜方块质量下限约束。

## CargoClass 兼容

| 分类 | CargoClass | 当前 CargoGood 数 |
| --- | --- | --- |
| 农业产品 | `agriculture` | 5 |
| 水产生鲜 | `aquatic` | 4 |
| 半成品资源 | `processed_resource` | 4 |
| 日常通用补给 | `general_supplies` | 4 |

仅允许上表分类，`none` 与其他未列出分类均不可装载。同一允许分类下的货物均可选择，但不能混装不同 CargoGood。

## 防护与运输要求

消除：防潮。对应 `cargoverse:moisture_proof`。

设计缺陷：无。未被消除的货物运输要求继续生效；所有型号保留 `time_limit`。御寒不代表恒温冷藏，防潮不代表抗腐蚀。

## 制造与投放

| 项目 | 值 |
| --- | --- |
| 规划加工费 | 90 VB（不含库存材料） |
| 最低许可证 | S |
| 最低繁荣等级 | 1 |
| 规划节点类型 | 农场、农鲜市场 |
| 当前配方状态 | 待编制材料配方、绑定制造台与供应节点 |

货柜定义已注册，可供系统引用；规划加工费与门槛尚未写入制造配方，不代表现有制造台可购买该型号。

## 当前 JSON

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/vbs/harvest/vbs_harvest_lm_s",
  "manufacturer": "cargoverse:vbs",
  "display_name": "VBS Harvest 农鲜周转柜 S 型",
  "description": "§lVBS Harvest 农鲜周转柜 S 型\n§r§7面向农鲜供应链的周转货柜，提供防潮保护，并发挥绿洲农业联盟的农业装载专长。\n§r§l制造商：绿洲农业联盟 / Verdant BioSystems\n§r§l系列：Harvest 农鲜周转柜",
  "size_class": "S",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 1,
  "capacity": 12,
  "empty_mass": 24,
  "max_durability": 85,
  "allowed_cargo_classes": [
    "agriculture",
    "aquatic",
    "processed_resource",
    "general_supplies"
  ],
  "special_designs": [
    "cargoverse:moisture_proof"
  ],
  "design_defects": [],
  "tags": [
    "series.vbs.harvest"
  ]
}
```

## 基础运输权益

本型号同时作为绿洲农业联盟的[初始基础货柜](<../../../05_基础货柜/oasis_basic.md>)。注册终端领取的基础资产占 **0 调度点**；普通购买／制造的同型号仍占 1 点。型号 JSON 中的 `dispatch_points` 保持普通版本成本，豁免依据资产标记。
