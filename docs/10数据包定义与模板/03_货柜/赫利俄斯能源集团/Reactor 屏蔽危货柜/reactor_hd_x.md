# HEC Reactor 屏蔽危货柜 X 型

[赫利俄斯能源集团](<../README.md>) → [Reactor 屏蔽危货柜](<README.md>) → X 型

恢复原有尺寸与结构模板，容量和空重按当前系列的 1∶2∶4∶7∶12 阶梯补回，耐久、分类许可与防护沿用当前系列。

## 定义

| 项目 | 内容 |
| --- | --- |
| 完整型号 | `HEC-Reactor-HD-X` |
| 资源 ID | `cargoverse:hec/reactor_hd_x` |
| 定义文件 | [reactor_hd_x.json](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/hec/reactor_hd_x.json>) |
| 制造商 | 赫利俄斯能源集团 |
| 系列全称 | Reactor 屏蔽危货柜 |
| 尺寸等级 | X |
| 调度点 | 6 |
| 结算单位 | `cargoverse:void_byte` |
| 标签 | `series.hec.reactor` |

## 结构模板

**正式模板已提供。** 当前引用：`cargoverse:cargo/hec/reactor/hec_reactor_hd_x`。

[当前 NBT 文件](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/hec/reactor/hec_reactor_hd_x.nbt>) · [模板接入状态](<../../缺失结构模板.md>)

## 数值

| 指标 | 定义基础值 | 默认实际值（含厂商通用倍率） |
| --- | --- | --- |
| 容量（t） | 42 | 42 |
| 空柜目标质量（Kpg） | 210 | 210 |
| 最大耐久 | 190 | 190 |

实际容量包含厂商通用倍率并向下取整；专项货物倍率另行计算。空重仍受模板中非货柜方块质量下限约束。

## CargoClass 兼容

`hazardous_material`。仅允许上述分类，不支持 none；同一货柜不可混装不同 CargoGood。

## 防护与运输要求

消除：放射性、勿倒置。`cargoverse:radioactive`、`cargoverse:keep_upright`

设计缺陷：无。所有货物的原有 time_limit 继续生效；御寒不代表恒温冷藏。

## 制造与投放

| 项目 | 规划 |
| --- | --- |
| 加工费 VB | 1400 |
| 最低许可证 | X |
| 最低繁荣等级 | 4 |
| 节点类型 | 危险物接收站、退役源处置站 |
| 当前配方 | 待编制材料配方与投放；定义已注册 |

## 当前 JSON

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/hec/reactor/hec_reactor_hd_x",
  "manufacturer": "cargoverse:hec",
  "display_name": "HEC Reactor 屏蔽危货柜 X 型",
  "description": "§lHEC Reactor 屏蔽危货柜 X 型\n§r§7以屏蔽与固定结构承运退役放射源等危险货物，较低容量换取高耐久与放射性防护。\n§r§l制造商：赫利俄斯能源集团 / Helios Energy Corporation\n§r§l系列：Reactor 屏蔽危货柜",
  "size_class": "X",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 6,
  "capacity": 42,
  "empty_mass": 210,
  "max_durability": 190,
  "allowed_cargo_classes": [
    "hazardous_material"
  ],
  "special_designs": [
    "cargoverse:radioactive",
    "cargoverse:keep_upright"
  ],
  "design_defects": [],
  "tags": [
    "series.hec.reactor"
  ]
}
```
