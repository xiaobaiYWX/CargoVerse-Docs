# SPL Express 防护快件舱 S 型

> **【已实现】实际物品货柜，已采用最终结构。**

[云港物流集团](<../README.md>) → [Express 防护快件舱](<README.md>) → S 型

## 职责与使用边界

小批轻量防护，S 空重仅为 Sentinel S 的一半，容量更小且更贵。与 Courier 的区别是防震和定向固定，不是航速加成。

- 目标形态：独立固体 solid。
- 当前 JSON 承载：独立固体 solid。
- 当前生效保护：防震 V、防潮 D、定向固定 O。
- 完整目标保护：防震、防潮、定向固定。
- 使用边界：仅 S；无温控或路线速度加成。
- 典型内容：小批仪器、药瓶、精密工具。仅为例子，同形态同条件的物品不因行业或制造商被排除。
- 当前阶段：本期物品，可制造。

保护外观不等于程序效果。遮光、温控、生态维持和放射性屏蔽等未列入“当前生效保护”的部分只能作为后续结构预留，不能标成已经实装。

## 定义

| 项目 | 内容 |
| --- | --- |
| 资源 ID | `cargoverse:spl/express_mc_s` |
| 定义文件 | [express_mc_s.json](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/spl/express_mc_s.json>) |
| 制造商 | 云港物流集团（`cargoverse:spl`） |
| 系列 | Express 防护快件舱 |
| 尺寸等级 | S |
| 普通调度点 | 1 |
| 结算单位 | `cargoverse:void_byte` |
| 标签 | `series.spl.express` |

## 数值

| 指标 | 当前定义值 |
| --- | --- |
| 容量 | 30 个实际物品 |
| 空柜目标质量 | 14 Kpg |
| 分类容量修正 | 无，使用定义容量 |

空重为配置目标，实际基础质量取模板结构质量与配置空重的较大值；载货质量另算。型号 ID 的后缀不替代实际尺寸或接口。

## CargoClass 兼容与保护

允许：独立固体（solid）。

当前生效保护：`cargoverse:fragile`、`cargoverse:moisture_proof`、`cargoverse:keep_upright`。

设计缺陷：无。未实现的目标保护不产生程序效果；准入与完整组件校验仍独立执行。

## 结构模板

| 项目 | 实际配置 |
| --- | --- |
| 定义 | [cargoverse:spl/express_mc_s](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/spl/express_mc_s.json>) |
| 名称／规格 | SPL Express 防护快件舱 S 型／S |
| 结构 ID | `cargoverse:cargo/spl/express/spl_express_mc_s` |
| NBT | [项目结构文件](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/spl/express/spl_express_mc_s.nbt>) |
| 包络 X×Y×Z | 6×4×5 |
| 实际接口 | 磁吸板×6 |
| 运行标记 | 分类 2、质量 2、词条 10（0～4 齐全） |

## 制造与投放

材料来自操作玩家物品栏，资金使用 VB；不扣贸易点仓库物品。同型号的各站实际配置如下，测试目录不等于正式投放。

| 制造目录 | 许可 | 最低繁荣 | 加工费 VB | 物品材料 |
| --- | --- | ---: | ---: | --- |
| [正式：market/sky_station/civic_distribution](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/market/sky_station/civic_distribution.json>) | S | 0 | 90 | `minecraft:iron_ingot`×8、`minecraft:copper_ingot`×8、`minecraft:white_wool`×4、`minecraft:repeater`×1 |
| [正式：market/sky_station/longhaul_port](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/market/sky_station/longhaul_port.json>) | S | 0 | 90 | `minecraft:iron_ingot`×8、`minecraft:copper_ingot`×8、`minecraft:white_wool`×4、`minecraft:repeater`×1 |
| [测试：market/test_station/all_containers](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/market/test_station/all_containers.json>) | S | 0 | 90 | `minecraft:iron_ingot`×8、`minecraft:copper_ingot`×8、`minecraft:white_wool`×4、`minecraft:repeater`×1 |

[统一制造与投放索引](<../../../08_货柜制造台/制造配方与投放总表.md>)。

## 当前 JSON

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/spl/express/spl_express_mc_s",
  "manufacturer": "cargoverse:spl",
  "display_name": "SPL Express 防护快件舱 S 型",
  "description": "实际物品运输货柜；承载形态与运输保护以本定义为准。",
  "size_class": "S",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 1,
  "capacity": 30,
  "empty_mass": 14,
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
    "series.spl.express"
  ],
  "cargo_class_capacity_modifiers": {}
}
```

## 验证边界

实际结构与型号参数以当前定义和模板为准；静态校验不代替碰撞、对接、Sable 装配及满载运输实测。已有物理货柜不因文档调整或重载自动换壳。

[返回系列](<README.md>) · [返回制造商](<../README.md>)
