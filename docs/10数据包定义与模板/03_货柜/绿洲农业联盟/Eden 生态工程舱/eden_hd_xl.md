# VBS Eden 生态工程舱 XL 型

[绿洲农业联盟](<../README.md>) → [Eden 生态工程舱](<README.md>) → XL 型

承运大型生态工程模块、活体及配套设备，采用缓冲、固定与御寒设计服务生态拓殖。

## 定义

| 项目 | 内容 |
| --- | --- |
| 完整型号 | `VBS-Eden-HD-XL` |
| 资源 ID | `cargoverse:vbs/eden_hd_xl` |
| 定义文件 | [eden_hd_xl.json](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/vbs/eden_hd_xl.json>) |
| 制造商 | 绿洲农业联盟 / Verdant BioSystems（`cargoverse:vbs`） |
| 系列全称 | Eden 生态工程舱 |
| 尺寸等级 | XL |
| 调度点 | 8 |
| 结算单位 | `cargoverse:void_byte` |
| 标签 | `series.vbs.eden` |

## 结构模板

**正式模板已提供。** 当前引用：`cargoverse:cargo/vbs/eden/vbs_eden_hd_xl`。结构文件存在，尚未在本轮重新验证游戏内碰撞、接口与实际质量。

[当前 NBT 文件](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/vbs/eden/vbs_eden_hd_xl.nbt>) · [缺失模板总表](<../../缺失结构模板.md>)

## 数值

| 指标 | 定义基础值 | 默认实际值（含厂商通用倍率） |
| --- | --- | --- |
| 容量（t） | 96 | 96 |
| 空柜目标质量（Kpg） | 288 | 288 |
| 最大耐久 | 180 | 180 |

绿洲农业联盟：当前 5 种农业货物与 4 种活体货物容量 ×1.25；水产与研究样本不享受该专项倍率。实际装载仍须满足本柜的分类许可。 指定货物容量按所有适用倍率相乘后一次向下取整，不能先取整默认容量再乘专项倍率。目标空重仍受结构中非货柜方块质量下限约束。

## CargoClass 兼容

| 分类 | CargoClass | 当前 CargoGood 数 |
| --- | --- | --- |
| 预制结构 | `prefab_structure` | 6 |
| 活体生物 | `livestock` | 4 |
| 机械设备 | `machinery` | 4 |

仅允许上表分类，`none` 与其他未列出分类均不可装载。同一允许分类下的货物均可选择，但不能混装不同 CargoGood。

## 防护与运输要求

消除：易碎、勿倒置、御寒。对应 `cargoverse:fragile`、`cargoverse:keep_upright`、`cargoverse:cold_proof`。

设计缺陷：无。未被消除的货物运输要求继续生效；所有型号保留 `time_limit`。御寒不代表恒温冷藏，防潮不代表抗腐蚀。

## 制造与投放

| 项目 | 值 |
| --- | --- |
| 规划加工费 | 1800 VB（不含库存材料） |
| 最低许可证 | XL |
| 最低繁荣等级 | 5 |
| 规划节点类型 | 生态拓殖项目、农业设备基地 |
| 当前配方状态 | 待编制材料配方、绑定制造台与供应节点 |

货柜定义已注册，可供系统引用；规划加工费与门槛尚未写入制造配方，不代表现有制造台可购买该型号。

## 当前 JSON

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/vbs/eden/vbs_eden_hd_xl",
  "manufacturer": "cargoverse:vbs",
  "display_name": "VBS Eden 生态工程舱 XL 型",
  "description": "§lVBS Eden 生态工程舱 XL 型\n§r§7承运大型生态工程模块、活体及配套设备，采用缓冲、固定与御寒设计服务生态拓殖。\n§r§l制造商：绿洲农业联盟 / Verdant BioSystems\n§r§l系列：Eden 生态工程舱",
  "size_class": "XL",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 8,
  "capacity": 96,
  "empty_mass": 288,
  "max_durability": 180,
  "allowed_cargo_classes": [
    "prefab_structure",
    "livestock",
    "machinery"
  ],
  "special_designs": [
    "cargoverse:fragile",
    "cargoverse:keep_upright",
    "cargoverse:cold_proof"
  ],
  "design_defects": [],
  "tags": [
    "series.vbs.eden"
  ]
}
```
