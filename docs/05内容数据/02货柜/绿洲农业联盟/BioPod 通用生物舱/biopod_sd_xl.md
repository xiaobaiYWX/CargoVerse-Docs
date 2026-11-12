# VBS BioPod 通用生物舱 XL 型

> **当前状态：待模板，制造关闭。模板：缺失。** 更新：2026-11-11。
> 这是已确定的正式扩充型号；需制作下列指定模板，完成校验后再开放制造和蓝图投放。

## 定位与承载

通用生物大宗运输，基础缓冲+2、调温稳压与遮光；所有已准入物种共用。X／XL提高单柜容量及每调度点运量，保护能力不随规格自动升级。

| 项目 | 当前定义 |
| --- | --- |
| 资源 ID | `cargoverse:vbs/biopod_sd_xl` |
| 规格／许可 | XL／XL |
| 介质 | living |
| 容量 | 224 舱位 |
| 定义空重 | 88 Kpg |
| 调度点 | 8 |
| 每调度点容量 | 28.00 舱位 |

实际空重受结构质量下限约束，模板未完成前不能将定义空重视为装配实测值。容量不是质量。

## G2新版结构模板

**新系列代号：`biopod_g2`；状态：需制作G2新版模板。** 更新：2026-11-12。

| 项目 | 路径／约定 |
| --- | --- |
| 新版模板资源 ID | `cargoverse:cargo/vbs/biopod_g2/vbs_biopod_g2_sd_xl` |
| 游戏导出相对路径 | `generated/cargoverse/structures/cargo/vbs/biopod_g2/vbs_biopod_g2_sd_xl.nbt` |
| 工程目标相对路径 | `data/cargoverse/structure/cargo/vbs/biopod_g2/vbs_biopod_g2_sd_xl.nbt` |
| 规格／接口代号 | XL／SD |
| 当前运行模板（旧版参考） | `cargoverse:cargo/vbs/biopod/vbs_biopod_sd_xl` |
| 稳定货柜定义 ID | `cargoverse:vbs/biopod_sd_xl`（保留） |

新版均尚未制作或接入。**后续搭建只按本节G2路径命名；旧路径仅用于核对当前运行状态，不再作为补建任务。** 本轮不指定长宽高、轨距或接口坐标，需在标准化尺寸表确认后搭建；接口代号目前沿系列既定命名保留，不代表几何标准已完成。

完成新模板后逐型号核对标记、归属、对接与结构质量，再切换运行 `template`；缺失模板型号须同时完成验收及制造开放。基础变体共用普通型号同规格G2模板。关闭兼容定义不自动启用。

[本系列目录](<README.md>) · [全系列新版代号](<../../新版模板系列代号.md>)


## 生物数据边界

单只原生数据预算仍为65536字节，整柜仍为1048576字节；不随X／XL舱位自动提高。可装数量同时受物种舱位和原生数据字节限制，复杂NBT个体可能先达到数据上限。满柜只数不能由舱位数直接推定，也不区分陆生与水生柜。

## 保护能力

沿用本系列L型全部能力参数，完整字段见下方现行定义。大柜不提高调温、调压速率，不提供未声明的防护。

## 制造配方与投放

| 项目 | 数值／安排 |
| --- | --- |
| 蓝图打印费 | 2240 VB |
| 理想制造时间 | 70 秒（1400 tick） |
| 实体材料 | minecraft:iron_ingot × 224、minecraft:glass × 56、minecraft:blue_ice × 14、create:fluid_pipe × 14、minecraft:white_wool × 28、minecraft:hay_block × 28 |
| 拟投放 | biosystems_station（建议，尚未投放）；X最低繁荣3、XL最低繁荣4 |
| 当前投放 | 无；自然站和A／B测试站均不出售缺失模板型号 |

配方按同系列L型成本的X两倍、XL三点五倍起步；实际材料、许可与费用均已落入独立配方。模板补齐后再验证投放；单方块测试工具即使可枚举配方，制造仍受 `not_manufacturable` 限制。

## 当前配置

[工程定义](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/vbs/biopod_sd_xl.json>) · [制造配方](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_manufacturing_recipes/vbs/biopod_sd_xl.json>)

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/vbs/biopod/vbs_biopod_sd_xl",
  "manufacturer": "cargoverse:vbs",
  "display_name": "VBS BioPod 通用生物舱 XL 型",
  "description": "通用生物运输舱，提供调温、稳压、遮光与基础缓冲，适用于所有已准入物种。；X／XL 大宗运输规格，指定系列模板待制作，当前禁止制造。",
  "size_class": "XL",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 8,
  "empty_mass": 88,
  "allowed_cargo_classes": [
    "living"
  ],
  "tags": [
    "series.vbs.biopod",
    "validation_content",
    "not_manufacturable",
    "missing_template"
  ],
  "cargo_class_capacity_modifiers": {},
  "capacity": 224,
  "living_chamber": {
    "max_entity_bytes": 65536,
    "max_total_bytes": 1048576
  },
  "abilities": {
    "cargoverse:containment": {
      "level": 1
    },
    "cargoverse:sealing": {
      "level": 2
    },
    "cargoverse:cushioning": {
      "level": 1,
      "velocity_change_bonus": 2
    },
    "cargoverse:vacuum_insulation": {
      "level": 1,
      "exchange_time_seconds": 240
    },
    "cargoverse:thermal_control": {
      "level": 1,
      "target_min": 5,
      "target_max": 45,
      "rate_per_second": 0.3,
      "supported_modes": [
        "cooling",
        "heating"
      ]
    },
    "cargoverse:pressure_control": {
      "level": 1,
      "target_min": 0.5,
      "target_max": 1.5,
      "rate_per_second": 0.02,
      "supported_modes": [
        "pressurizing",
        "depressurizing"
      ]
    },
    "cargoverse:light_blocking": {
      "level": 1,
      "reduction": 15
    }
  }
}
```

[系列目录](README.md) · [制造商目录](../README.md)
