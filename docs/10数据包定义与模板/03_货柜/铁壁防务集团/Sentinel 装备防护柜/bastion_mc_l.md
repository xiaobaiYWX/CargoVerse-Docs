# BDS Sentinel 装备防护柜 L 型

> **【已实现】实际物品货柜，已采用最终结构。**

[铁壁防务集团](<../README.md>) → [Sentinel 装备防护柜](<README.md>) → L 型

## 职责与使用边界

合并 Bastion 为 S/M/L/X 封闭防护线，与 Vulcan 同保护竞争，以较低成本换较小容量和较高空重。

- 目标形态：独立固体 solid。
- 当前 JSON 承载：独立固体 solid。
- 当前生效保护：防震 V、防潮 D、定向固定 O。
- 完整目标保护：防震、防潮、定向固定。
- 使用边界：不限定武器工具护甲；不支持裸液体、气体或活物。
- 典型内容：武器工具护甲、民用仪器、普通玻璃和瓶件。仅为例子，同形态同条件的物品不因行业或制造商被排除。
- 当前阶段：本期物品，可制造。

保护外观不等于程序效果。遮光、温控、生态维持和放射性屏蔽等未列入“当前生效保护”的部分只能作为后续结构预留，不能标成已经实装。

## 定义

| 项目 | 内容 |
| --- | --- |
| 资源 ID | `cargoverse:bds/bastion_mc_l` |
| 定义文件 | [bastion_mc_l.json](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/bds/bastion_mc_l.json>) |
| 制造商 | 铁壁防务集团（`cargoverse:bds`） |
| 系列 | Sentinel 装备防护柜 |
| 尺寸等级 | L |
| 普通调度点 | 4 |
| 结算单位 | `cargoverse:void_byte` |
| 标签 | `series.bds.bastion` |

## 数值

| 指标 | 当前定义值 |
| --- | --- |
| 容量 | 240 个实际物品 |
| 空柜目标质量 | 135 Kpg |
| 分类容量修正 | 无，使用定义容量 |

空重为配置目标，实际基础质量取模板结构质量与配置空重的较大值；载货质量另算。型号 ID 的后缀不替代实际尺寸或接口。

## CargoClass 兼容与保护

允许：独立固体（solid）。

当前生效保护：`cargoverse:fragile`、`cargoverse:moisture_proof`、`cargoverse:keep_upright`。

设计缺陷：无。未实现的目标保护不产生程序效果；准入与完整组件校验仍独立执行。

## 结构模板

| 项目 | 实际配置 |
| --- | --- |
| 定义 | [cargoverse:bds/bastion_mc_l](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/bds/bastion_mc_l.json>) |
| 名称／规格 | BDS Sentinel 装备防护柜 L 型／L |
| 结构 ID | `cargoverse:cargo/bds/bastion/bds_bastion_mc_l` |
| NBT | [项目结构文件](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/bds/bastion/bds_bastion_mc_l.nbt>) |
| 包络 X×Y×Z | 11×6×11 |
| 实际接口 | 磁吸板×44 |
| 运行标记 | 分类 2、质量 4、词条 10（0～4 齐全） |

## 制造与投放

材料来自操作玩家物品栏，资金使用 VB；不扣贸易点仓库物品。同型号的各站实际配置如下，测试目录不等于正式投放。

| 制造目录 | 许可 | 最低繁荣 | 加工费 VB | 物品材料 |
| --- | --- | ---: | ---: | --- |
| [正式：factory/sky_station/defense_arsenal](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/factory/sky_station/defense_arsenal.json>) | L | 2 | 600 | `minecraft:iron_ingot`×96、`minecraft:chain`×16、`minecraft:leather`×16、`minecraft:piston`×4 |
| [正式：factory/sky_station/security_works](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/factory/sky_station/security_works.json>) | L | 2 | 600 | `minecraft:iron_ingot`×96、`minecraft:chain`×16、`minecraft:leather`×16、`minecraft:piston`×4 |
| [正式：market/sky_station/frontier_garrison](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/market/sky_station/frontier_garrison.json>) | L | 2 | 600 | `minecraft:iron_ingot`×96、`minecraft:chain`×16、`minecraft:leather`×16、`minecraft:piston`×4 |
| [测试：market/test_station/all_containers](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/market/test_station/all_containers.json>) | L | 2 | 600 | `minecraft:iron_ingot`×96、`minecraft:chain`×16、`minecraft:leather`×16、`minecraft:piston`×4 |

[统一制造与投放索引](<../../../08_货柜制造台/制造配方与投放总表.md>)。

## 当前 JSON

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/bds/bastion/bds_bastion_mc_l",
  "manufacturer": "cargoverse:bds",
  "display_name": "BDS Sentinel 装备防护柜 L 型",
  "description": "实际物品运输货柜；承载形态与运输保护以本定义为准。",
  "size_class": "L",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 4,
  "capacity": 240,
  "empty_mass": 135,
  "allowed_cargo_classes": [
    "solid"
  ],
  "special_designs": [
    "cargoverse:fragile",
    "cargoverse:moisture_proof",
    "cargoverse:keep_upright"
  ],
  "design_defects": [],
  "tags": [
    "series.bds.bastion"
  ],
  "cargo_class_capacity_modifiers": {}
}
```

## 验证边界

实际结构与型号参数以当前定义和模板为准；静态校验不代替碰撞、对接、Sable 装配及满载运输实测。已有物理货柜不因文档调整或重载自动换壳。

[返回系列](<README.md>) · [返回制造商](<../README.md>)
