# HEC Apollo 燃料化工柜 L 型

[赫利俄斯能源集团](<../README.md>) → [Apollo 燃料化工柜](<README.md>) → L 型

面向燃料与工业化学材料供应，使用防火、防潮和固定设计满足能源运输需求。

## 定义

| 项目 | 内容 |
| --- | --- |
| 完整型号 | `HEC-Apollo-SD-L` |
| 资源 ID | `cargoverse:hec/apollo_sd_l` |
| 定义文件 | [apollo_sd_l.json](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/hec/apollo_sd_l.json>) |
| 制造商 | 赫利俄斯能源集团 / Helios Energy Corporation（`cargoverse:hec`） |
| 系列全称 | Apollo 燃料化工柜 |
| 尺寸等级 | L |
| 调度点 | 4 |
| 结算单位 | `cargoverse:void_byte` |
| 标签 | `series.hec.apollo` |

## 结构模板

**正式模板已提供。** 当前引用：`cargoverse:cargo/hec/apollo/hec_apollo_sd_l`。结构文件存在，尚未在本轮重新验证游戏内碰撞、接口与实际质量。

[当前 NBT 文件](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/hec/apollo/hec_apollo_sd_l.nbt>) · [缺失模板总表](<../../缺失结构模板.md>)

## 数值

| 指标 | 定义基础值 | 默认实际值（含厂商通用倍率） |
| --- | --- | --- |
| 容量（t） | 40 | 40 |
| 空柜目标质量（Kpg） | 112 | 112 |
| 最大耐久 | 130 | 130 |

本厂商当前无额外数值修正。 指定货物容量按所有适用倍率相乘后一次向下取整，不能先取整默认容量再乘专项倍率。目标空重仍受结构中非货柜方块质量下限约束。

## CargoClass 兼容

| 分类 | CargoClass | 当前 CargoGood 数 |
| --- | --- | --- |
| 能源燃料 | `energy_fuel` | 4 |
| 化工原料 | `chemical_material` | 5 |

仅允许上表分类，`none` 与其他未列出分类均不可装载。同一允许分类下的货物均可选择，但不能混装不同 CargoGood。

## 防护与运输要求

消除：易燃、勿倒置、防潮。对应 `cargoverse:flammable`、`cargoverse:keep_upright`、`cargoverse:moisture_proof`。

设计缺陷：无。未被消除的货物运输要求继续生效；所有型号保留 `time_limit`。御寒不代表恒温冷藏，防潮不代表抗腐蚀。

## 制造与投放

| 项目 | 值 |
| --- | --- |
| 规划加工费 | 440 VB（不含库存材料） |
| 最低许可证 | L |
| 最低繁荣等级 | 3 |
| 规划节点类型 | 能源补给站、化工厂 |
| 当前配方状态 | 待编制材料配方、绑定制造台与供应节点 |

货柜定义已注册，可供系统引用；规划加工费与门槛尚未写入制造配方，不代表现有制造台可购买该型号。

## 当前 JSON

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/hec/apollo/hec_apollo_sd_l",
  "manufacturer": "cargoverse:hec",
  "display_name": "HEC Apollo 燃料化工柜 L 型",
  "description": "§lHEC Apollo 燃料化工柜 L 型\n§r§7面向燃料与工业化学材料供应，使用防火、防潮和固定设计满足能源运输需求。\n§r§l制造商：赫利俄斯能源集团 / Helios Energy Corporation\n§r§l系列：Apollo 燃料化工柜",
  "size_class": "L",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 4,
  "capacity": 40,
  "empty_mass": 112,
  "max_durability": 130,
  "allowed_cargo_classes": [
    "energy_fuel",
    "chemical_material"
  ],
  "special_designs": [
    "cargoverse:flammable",
    "cargoverse:keep_upright",
    "cargoverse:moisture_proof"
  ],
  "design_defects": [],
  "tags": [
    "series.hec.apollo"
  ]
}
```
