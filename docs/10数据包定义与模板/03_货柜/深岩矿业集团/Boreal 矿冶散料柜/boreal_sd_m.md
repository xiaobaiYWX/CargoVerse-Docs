# DMC Boreal 矿冶散料柜 M 型


[深岩矿业集团](<../README.md>) → [Boreal 矿冶散料柜](<README.md>) → M 型

承运原矿、精矿和冶炼材料，结合矿业承载设计与耐用结构服务矿冶供应链。

## 定义

| 项目 | 内容 |
| --- | --- |
| 完整型号 | `DMC-Boreal-SD-M` |
| 资源 ID | `cargoverse:dmc/boreal_sd_m` |
| 定义文件 | [boreal_sd_m.json](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/dmc/boreal_sd_m.json>) |
| 制造商 | 深岩矿业集团 / Deepcore Mining Corporation（`cargoverse:dmc`） |
| 系列全称 | Boreal 矿冶散料柜 |
| 尺寸等级 | M |
| 调度点 | 2 |
| 结算单位 | `cargoverse:void_byte` |
| 标签 | `series.dmc.boreal` |

## 结构模板

**正式模板已提供。** 当前引用：`cargoverse:cargo/dmc/boreal/dmc_boreal_sd_m`。结构文件存在，尚未在本轮重新验证游戏内碰撞、接口与实际质量。

[当前 NBT 文件](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/dmc/boreal/dmc_boreal_sd_m.nbt>) · [缺失模板总表](<../../缺失结构模板.md>)

## 数值

| 指标 | 定义基础值 | 默认实际值（含厂商通用倍率） |
| --- | --- | --- |
| 容量（t） | 24 | 24 |
| 空柜目标质量（Kpg） | 44 | 57.2 |
| 最大耐久 | 130 | 195 |

深岩矿业集团：空重 ×1.3、耐久 ×1.5；赤铁原矿与铜原矿另享容量 ×1.3，精矿和其他稀材不享受该专项倍率。 指定货物容量按所有适用倍率相乘后一次向下取整，不能先取整默认容量再乘专项倍率。目标空重仍受结构中非货柜方块质量下限约束。

## CargoClass 兼容

| 分类 | CargoClass | 当前 CargoGood 数 |
| --- | --- | --- |
| 原始资源 | `raw_resource` | 4 |
| 半成品资源 | `processed_resource` | 4 |
| 精加工资源 | `refined_resource` | 4 |

仅允许上表分类，`none` 与其他未列出分类均不可装载。同一允许分类下的货物均可选择，但不能混装不同 CargoGood。

## 防护与运输要求

消除：无。

设计缺陷：无。未被消除的货物运输要求继续生效；所有型号保留 `time_limit`。御寒不代表恒温冷藏，防潮不代表抗腐蚀。

## 制造与投放

| 项目 | v2 实体材料设计 |
| --- | --- |
| 加工费 | 180 VB |
| 实体材料 | 铁锭 ×40、铜锭 ×16、锁链 ×8、红石 ×4 |
| 最低许可证 | M |
| 最低繁荣等级 | 1 |
| 材料最少占格 | 4 格，按每种物品 64 堆叠 |
| 当前配方状态 | 配方设计完成，尚未写入运行时制造定义 |

正式提供节点：[重工材料与矿机厂](<../../../07_贸易点/factory/重工材料与矿机厂/货柜制造台定义.md>)（固定中心）、[深岩露天矿站](<../../../07_贸易点/resource/深岩露天矿站/货柜制造台定义.md>)（仅抽中工坊时）。同型号跨站使用同一配方与加工费。材料来自玩家随身物品栏，不扣贸易点库存；正常占用 2 调度点，基础领取另行处理。

[统一配方与定价依据](<../../../08_货柜制造台/制造配方与投放总表.md>)。数值为首轮设计目标，尚未完成实机平衡。

## 当前 JSON

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/dmc/boreal/dmc_boreal_sd_m",
  "manufacturer": "cargoverse:dmc",
  "display_name": "DMC Boreal 矿冶散料柜 M 型",
  "description": "§lDMC Boreal 矿冶散料柜 M 型\n§r§7承运原矿、精矿和冶炼材料，结合矿业承载设计与耐用结构服务矿冶供应链。\n§r§l制造商：深岩矿业集团 / Deepcore Mining Corporation\n§r§l系列：Boreal 矿冶散料柜",
  "size_class": "M",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 2,
  "capacity": 24,
  "empty_mass": 44,
  "max_durability": 130,
  "allowed_cargo_classes": [
    "raw_resource",
    "processed_resource",
    "refined_resource"
  ],
  "special_designs": [],
  "design_defects": [],
  "tags": [
    "series.dmc.boreal"
  ]
}
```

## 基础运输权益

本型号同时作为深岩矿业集团的[初始基础货柜](<../../../05_基础货柜/dmc_basic.md>)。注册终端领取的基础资产占 **0 调度点**；普通购买／制造的同型号仍占 2 点。型号 JSON 中的 `dispatch_points` 保持普通版本成本，豁免依据资产标记。
