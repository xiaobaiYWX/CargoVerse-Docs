# DMC Silo 密闭粉料柜 X 型

> **【已实现／仅测试投放】运输与结构已接入；正式制造投放及成本平衡未定稿。**

[深岩矿业集团](<../README.md>) → [Silo 密闭粉料柜](<README.md>) → X 型

## 职责与使用边界

以密闭围护和防潮保护作为定位；与 Boreal 均承载独立固体，不再以粉末／颗粒形态划分硬准入。

- 目标形态：独立固体 solid。
- 当前 JSON 承载：独立固体 solid。
- 当前生效保护：防潮 D。
- 完整目标保护：防漏粉、防潮。
- 使用边界：密闭不代表液密气密；当前 solid 装载仍按具体物品准入与条件判断，腐蚀专项未实现。
- 典型内容：矿粉、面粉、染料粉和适配种粒；食品与矿业用途共用能力。仅为例子，同形态同条件的物品不因行业或制造商被排除。
- 当前阶段：本期物品，可制造。

保护外观不等于程序效果。遮光、温控、生态维持和放射性屏蔽等未列入“当前生效保护”的部分只能作为后续结构预留，不能标成已经实装。

## 定义

| 项目 | 内容 |
| --- | --- |
| 资源 ID | `cargoverse:dmc/silo_sd_x` |
| 定义文件 | [silo_sd_x.json](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/dmc/silo_sd_x.json>) |
| 制造商 | 深岩矿业集团（`cargoverse:dmc`） |
| 系列 | Silo 密闭粉料柜 |
| 尺寸等级 | X |
| 普通调度点 | 6 |
| 结算单位 | `cargoverse:void_byte` |
| 标签 | `series.dmc.silo` |

## 数值

| 指标 | 当前定义值 |
| --- | --- |
| 容量 | 550 个实际物品 |
| 空柜目标质量 | 285 Kpg |
| 分类容量修正 | 无，使用定义容量 |

空重为配置目标，实际基础质量取模板结构质量与配置空重的较大值；载货质量另算。型号 ID 的后缀不替代实际尺寸或接口。

## CargoClass 兼容与保护

允许：独立固体（solid）。

当前生效保护：`cargoverse:moisture_proof`。

设计缺陷：无。未实现的目标保护不产生程序效果；准入与完整组件校验仍独立执行。

## 结构模板

| 项目 | 实际配置 |
| --- | --- |
| 定义 | [cargoverse:dmc/silo_sd_x](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/dmc/silo_sd_x.json>) |
| 名称／规格 | DMC Silo 密闭粉料柜 X 型／X |
| 结构 ID | `cargoverse:cargo/dmc/titanhaul/dmc_titanhaul_hd_x` |
| NBT | [项目结构文件](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/dmc/titanhaul/dmc_titanhaul_hd_x.nbt>) |
| 包络 X×Y×Z | 16×9×9 |
| 实际接口 | 重型连接点×4 |
| 运行标记 | 分类 2、质量 4、词条 10（0～4 齐全） |

## 制造与投放

材料来自操作玩家物品栏，资金使用 VB；不扣贸易点仓库物品。同型号的各站实际配置如下，测试目录不等于正式投放。

| 制造目录 | 许可 | 最低繁荣 | 加工费 VB | 物品材料 |
| --- | --- | ---: | ---: | --- |
| [测试：market/test_station/all_containers](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/market/test_station/all_containers.json>) | X | 3 | 980 | `minecraft:iron_ingot`×196、`minecraft:copper_ingot`×56、`minecraft:chain`×28、`minecraft:piston`×7 |

[统一制造与投放索引](<../../../08_货柜制造台/制造配方与投放总表.md>)。

## 当前 JSON

```json
{
  "schema_version": 1,
  "manufacturer": "cargoverse:dmc",
  "trade_currency": "cargoverse:void_byte",
  "template": "cargoverse:cargo/dmc/titanhaul/dmc_titanhaul_hd_x",
  "display_name": "DMC Silo 密闭粉料柜 X 型",
  "description": "实际物品运输货柜；承载形态与运输保护以本定义为准。",
  "size_class": "X",
  "dispatch_points": 6,
  "empty_mass": 285,
  "allowed_cargo_classes": [
    "solid"
  ],
  "cargo_class_capacity_modifiers": {},
  "special_designs": [
    "cargoverse:moisture_proof"
  ],
  "design_defects": [],
  "tags": [
    "series.dmc.silo"
  ],
  "capacity": 550
}
```

## 验证边界

实际结构与型号参数以当前定义和模板为准；静态校验不代替碰撞、对接、Sable 装配及满载运输实测。已有物理货柜不因文档调整或重载自动换壳。

[返回系列](<README.md>) · [返回制造商](<../README.md>)
