# AUI Titan 大宗结构柜 L 型

[天穹联合工业](<../README.md>) → [Titan 大宗结构柜](<README.md>) → L 型

面向金属、钢梁和结构模块的大宗运输，以较高装载容量承接大型工程货流。

## 定义

| 项目 | 内容 |
| --- | --- |
| 完整型号 | `AUI-Titan-HD-L` |
| 资源 ID | `cargoverse:aui/titan_hd_l` |
| 定义文件 | [titan_hd_l.json](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/aui/titan_hd_l.json>) |
| 制造商 | 天穹联合工业 / Aether Union Industries（`cargoverse:aui`） |
| 系列全称 | Titan 大宗结构柜 |
| 尺寸等级 | L |
| 调度点 | 4 |
| 结算单位 | `cargoverse:void_byte` |
| 标签 | `series.aui.titan` |

## 结构模板

**正式模板已提供。** 当前引用：`cargoverse:cargo/aui/titan/aui_titan_hd_l`。结构文件存在，尚未在本轮重新验证游戏内碰撞、接口与实际质量。

[当前 NBT 文件](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/aui/titan/aui_titan_hd_l.nbt>) · [缺失模板总表](<../../缺失结构模板.md>)

## 数值

| 指标 | 定义基础值 | 默认实际值（含厂商通用倍率） |
| --- | --- | --- |
| 容量（t） | 48 | 52 |
| 空柜目标质量（Kpg） | 100 | 100 |
| 最大耐久 | 150 | 150 |

天穹联合工业：容量 ×1.1，空重与耐久不变。 指定货物容量按所有适用倍率相乘后一次向下取整，不能先取整默认容量再乘专项倍率。目标空重仍受结构中非货柜方块质量下限约束。

## CargoClass 兼容

| 分类 | CargoClass | 当前 CargoGood 数 |
| --- | --- | --- |
| 原始资源 | `raw_resource` | 4 |
| 半成品资源 | `processed_resource` | 4 |
| 精加工资源 | `refined_resource` | 4 |
| 建筑材料 | `construction_material` | 4 |
| 预制结构 | `prefab_structure` | 6 |

仅允许上表分类，`none` 与其他未列出分类均不可装载。同一允许分类下的货物均可选择，但不能混装不同 CargoGood。

## 防护与运输要求

消除：无。

设计缺陷：无。未被消除的货物运输要求继续生效；所有型号保留 `time_limit`。御寒不代表恒温冷藏，防潮不代表抗腐蚀。

## 制造与投放

| 项目 | 值 |
| --- | --- |
| 规划加工费 | 400 VB（不含库存材料） |
| 最低许可证 | L |
| 最低繁荣等级 | 3 |
| 规划节点类型 | 大型造船港、建材集散站 |
| 当前配方状态 | 待编制材料配方、绑定制造台与供应节点 |

货柜定义已注册，可供系统引用；规划加工费与门槛尚未写入制造配方，不代表现有制造台可购买该型号。

## 当前 JSON

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/aui/titan/aui_titan_hd_l",
  "manufacturer": "cargoverse:aui",
  "display_name": "AUI Titan 大宗结构柜 L 型",
  "description": "§lAUI Titan 大宗结构柜 L 型\n§r§7面向金属、钢梁和结构模块的大宗运输，以较高装载容量承接大型工程货流。\n§r§l制造商：天穹联合工业 / Aether Union Industries\n§r§l系列：Titan 大宗结构柜",
  "size_class": "L",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 4,
  "capacity": 48,
  "empty_mass": 100,
  "max_durability": 150,
  "allowed_cargo_classes": [
    "raw_resource",
    "processed_resource",
    "refined_resource",
    "construction_material",
    "prefab_structure"
  ],
  "special_designs": [],
  "design_defects": [],
  "tags": [
    "series.aui.titan"
  ]
}
```
