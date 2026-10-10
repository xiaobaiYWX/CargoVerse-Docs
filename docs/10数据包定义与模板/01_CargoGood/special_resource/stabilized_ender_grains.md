# 稳相末影晶粒

状态：正式 CargoGood 定义；整数数值批次 2026-10-02。计量口径见[整数数值基线](<../整数数值基线.md>)，后续按实际航运测试校准。

## 定义

| 项目 | 内容 |
| --- | --- |
| 资源 ID | `cargoverse:special_resource/stabilized_ender_grains` |
| JSON 文件 | `src/main/resources/data/cargoverse/cargo_goods/special_resource/stabilized_ender_grains.json` |
| Schema 版本 | 1 |
| CargoClass | `special_resource` |
| 显示名称 | 稳相末影晶粒 |
| UI 图标 | `cargoverse:textures/gui/cargo_goods/special_resource/stabilized_ender_grains.png`（32×32 RGBA PNG） |
| 科技等级 | 4 |
| 结算单位 | `cargoverse:void_byte` |

## 数值

| 项目 | 数值 | 单位 |
| --- | ---: | --- |
| 单位质量 | 2 | Kpg/t |
| 单位基础价值 | 90 | VB/t |
| 单位许可证经验 | 12 | exp/t |
| 单位繁荣经验 | 6 | exp/t |
| 基础完整度 | 200 | 点 |

## 运输要求

| 词条 ID | 参数 |
| --- | --- |
| `cargoverse:moisture_proof` | `damage_per_second` = 1 |

## 内容定位与投放

末影材料稳定化设施→高端定位设备、相位研究；已稳定的功能材料；防潮

- 设计来源：[H03 虚空相位研究站](<../../07_贸易点/resource/虚空相位研究站/00_总体说明.md>)；主要去处：[R03 远界异常交换站](<../../07_贸易点/resource/远界异常交换站/00_总体说明.md>)。按[资源表版贸易点设计](<../../07_贸易点/设计总览.md>)投放，贸易点与资源表已同步数据包，自然结构已接入。
- 当前主要来源采用持续周转：初始 200 t、容量 400 t、日补 100 t；主要买方长期不限额收购。按[数量与运力基线](<../数量与运力基线.md>)配置，t 表示货物数量而非吨。
- 基础估值沿用现值；质量按物流定位取整数，经验按科技层级使用整数计分，完整度与损耗等比调整；详见[整数数值基线](<../整数数值基线.md>)。
- 资源表、商店或制造台均通过完整 CargoGood ID 显式引用本货物。

[返回 CargoGood 目录](../README.md)

图标采用统一像素风格的独立实物轮廓，由内置 image_gen 生成并导出为 32×32；透明底、最近邻缩放，无文字标签。
