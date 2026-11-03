# SPL Cistern 常规液罐 L 型

可制造。更新于 2026-11-03。

[系列目录](README.md) · [制造商目录](../README.md)

## 定义与承载

| 项目 | 当前值 |
| --- | --- |
| 资源 ID | `cargoverse:spl/cistern_sd_l` |
| 介质 | liquid |
| 尺寸 | L |
| 容量 | 240 桶 |
| 定义空重 | 140 Kpg |
| 调度点 | 4 |
| 标签 | series.spl.cistern |

实际空重取结构质量与配置空重的较大值，载荷质量另计。固体按冻结组大小计量，流体一桶为 1000 mB，生物按物种舱位确定可装只数。

## 当前保护能力

| 能力 | 参数 |
| --- | --- |
| 密封 | `level=1` |

完整运输条件随货物冻结，保护能力影响对应的围护、密封或内部环境求值。设备初始按需自动工作，实际降温与调压需要时间。

## 结构模板
| 项目 | 当前事实／制作目标 |
| --- | --- |
| 定义 | [cargoverse:spl/cistern_sd_l](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/spl/cistern_sd_l.json>) |
| 当前实际引用 | `cargoverse:cargo/aui/atlas/aui_atlas_sd_l` |
| 当前 NBT | [Atlas L 占位结构](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/aui/atlas/aui_atlas_sd_l.nbt>)；包络 13×6×6，体积 468；标准对接接口×6 |
| 专用路径建议 | `cargoverse:cargo/spl/cistern/spl_cistern_sd_l`；这是原候选／设计目标，不是已批准的分配结果 |
| 制作优先级 | 后续专项：先预留职责，不为未实现机制赶工 |
| 最终采用 | 待你分配；未切换运行引用 |

**无本型号原专用 NBT。** 当前能引用 Atlas 只表示占位可加载，不能当作粉料柜／封存柜／罐体等职责已经在模型中完成。

## 制造配方与投放

| 目录 | 许可证 | 繁荣等级 | 加工费 VB | 实体材料 |
| --- | --- | ---: | ---: | --- |
| [biosystems_station](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/factory/sky_station/biosystems_station.json>) | L | 2 | 360 | minecraft:iron_ingot × 64、minecraft:oak_planks × 32、minecraft:glass × 16、minecraft:redstone × 8、create:fluid_tank × 4 |
| [all_containers](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/market/test_station/all_containers.json>) | L | 2 | 360 | minecraft:iron_ingot × 64、minecraft:oak_planks × 32、minecraft:glass × 16、minecraft:redstone × 8、create:fluid_tank × 4 |

## 当前 JSON

[工程定义](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/spl/cistern_sd_l.json>)

```json
{
  "schema_version": 1,
  "manufacturer": "cargoverse:spl",
  "trade_currency": "cargoverse:void_byte",
  "template": "cargoverse:cargo/aui/atlas/aui_atlas_sd_l",
  "display_name": "SPL Cistern 常规液罐 L 型",
  "description": "液体运输罐柜；容量按1000mB为一个单位，实际载荷与保护由数据包定义。",
  "size_class": "L",
  "dispatch_points": 4,
  "empty_mass": 140,
  "allowed_cargo_classes": [
    "liquid"
  ],
  "cargo_class_capacity_modifiers": {},
  "special_designs": [],
  "design_defects": [],
  "tags": [
    "series.spl.cistern"
  ],
  "capacity": 240,
  "abilities": {
    "cargoverse:sealing": {
      "level": 1
    }
  }
}
```

## 实机验收

模板装配、满载起吊、对接及持续航程需在游戏中核验。当前数值以数据包配置为准。
