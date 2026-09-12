# SPL Cargo 干线周转柜 M 型

[云港物流集团](<../README.md>) → [Cargo 干线周转柜](<README.md>) → M 型

面向区域集散与干线周转，以较低空重和制造费提高常规干货运输效率。

## 定义

| 项目 | 内容 |
| --- | --- |
| 完整型号 | `SPL-Cargo-MC-M` |
| 资源 ID | `cargoverse:spl/cargo_mc_m` |
| 定义文件 | [cargo_mc_m.json](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/spl/cargo_mc_m.json>) |
| 制造商 | 云港物流集团 / Skyport Logistics（`cargoverse:spl`） |
| 系列全称 | Cargo 干线周转柜 |
| 尺寸等级 | M |
| 调度点 | 2 |
| 结算单位 | `cargoverse:void_byte` |
| 标签 | `series.spl.cargo` |

## 结构模板

**正式模板已提供。** 当前引用：`cargoverse:cargo/spl/cargo/spl_cargo_mc_m`。结构文件存在，尚未在本轮重新验证游戏内碰撞、接口与实际质量。

[当前 NBT 文件](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/spl/cargo/spl_cargo_mc_m.nbt>) · [缺失模板总表](<../../缺失结构模板.md>)

## 数值

| 指标 | 定义基础值 | 默认实际值（含厂商通用倍率） |
| --- | --- | --- |
| 容量（t） | 22 | 22 |
| 空柜目标质量（Kpg） | 36 | 36 |
| 最大耐久 | 90 | 90 |

本厂商当前无额外数值修正。 指定货物容量按所有适用倍率相乘后一次向下取整，不能先取整默认容量再乘专项倍率。目标空重仍受结构中非货柜方块质量下限约束。

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

仅允许上表分类，`none` 与其他未列出分类均不可装载。同一允许分类下的货物均可选择，但不能混装不同 CargoGood。

## 防护与运输要求

消除：无。

设计缺陷：无。未被消除的货物运输要求继续生效；所有型号保留 `time_limit`。御寒不代表恒温冷藏，防潮不代表抗腐蚀。

## 制造与投放

| 项目 | 值 |
| --- | --- |
| 规划加工费 | 140 VB（不含库存材料） |
| 最低许可证 | M |
| 最低繁荣等级 | 2 |
| 规划节点类型 | 区域集散港、干线物流站 |
| 当前配方状态 | 待编制材料配方、绑定制造台与供应节点 |

货柜定义已注册，可供系统引用；规划加工费与门槛尚未写入制造配方，不代表现有制造台可购买该型号。

## 当前 JSON

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/spl/cargo/spl_cargo_mc_m",
  "manufacturer": "cargoverse:spl",
  "display_name": "SPL Cargo 干线周转柜 M 型",
  "description": "§lSPL Cargo 干线周转柜 M 型\n§r§7面向区域集散与干线周转，以较低空重和制造费提高常规干货运输效率。\n§r§l制造商：云港物流集团 / Skyport Logistics\n§r§l系列：Cargo 干线周转柜",
  "size_class": "M",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 2,
  "capacity": 22,
  "empty_mass": 36,
  "max_durability": 90,
  "allowed_cargo_classes": [
    "agriculture",
    "raw_resource",
    "processed_resource",
    "refined_resource",
    "mechanical_parts",
    "construction_material",
    "general_supplies"
  ],
  "special_designs": [],
  "design_defects": [],
  "tags": [
    "series.spl.cargo"
  ]
}
```
