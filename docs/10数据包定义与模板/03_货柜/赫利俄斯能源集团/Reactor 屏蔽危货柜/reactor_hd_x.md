# HEC Reactor 屏蔽危货柜 X 型

> 分类同步说明（2026-10-20）：本页兼容类别已更新为十四类方案。其他型号/投放规划可能保留历史设计，完整运行时定义以项目 JSON 为准；本轮不重平衡容量、质量或制造价格。


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

| 指标 | 定义基础值 | 实际值 |
| --- | ---: | ---: |
| 容量（个） | 210 | 210 |
| 空柜目标质量（Kpg） | 210 | 210 |

未配置 CargoClass 容量修正，所有允许分类均使用基础容量。

容量、空重、防护与缺陷均由本货柜型号直接定义；未列出的允许分类使用基础容量。指定分类容量在最终乘算后一次向下取整。目标空重仍受结构中非货柜方块质量下限约束。

## CargoClass 兼容

| 分类 | CargoClass |
| --- | --- |
| 化工与药剂 | `chemical_material` |
| 燃料与能源 | `energy_fuel` |
| 原料资源 | `raw_resource` |
| 加工材料 | `processed_resource` |

仅允许上述类别，不支持 none；一柜只装一种精确物品变体。首批物品标签与运输参数已配置；未覆盖物品使用默认运输规则，不代表全部物品已经归类或平衡。

## 防护与运输要求

消除：放射性、勿倒置。`cargoverse:radioactive`、`cargoverse:keep_upright`

设计缺陷：无。所有货物的原有 time_limit 继续生效；御寒不代表恒温冷藏。

## 制造与投放

| 项目 | v2 实体材料设计 |
| --- | --- |
| 加工费 | 1400 VB |
| 实体材料 | 铁锭 ×168、黑曜石 ×56、玻璃 ×28、红石比较器 ×7 |
| 最低许可证 | X |
| 最低繁荣等级 | 3 |
| 材料最少占格 | 6 格，按每种物品 64 堆叠 |
| 当前配方状态 | 配方设计完成，尚未写入运行时制造定义 |

正式提供节点：[E03 净水与环境处理站](<../../../07_贸易点/factory/净水与环境处理站/定义设计/01_货柜制造台定义.md>)（固定专业工坊）。同型号跨站使用同一实体配方、加工费和门槛；玩家背包供料，不扣贸易点库存。普通资产按当前型号占用调度点，基础领取独立处理。

[统一配方与定价依据](<../../../08_货柜制造台/制造配方与投放总表.md>)。数值为首轮设计目标，尚未完成实机平衡。

## 当前 JSON

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/hec/reactor/hec_reactor_hd_x",
  "manufacturer": "cargoverse:hec",
  "display_name": "HEC Reactor 屏蔽危货柜 X 型",
  "description": "§lHEC Reactor 屏蔽危货柜 X 型\n§r§7以屏蔽与固定结构承运退役放射源等危险货物，较低容量换取屏蔽与放射性防护。\n§r§l制造商：赫利俄斯能源集团 / Helios Energy Corporation\n§r§l系列：Reactor 屏蔽危货柜",
  "size_class": "X",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 6,
  "capacity": 210,
  "empty_mass": 210,
  "allowed_cargo_classes": [
    "chemical_material",
    "energy_fuel",
    "raw_resource",
    "processed_resource"
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
