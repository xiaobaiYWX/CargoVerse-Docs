# AUI Titan 大宗干货柜 X 型

可制造。更新于 2026-11-03。

[系列目录](README.md) · [制造商目录](../README.md)

## 定义与承载

| 项目 | 当前值 |
| --- | --- |
| 资源 ID | `cargoverse:aui/titan_hd_x` |
| 介质 | solid |
| 尺寸 | X |
| 容量 | 750 组 |
| 定义空重 | 235 Kpg |
| 调度点 | 6 |
| 标签 | series.aui.titan |

实际空重取结构质量与配置空重的较大值，载荷质量另计。固体按冻结组大小计量，流体一桶为 1000 mB，生物按物种舱位确定可装只数。

## 当前保护能力

| 能力 | 参数 |
| --- | --- |
| 围护 | `level=1` |

完整运输条件随货物冻结，保护能力影响对应的围护、密封或内部环境求值。设备初始按需自动工作，实际降温与调压需要时间。

## 结构模板
| 项目 | 实际配置 |
| --- | --- |
| 定义 | [cargoverse:aui/titan_hd_x](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/aui/titan_hd_x.json>) |
| 名称／规格 | AUI Titan 重型框架柜 X 型／X |
| 结构 ID | `cargoverse:cargo/aui/titan/aui_titan_hd_x` |
| NBT | [项目结构文件](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/aui/titan/aui_titan_hd_x.nbt>) |
| 包络 X×Y×Z | 16×10×9 |
| 实际接口 | 重型连接点×4 |
| 运行标记 | 分类 4、质量 4、词条 10（0～4 齐全） |

## 制造配方与投放

| 目录 | 许可证 | 繁荣等级 | 加工费 VB | 实体材料 |
| --- | --- | ---: | ---: | --- |
| [airship_yard](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/factory/sky_station/airship_yard.json>) | X | 3 | 700 | minecraft:iron_ingot × 168、minecraft:oak_planks × 84、minecraft:chain × 28、minecraft:redstone × 14 |
| [standard_assembly](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/factory/sky_station/standard_assembly.json>) | X | 3 | 700 | minecraft:iron_ingot × 168、minecraft:oak_planks × 84、minecraft:chain × 28、minecraft:redstone × 14 |
| [all_containers](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/market/test_station/all_containers.json>) | X | 3 | 700 | minecraft:iron_ingot × 168、minecraft:oak_planks × 84、minecraft:chain × 28、minecraft:redstone × 14 |

## 当前 JSON

[工程定义](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/aui/titan_hd_x.json>)

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/aui/titan/aui_titan_hd_x",
  "manufacturer": "cargoverse:aui",
  "display_name": "AUI Titan 大宗干货柜 X 型",
  "description": "实际物品运输货柜；承载形态与运输保护以本定义为准。",
  "size_class": "X",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 6,
  "capacity": 750,
  "empty_mass": 235,
  "allowed_cargo_classes": [
    "solid"
  ],
  "special_designs": [],
  "design_defects": [],
  "tags": [
    "series.aui.titan"
  ],
  "cargo_class_capacity_modifiers": {},
  "abilities": {
    "cargoverse:containment": {
      "level": 1
    }
  }
}
```

## 实机验收

模板装配、满载起吊、对接及持续航程需在游戏中核验。当前数值以数据包配置为准。
