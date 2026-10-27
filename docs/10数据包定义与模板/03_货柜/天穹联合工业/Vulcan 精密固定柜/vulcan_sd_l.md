# AUI Vulcan 精密固定柜 L 型

> **【已实现】实际物品货柜，已采用最终结构。**

[天穹联合工业](<../README.md>) → [Vulcan 精密固定柜](<README.md>) → L 型

## 职责与使用边界

合并 Nomad 的定向固定需求。与 Sentinel 同保护竞争，以较高成本换容量和较低空重；不再拆精密型与工程型。

- 目标形态：独立固体 solid。
- 当前 JSON 承载：独立固体 solid。
- 当前数值能力〔候选〕：围护 1、密封 1、缓冲 3；隔热、调温、遮光、承压均为 0。
- 能力方向：缓冲与液态水隔离，不提供无限防震或旧定向固定效果。
- 使用边界：同属 solid 的颗粒／粉末不按用途拒装；围护 2 需求仍有缺口。
- 典型内容：精密机构、传感器、玻璃与护目镜。仅为例子，同形态同条件的物品不因行业或制造商被排除。
- 当前阶段：本期物品，可制造。

保护外观不等于程序效果。遮光、温控、生态维持和放射性屏蔽等未列入“当前生效保护”的部分只能作为后续结构预留，不能标成已经实装。

## 定义

| 项目 | 内容 |
| --- | --- |
| 资源 ID | `cargoverse:aui/vulcan_sd_l` |
| 定义文件 | [vulcan_sd_l.json](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/aui/vulcan_sd_l.json>) |
| 制造商 | 天穹联合工业（`cargoverse:aui`） |
| 系列 | Vulcan 精密固定柜 |
| 尺寸等级 | L |
| 普通调度点 | 4 |
| 结算单位 | `cargoverse:void_byte` |
| 标签 | `series.aui.vulcan` |

## 数值

| 指标 | 当前定义值 |
| --- | --- |
| 容量 | 270 个实际物品 |
| 空柜目标质量 | 125 Kpg |
| 分类容量修正 | 无，使用定义容量 |

空重为配置目标，实际基础质量取模板结构质量与配置空重的较大值；载货质量另算。型号 ID 的后缀不替代实际尺寸或接口。

## CargoClass 兼容与保护

允许：独立固体（solid）。

当前七项能力：围护 1、密封 1、缓冲 3、隔热 0、调温 0、遮光 0、承压 0。JSON 中暂留的 special_designs 仅是待清理资料，既不执行免疫，也不删除玻璃固有易碎特性。

设计缺陷：无。未实现的目标保护不产生程序效果；准入与完整组件校验仍独立执行。

## 结构模板

| 项目 | 实际配置 |
| --- | --- |
| 定义 | [cargoverse:aui/vulcan_sd_l](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/aui/vulcan_sd_l.json>) |
| 名称／规格 | AUI Vulcan 精密固定柜 L 型／L |
| 结构 ID | `cargoverse:cargo/aui/vulcan/aui_vulcan_sd_l` |
| NBT | [项目结构文件](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/aui/vulcan/aui_vulcan_sd_l.nbt>) |
| 包络 X×Y×Z | 15×6×7 |
| 实际接口 | 标准对接接口×8 |
| 运行标记 | 分类 2、质量 2、词条 10（0～4 齐全） |

## 制造与投放

材料来自操作玩家物品栏，资金使用 VB；不扣贸易点仓库物品。同型号的各站实际配置如下，测试目录不等于正式投放。

| 制造目录 | 许可 | 最低繁荣 | 加工费 VB | 物品材料 |
| --- | --- | ---: | ---: | --- |
| [正式：factory/sky_station/airship_yard](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/factory/sky_station/airship_yard.json>) | L | 2 | 480 | `minecraft:iron_ingot`×64、`minecraft:glass`×16、`minecraft:white_wool`×16、`minecraft:comparator`×4 |
| [正式：factory/sky_station/modular_equipment](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/factory/sky_station/modular_equipment.json>) | L | 2 | 480 | `minecraft:iron_ingot`×64、`minecraft:glass`×16、`minecraft:white_wool`×16、`minecraft:comparator`×4 |
| [测试：market/test_station/all_containers](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/market/test_station/all_containers.json>) | L | 2 | 480 | `minecraft:iron_ingot`×64、`minecraft:glass`×16、`minecraft:white_wool`×16、`minecraft:comparator`×4 |

[统一制造与投放索引](<../../../08_货柜制造台/制造配方与投放总表.md>)。

## 当前 JSON

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/aui/vulcan/aui_vulcan_sd_l",
  "manufacturer": "cargoverse:aui",
  "display_name": "AUI Vulcan 精密固定柜 L 型",
  "description": "实际物品运输货柜；承载形态与运输保护以本定义为准。",
  "size_class": "L",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 4,
  "capacity": 270,
  "empty_mass": 125,
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
    "series.aui.vulcan"
  ],
  "cargo_class_capacity_modifiers": {},
  "transport_capabilities": {
    "containment_level": 1,
    "sealing_level": 1,
    "cushioning_level": 3,
    "insulation_level": 0,
    "thermal_control_level": 0,
    "light_blocking_level": 0,
    "pressure_resistance_level": 0
  }
}
```

## 验证边界

实际结构与型号参数以当前定义和模板为准；静态校验不代替碰撞、对接、Sable 装配及满载运输实测。已有物理货柜不因文档调整或重载自动换壳。

[返回系列](<README.md>) · [返回制造商](<../README.md>)
