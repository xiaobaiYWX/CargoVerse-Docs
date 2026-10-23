# SPL Courier 轻型配送柜 M 型

> **【已实现】实际物品货柜，已采用最终结构。**

[云港物流集团](<../README.md>) → [Courier 轻型配送柜](<README.md>) → M 型

## 职责与使用边界

合并 Cargo 为 S/M/L 配送线，统一防潮。与 Atlas 比更轻但更贵，与 Harvest 比更轻但容量较小。

- 目标形态：独立固体 solid。
- 当前 JSON 承载：独立固体 solid。
- 当前生效保护：防潮 D。
- 完整目标保护：防潮。
- 使用边界：无密封散料能力、无温控。
- 典型内容：生活成品、工具、书籍、包装物品。仅为例子，同形态同条件的物品不因行业或制造商被排除。
- 当前阶段：本期物品，可制造。

保护外观不等于程序效果。遮光、温控、生态维持和放射性屏蔽等未列入“当前生效保护”的部分只能作为后续结构预留，不能标成已经实装。

## 定义

| 项目 | 内容 |
| --- | --- |
| 资源 ID | `cargoverse:spl/courier_mc_m` |
| 定义文件 | [courier_mc_m.json](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/spl/courier_mc_m.json>) |
| 制造商 | 云港物流集团（`cargoverse:spl`） |
| 系列 | Courier 轻型配送柜 |
| 尺寸等级 | M |
| 普通调度点 | 2 |
| 结算单位 | `cargoverse:void_byte` |
| 标签 | `series.spl.courier` |

## 数值

| 指标 | 当前定义值 |
| --- | --- |
| 容量 | 120 个实际物品 |
| 空柜目标质量 | 36 Kpg |
| 分类容量修正 | 无，使用定义容量 |

空重为配置目标，实际基础质量取模板结构质量与配置空重的较大值；载货质量另算。型号 ID 的后缀不替代实际尺寸或接口。

## CargoClass 兼容与保护

允许：独立固体（solid）。

当前生效保护：`cargoverse:moisture_proof`。

设计缺陷：无。未实现的目标保护不产生程序效果；准入与完整组件校验仍独立执行。

## 结构模板

| 项目 | 实际配置 |
| --- | --- |
| 定义 | [cargoverse:spl/courier_mc_m](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/spl/courier_mc_m.json>) |
| 名称／规格 | SPL Courier 轻型配送柜 M 型／M |
| 结构 ID | `cargoverse:cargo/spl/cargo/spl_cargo_mc_m` |
| NBT | [项目结构文件](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/spl/cargo/spl_cargo_mc_m.nbt>) |
| 包络 X×Y×Z | 10×5×6 |
| 实际接口 | 磁吸板×40 |
| 运行标记 | 分类 2、质量 4、词条 10（0～4 齐全） |

## 制造与投放

材料来自操作玩家物品栏，资金使用 VB；不扣贸易点仓库物品。同型号的各站实际配置如下，测试目录不等于正式投放。

| 制造目录 | 许可 | 最低繁荣 | 加工费 VB | 物品材料 |
| --- | --- | ---: | ---: | --- |
| [正式：market/sky_station/civic_distribution](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/market/sky_station/civic_distribution.json>) | M | 1 | 120 | `minecraft:iron_ingot`×16、`minecraft:oak_planks`×16、`minecraft:white_wool`×8、`minecraft:redstone`×4 |
| [正式：market/sky_station/longhaul_port](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/market/sky_station/longhaul_port.json>) | M | 1 | 120 | `minecraft:iron_ingot`×16、`minecraft:oak_planks`×16、`minecraft:white_wool`×8、`minecraft:redstone`×4 |
| [测试：market/test_station/all_containers](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/market/test_station/all_containers.json>) | M | 1 | 120 | `minecraft:iron_ingot`×16、`minecraft:oak_planks`×16、`minecraft:white_wool`×8、`minecraft:redstone`×4 |

[统一制造与投放索引](<../../../08_货柜制造台/制造配方与投放总表.md>)。

## 当前 JSON

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/spl/cargo/spl_cargo_mc_m",
  "manufacturer": "cargoverse:spl",
  "display_name": "SPL Courier 轻型配送柜 M 型",
  "description": "实际物品运输货柜；承载形态与运输保护以本定义为准。",
  "size_class": "M",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 2,
  "capacity": 120,
  "empty_mass": 36,
  "allowed_cargo_classes": [
    "solid"
  ],
  "special_designs": [
    "cargoverse:moisture_proof"
  ],
  "design_defects": [],
  "tags": [
    "series.spl.courier"
  ],
  "cargo_class_capacity_modifiers": {}
}
```

## 验证边界

实际结构与型号参数以当前定义和模板为准；静态校验不代替碰撞、对接、Sable 装配及满载运输实测。已有物理货柜不因文档调整或重载自动换壳。

[返回系列](<README.md>) · [返回制造商](<../README.md>)
