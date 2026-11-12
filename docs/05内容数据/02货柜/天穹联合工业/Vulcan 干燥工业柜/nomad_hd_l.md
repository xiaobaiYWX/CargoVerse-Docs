# AUI Vulcan 干燥工业柜 L 型

## G2新版结构模板

**新系列代号：`vulcan_g2`；状态：仅旧定义映射，不另制模板。** 更新：2026-11-12。

| 项目 | 路径／约定 |
| --- | --- |
| 新版模板资源 ID | `cargoverse:cargo/aui/vulcan_g2/aui_vulcan_g2_sd_l` |
| 游戏导出相对路径 | `generated/cargoverse/structures/cargo/aui/vulcan_g2/aui_vulcan_g2_sd_l.nbt` |
| 工程目标相对路径 | `data/cargoverse/structure/cargo/aui/vulcan_g2/aui_vulcan_g2_sd_l.nbt` |
| 规格／接口代号 | L／SD |
| 当前运行模板（旧版参考） | `cargoverse:cargo/aui/atlas/aui_atlas_sd_l` |
| 稳定货柜定义 ID | `cargoverse:aui/nomad_hd_l`（保留） |

新版均尚未制作或接入。**后续搭建只按本节G2路径命名；旧路径仅用于核对当前运行状态，不再作为补建任务。** 本轮不指定长宽高、轨距或接口坐标，需在标准化尺寸表确认后搭建；接口代号目前沿系列既定命名保留，不代表几何标准已完成。

完成新模板后逐型号核对标记、归属、对接与结构质量，再切换运行 `template`；缺失模板型号须同时完成验收及制造开放。基础变体共用普通型号同规格G2模板。关闭兼容定义不自动启用。

[本系列目录](<README.md>) · [全系列新版代号](<../../新版模板系列代号.md>)

> **当前状态：暂不开放，制造关闭。模板：已有本系列模板，引用待调整。**
> 制作安排：仅旧定义映射，不另制模板；以本页G2新版结构模板章节为准。

## 定义与承载

| 项目 | 当前值 |
| --- | --- |
| 资源 ID | `cargoverse:aui/nomad_hd_l` |
| 介质 | solid |
| 规格 | L |
| 容量 | 270 组 |
| 定义空重 | 125 Kpg |
| 调度点 | 4 |

## 当前配置

[工程定义](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/aui/nomad_hd_l.json>)

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/aui/atlas/aui_atlas_sd_l",
  "manufacturer": "cargoverse:aui",
  "display_name": "AUI Vulcan 干燥工业柜 L 型",
  "description": "临时使用对应规格 AUI 标准干柜结构；实际承载与保护以本定义为准。",
  "size_class": "L",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 4,
  "capacity": 270,
  "empty_mass": 125,
  "allowed_cargo_classes": [
    "solid"
  ],
  "tags": [
    "series.aui.vulcan",
    "not_manufacturable"
  ],
  "cargo_class_capacity_modifiers": {},
  "abilities": {
    "cargoverse:containment": {
      "level": 2
    },
    "cargoverse:sealing": {
      "level": 1
    },
    "cargoverse:cushioning": {
      "level": 1,
      "velocity_change_bonus": 2
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

[系列目录](<README.md>) · [制造商目录](<../README.md>)
