# VBS BioPod 生物物资舱 M 型

> 分类同步说明（2026-10-20）：本页兼容类别已更新为十四类方案。其他型号/投放规划可能保留历史设计，完整运行时定义以项目 JSON 为准；本轮不重平衡容量、质量或制造价格。


[绿洲农业联盟](<../README.md>) → [BioPod 生物物资舱](<README.md>) → M 型

通过固定与御寒设计承运农业物资、食品和药剂物品，不支持活体实体或装有生物的容器。

## 定义

| 项目 | 内容 |
| --- | --- |
| 完整型号 | `VBS-BioPod-SD-M` |
| 资源 ID | `cargoverse:vbs/biopod_sd_m` |
| 定义文件 | [biopod_sd_m.json](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/vbs/biopod_sd_m.json>) |
| 制造商 | 绿洲农业联盟 / Verdant BioSystems（`cargoverse:vbs`） |
| 系列全称 | BioPod 生物物资舱 |
| 尺寸等级 | M |
| 调度点 | 2 |
| 结算单位 | `cargoverse:void_byte` |
| 标签 | `series.vbs.biopod` |

## 结构模板

**正式模板已提供。** 当前引用：`cargoverse:cargo/vbs/biopod/vbs_biopod_sd_m`。结构文件存在，尚未在本轮重新验证游戏内碰撞、接口与实际质量。

[当前 NBT 文件](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/vbs/biopod/vbs_biopod_sd_m.nbt>) · [缺失模板总表](<../../缺失结构模板.md>)

## 数值

| 指标 | 定义基础值 | 实际值 |
| --- | ---: | ---: |
| 容量（个） | 80 | 80 |
| 空柜目标质量（Kpg） | 60 | 60 |

| 容量修正分类 | CargoClass | 倍率 | 实际容量（个） |
| --- | --- | ---: | ---: |
| 食品与食材 | `food` | 1.25 | 100 |

容量、空重、防护与缺陷均由本货柜型号直接定义；未列出的允许分类使用基础容量。指定分类容量在最终乘算后一次向下取整。目标空重仍受结构中非货柜方块质量下限约束。

## CargoClass 兼容

| 分类 | CargoClass |
| --- | --- |
| 农业物资 | `agriculture` |
| 食品与食材 | `food` |
| 化工与药剂 | `chemical_material` |

仅允许上述类别，不支持 none；一柜只装一种精确物品变体。首批物品标签与运输参数已配置；未覆盖物品使用默认运输规则，不代表全部物品已经归类或平衡。

## 防护与运输要求

消除：御寒、勿倒置。对应 `cargoverse:cold_proof`、`cargoverse:keep_upright`。

设计缺陷：无。未被消除的货物运输要求继续生效；所有型号保留 `time_limit`。御寒不代表恒温冷藏，防潮不代表抗腐蚀。

## 制造与投放

| 项目 | v2 实体材料设计 |
| --- | --- |
| 加工费 | 240 VB |
| 实体材料 | 铁锭 ×24、玻璃 ×24、白色羊毛 ×8、铜锭 ×8 |
| 最低许可证 | M |
| 最低繁荣等级 | 1 |
| 材料最少占格 | 4 格，按每种物品 64 堆叠 |
| 当前配方状态 | 配方设计完成，尚未写入运行时制造定义 |

正式提供节点：[V02 云泽水产与育种站](<../../../07_贸易点/resource/云泽水产与育种站/定义设计/01_货柜制造台定义.md>)（固定专业工坊）、[V03 绿洲生物工程站](<../../../07_贸易点/factory/绿洲生物工程站/定义设计/01_货柜制造台定义.md>)（固定专业工坊）。同型号跨站使用同一实体配方、加工费和门槛；玩家背包供料，不扣贸易点库存。普通资产按当前型号占用调度点，基础领取独立处理。

[统一配方与定价依据](<../../../08_货柜制造台/制造配方与投放总表.md>)。数值为首轮设计目标，尚未完成实机平衡。

## 当前 JSON

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/vbs/biopod/vbs_biopod_sd_m",
  "manufacturer": "cargoverse:vbs",
  "display_name": "VBS BioPod 生物物资舱 M 型",
  "description": "§lVBS BioPod 生物物资舱 M 型\n§r§7通过固定与御寒设计承运农业物资、食品和药剂物品，不支持活体实体或装有生物的容器。\n§r§l制造商：绿洲农业联盟 / Verdant BioSystems\n§r§l系列：BioPod 生物物资舱",
  "size_class": "M",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 2,
  "capacity": 80,
  "empty_mass": 60,
  "allowed_cargo_classes": [
    "agriculture",
    "food",
    "chemical_material"
  ],
  "special_designs": [
    "cargoverse:cold_proof",
    "cargoverse:keep_upright"
  ],
  "design_defects": [],
  "tags": [
    "series.vbs.biopod"
  ],
  "cargo_class_capacity_modifiers": {
    "food": 1.25
  }
}
```
