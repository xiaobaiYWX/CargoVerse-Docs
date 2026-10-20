# HRI Explorer 科考样本舱 L 型

> 分类同步说明（2026-10-20）：本页兼容类别已更新为十四类方案。其他型号/投放规划可能保留历史设计，完整运行时定义以项目 JSON 为准；本轮不重平衡容量、质量或制造价格。


[地平线研究院](<../README.md>) → [Explorer 科考样本舱](<README.md>) → L 型

恢复原有尺寸与结构模板，容量和空重按当前系列的 1∶2∶4∶7∶12 阶梯补回，耐久、分类许可与防护沿用当前系列。

## 定义

| 项目 | 内容 |
| --- | --- |
| 完整型号 | `HRI-Explorer-SI-L` |
| 资源 ID | `cargoverse:hri/explorer_si_l` |
| 定义文件 | [explorer_si_l.json](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/hri/explorer_si_l.json>) |
| 制造商 | 地平线研究院 |
| 系列全称 | Explorer 科考样本舱 |
| 尺寸等级 | L |
| 调度点 | 4 |
| 结算单位 | `cargoverse:void_byte` |
| 标签 | `series.hri.explorer` |

## 结构模板

**正式模板已提供。** 当前引用：`cargoverse:cargo/hri/explorer/hri_explorer_si_l`。

[当前 NBT 文件](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/hri/explorer/hri_explorer_si_l.nbt>) · [模板接入状态](<../../缺失结构模板.md>)

## 数值

| 指标 | 定义基础值 | 实际值 |
| --- | ---: | ---: |
| 容量（个） | 128 | 128 |
| 空柜目标质量（Kpg） | 105.6 | 105.6 |

未配置 CargoClass 容量修正，所有允许分类均使用基础容量。

容量、空重、防护与缺陷均由本货柜型号直接定义；未列出的允许分类使用基础容量。指定分类容量在最终乘算后一次向下取整。目标空重仍受结构中非货柜方块质量下限约束。

## CargoClass 兼容

| 分类 | CargoClass |
| --- | --- |
| 原料资源 | `raw_resource` |
| 加工材料 | `processed_resource` |
| 工具与装备 | `tools_equipment` |
| 化工与药剂 | `chemical_material` |
| 红石与控制 | `electronics` |
| 通用物资 | `general_supplies` |

仅允许上述类别，不支持 none；一柜只装一种精确物品变体。首批物品标签与运输参数已配置；未覆盖物品使用默认运输规则，不代表全部物品已经归类或平衡。

## 防护与运输要求

消除：易碎、防潮、避光。`cargoverse:fragile`、`cargoverse:moisture_proof`、`cargoverse:light_sensitive`

设计缺陷：无。所有货物的原有 time_limit 继续生效；御寒不代表恒温冷藏。

## 制造与投放

| 项目 | v2 实体材料设计 |
| --- | --- |
| 加工费 | 720 VB |
| 实体材料 | 铁锭 ×48、玻璃 ×32、白色羊毛 ×32、红石 ×16 |
| 最低许可证 | L |
| 最低繁荣等级 | 2 |
| 材料最少占格 | 4 格，按每种物品 64 堆叠 |
| 当前配方状态 | 配方设计完成，尚未写入运行时制造定义 |

正式提供节点：[H02 精密电子与测绘中心](<../../../07_贸易点/factory/精密电子与测绘中心/定义设计/01_货柜制造台定义.md>)（固定专业工坊）。同型号跨站使用同一实体配方、加工费和门槛；玩家背包供料，不扣贸易点库存。普通资产按当前型号占用调度点，基础领取独立处理。

[统一配方与定价依据](<../../../08_货柜制造台/制造配方与投放总表.md>)。数值为首轮设计目标，尚未完成实机平衡。

## 当前 JSON

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/hri/explorer/hri_explorer_si_l",
  "manufacturer": "cargoverse:hri",
  "display_name": "HRI Explorer 科考样本舱 L 型",
  "description": "§lHRI Explorer 科考样本舱 L 型\n§r§7面向科考样本和采样器材往返，通过缓冲、防潮与遮光设计保护研究物资。\n§r§l制造商：地平线研究院 / Horizon Research Institute\n§r§l系列：Explorer 科考样本舱",
  "size_class": "L",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 4,
  "capacity": 128,
  "empty_mass": 105.6,
  "allowed_cargo_classes": [
    "raw_resource",
    "processed_resource",
    "tools_equipment",
    "chemical_material",
    "electronics",
    "general_supplies"
  ],
  "special_designs": [
    "cargoverse:fragile",
    "cargoverse:moisture_proof",
    "cargoverse:light_sensitive"
  ],
  "design_defects": [],
  "tags": [
    "series.hri.explorer"
  ]
}
```
