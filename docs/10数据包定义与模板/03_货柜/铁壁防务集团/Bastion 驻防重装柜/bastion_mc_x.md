# BDS Bastion 驻防重装柜 X 型

[铁壁防务集团](<../README.md>) → [Bastion 驻防重装柜](<README.md>) → X 型

面向驻防装备、巡逻载具与维护物资运输，以坚固外壳及缓冲、防潮设计保障驻地供给。

## 定义

| 项目 | 内容 |
| --- | --- |
| 完整型号 | `BDS-Bastion-MC-X` |
| 资源 ID | `cargoverse:bds/bastion_mc_x` |
| 定义文件 | [bastion_mc_x.json](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/bds/bastion_mc_x.json>) |
| 制造商 | 铁壁防务集团 / Bastion Defense Systems（`cargoverse:bds`） |
| 系列全称 | Bastion 驻防重装柜 |
| 尺寸等级 | X |
| 调度点 | 6 |
| 结算单位 | `cargoverse:void_byte` |
| 标签 | `series.bds.bastion` |

## 结构模板

**正式模板已提供。** 当前引用：`cargoverse:cargo/bds/bastion/bds_bastion_mc_x`。结构文件存在，尚未在本轮重新验证游戏内碰撞、接口与实际质量。

[当前 NBT 文件](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/bds/bastion/bds_bastion_mc_x.nbt>) · [缺失模板总表](<../../缺失结构模板.md>)

## 数值

| 指标 | 定义基础值 | 默认实际值（含厂商通用倍率） |
| --- | --- | --- |
| 容量（t） | 52 | 52 |
| 空柜目标质量（Kpg） | 168 | 168 |
| 最大耐久 | 220 | 220 |

本厂商当前无额外数值修正。 指定货物容量按所有适用倍率相乘后一次向下取整，不能先取整默认容量再乘专项倍率。目标空重仍受结构中非货柜方块质量下限约束。

## CargoClass 兼容

| 分类 | CargoClass | 当前 CargoGood 数 |
| --- | --- | --- |
| 武器护甲 | `weapon_armor` | 4 |
| 完整载具 | `vehicle` | 4 |
| 日常通用补给 | `general_supplies` | 4 |
| 机械零件 | `mechanical_parts` | 5 |

仅允许上表分类，`none` 与其他未列出分类均不可装载。同一允许分类下的货物均可选择，但不能混装不同 CargoGood。

## 防护与运输要求

消除：易碎、防潮。对应 `cargoverse:fragile`、`cargoverse:moisture_proof`。

设计缺陷：无。未被消除的货物运输要求继续生效；所有型号保留 `time_limit`。御寒不代表恒温冷藏，防潮不代表抗腐蚀。

## 制造与投放

| 项目 | 值 |
| --- | --- |
| 规划加工费 | 1050 VB（不含库存材料） |
| 最低许可证 | X |
| 最低繁荣等级 | 4 |
| 规划节点类型 | 驻防基地、巡逻艇基地 |
| 当前配方状态 | 待编制材料配方、绑定制造台与供应节点 |

货柜定义已注册，可供系统引用；规划加工费与门槛尚未写入制造配方，不代表现有制造台可购买该型号。

## 当前 JSON

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/bds/bastion/bds_bastion_mc_x",
  "manufacturer": "cargoverse:bds",
  "display_name": "BDS Bastion 驻防重装柜 X 型",
  "description": "§lBDS Bastion 驻防重装柜 X 型\n§r§7面向驻防装备、巡逻载具与维护物资运输，以坚固外壳及缓冲、防潮设计保障驻地供给。\n§r§l制造商：铁壁防务集团 / Bastion Defense Systems\n§r§l系列：Bastion 驻防重装柜",
  "size_class": "X",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 6,
  "capacity": 52,
  "empty_mass": 168,
  "max_durability": 220,
  "allowed_cargo_classes": [
    "weapon_armor",
    "vehicle",
    "general_supplies",
    "mechanical_parts"
  ],
  "special_designs": [
    "cargoverse:fragile",
    "cargoverse:moisture_proof"
  ],
  "design_defects": [],
  "tags": [
    "series.bds.bastion"
  ]
}
```
