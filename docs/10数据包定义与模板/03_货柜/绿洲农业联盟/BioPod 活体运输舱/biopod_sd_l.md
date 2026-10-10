# VBS BioPod 活体运输舱 L 型


[绿洲农业联盟](<../README.md>) → [BioPod 活体运输舱](<README.md>) → L 型

通过固定与御寒设计承运活体、水产和生物相关货物，适合繁育场及生态设施补给。

## 定义

| 项目 | 内容 |
| --- | --- |
| 完整型号 | `VBS-BioPod-SD-L` |
| 资源 ID | `cargoverse:vbs/biopod_sd_l` |
| 定义文件 | [biopod_sd_l.json](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/vbs/biopod_sd_l.json>) |
| 制造商 | 绿洲农业联盟 / Verdant BioSystems（`cargoverse:vbs`） |
| 系列全称 | BioPod 活体运输舱 |
| 尺寸等级 | L |
| 调度点 | 4 |
| 结算单位 | `cargoverse:void_byte` |
| 标签 | `series.vbs.biopod` |

## 结构模板

**正式模板已接入。** 当前引用：`cargoverse:cargo/vbs/biopod/vbs_biopod_sd_l`。

包络尺寸（X × Y × Z）：**11 × 6 × 7** 方块；体积 462 方块³。

模板中的连接部件：`cargoverse:cargo_docking_port` ×6。已校验压缩 NBT、尺寸、方块位置与调色板索引；游戏内连接、碰撞和实际质量尚未重新实测。

[当前 NBT 文件](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/vbs/biopod/vbs_biopod_sd_l.nbt>) · [模板接入与缺失清单](<../../缺失结构模板.md>)

## 数值

| 指标 | 定义基础值 | 实际值 |
| --- | ---: | ---: |
| 容量（t） | 160 | 160 |
| 空柜目标质量（Kpg） | 120 | 120 |

| 容量修正分类 | CargoClass | 倍率 | 实际容量（t） |
| --- | --- | ---: | ---: |
| 活体与育种 | `livestock` | 1.25 | 200 |

容量、空重、防护与缺陷均由本货柜型号直接定义；未列出的允许分类使用基础容量。指定分类容量在最终乘算后一次向下取整。目标空重仍受结构中非货柜方块质量下限约束。

## CargoClass 兼容

| 分类 | CargoClass | 当前 CargoGood 数 |
| --- | --- | --- |
| 活体生物 | `livestock` | 4 |
| 水产生鲜 | `aquatic` | 4 |
| 科研样本 | `research_sample` | 4 |
| 医疗物资 | `medical_supply` | 4 |

仅允许上表分类，`none` 与其他未列出分类均不可装载。同一允许分类下的货物均可选择，但不能混装不同 CargoGood。

## 防护与运输要求

消除：御寒、勿倒置。对应 `cargoverse:cold_proof`、`cargoverse:keep_upright`。

设计缺陷：无。未被消除的货物运输要求继续生效；所有型号保留 `time_limit`。御寒不代表恒温冷藏，防潮不代表抗腐蚀。

## 制造与投放

| 项目 | v2 实体材料设计 |
| --- | --- |
| 加工费 | 480 VB |
| 实体材料 | 铁锭 ×48、玻璃 ×48、白色羊毛 ×16、铜锭 ×16 |
| 最低许可证 | L |
| 最低繁荣等级 | 2 |
| 材料最少占格 | 4 格，按每种物品 64 堆叠 |
| 当前配方状态 | 配方设计完成，尚未写入运行时制造定义 |

正式提供节点：[V02 云泽水产与育种站](<../../../07_贸易点/resource/云泽水产与育种站/定义设计/01_货柜制造台定义.md>)（固定专业工坊）。同型号跨站使用同一实体配方、加工费和门槛；玩家背包供料，不扣贸易点库存。普通资产按当前型号占用调度点，基础领取独立处理。

[统一配方与定价依据](<../../../08_货柜制造台/制造配方与投放总表.md>)。数值为首轮设计目标，尚未完成实机平衡。

## 当前 JSON

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/vbs/biopod/vbs_biopod_sd_l",
  "manufacturer": "cargoverse:vbs",
  "display_name": "VBS BioPod 活体运输舱 L 型",
  "description": "§lVBS BioPod 活体运输舱 L 型\n§r§7通过固定与御寒设计承运活体、水产和生物相关货物，适合繁育场及生态设施补给。\n§r§l制造商：绿洲农业联盟 / Verdant BioSystems\n§r§l系列：BioPod 活体运输舱",
  "size_class": "L",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 4,
  "capacity": 160,
  "empty_mass": 120,
  "allowed_cargo_classes": [
    "livestock",
    "aquatic",
    "research_sample",
    "medical_supply"
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
    "livestock": 1.25
  }
}
```
