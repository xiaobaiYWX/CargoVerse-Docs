# DMC Boreal 矿料重载柜 M 型

可制造。更新于 2026-11-03。

[系列目录](README.md) · [制造商目录](../README.md)

## 定义与承载

| 项目 | 当前值 |
| --- | --- |
| 资源 ID | `cargoverse:dmc/boreal_sd_m` |
| 介质 | solid |
| 尺寸 | M |
| 容量 | 150 组 |
| 定义空重 | 65 Kpg |
| 调度点 | 2 |
| 标签 | series.dmc.boreal |

实际空重取结构质量与配置空重的较大值，载荷质量另计。固体按冻结组大小计量，流体一桶为 1000 mB，生物按物种舱位确定可装只数。

## 当前保护能力

| 能力 | 参数 |
| --- | --- |
| 围护 | `level=1` |
| 缓冲衬垫 | `level=1`，`velocity_change_bonus=2` |

完整运输条件随货物冻结，保护能力影响对应的围护、密封或内部环境求值。设备初始按需自动工作，实际降温与调压需要时间。

## 结构模板
| 项目 | 实际配置 |
| --- | --- |
| 定义 | [cargoverse:dmc/boreal_sd_m](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/dmc/boreal_sd_m.json>) |
| 名称／规格 | DMC Boreal 封闭散料柜 M 型／M |
| 结构 ID | `cargoverse:cargo/dmc/boreal/dmc_boreal_sd_m` |
| NBT | [项目结构文件](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/dmc/boreal/dmc_boreal_sd_m.nbt>) |
| 包络 X×Y×Z | 10×6×5 |
| 实际接口 | 标准对接接口×4 |
| 运行标记 | 分类 2、质量 2、词条 10（0～4 齐全） |

## 制造配方与投放

| 目录 | 许可证 | 繁荣等级 | 加工费 VB | 实体材料 |
| --- | --- | ---: | ---: | --- |
| [heavy_works](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/factory/sky_station/heavy_works.json>) | M | 0 | 200 | minecraft:iron_ingot × 40、minecraft:copper_ingot × 16、minecraft:chain × 8、minecraft:redstone × 4、minecraft:white_wool × 4 |
| [mineral_refinery](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/factory/sky_station/mineral_refinery.json>) | M | 0 | 200 | minecraft:iron_ingot × 40、minecraft:copper_ingot × 16、minecraft:chain × 8、minecraft:redstone × 4、minecraft:white_wool × 4 |
| [all_containers](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/market/test_station/all_containers.json>) | M | 0 | 200 | minecraft:iron_ingot × 40、minecraft:copper_ingot × 16、minecraft:chain × 8、minecraft:redstone × 4、minecraft:white_wool × 4 |
| [deepcore_mine](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/resource/sky_station/deepcore_mine.json>) | M | 0 | 200 | minecraft:iron_ingot × 40、minecraft:copper_ingot × 16、minecraft:chain × 8、minecraft:redstone × 4、minecraft:white_wool × 4 |

## 基础运输权益
本型号对应[制造商初始基础货柜权益](<../../../05_基础货柜/dmc_basic.md>)。通过基础权益领取的资产免调度点；普通制造的同型号仍使用 2 点，不修改型号定义。

## 当前 JSON

[工程定义](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/dmc/boreal_sd_m.json>)

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/dmc/boreal/dmc_boreal_sd_m",
  "manufacturer": "cargoverse:dmc",
  "display_name": "DMC Boreal 矿料重载柜 M 型",
  "description": "实际物品运输货柜；承载形态与运输保护以本定义为准。",
  "size_class": "M",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 2,
  "capacity": 150,
  "empty_mass": 65,
  "allowed_cargo_classes": [
    "solid"
  ],
  "special_designs": [],
  "design_defects": [],
  "tags": [
    "series.dmc.boreal"
  ],
  "cargo_class_capacity_modifiers": {},
  "abilities": {
    "cargoverse:containment": {
      "level": 1
    },
    "cargoverse:cushioning": {
      "level": 1,
      "velocity_change_bonus": 2
    }
  }
}
```

## 实机验收

模板装配、满载起吊、对接及持续航程需在游戏中核验。当前数值以数据包配置为准。
