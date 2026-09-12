# BDS Sentinel 安防装备柜 S 型

[铁壁防务集团](<../README.md>) → [Sentinel 安防装备柜](<README.md>) → S 型

承运小批安防装备、电子器件与工具，以高耐久结构和缓冲、防潮设计保障航线补给。

## 定义

| 项目 | 内容 |
| --- | --- |
| 完整型号 | `BDS-Sentinel-MC-S` |
| 资源 ID | `cargoverse:bds/sentinel_mc_s` |
| 定义文件 | [sentinel_mc_s.json](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/bds/sentinel_mc_s.json>) |
| 制造商 | 铁壁防务集团 / Bastion Defense Systems（`cargoverse:bds`） |
| 系列全称 | Sentinel 安防装备柜 |
| 尺寸等级 | S |
| 调度点 | 1 |
| 结算单位 | `cargoverse:void_byte` |
| 标签 | `series.bds.sentinel` |

## 结构模板

**正式模板已提供。** 当前引用：`cargoverse:cargo/bds/sentinel/bds_sentinel_mc_s`。结构文件存在，尚未在本轮重新验证游戏内碰撞、接口与实际质量。

[当前 NBT 文件](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/bds/sentinel/bds_sentinel_mc_s.nbt>) · [缺失模板总表](<../../缺失结构模板.md>)

## 数值

| 指标 | 定义基础值 | 默认实际值（含厂商通用倍率） |
| --- | --- | --- |
| 容量（t） | 8 | 8 |
| 空柜目标质量（Kpg） | 28 | 28 |
| 最大耐久 | 180 | 180 |

本厂商当前无额外数值修正。 指定货物容量按所有适用倍率相乘后一次向下取整，不能先取整默认容量再乘专项倍率。目标空重仍受结构中非货柜方块质量下限约束。

## CargoClass 兼容

| 分类 | CargoClass | 当前 CargoGood 数 |
| --- | --- | --- |
| 武器护甲 | `weapon_armor` | 4 |
| 电子设备 | `electronics` | 6 |
| 工具器械 | `tools_equipment` | 4 |

仅允许上表分类，`none` 与其他未列出分类均不可装载。同一允许分类下的货物均可选择，但不能混装不同 CargoGood。

## 防护与运输要求

消除：易碎、防潮。对应 `cargoverse:fragile`、`cargoverse:moisture_proof`。

设计缺陷：无。未被消除的货物运输要求继续生效；所有型号保留 `time_limit`。御寒不代表恒温冷藏，防潮不代表抗腐蚀。

## 制造与投放

| 项目 | 值 |
| --- | --- |
| 规划加工费 | 140 VB（不含库存材料） |
| 最低许可证 | S |
| 最低繁荣等级 | 1 |
| 规划节点类型 | 航线警戒站、小型防务港 |
| 当前配方状态 | 待编制材料配方、绑定制造台与供应节点 |

货柜定义已注册，可供系统引用；规划加工费与门槛尚未写入制造配方，不代表现有制造台可购买该型号。

## 当前 JSON

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/bds/sentinel/bds_sentinel_mc_s",
  "manufacturer": "cargoverse:bds",
  "display_name": "BDS Sentinel 安防装备柜 S 型",
  "description": "§lBDS Sentinel 安防装备柜 S 型\n§r§7承运小批安防装备、电子器件与工具，以高耐久结构和缓冲、防潮设计保障航线补给。\n§r§l制造商：铁壁防务集团 / Bastion Defense Systems\n§r§l系列：Sentinel 安防装备柜",
  "size_class": "S",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 1,
  "capacity": 8,
  "empty_mass": 28,
  "max_durability": 180,
  "allowed_cargo_classes": [
    "weapon_armor",
    "electronics",
    "tools_equipment"
  ],
  "special_designs": [
    "cargoverse:fragile",
    "cargoverse:moisture_proof"
  ],
  "design_defects": [],
  "tags": [
    "series.bds.sentinel"
  ]
}
```

## 基础运输权益

本型号同时作为铁壁防务集团的[初始基础货柜](<../../../05_基础货柜/bds_basic.md>)。注册终端领取的基础资产占 **0 调度点**；普通购买／制造的同型号仍占 1 点。型号 JSON 中的 `dispatch_points` 保持普通版本成本，豁免依据资产标记。
