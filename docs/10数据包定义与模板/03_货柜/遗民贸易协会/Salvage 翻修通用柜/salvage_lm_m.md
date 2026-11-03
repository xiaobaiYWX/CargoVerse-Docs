# REX Salvage 修复货柜 M 型

可制造。更新于 2026-11-03。

[系列目录](README.md) · [制造商目录](../README.md)

## 定义与承载

| 项目 | 当前值 |
| --- | --- |
| 资源 ID | `cargoverse:rex/salvage_lm_m` |
| 介质 | solid |
| 尺寸 | M |
| 容量 | 110 组 |
| 定义空重 | 68 Kpg |
| 调度点 | 2 |
| 标签 | series.rex.salvage |

实际空重取结构质量与配置空重的较大值，载荷质量另计。固体按冻结组大小计量，流体一桶为 1000 mB，生物按物种舱位确定可装只数。

## 当前保护能力

| 能力 | 参数 |
| --- | --- |
| 围护 | `level=1` |
| 缓冲衬垫 | `level=2`，`velocity_change_bonus=5` |
| 遮光结构 | `level=1`，`reduction=15` |

完整运输条件随货物冻结，保护能力影响对应的围护、密封或内部环境求值。设备初始按需自动工作，实际降温与调压需要时间。

## 结构模板
| 项目 | 实际配置 |
| --- | --- |
| 定义 | [cargoverse:rex/salvage_lm_m](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/rex/salvage_lm_m.json>) |
| 名称／规格 | REX Salvage 翻修通用柜 M 型／M |
| 结构 ID | `cargoverse:cargo/rex/salvage/rex_salvage_lm_m` |
| NBT | [项目结构文件](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/rex/salvage/rex_salvage_lm_m.nbt>) |
| 包络 X×Y×Z | 8×6×6 |
| 实际接口 | 绳索连接器×4 |
| 运行标记 | 分类 2、质量 4、词条 10（0～4 齐全） |

## 制造配方与投放

| 目录 | 许可证 | 繁荣等级 | 加工费 VB | 实体材料 |
| --- | --- | ---: | ---: | --- |
| [all_containers](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/market/test_station/all_containers.json>) | M | 1 | 160 | minecraft:iron_ingot × 16、minecraft:copper_ingot × 16、minecraft:oak_planks × 16、minecraft:leather × 8、minecraft:white_wool × 4 |
| [remnant_exchange](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/resource/sky_station/remnant_exchange.json>) | M | 1 | 160 | minecraft:iron_ingot × 16、minecraft:copper_ingot × 16、minecraft:oak_planks × 16、minecraft:leather × 8、minecraft:white_wool × 4 |

## 当前 JSON

[工程定义](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/rex/salvage_lm_m.json>)

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/rex/salvage/rex_salvage_lm_m",
  "manufacturer": "cargoverse:rex",
  "display_name": "REX Salvage 修复货柜 M 型",
  "description": "实际物品运输货柜；承载形态与运输保护以本定义为准。",
  "size_class": "M",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 2,
  "capacity": 110,
  "empty_mass": 68,
  "allowed_cargo_classes": [
    "solid"
  ],
  "special_designs": [],
  "design_defects": [],
  "tags": [
    "series.rex.salvage"
  ],
  "cargo_class_capacity_modifiers": {},
  "abilities": {
    "cargoverse:containment": {
      "level": 1
    },
    "cargoverse:cushioning": {
      "level": 2,
      "velocity_change_bonus": 5
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
