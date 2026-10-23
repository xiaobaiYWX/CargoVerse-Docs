# HEC Apollo 封装敏感品柜 M 型

> **【已实现】实际物品货柜，已采用最终结构。**

[赫利俄斯能源集团](<../README.md>) → [Apollo 封装敏感品柜](<README.md>) → M 型

## 职责与使用边界

HEC 基础柜及封装易燃内容运输；支持普通整件品，以额外保护换空重与投入，不是裸液体罐。

- 目标形态：独立固体 solid。
- 当前 JSON 承载：独立固体 solid。
- 当前生效保护：防潮 D、定向固定 O、易燃保护 I。
- 完整目标保护：防潮、定向固定、易燃保护。
- 使用边界：不等于防爆、液体罐或抗所有腐蚀；无温控。
- 典型内容：封装试剂、药瓶、可燃固体，也可装普通工具和木料。仅为例子，同形态同条件的物品不因行业或制造商被排除。
- 当前阶段：本期物品，可制造。

保护外观不等于程序效果。遮光、温控、生态维持和放射性屏蔽等未列入“当前生效保护”的部分只能作为后续结构预留，不能标成已经实装。

## 定义

| 项目 | 内容 |
| --- | --- |
| 资源 ID | `cargoverse:hec/apollo_sd_s` |
| 定义文件 | [apollo_sd_s.json](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/hec/apollo_sd_s.json>) |
| 制造商 | 赫利俄斯能源集团（`cargoverse:hec`） |
| 系列 | Apollo 封装敏感品柜 |
| 尺寸等级 | M |
| 普通调度点 | 2 |
| 结算单位 | `cargoverse:void_byte` |
| 标签 | `series.hec.apollo` |

## 数值

| 指标 | 当前定义值 |
| --- | --- |
| 容量 | 110 个实际物品 |
| 空柜目标质量 | 60 Kpg |
| 分类容量修正 | 无，使用定义容量 |

空重为配置目标，实际基础质量取模板结构质量与配置空重的较大值；载货质量另算。型号 ID 的后缀不替代实际尺寸或接口。

## CargoClass 兼容与保护

允许：独立固体（solid）。

当前生效保护：`cargoverse:moisture_proof`、`cargoverse:keep_upright`、`cargoverse:flammable`。

设计缺陷：无。未实现的目标保护不产生程序效果；准入与完整组件校验仍独立执行。

## 结构模板

| 项目 | 实际配置 |
| --- | --- |
| 定义 | [cargoverse:hec/apollo_sd_s](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/hec/apollo_sd_s.json>) |
| 名称／规格 | HEC Apollo 封装敏感品柜 M 型／M |
| 结构 ID | `cargoverse:cargo/hec/reactor/hec_reactor_hd_m` |
| NBT | [项目结构文件](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/hec/reactor/hec_reactor_hd_m.nbt>) |
| 包络 X×Y×Z | 10×6×5 |
| 实际接口 | 重型连接点×4 |
| 运行标记 | 分类 2、质量 2、词条 10（0～4 齐全） |

## 制造与投放

材料来自操作玩家物品栏，资金使用 VB；不扣贸易点仓库物品。同型号的各站实际配置如下，测试目录不等于正式投放。

| 制造目录 | 许可 | 最低繁荣 | 加工费 VB | 物品材料 |
| --- | --- | ---: | ---: | --- |
| [正式：factory/sky_station/biosystems_station](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/factory/sky_station/biosystems_station.json>) | M | 0 | 110 | `minecraft:iron_ingot`×16、`minecraft:copper_ingot`×8、`minecraft:glass`×4、`minecraft:redstone`×2 |
| [正式：factory/sky_station/chemical_works](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/factory/sky_station/chemical_works.json>) | M | 0 | 110 | `minecraft:iron_ingot`×16、`minecraft:copper_ingot`×8、`minecraft:glass`×4、`minecraft:redstone`×2 |
| [正式：factory/sky_station/fuel_depot](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/factory/sky_station/fuel_depot.json>) | M | 0 | 110 | `minecraft:iron_ingot`×16、`minecraft:copper_ingot`×8、`minecraft:glass`×4、`minecraft:redstone`×2 |
| [测试：market/test_station/all_containers](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/market/test_station/all_containers.json>) | M | 0 | 110 | `minecraft:iron_ingot`×16、`minecraft:copper_ingot`×8、`minecraft:glass`×4、`minecraft:redstone`×2 |

[统一制造与投放索引](<../../../08_货柜制造台/制造配方与投放总表.md>)。

## 基础运输权益

本型号对应[制造商初始基础货柜权益](<../../../05_基础货柜/hec_basic.md>)。通过基础权益领取的资产免调度点；普通制造的同型号仍使用 2 点，不修改型号定义。

## 当前 JSON

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/hec/reactor/hec_reactor_hd_m",
  "manufacturer": "cargoverse:hec",
  "display_name": "HEC Apollo 封装敏感品柜 M 型",
  "description": "实际物品运输货柜；承载形态与运输保护以本定义为准。",
  "size_class": "M",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 2,
  "capacity": 110,
  "empty_mass": 60,
  "allowed_cargo_classes": [
    "solid"
  ],
  "special_designs": [
    "cargoverse:moisture_proof",
    "cargoverse:keep_upright",
    "cargoverse:flammable"
  ],
  "design_defects": [],
  "tags": [
    "series.hec.apollo"
  ],
  "cargo_class_capacity_modifiers": {}
}
```

## 验证边界

实际结构与型号参数以当前定义和模板为准；静态校验不代替碰撞、对接、Sable 装配及满载运输实测。已有物理货柜不因文档调整或重载自动换壳。

[返回系列](<README.md>) · [返回制造商](<../README.md>)
