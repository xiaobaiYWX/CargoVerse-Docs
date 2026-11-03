# BDS Sentinel 保护货柜 M 型

可制造。更新于 2026-11-03。

[系列目录](README.md) · [制造商目录](../README.md)

## 定义与承载

| 项目 | 当前值 |
| --- | --- |
| 资源 ID | `cargoverse:bds/sentinel_mc_m` |
| 介质 | solid |
| 尺寸 | M |
| 容量 | 95 组 |
| 定义空重 | 65 Kpg |
| 调度点 | 2 |
| 标签 | series.bds.sentinel |

实际空重取结构质量与配置空重的较大值，载荷质量另计。固体按冻结组大小计量，流体一桶为 1000 mB，生物按物种舱位确定可装只数。

## 当前保护能力

| 能力 | 参数 |
| --- | --- |
| 围护 | `level=1` |
| 密封 | `level=1` |
| 缓冲衬垫 | `level=2`，`velocity_change_bonus=5` |
| 朝向保持 | `level=1` |
| 遮光结构 | `level=1`，`reduction=15` |

完整运输条件随货物冻结，保护能力影响对应的围护、密封或内部环境求值。设备初始按需自动工作，实际降温与调压需要时间。

## 结构模板
| 项目 | 实际配置 |
| --- | --- |
| 定义 | [cargoverse:bds/sentinel_mc_m](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/bds/sentinel_mc_m.json>) |
| 名称／规格 | BDS Sentinel 装备防护柜 M 型／M |
| 结构 ID | `cargoverse:cargo/bds/sentinel/bds_sentinel_mc_m` |
| NBT | [项目结构文件](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/bds/sentinel/bds_sentinel_mc_m.nbt>) |
| 包络 X×Y×Z | 6×6×6 |
| 实际接口 | 磁吸板×32 |
| 运行标记 | 分类 4、质量 4、词条 20（0～4 齐全） |

## 制造配方与投放

| 目录 | 许可证 | 繁荣等级 | 加工费 VB | 实体材料 |
| --- | --- | ---: | ---: | --- |
| [defense_arsenal](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/factory/sky_station/defense_arsenal.json>) | M | 1 | 320 | minecraft:iron_ingot × 40、minecraft:leather × 8、minecraft:chain × 4、minecraft:redstone × 4、create:cogwheel × 2、minecraft:white_wool × 4 |
| [security_works](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/factory/sky_station/security_works.json>) | M | 1 | 320 | minecraft:iron_ingot × 40、minecraft:leather × 8、minecraft:chain × 4、minecraft:redstone × 4、create:cogwheel × 2、minecraft:white_wool × 4 |
| [all_containers](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/market/test_station/all_containers.json>) | M | 1 | 320 | minecraft:iron_ingot × 40、minecraft:leather × 8、minecraft:chain × 4、minecraft:redstone × 4、create:cogwheel × 2、minecraft:white_wool × 4 |

## 当前 JSON

[工程定义](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/bds/sentinel_mc_m.json>)

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/bds/sentinel/bds_sentinel_mc_m",
  "manufacturer": "cargoverse:bds",
  "display_name": "BDS Sentinel 保护货柜 M 型",
  "description": "实际物品运输货柜；承载形态与运输保护以本定义为准。",
  "size_class": "M",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 2,
  "capacity": 95,
  "empty_mass": 65,
  "allowed_cargo_classes": [
    "solid"
  ],
  "special_designs": [],
  "design_defects": [],
  "tags": [
    "series.bds.sentinel"
  ],
  "cargo_class_capacity_modifiers": {},
  "abilities": {
    "cargoverse:containment": {
      "level": 1
    },
    "cargoverse:sealing": {
      "level": 1
    },
    "cargoverse:cushioning": {
      "level": 2,
      "velocity_change_bonus": 5
    },
    "cargoverse:orientation_control": {
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
