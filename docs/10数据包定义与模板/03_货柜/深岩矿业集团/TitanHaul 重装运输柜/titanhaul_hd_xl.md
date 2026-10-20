# DMC TitanHaul 重装运输柜 XL 型

> 分类同步说明（2026-10-20）：本页兼容类别已更新为十四类方案。其他型号/投放规划可能保留历史设计，完整运行时定义以项目 JSON 为准；本轮不重平衡容量、质量或制造价格。


[深岩矿业集团](<../README.md>) → [TitanHaul 重装运输柜](<README.md>) → XL 型

面向采矿设备、重型载具及重建材的大宗运输，以厚重结构换取高容量与稳定承载。

## 定义

| 项目 | 内容 |
| --- | --- |
| 完整型号 | `DMC-TitanHaul-HD-XL` |
| 资源 ID | `cargoverse:dmc/titanhaul_hd_xl` |
| 定义文件 | [titanhaul_hd_xl.json](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/dmc/titanhaul_hd_xl.json>) |
| 制造商 | 深岩矿业集团 / Deepcore Mining Corporation（`cargoverse:dmc`） |
| 系列全称 | TitanHaul 重装运输柜 |
| 尺寸等级 | XL |
| 调度点 | 8 |
| 结算单位 | `cargoverse:void_byte` |
| 标签 | `series.dmc.titanhaul` |

## 结构模板

**正式模板已提供。** 当前引用：`cargoverse:cargo/dmc/titanhaul/dmc_titanhaul_hd_xl`。结构文件存在，尚未在本轮重新验证游戏内碰撞、接口与实际质量。

[当前 NBT 文件](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/dmc/titanhaul/dmc_titanhaul_hd_xl.nbt>) · [缺失模板总表](<../../缺失结构模板.md>)

## 数值

| 指标 | 定义基础值 | 实际值 |
| --- | ---: | ---: |
| 容量（个） | 780 | 780 |
| 空柜目标质量（Kpg） | 421.2 | 421.2 |

| 容量修正分类 | CargoClass | 倍率 | 实际容量（个） |
| --- | --- | ---: | ---: |
| 原始资源 | `raw_resource` | 1.3 | 1014 |

容量、空重、防护与缺陷均由本货柜型号直接定义；未列出的允许分类使用基础容量。指定分类容量在最终乘算后一次向下取整。目标空重仍受结构中非货柜方块质量下限约束。

## CargoClass 兼容

| 分类 | CargoClass |
| --- | --- |
| 原料资源 | `raw_resource` |
| 机械设备 | `machinery` |
| 载具与部件 | `vehicle` |
| 建筑构件 | `construction_material` |
| 物流与仓储 | `logistics_equipment` |

仅允许上述类别，不支持 none；一柜只装一种精确物品变体。首批物品标签与运输参数已配置；未覆盖物品使用默认运输规则，不代表全部物品已经归类或平衡。

## 防护与运输要求

消除：无。

设计缺陷：无。未被消除的货物运输要求继续生效；所有型号保留 `time_limit`。御寒不代表恒温冷藏，防潮不代表抗腐蚀。

## 制造与投放

| 项目 | v2 实体材料设计 |
| --- | --- |
| 加工费 | 1680 VB |
| 实体材料 | 铁锭 ×336、铜锭 ×96、锁链 ×48、活塞 ×12 |
| 最低许可证 | XL |
| 最低繁荣等级 | 4 |
| 材料最少占格 | 10 格，按每种物品 64 堆叠 |
| 当前配方状态 | 配方设计完成，尚未写入运行时制造定义 |

正式提供节点：[D03 重工材料与矿机厂](<../../../07_贸易点/factory/重工材料与矿机厂/定义设计/01_货柜制造台定义.md>)（固定专业工坊）。同型号跨站使用同一实体配方、加工费和门槛；玩家背包供料，不扣贸易点库存。普通资产按当前型号占用调度点，基础领取独立处理。

[统一配方与定价依据](<../../../08_货柜制造台/制造配方与投放总表.md>)。数值为首轮设计目标，尚未完成实机平衡。

## 当前 JSON

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/dmc/titanhaul/dmc_titanhaul_hd_xl",
  "manufacturer": "cargoverse:dmc",
  "display_name": "DMC TitanHaul 重装运输柜 XL 型",
  "description": "§lDMC TitanHaul 重装运输柜 XL 型\n§r§7面向采矿设备、重型载具及重建材的大宗运输，以厚重结构换取高容量与稳定承载。\n§r§l制造商：深岩矿业集团 / Deepcore Mining Corporation\n§r§l系列：TitanHaul 重装运输柜",
  "size_class": "XL",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 8,
  "capacity": 780,
  "empty_mass": 421.2,
  "allowed_cargo_classes": [
    "raw_resource",
    "machinery",
    "vehicle",
    "construction_material",
    "logistics_equipment"
  ],
  "special_designs": [],
  "design_defects": [],
  "tags": [
    "series.dmc.titanhaul"
  ],
  "cargo_class_capacity_modifiers": {
    "raw_resource": 1.3
  }
}
```
