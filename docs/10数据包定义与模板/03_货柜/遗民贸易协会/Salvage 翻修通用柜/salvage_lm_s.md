# REX Salvage 翻修通用柜 S 型

> **【已实现】实际物品货柜，已采用最终结构。**

[遗民贸易协会](<../README.md>) → [Salvage 翻修通用柜](<README.md>) → S 型

## 职责与使用边界

最低制造成本的翻修干货，与各厂通用柜竞争；容量较小、空重较高，基本承载仍可靠。

- 目标形态：独立固体 solid。
- 当前 JSON 承载：独立固体 solid。
- 当前生效保护：无专用保护。
- 完整目标保护：基本围护与固定；无专用保护。
- 使用边界：高空重、不耐湿货物无保护；不以旧壳来源声称万能能力。
- 典型内容：回收整件物、石砖、木材、工具与普通包装货物。仅为例子，同形态同条件的物品不因行业或制造商被排除。
- 当前阶段：本期物品，可制造。

保护外观不等于程序效果。遮光、温控、生态维持和放射性屏蔽等未列入“当前生效保护”的部分只能作为后续结构预留，不能标成已经实装。

## 定义

| 项目 | 内容 |
| --- | --- |
| 资源 ID | `cargoverse:rex/salvage_lm_s` |
| 定义文件 | [salvage_lm_s.json](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/rex/salvage_lm_s.json>) |
| 制造商 | 遗民贸易协会（`cargoverse:rex`） |
| 系列 | Salvage 翻修通用柜 |
| 尺寸等级 | S |
| 普通调度点 | 1 |
| 结算单位 | `cargoverse:void_byte` |
| 标签 | `series.rex.salvage` |

## 数值

| 指标 | 当前定义值 |
| --- | --- |
| 容量 | 45 个实际物品 |
| 空柜目标质量 | 30 Kpg |
| 分类容量修正 | 无，使用定义容量 |

空重为配置目标，实际基础质量取模板结构质量与配置空重的较大值；载货质量另算。型号 ID 的后缀不替代实际尺寸或接口。

## CargoClass 兼容与保护

允许：独立固体（solid）。

当前生效保护：无。

设计缺陷：无。未实现的目标保护不产生程序效果；准入与完整组件校验仍独立执行。

## 结构模板

| 项目 | 实际配置 |
| --- | --- |
| 定义 | [cargoverse:rex/salvage_lm_s](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/rex/salvage_lm_s.json>) |
| 名称／规格 | REX Salvage 翻修通用柜 S 型／S |
| 结构 ID | `cargoverse:cargo/rex/salvage/rex_salvage_lm_s` |
| NBT | [项目结构文件](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/rex/salvage/rex_salvage_lm_s.nbt>) |
| 包络 X×Y×Z | 6×5×5 |
| 实际接口 | 绳索连接器×4 |
| 运行标记 | 分类 2、质量 2、词条 10（0～4 齐全） |

## 制造与投放

材料来自操作玩家物品栏，资金使用 VB；不扣贸易点仓库物品。同型号的各站实际配置如下，测试目录不等于正式投放。

| 制造目录 | 许可 | 最低繁荣 | 加工费 VB | 物品材料 |
| --- | --- | ---: | ---: | --- |
| [正式：market/sky_station/heritage_gallery](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/market/sky_station/heritage_gallery.json>) | S | 0 | 70 | `minecraft:iron_ingot`×8、`minecraft:copper_ingot`×8、`minecraft:oak_planks`×8、`minecraft:leather`×4 |
| [测试：market/test_station/all_containers](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/market/test_station/all_containers.json>) | S | 0 | 70 | `minecraft:iron_ingot`×8、`minecraft:copper_ingot`×8、`minecraft:oak_planks`×8、`minecraft:leather`×4 |
| [正式：resource/sky_station/far_reach_exchange](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/resource/sky_station/far_reach_exchange.json>) | S | 0 | 70 | `minecraft:iron_ingot`×8、`minecraft:copper_ingot`×8、`minecraft:oak_planks`×8、`minecraft:leather`×4 |
| [正式：resource/sky_station/remnant_exchange](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/resource/sky_station/remnant_exchange.json>) | S | 0 | 70 | `minecraft:iron_ingot`×8、`minecraft:copper_ingot`×8、`minecraft:oak_planks`×8、`minecraft:leather`×4 |

[统一制造与投放索引](<../../../08_货柜制造台/制造配方与投放总表.md>)。

## 基础运输权益

本型号对应[制造商初始基础货柜权益](<../../../05_基础货柜/rex_basic.md>)。通过基础权益领取的资产免调度点；普通制造的同型号仍使用 1 点，不修改型号定义。

## 当前 JSON

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/rex/salvage/rex_salvage_lm_s",
  "manufacturer": "cargoverse:rex",
  "display_name": "REX Salvage 翻修通用柜 S 型",
  "description": "实际物品运输货柜；承载形态与运输保护以本定义为准。",
  "size_class": "S",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 1,
  "capacity": 45,
  "empty_mass": 30,
  "allowed_cargo_classes": [
    "solid"
  ],
  "special_designs": [],
  "design_defects": [],
  "tags": [
    "series.rex.salvage"
  ],
  "cargo_class_capacity_modifiers": {}
}
```

## 验证边界

实际结构与型号参数以当前定义和模板为准；静态校验不代替碰撞、对接、Sable 装配及满载运输实测。已有物理货柜不因文档调整或重载自动换壳。

[返回系列](<README.md>) · [返回制造商](<../README.md>)
