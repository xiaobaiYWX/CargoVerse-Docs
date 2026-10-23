# AUI Hermes 轻量干货柜 L 型

> **【已实现】实际物品货柜，已采用最终结构。**

[天穹联合工业](<../README.md>) → [Hermes 轻量干货柜](<README.md>) → L 型

## 职责与使用边界

同厂 Atlas 的明确轻量分支：牺牲容量、提高投入以显著降低空重；与 Courier 竞争重量敏感的运输。

- 目标形态：独立固体 solid。
- 当前 JSON 承载：独立固体 solid。
- 当前生效保护：无专用保护。
- 完整目标保护：基本固定；无专用保护。
- 使用边界：敏感货物无保护；不能因轻量化增加未设计的失效概率。
- 典型内容：低密度制品、纸箱、蒙皮、日常工具。仅为例子，同形态同条件的物品不因行业或制造商被排除。
- 当前阶段：本期物品，可制造。

保护外观不等于程序效果。遮光、温控、生态维持和放射性屏蔽等未列入“当前生效保护”的部分只能作为后续结构预留，不能标成已经实装。

## 定义

| 项目 | 内容 |
| --- | --- |
| 资源 ID | `cargoverse:aui/hermes_mc_l` |
| 定义文件 | [hermes_mc_l.json](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/aui/hermes_mc_l.json>) |
| 制造商 | 天穹联合工业（`cargoverse:aui`） |
| 系列 | Hermes 轻量干货柜 |
| 尺寸等级 | L |
| 普通调度点 | 4 |
| 结算单位 | `cargoverse:void_byte` |
| 标签 | `series.aui.hermes` |

## 数值

| 指标 | 当前定义值 |
| --- | --- |
| 容量 | 270 个实际物品 |
| 空柜目标质量 | 58 Kpg |
| 分类容量修正 | 无，使用定义容量 |

空重为配置目标，实际基础质量取模板结构质量与配置空重的较大值；载货质量另算。型号 ID 的后缀不替代实际尺寸或接口。

## CargoClass 兼容与保护

允许：独立固体（solid）。

当前生效保护：无。

设计缺陷：无。未实现的目标保护不产生程序效果；准入与完整组件校验仍独立执行。

## 结构模板

| 项目 | 实际配置 |
| --- | --- |
| 定义 | [cargoverse:aui/hermes_mc_l](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/aui/hermes_mc_l.json>) |
| 名称／规格 | AUI Hermes 轻量干货柜 L 型／L |
| 结构 ID | `cargoverse:cargo/aui/hermes/aui_hermes_mc_l` |
| NBT | [项目结构文件](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/aui/hermes/aui_hermes_mc_l.nbt>) |
| 包络 X×Y×Z | 11×7×6 |
| 实际接口 | 磁吸板×112 |
| 运行标记 | 分类 2、质量 4、词条 10（0～4 齐全） |

## 制造与投放

材料来自操作玩家物品栏，资金使用 VB；不扣贸易点仓库物品。同型号的各站实际配置如下，测试目录不等于正式投放。

| 制造目录 | 许可 | 最低繁荣 | 加工费 VB | 物品材料 |
| --- | --- | ---: | ---: | --- |
| [正式：factory/sky_station/modular_equipment](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/factory/sky_station/modular_equipment.json>) | L | 2 | 400 | `minecraft:iron_ingot`×40、`minecraft:copper_ingot`×32、`minecraft:white_wool`×16、`minecraft:redstone`×8 |
| [测试：market/test_station/all_containers](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/market/test_station/all_containers.json>) | L | 2 | 400 | `minecraft:iron_ingot`×40、`minecraft:copper_ingot`×32、`minecraft:white_wool`×16、`minecraft:redstone`×8 |

[统一制造与投放索引](<../../../08_货柜制造台/制造配方与投放总表.md>)。

## 当前 JSON

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/aui/hermes/aui_hermes_mc_l",
  "manufacturer": "cargoverse:aui",
  "display_name": "AUI Hermes 轻量干货柜 L 型",
  "description": "实际物品运输货柜；承载形态与运输保护以本定义为准。",
  "size_class": "L",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 4,
  "capacity": 270,
  "empty_mass": 58,
  "allowed_cargo_classes": [
    "solid"
  ],
  "special_designs": [],
  "design_defects": [],
  "tags": [
    "series.aui.hermes"
  ],
  "cargo_class_capacity_modifiers": {}
}
```

## 验证边界

实际结构与型号参数以当前定义和模板为准；静态校验不代替碰撞、对接、Sable 装配及满载运输实测。已有物理货柜不因文档调整或重载自动换壳。

[返回系列](<README.md>) · [返回制造商](<../README.md>)
