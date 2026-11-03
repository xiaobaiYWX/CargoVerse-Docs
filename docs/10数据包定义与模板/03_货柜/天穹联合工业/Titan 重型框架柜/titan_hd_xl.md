# AUI Titan 大宗干货柜 XL 型

可制造。更新于 2026-11-03。

[系列目录](README.md) · [制造商目录](../README.md)

## 定义与承载

| 项目 | 当前值 |
| --- | --- |
| 资源 ID | `cargoverse:aui/titan_hd_xl` |
| 介质 | solid |
| 尺寸 | XL |
| 容量 | 1250 组 |
| 定义空重 | 390 Kpg |
| 调度点 | 8 |
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
| 定义 | [cargoverse:aui/titan_hd_xl](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/aui/titan_hd_xl.json>) |
| 名称／规格 | AUI Titan 重型框架柜 XL 型／XL |
| 结构 ID | `cargoverse:cargo/aui/titan/aui_titan_hd_xl` |
| NBT | [项目结构文件](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/aui/titan/aui_titan_hd_xl.nbt>) |
| 包络 X×Y×Z | 21×11×10 |
| 实际接口 | 重型连接点×4 |
| 运行标记 | 分类 4、质量 4、词条 10（0～4 齐全） |

## 制造配方与投放

| 目录 | 许可证 | 繁荣等级 | 加工费 VB | 实体材料 |
| --- | --- | ---: | ---: | --- |
| [standard_assembly](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/factory/sky_station/standard_assembly.json>) | XL | 4 | 1200 | minecraft:iron_ingot × 288、minecraft:oak_planks × 144、minecraft:chain × 48、minecraft:redstone × 24 |
| [all_containers](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/market/test_station/all_containers.json>) | XL | 4 | 1200 | minecraft:iron_ingot × 288、minecraft:oak_planks × 144、minecraft:chain × 48、minecraft:redstone × 24 |

## 当前 JSON

[工程定义](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/aui/titan_hd_xl.json>)

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/aui/titan/aui_titan_hd_xl",
  "manufacturer": "cargoverse:aui",
  "display_name": "AUI Titan 大宗干货柜 XL 型",
  "description": "实际物品运输货柜；承载形态与运输保护以本定义为准。",
  "size_class": "XL",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 8,
  "capacity": 1250,
  "empty_mass": 390,
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
