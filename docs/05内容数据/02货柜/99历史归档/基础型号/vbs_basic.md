# VBS Harvest 保鲜货柜 S 型（基础型）

## G2新版结构模板

**新系列代号：`harvest_g2`；状态：沿普通型号共用，不重复制作。** 更新：2026-11-12。

| 项目 | 路径／约定 |
| --- | --- |
| 新版模板资源 ID | `cargoverse:cargo/vbs/harvest_g2/vbs_harvest_g2_lm_s` |
| 游戏导出相对路径 | `generated/cargoverse/structures/cargo/vbs/harvest_g2/vbs_harvest_g2_lm_s.nbt` |
| 工程目标相对路径 | `data/cargoverse/structure/cargo/vbs/harvest_g2/vbs_harvest_g2_lm_s.nbt` |
| 规格／接口代号 | S／LM |
| 当前运行模板（旧版参考） | `cargoverse:cargo/vbs/harvest/vbs_harvest_lm_s` |
| 稳定货柜定义 ID | `cargoverse:vbs/starter_harvest_lm_s`（保留） |

新版均尚未制作或接入。**后续搭建只按本节G2路径命名；旧路径仅用于核对当前运行状态，不再作为补建任务。** 本轮不指定长宽高、轨距或接口坐标，需在标准化尺寸表确认后搭建；接口代号目前沿系列既定命名保留，不代表几何标准已完成。

完成新模板后逐型号核对标记、归属、对接与结构质量，再切换运行 `template`；缺失模板型号须同时完成验收及制造开放。基础变体共用普通型号同规格G2模板。关闭兼容定义不自动启用。

[本系列目录](<../../绿洲农业联盟/Harvest 保鲜货柜/README.md>) · [全系列新版代号](<../../新版模板系列代号.md>)

> **当前状态：基础型，可制造。模板：本系列模板已绑定。**
> 制作安排：沿普通型号共用，不重复制作；以本页G2新版结构模板章节为准。

## 定义与承载

| 项目 | 当前值 |
| --- | --- |
| 资源 ID | `cargoverse:vbs/starter_harvest_lm_s` |
| 介质 | solid |
| 规格 | S |
| 容量 | 60 组 |
| 定义空重 | 26 Kpg |
| 调度点 | 0 |

## 当前配置

[工程定义](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/vbs/starter_harvest_lm_s.json>)

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/vbs/harvest/vbs_harvest_lm_s",
  "manufacturer": "cargoverse:vbs",
  "display_name": "VBS Harvest 保鲜货柜 S 型（基础型）",
  "description": "基础货柜：每名玩家同时只能拥有一个，不占调度点。实际物品运输货柜；承载形态与运输保护以本定义为准。",
  "size_class": "S",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 0,
  "capacity": 60,
  "empty_mass": 26,
  "allowed_cargo_classes": [
    "solid"
  ],
  "tags": [
    "series.vbs.harvest",
    "starter"
  ],
  "cargo_class_capacity_modifiers": {},
  "abilities": {
    "cargoverse:containment": {
      "level": 1
    },
    "cargoverse:sealing": {
      "level": 1
    },
    "cargoverse:vacuum_insulation": {
      "level": 1,
      "exchange_time_seconds": 240
    },
    "cargoverse:thermal_control": {
      "level": 1,
      "target_min": 2,
      "target_max": 40,
      "rate_per_second": 0.3,
      "supported_modes": [
        "cooling",
        "heating"
      ]
    },
    "cargoverse:light_blocking": {
      "level": 1,
      "reduction": 15
    }
  }
}
```
