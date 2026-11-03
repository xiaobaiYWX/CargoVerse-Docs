# DMC CoreVault 干燥精矿柜 M 型

可制造。更新于 2026-11-03。

[系列目录](README.md) · [制造商目录](../README.md)

## 定义与承载

| 项目 | 当前值 |
| --- | --- |
| 资源 ID | `cargoverse:dmc/corevault_sd_m` |
| 介质 | solid |
| 尺寸 | M |
| 容量 | 110 组 |
| 定义空重 | 72 Kpg |
| 调度点 | 2 |
| 标签 | series.dmc.corevault |

实际空重取结构质量与配置空重的较大值，载荷质量另计。固体按冻结组大小计量，流体一桶为 1000 mB，生物按物种舱位确定可装只数。

## 当前保护能力

| 能力 | 参数 |
| --- | --- |
| 围护 | `level=2` |
| 密封 | `level=1` |
| 湿度控制 | `level=1`，`target_min=20`，`target_max=60`，`rate_per_second=1`，`supported_modes=["dehumidifying"]` |
| 遮光结构 | `level=1`，`reduction=15` |

完整运输条件随货物冻结，保护能力影响对应的围护、密封或内部环境求值。设备初始按需自动工作，实际降温与调压需要时间。

## 结构模板
| 项目 | 实际配置 |
| --- | --- |
| 定义 | [cargoverse:dmc/corevault_sd_m](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/dmc/corevault_sd_m.json>) |
| 名称／规格 | DMC CoreVault 小批固体防护柜 M 型／M |
| 结构 ID | `cargoverse:cargo/dmc/corevault/dmc_corevault_sd_m` |
| NBT | [项目结构文件](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/dmc/corevault/dmc_corevault_sd_m.nbt>) |
| 包络 X×Y×Z | 8×5×7 |
| 实际接口 | 标准对接接口×4 |
| 运行标记 | 分类 2、质量 2、词条 10（0～4 齐全） |

## 制造配方与投放

| 目录 | 许可证 | 繁荣等级 | 加工费 VB | 实体材料 |
| --- | --- | ---: | ---: | --- |
| [heavy_works](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/factory/sky_station/heavy_works.json>) | M | 1 | 300 | minecraft:iron_ingot × 32、minecraft:glass × 8、minecraft:white_wool × 16、minecraft:redstone × 8、minecraft:sponge × 2 |
| [all_containers](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/market/test_station/all_containers.json>) | M | 1 | 300 | minecraft:iron_ingot × 32、minecraft:glass × 8、minecraft:white_wool × 16、minecraft:redstone × 8、minecraft:sponge × 2 |

## 当前 JSON

[工程定义](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/dmc/corevault_sd_m.json>)

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/dmc/corevault/dmc_corevault_sd_m",
  "manufacturer": "cargoverse:dmc",
  "display_name": "DMC CoreVault 干燥精矿柜 M 型",
  "description": "实际物品运输货柜；承载形态与运输保护以本定义为准。",
  "size_class": "M",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 2,
  "capacity": 110,
  "empty_mass": 72,
  "allowed_cargo_classes": [
    "solid"
  ],
  "special_designs": [],
  "design_defects": [],
  "tags": [
    "series.dmc.corevault"
  ],
  "cargo_class_capacity_modifiers": {},
  "abilities": {
    "cargoverse:containment": {
      "level": 2
    },
    "cargoverse:sealing": {
      "level": 1
    },
    "cargoverse:humidity_control": {
      "level": 1,
      "target_min": 20,
      "target_max": 60,
      "rate_per_second": 1,
      "supported_modes": [
        "dehumidifying"
      ]
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
