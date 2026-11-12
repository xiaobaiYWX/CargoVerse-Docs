# SPL Cistern 常规液罐 XL 型

> **当前状态：待模板，制造关闭。模板：缺失。** 更新：2026-11-11。
> 这是已确定的正式扩充型号；需制作下列指定模板，完成校验后再开放制造和蓝图投放。

## 定位与承载

常规流体大宗运输，保留密封1，无主动调温与稳压。X／XL提高单柜容量及每调度点运量，保护能力不随规格自动升级。

| 项目 | 当前定义 |
| --- | --- |
| 资源 ID | `cargoverse:spl/cistern_sd_xl` |
| 规格／许可 | XL／XL |
| 介质 | liquid |
| 容量 | 800 桶 |
| 定义空重 | 420 Kpg |
| 调度点 | 8 |
| 每调度点容量 | 100.00 桶 |

实际空重受结构质量下限约束，模板未完成前不能将定义空重视为装配实测值。容量不是质量。

## G2新版结构模板

**新系列代号：`cistern_g2`；状态：需制作G2新版模板。** 更新：2026-11-12。

| 项目 | 路径／约定 |
| --- | --- |
| 新版模板资源 ID | `cargoverse:cargo/spl/cistern_g2/spl_cistern_g2_sd_xl` |
| 游戏导出相对路径 | `generated/cargoverse/structures/cargo/spl/cistern_g2/spl_cistern_g2_sd_xl.nbt` |
| 工程目标相对路径 | `data/cargoverse/structure/cargo/spl/cistern_g2/spl_cistern_g2_sd_xl.nbt` |
| 规格／接口代号 | XL／SD |
| 当前运行模板（旧版参考） | `cargoverse:cargo/spl/cistern/spl_cistern_sd_xl` |
| 稳定货柜定义 ID | `cargoverse:spl/cistern_sd_xl`（保留） |

新版均尚未制作或接入。**后续搭建只按本节G2路径命名；旧路径仅用于核对当前运行状态，不再作为补建任务。** 本轮不指定长宽高、轨距或接口坐标，需在标准化尺寸表确认后搭建；接口代号目前沿系列既定命名保留，不代表几何标准已完成。

完成新模板后逐型号核对标记、归属、对接与结构质量，再切换运行 `template`；缺失模板型号须同时完成验收及制造开放。基础变体共用普通型号同规格G2模板。关闭兼容定义不自动启用。

[本系列目录](<README.md>) · [全系列新版代号](<../../新版模板系列代号.md>)


## 保护能力

沿用本系列L型全部能力参数，完整字段见下方现行定义。大柜不提高调温、调压速率，不提供未声明的防护。

## 制造配方与投放

| 项目 | 数值／安排 |
| --- | --- |
| 蓝图打印费 | 1260 VB |
| 理想制造时间 | 70 秒（1400 tick） |
| 实体材料 | minecraft:iron_ingot × 224、minecraft:oak_planks × 112、minecraft:glass × 56、minecraft:redstone × 28、create:fluid_tank × 14 |
| 拟投放 | biosystems_station；X最低繁荣3、XL最低繁荣4 |
| 当前投放 | 无；自然站和A／B测试站均不出售缺失模板型号 |

配方按同系列L型成本的X两倍、XL三点五倍起步；实际材料、许可与费用均已落入独立配方。模板补齐后再验证投放；单方块测试工具即使可枚举配方，制造仍受 `not_manufacturable` 限制。

## 当前配置

[工程定义](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/spl/cistern_sd_xl.json>) · [制造配方](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_manufacturing_recipes/spl/cistern_sd_xl.json>)

```json
{
  "schema_version": 1,
  "manufacturer": "cargoverse:spl",
  "trade_currency": "cargoverse:void_byte",
  "template": "cargoverse:cargo/spl/cistern/spl_cistern_sd_xl",
  "display_name": "SPL Cistern 常规液罐 XL 型",
  "description": "液体运输罐柜；X／XL 大宗运输规格，指定系列模板待制作，当前禁止制造。",
  "size_class": "XL",
  "dispatch_points": 8,
  "empty_mass": 420,
  "allowed_cargo_classes": [
    "liquid"
  ],
  "cargo_class_capacity_modifiers": {},
  "tags": [
    "series.spl.cistern",
    "not_manufacturable",
    "missing_template"
  ],
  "capacity": 800,
  "abilities": {
    "cargoverse:sealing": {
      "level": 1
    }
  }
}
```

[系列目录](README.md) · [制造商目录](../README.md)
