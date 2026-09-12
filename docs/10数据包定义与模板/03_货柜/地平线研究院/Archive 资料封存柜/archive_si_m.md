# HRI Archive 资料封存柜 M 型

[地平线研究院](<../README.md>) → [Archive 资料封存柜](<README.md>) → M 型

为地平线研究院封存资料、文物与异常介质，采用缓冲、防潮、遮光及固定设计。

## 定义

| 项目 | 内容 |
| --- | --- |
| 完整型号 | `HRI-Archive-SI-M` |
| 资源 ID | `cargoverse:hri/archive_si_m` |
| 定义文件 | [archive_si_m.json](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/hri/archive_si_m.json>) |
| 制造商 | 地平线研究院 / Horizon Research Institute（`cargoverse:hri`） |
| 系列全称 | Archive 资料封存柜 |
| 尺寸等级 | M |
| 调度点 | 2 |
| 结算单位 | `cargoverse:void_byte` |
| 标签 | `series.hri.archive` |

## 结构模板

**正式模板已提供。** 当前引用：`cargoverse:cargo/hri/archive/hri_archive_si_m`。结构文件存在，尚未在本轮重新验证游戏内碰撞、接口与实际质量。

[当前 NBT 文件](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/hri/archive/hri_archive_si_m.nbt>) · [缺失模板总表](<../../缺失结构模板.md>)

## 数值

| 指标 | 定义基础值 | 默认实际值（含厂商通用倍率） |
| --- | --- | --- |
| 容量（t） | 16 | 12 |
| 空柜目标质量（Kpg） | 60 | 66 |
| 最大耐久 | 130 | 169 |

地平线研究院：容量 ×0.8、空重 ×1.1、耐久 ×1.3。 指定货物容量按所有适用倍率相乘后一次向下取整，不能先取整默认容量再乘专项倍率。目标空重仍受结构中非货柜方块质量下限约束。

## CargoClass 兼容

| 分类 | CargoClass | 当前 CargoGood 数 |
| --- | --- | --- |
| 电子设备 | `electronics` | 6 |
| 贵重物品 | `valuables` | 4 |
| 异常货物 | `anomalous_cargo` | 4 |

仅允许上表分类，`none` 与其他未列出分类均不可装载。同一允许分类下的货物均可选择，但不能混装不同 CargoGood。

## 防护与运输要求

消除：易碎、防潮、避光、勿倒置。对应 `cargoverse:fragile`、`cargoverse:moisture_proof`、`cargoverse:light_sensitive`、`cargoverse:keep_upright`。

设计缺陷：无。未被消除的货物运输要求继续生效；所有型号保留 `time_limit`。御寒不代表恒温冷藏，防潮不代表抗腐蚀。

## 制造与投放

| 项目 | 值 |
| --- | --- |
| 规划加工费 | 400 VB（不含库存材料） |
| 最低许可证 | M |
| 最低繁荣等级 | 2 |
| 规划节点类型 | 地平线研究院资料站、遗迹研究中心 |
| 当前配方状态 | 待编制材料配方、绑定制造台与供应节点 |

货柜定义已注册，可供系统引用；规划加工费与门槛尚未写入制造配方，不代表现有制造台可购买该型号。

## 当前 JSON

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/hri/archive/hri_archive_si_m",
  "manufacturer": "cargoverse:hri",
  "display_name": "HRI Archive 资料封存柜 M 型",
  "description": "§lHRI Archive 资料封存柜 M 型\n§r§7为地平线研究院封存资料、文物与异常介质，采用缓冲、防潮、遮光及固定设计。\n§r§l制造商：地平线研究院 / Horizon Research Institute\n§r§l系列：Archive 资料封存柜",
  "size_class": "M",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 2,
  "capacity": 16,
  "empty_mass": 60,
  "max_durability": 130,
  "allowed_cargo_classes": [
    "electronics",
    "valuables",
    "anomalous_cargo"
  ],
  "special_designs": [
    "cargoverse:fragile",
    "cargoverse:moisture_proof",
    "cargoverse:light_sensitive",
    "cargoverse:keep_upright"
  ],
  "design_defects": [],
  "tags": [
    "series.hri.archive"
  ]
}
```
