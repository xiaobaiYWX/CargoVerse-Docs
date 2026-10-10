# 桶装航空燃油

状态：正式 CargoGood 定义；整数数值批次 2026-10-02。计量口径见[整数数值基线](<../整数数值基线.md>)，后续按实际航运测试校准。

## 定义

| 项目 | 内容 |
| --- | --- |
| 资源 ID | `cargoverse:energy_fuel/aviation_fuel_drums` |
| JSON 文件 | `src/main/resources/data/cargoverse/cargo_goods/energy_fuel/aviation_fuel_drums.json` |
| Schema 版本 | 1 |
| CargoClass | `energy_fuel` |
| 显示名称 | 桶装航空燃油 |
| UI 图标 | `cargoverse:textures/gui/cargo_goods/energy_fuel/aviation_fuel_drums.png`（32×32 RGBA PNG） |
| 科技等级 | 3 |
| 结算单位 | `cargoverse:void_byte` |

## 数值

| 项目 | 数值 | 单位 |
| --- | ---: | --- |
| 单位质量 | 3 | Kpg/t |
| 单位基础价值 | 40 | VB/t |
| 单位许可证经验 | 8 | exp/t |
| 单位繁荣经验 | 4 | exp/t |
| 基础完整度 | 200 | 点 |

## 运输要求

| 词条 ID | 参数 |
| --- | --- |
| `cargoverse:keep_upright` | `damage_per_second` = 1；`min_up_dot` = 0.6 |
| `cargoverse:flammable` | `ignition_temperature` = 200；`sunlight_threshold` = 12；`sunlight_heat_per_second` = 2；`hot_biome_temperature_threshold` = 1.5；`hot_biome_heat_per_second` = 3；`cold_biome_temperature_threshold` = 0.15；`cold_biome_cooling_per_second` = 2；`shade_cooling_per_second` = 1；`burning_damage_per_second` = 2 |

## 内容定位与投放

燃料精制厂→机场、航运维护站；高频能源货；易燃、勿倒置

- 设计来源：[E01 赫利俄斯燃料供应站](<../../07_贸易点/factory/赫利俄斯燃料供应站/00_总体说明.md>)；主要去处：[A03 飞艇总装与航修港](<../../07_贸易点/factory/飞艇总装与航修港/00_总体说明.md>)。按[资源表版贸易点设计](<../../07_贸易点/设计总览.md>)投放，贸易点与资源表已同步数据包，自然结构已接入。
- 当前主要来源采用持续周转：初始 400 t、容量 800 t、日补 200 t；主要买方长期不限额收购。按[数量与运力基线](<../数量与运力基线.md>)配置，t 表示货物数量而非吨。
- 基础估值沿用现值；质量按物流定位取整数，经验按科技层级使用整数计分，完整度与损耗等比调整；详见[整数数值基线](<../整数数值基线.md>)。
- 资源表、商店或制造台均通过完整 CargoGood ID 显式引用本货物。

[返回 CargoGood 目录](../README.md)

图标采用统一像素风格的独立实物轮廓，由内置 image_gen 生成并导出为 32×32；透明底、最近邻缩放，无文字标签。
