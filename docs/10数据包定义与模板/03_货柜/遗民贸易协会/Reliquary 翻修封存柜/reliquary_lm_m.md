# REX Reliquary 翻修封存柜 M 型

> **【已实现／仅测试投放】运输与结构已接入；正式制造投放及成本平衡未定稿。**

[遗民贸易协会](<../README.md>) → [Reliquary 翻修封存柜](<README.md>) → M 型

## 职责与使用边界

REX 的翻修封存柜，与 HRI Explorer 具有相同常用保护及 S/M 容量，以较高空重换较低成本；遗物只是典型货物，不是白名单。

- 目标形态：独立固体 solid。
- 当前 JSON 承载：独立固体 solid。
- 当前生效保护：防震 V、防潮 D、定向固定 O。
- 完整目标保护：防震、防潮、遮光、定向固定。
- 使用边界：无温控，不运裸液体、气体或活体；不宣称未知技术赋予万能保护。
- 典型内容：遗迹器物、唱片、文书、玻璃、仪表及普通瓶装物品。仅为例子，同形态同条件的物品不因行业或制造商被排除。
- 当前阶段：本期物品，可制造。

保护外观不等于程序效果。遮光、温控、生态维持和放射性屏蔽等未列入“当前生效保护”的部分只能作为后续结构预留，不能标成已经实装。

## 定义

| 项目 | 内容 |
| --- | --- |
| 资源 ID | `cargoverse:rex/reliquary_lm_m` |
| 定义文件 | [reliquary_lm_m.json](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/rex/reliquary_lm_m.json>) |
| 制造商 | 遗民贸易协会（`cargoverse:rex`） |
| 系列 | Reliquary 翻修封存柜 |
| 尺寸等级 | M |
| 普通调度点 | 2 |
| 结算单位 | `cargoverse:void_byte` |
| 标签 | `series.rex.reliquary` |

## 数值

| 指标 | 当前定义值 |
| --- | --- |
| 容量 | 85 个实际物品 |
| 空柜目标质量 | 80 Kpg |
| 分类容量修正 | 无，使用定义容量 |

空重为配置目标，实际基础质量取模板结构质量与配置空重的较大值；载货质量另算。型号 ID 的后缀不替代实际尺寸或接口。

## CargoClass 兼容与保护

允许：独立固体（solid）。

当前生效保护：`cargoverse:fragile`、`cargoverse:moisture_proof`、`cargoverse:keep_upright`。

设计缺陷：无。未实现的目标保护不产生程序效果；准入与完整组件校验仍独立执行。

## 结构模板

| 项目 | 实际配置 |
| --- | --- |
| 定义 | [cargoverse:rex/reliquary_lm_m](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/rex/reliquary_lm_m.json>) |
| 名称／规格 | REX Reliquary 翻修封存柜 M 型／M |
| 结构 ID | `cargoverse:cargo/rex/recycle/rex_recycle_lm_m` |
| NBT | [项目结构文件](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/rex/recycle/rex_recycle_lm_m.nbt>) |
| 包络 X×Y×Z | 6×6×6 |
| 实际接口 | 绳索连接器×4 |
| 运行标记 | 分类 2、质量 4、词条 10（0～4 齐全） |

## 制造与投放

材料来自操作玩家物品栏，资金使用 VB；不扣贸易点仓库物品。同型号的各站实际配置如下，测试目录不等于正式投放。

| 制造目录 | 许可 | 最低繁荣 | 加工费 VB | 物品材料 |
| --- | --- | ---: | ---: | --- |
| [测试：market/test_station/all_containers](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/market/test_station/all_containers.json>) | M | 1 | 160 | `minecraft:iron_ingot`×32、`minecraft:oak_planks`×16、`minecraft:glass`×8、`minecraft:redstone`×4 |

[统一制造与投放索引](<../../../08_货柜制造台/制造配方与投放总表.md>)。

## 当前 JSON

```json
{
  "schema_version": 1,
  "manufacturer": "cargoverse:rex",
  "trade_currency": "cargoverse:void_byte",
  "template": "cargoverse:cargo/rex/recycle/rex_recycle_lm_m",
  "display_name": "REX Reliquary 翻修封存柜 M 型",
  "description": "实际物品运输货柜；承载形态与运输保护以本定义为准。",
  "size_class": "M",
  "dispatch_points": 2,
  "empty_mass": 80,
  "allowed_cargo_classes": [
    "solid"
  ],
  "cargo_class_capacity_modifiers": {},
  "special_designs": [
    "cargoverse:fragile",
    "cargoverse:moisture_proof",
    "cargoverse:keep_upright"
  ],
  "design_defects": [],
  "tags": [
    "series.rex.reliquary"
  ],
  "capacity": 85
}
```

## 验证边界

实际结构与型号参数以当前定义和模板为准；静态校验不代替碰撞、对接、Sable 装配及满载运输实测。已有物理货柜不因文档调整或重载自动换壳。

[返回系列](<README.md>) · [返回制造商](<../README.md>)
