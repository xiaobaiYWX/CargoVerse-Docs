# DMC Silo 密闭粉料柜 XL 型

可制造。更新于 2026-11-03。

[系列目录](README.md) · [制造商目录](../README.md)

## 定义与承载

| 项目 | 当前值 |
| --- | --- |
| 资源 ID | `cargoverse:dmc/silo_sd_xl` |
| 介质 | solid |
| 尺寸 | XL |
| 容量 | 915 组 |
| 定义空重 | 475 Kpg |
| 调度点 | 8 |
| 标签 | series.dmc.silo |

实际空重取结构质量与配置空重的较大值，载荷质量另计。固体按冻结组大小计量，流体一桶为 1000 mB，生物按物种舱位确定可装只数。

## 当前保护能力

| 能力 | 参数 |
| --- | --- |
| 围护 | `level=2` |
| 密封 | `level=1` |
| 遮光结构 | `level=1`，`reduction=15` |

完整运输条件随货物冻结，保护能力影响对应的围护、密封或内部环境求值。设备初始按需自动工作，实际降温与调压需要时间。

## 结构模板
| 项目 | 实际配置 |
| --- | --- |
| 定义 | [cargoverse:dmc/silo_sd_xl](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/dmc/silo_sd_xl.json>) |
| 名称／规格 | DMC Silo 密闭粉料柜 XL 型／XL |
| 结构 ID | `cargoverse:cargo/dmc/titanhaul/dmc_titanhaul_hd_xl` |
| NBT | [项目结构文件](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/dmc/titanhaul/dmc_titanhaul_hd_xl.nbt>) |
| 包络 X×Y×Z | 21×10×10 |
| 实际接口 | 重型连接点×4 |
| 运行标记 | 分类 2、质量 4、词条 10（0～4 齐全） |

## 制造配方与投放

| 目录 | 许可证 | 繁荣等级 | 加工费 VB | 实体材料 |
| --- | --- | ---: | ---: | --- |
| [mineral_refinery](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/factory/sky_station/mineral_refinery.json>) | XL | 4 | 1680 | minecraft:iron_ingot × 336、minecraft:copper_ingot × 96、minecraft:chain × 48、minecraft:piston × 12 |
| [all_containers](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/market/test_station/all_containers.json>) | XL | 4 | 1680 | minecraft:iron_ingot × 336、minecraft:copper_ingot × 96、minecraft:chain × 48、minecraft:piston × 12 |

## 当前 JSON

[工程定义](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/dmc/silo_sd_xl.json>)

```json
{
  "schema_version": 1,
  "manufacturer": "cargoverse:dmc",
  "trade_currency": "cargoverse:void_byte",
  "template": "cargoverse:cargo/dmc/titanhaul/dmc_titanhaul_hd_xl",
  "display_name": "DMC Silo 密闭粉料柜 XL 型",
  "description": "实际物品运输货柜；承载形态与运输保护以本定义为准。",
  "size_class": "XL",
  "dispatch_points": 8,
  "empty_mass": 475,
  "allowed_cargo_classes": [
    "solid"
  ],
  "cargo_class_capacity_modifiers": {},
  "special_designs": [],
  "design_defects": [],
  "tags": [
    "series.dmc.silo"
  ],
  "capacity": 915,
  "abilities": {
    "cargoverse:containment": {
      "level": 2
    },
    "cargoverse:sealing": {
      "level": 1
    },
    "cargoverse:light_blocking": {
      "level": 1,
      "reduction": 15
    }
  }
}
```

## 实机验收

模板装配、满载起吊、对接及持续航程需在游戏中核验。当前数值以数据包配置为准。
