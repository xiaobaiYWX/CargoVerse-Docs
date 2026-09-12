# BDS Fortress 工事运输堡 XL 型

[铁壁防务集团](<../README.md>) → [Fortress 工事运输堡](<README.md>) → XL 型

承运大型防御工事、建材和配套装备，以高耐久结构、缓冲及固定设计保障工程交付。

## 定义

| 项目 | 内容 |
| --- | --- |
| 完整型号 | `BDS-Fortress-HD-XL` |
| 资源 ID | `cargoverse:bds/fortress_hd_xl` |
| 定义文件 | [fortress_hd_xl.json](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/bds/fortress_hd_xl.json>) |
| 制造商 | 铁壁防务集团 / Bastion Defense Systems（`cargoverse:bds`） |
| 系列全称 | Fortress 工事运输堡 |
| 尺寸等级 | XL |
| 调度点 | 8 |
| 结算单位 | `cargoverse:void_byte` |
| 标签 | `series.bds.fortress` |

## 结构模板

**正式模板已更新。** 当前引用：`cargoverse:cargo/bds/fortress/bds_fortress_hd_xl`。

已同步开发存档中的新版 NBT，包络尺寸（X × Y × Z）：**16 × 16 × 16** 方块，体积 4096 方块³。NBT 与复制校验通过；货柜数值保持不变，游戏内连接、碰撞与实际质量仍待实测。

[当前 NBT 文件](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/bds/fortress/bds_fortress_hd_xl.nbt>) · [缺失模板总表](<../../缺失结构模板.md>)

## 数值

| 指标 | 定义基础值 | 默认实际值（含厂商通用倍率） |
| --- | --- | --- |
| 容量（t） | 72 | 72 |
| 空柜目标质量（Kpg） | 288 | 288 |
| 最大耐久 | 300 | 300 |

本厂商当前无额外数值修正。 指定货物容量按所有适用倍率相乘后一次向下取整，不能先取整默认容量再乘专项倍率。目标空重仍受结构中非货柜方块质量下限约束。

## CargoClass 兼容

| 分类 | CargoClass | 当前 CargoGood 数 |
| --- | --- | --- |
| 预制结构 | `prefab_structure` | 6 |
| 建筑材料 | `construction_material` | 4 |
| 武器护甲 | `weapon_armor` | 4 |
| 机械设备 | `machinery` | 4 |

仅允许上表分类，`none` 与其他未列出分类均不可装载。同一允许分类下的货物均可选择，但不能混装不同 CargoGood。

## 防护与运输要求

消除：易碎、勿倒置。对应 `cargoverse:fragile`、`cargoverse:keep_upright`。

设计缺陷：无。未被消除的货物运输要求继续生效；所有型号保留 `time_limit`。御寒不代表恒温冷藏，防潮不代表抗腐蚀。

## 制造与投放

| 项目 | 值 |
| --- | --- |
| 规划加工费 | 2280 VB（不含库存材料） |
| 最低许可证 | XL |
| 最低繁荣等级 | 5 |
| 规划节点类型 | 防御工程集散地 |
| 当前配方状态 | 待编制材料配方、绑定制造台与供应节点 |

货柜定义已注册，可供系统引用；规划加工费与门槛尚未写入制造配方，不代表现有制造台可购买该型号。

## 当前 JSON

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/bds/fortress/bds_fortress_hd_xl",
  "manufacturer": "cargoverse:bds",
  "display_name": "BDS Fortress 工事运输堡 XL 型",
  "description": "§lBDS Fortress 工事运输堡 XL 型\n§r§7承运大型防御工事、建材和配套装备，以高耐久结构、缓冲及固定设计保障工程交付。\n§r§l制造商：铁壁防务集团 / Bastion Defense Systems\n§r§l系列：Fortress 工事运输堡",
  "size_class": "XL",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 8,
  "capacity": 72,
  "empty_mass": 288,
  "max_durability": 300,
  "allowed_cargo_classes": [
    "prefab_structure",
    "construction_material",
    "weapon_armor",
    "machinery"
  ],
  "special_designs": [
    "cargoverse:fragile",
    "cargoverse:keep_upright"
  ],
  "design_defects": [],
  "tags": [
    "series.bds.fortress"
  ]
}
```
