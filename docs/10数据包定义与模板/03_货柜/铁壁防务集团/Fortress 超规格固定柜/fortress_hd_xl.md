# BDS Fortress 超规格固定柜 XL 型

> **【已实现】实际物品货柜，已采用最终结构。**

[铁壁防务集团](<../README.md>) → [Fortress 超规格固定柜](<README.md>) → XL 型

## 职责与使用边界

保留开放固定平台，与 Sentinel 封闭箱体形成明确的结构和保护差别；XL 大容量但不防潮，不能仅凭等级获得封闭能力。

- 目标形态：独立固体 solid。
- 当前 JSON 承载：独立固体 solid。
- 当前生效保护：防震 V、定向固定 O。
- 完整目标保护：防震、定向固定；不防潮。
- 使用边界：无防潮，未封装粉末散料不支持；仅 XL。
- 典型内容：大型装配件、耐候设备和整件工程材料。仅为例子，同形态同条件的物品不因行业或制造商被排除。
- 当前阶段：本期物品，可制造。

保护外观不等于程序效果。遮光、温控、生态维持和放射性屏蔽等未列入“当前生效保护”的部分只能作为后续结构预留，不能标成已经实装。

## 定义

| 项目 | 内容 |
| --- | --- |
| 资源 ID | `cargoverse:bds/fortress_hd_xl` |
| 定义文件 | [fortress_hd_xl.json](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/bds/fortress_hd_xl.json>) |
| 制造商 | 铁壁防务集团（`cargoverse:bds`） |
| 系列 | Fortress 超规格固定柜 |
| 尺寸等级 | XL |
| 普通调度点 | 8 |
| 结算单位 | `cargoverse:void_byte` |
| 标签 | `series.bds.fortress` |

## 数值

| 指标 | 当前定义值 |
| --- | --- |
| 容量 | 1200 个实际物品 |
| 空柜目标质量 | 555 Kpg |
| 分类容量修正 | 无，使用定义容量 |

空重为配置目标，实际基础质量取模板结构质量与配置空重的较大值；载货质量另算。型号 ID 的后缀不替代实际尺寸或接口。

## CargoClass 兼容与保护

允许：独立固体（solid）。

当前生效保护：`cargoverse:fragile`、`cargoverse:keep_upright`。

设计缺陷：无。未实现的目标保护不产生程序效果；准入与完整组件校验仍独立执行。

## 结构模板

| 项目 | 实际配置 |
| --- | --- |
| 定义 | [cargoverse:bds/fortress_hd_xl](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/bds/fortress_hd_xl.json>) |
| 名称／规格 | BDS Fortress 超规格固定柜 XL 型／XL |
| 结构 ID | `cargoverse:cargo/bds/fortress/bds_fortress_hd_xl` |
| NBT | [项目结构文件](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/bds/fortress/bds_fortress_hd_xl.nbt>) |
| 包络 X×Y×Z | 16×16×16 |
| 实际接口 | 重型连接点×4 |
| 运行标记 | 分类 4、质量 8、词条 20（0～4 齐全） |

## 制造与投放

材料来自操作玩家物品栏，资金使用 VB；不扣贸易点仓库物品。同型号的各站实际配置如下，测试目录不等于正式投放。

| 制造目录 | 许可 | 最低繁荣 | 加工费 VB | 物品材料 |
| --- | --- | ---: | ---: | --- |
| [正式：factory/sky_station/security_works](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/factory/sky_station/security_works.json>) | XL | 4 | 2280 | `minecraft:iron_ingot`×336、`minecraft:obsidian`×96、`minecraft:chain`×48、`minecraft:redstone`×48 |
| [测试：market/test_station/all_containers](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/market/test_station/all_containers.json>) | XL | 4 | 2280 | `minecraft:iron_ingot`×336、`minecraft:obsidian`×96、`minecraft:chain`×48、`minecraft:redstone`×48 |

[统一制造与投放索引](<../../../08_货柜制造台/制造配方与投放总表.md>)。

## 当前 JSON

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/bds/fortress/bds_fortress_hd_xl",
  "manufacturer": "cargoverse:bds",
  "display_name": "BDS Fortress 超规格固定柜 XL 型",
  "description": "实际物品运输货柜；承载形态与运输保护以本定义为准。",
  "size_class": "XL",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 8,
  "capacity": 1200,
  "empty_mass": 555,
  "allowed_cargo_classes": [
    "solid"
  ],
  "special_designs": [
    "cargoverse:fragile",
    "cargoverse:keep_upright"
  ],
  "design_defects": [],
  "tags": [
    "series.bds.fortress"
  ],
  "cargo_class_capacity_modifiers": {}
}
```

## 验证边界

实际结构与型号参数以当前定义和模板为准；静态校验不代替碰撞、对接、Sable 装配及满载运输实测。已有物理货柜不因文档调整或重载自动换壳。

[返回系列](<README.md>) · [返回制造商](<../README.md>)
