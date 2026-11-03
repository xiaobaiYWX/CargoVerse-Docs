# SPL Express 正放快运柜 S 型

可制造。更新于 2026-11-03。

[系列目录](README.md) · [制造商目录](../README.md)

## 定义与承载

| 项目 | 当前值 |
| --- | --- |
| 资源 ID | `cargoverse:spl/express_mc_s` |
| 介质 | solid |
| 尺寸 | S |
| 容量 | 30 组 |
| 定义空重 | 14 Kpg |
| 调度点 | 1 |
| 标签 | series.spl.express |

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
| 定义 | [cargoverse:spl/express_mc_s](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/spl/express_mc_s.json>) |
| 名称／规格 | SPL Express 防护快件舱 S 型／S |
| 结构 ID | `cargoverse:cargo/spl/express/spl_express_mc_s` |
| NBT | [项目结构文件](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/spl/express/spl_express_mc_s.nbt>) |
| 包络 X×Y×Z | 6×4×5 |
| 实际接口 | 磁吸板×6 |
| 运行标记 | 分类 2、质量 2、词条 10（0～4 齐全） |

## 制造配方与投放

| 目录 | 许可证 | 繁荣等级 | 加工费 VB | 实体材料 |
| --- | --- | ---: | ---: | --- |
| [civic_distribution](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/market/sky_station/civic_distribution.json>) | S | 0 | 110 | minecraft:iron_ingot × 8、minecraft:copper_ingot × 8、minecraft:white_wool × 4、minecraft:repeater × 1、create:cogwheel × 1 |
| [longhaul_port](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/market/sky_station/longhaul_port.json>) | S | 0 | 110 | minecraft:iron_ingot × 8、minecraft:copper_ingot × 8、minecraft:white_wool × 4、minecraft:repeater × 1、create:cogwheel × 1 |
| [all_containers](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/market/test_station/all_containers.json>) | S | 0 | 110 | minecraft:iron_ingot × 8、minecraft:copper_ingot × 8、minecraft:white_wool × 4、minecraft:repeater × 1、create:cogwheel × 1 |

## 当前 JSON

[工程定义](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/spl/express_mc_s.json>)

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/spl/express/spl_express_mc_s",
  "manufacturer": "cargoverse:spl",
  "display_name": "SPL Express 正放快运柜 S 型",
  "description": "实际物品运输货柜；承载形态与运输保护以本定义为准。",
  "size_class": "S",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 1,
  "capacity": 30,
  "empty_mass": 14,
  "allowed_cargo_classes": [
    "solid"
  ],
  "special_designs": [],
  "design_defects": [],
  "tags": [
    "series.spl.express"
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
