# DMC TitanHaul 重装运输柜 X 型

[深岩矿业集团](<../README.md>) → [TitanHaul 重装运输柜](<README.md>) → X 型

面向采矿设备、重型载具及重建材的大宗运输，以厚重结构换取高容量与耐久。

## 定义

| 项目 | 内容 |
| --- | --- |
| 完整型号 | `DMC-TitanHaul-HD-X` |
| 资源 ID | `cargoverse:dmc/titanhaul_hd_x` |
| 定义文件 | [titanhaul_hd_x.json](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/dmc/titanhaul_hd_x.json>) |
| 制造商 | 深岩矿业集团 / Deepcore Mining Corporation（`cargoverse:dmc`） |
| 系列全称 | TitanHaul 重装运输柜 |
| 尺寸等级 | X |
| 调度点 | 6 |
| 结算单位 | `cargoverse:void_byte` |
| 标签 | `series.dmc.titanhaul` |

## 结构模板

**正式模板已提供。** 当前引用：`cargoverse:cargo/dmc/titanhaul/dmc_titanhaul_hd_x`。结构文件存在，尚未在本轮重新验证游戏内碰撞、接口与实际质量。

[当前 NBT 文件](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/dmc/titanhaul/dmc_titanhaul_hd_x.nbt>) · [缺失模板总表](<../../缺失结构模板.md>)

## 数值

| 指标 | 定义基础值 | 默认实际值（含厂商通用倍率） |
| --- | --- | --- |
| 容量（t） | 91 | 91 |
| 空柜目标质量（Kpg） | 189 | 245.7 |
| 最大耐久 | 180 | 270 |

深岩矿业集团：空重 ×1.3、耐久 ×1.5；赤铁原矿与铜原矿另享容量 ×1.3，精矿和其他稀材不享受该专项倍率。 指定货物容量按所有适用倍率相乘后一次向下取整，不能先取整默认容量再乘专项倍率。目标空重仍受结构中非货柜方块质量下限约束。

## CargoClass 兼容

| 分类 | CargoClass | 当前 CargoGood 数 |
| --- | --- | --- |
| 原始资源 | `raw_resource` | 4 |
| 机械设备 | `machinery` | 4 |
| 完整载具 | `vehicle` | 4 |
| 建筑材料 | `construction_material` | 4 |

仅允许上表分类，`none` 与其他未列出分类均不可装载。同一允许分类下的货物均可选择，但不能混装不同 CargoGood。

## 防护与运输要求

消除：无。

设计缺陷：无。未被消除的货物运输要求继续生效；所有型号保留 `time_limit`。御寒不代表恒温冷藏，防潮不代表抗腐蚀。

## 制造与投放

| 项目 | 值 |
| --- | --- |
| 规划加工费 | 980 VB（不含库存材料） |
| 最低许可证 | X |
| 最低繁荣等级 | 4 |
| 规划节点类型 | 大型矿区、重工装备港 |
| 当前配方状态 | 待编制材料配方、绑定制造台与供应节点 |

货柜定义已注册，可供系统引用；规划加工费与门槛尚未写入制造配方，不代表现有制造台可购买该型号。

## 当前 JSON

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/dmc/titanhaul/dmc_titanhaul_hd_x",
  "manufacturer": "cargoverse:dmc",
  "display_name": "DMC TitanHaul 重装运输柜 X 型",
  "description": "§lDMC TitanHaul 重装运输柜 X 型\n§r§7面向采矿设备、重型载具及重建材的大宗运输，以厚重结构换取高容量与耐久。\n§r§l制造商：深岩矿业集团 / Deepcore Mining Corporation\n§r§l系列：TitanHaul 重装运输柜",
  "size_class": "X",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 6,
  "capacity": 91,
  "empty_mass": 189,
  "max_durability": 180,
  "allowed_cargo_classes": [
    "raw_resource",
    "machinery",
    "vehicle",
    "construction_material"
  ],
  "special_designs": [],
  "design_defects": [],
  "tags": [
    "series.dmc.titanhaul"
  ]
}
```
