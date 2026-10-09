# SPL Courier 轻型配送柜 S 型


[云港物流集团](<../README.md>) → [Courier 轻型配送柜](<README.md>) → S 型

为偏远聚落配送和独立运输者设计的轻型货柜，空重较低，适合小批物资周转。

## 定义

| 项目 | 内容 |
| --- | --- |
| 完整型号 | `SPL-Courier-MC-S` |
| 资源 ID | `cargoverse:spl/courier_mc_s` |
| 定义文件 | [courier_mc_s.json](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/spl/courier_mc_s.json>) |
| 制造商 | 云港物流集团 / Skyport Logistics（`cargoverse:spl`） |
| 系列全称 | Courier 轻型配送柜 |
| 尺寸等级 | S |
| 调度点 | 1 |
| 结算单位 | `cargoverse:void_byte` |
| 标签 | `series.spl.courier` |

## 结构模板

**正式模板已提供。** 当前引用：`cargoverse:cargo/spl/courier/spl_courier_mc_s`。结构文件存在，尚未在本轮重新验证游戏内碰撞、接口与实际质量。

[当前 NBT 文件](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/spl/courier/spl_courier_mc_s.nbt>) · [缺失模板总表](<../../缺失结构模板.md>)

## 数值

| 指标 | 定义基础值 | 实际值 |
| --- | ---: | ---: |
| 容量（t） | 50 | 50 |
| 空柜目标质量（Kpg） | 16 | 16 |

未配置 CargoClass 容量修正，所有允许分类均使用基础容量。

容量倍率属于本货柜型号；未列出的允许分类使用基础容量。空重仍应用制造商倍率。指定分类容量在最终乘算后一次向下取整。目标空重仍受结构中非货柜方块质量下限约束。

## CargoClass 兼容

| 分类 | CargoClass | 当前 CargoGood 数 |
| --- | --- | --- |
| 农业产品 | `agriculture` | 5 |
| 水产生鲜 | `aquatic` | 4 |
| 日常通用补给 | `general_supplies` | 4 |
| 医疗物资 | `medical_supply` | 4 |
| 电子设备 | `electronics` | 6 |
| 工具器械 | `tools_equipment` | 4 |
| 贵重物品 | `valuables` | 4 |

仅允许上表分类，`none` 与其他未列出分类均不可装载。同一允许分类下的货物均可选择，但不能混装不同 CargoGood。

## 防护与运输要求

消除：无。

设计缺陷：无。未被消除的货物运输要求继续生效；所有型号保留 `time_limit`。御寒不代表恒温冷藏，防潮不代表抗腐蚀。

## 制造与投放

| 项目 | v2 实体材料设计 |
| --- | --- |
| 加工费 | 60 VB |
| 实体材料 | 铁锭 ×8、橡木木板 ×8、白色羊毛 ×4、红石 ×2 |
| 最低许可证 | S |
| 最低繁荣等级 | 0 |
| 材料最少占格 | 4 格，按每种物品 64 堆叠 |
| 当前配方状态 | 配方设计完成，尚未写入运行时制造定义 |

正式提供节点：[B03 边境驻防补给港](<../../../07_贸易点/market/边境驻防补给港/定义设计/01_货柜制造台定义.md>)（固定配套制造台）、[S01 云港民生集配站](<../../../07_贸易点/market/云港民生集配站/定义设计/01_货柜制造台定义.md>)（固定配套制造台）、[S02 远航货运枢纽](<../../../07_贸易点/market/远航货运枢纽/定义设计/01_货柜制造台定义.md>)（固定专业工坊）、[S03 天空城综合市场](<../../../07_贸易点/market/天空城综合市场/定义设计/01_货柜制造台定义.md>)（固定配套制造台）。同型号跨站使用同一实体配方、加工费和门槛；玩家背包供料，不扣贸易点库存。普通资产按当前型号占用调度点，基础领取独立处理。

[统一配方与定价依据](<../../../08_货柜制造台/制造配方与投放总表.md>)。数值为首轮设计目标，尚未完成实机平衡。

## 当前 JSON

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/spl/courier/spl_courier_mc_s",
  "manufacturer": "cargoverse:spl",
  "display_name": "SPL Courier 轻型配送柜 S 型",
  "description": "§lSPL Courier 轻型配送柜 S 型\n§r§7为偏远聚落配送和独立运输者设计的轻型货柜，空重较低，适合小批物资周转。\n§r§l制造商：云港物流集团 / Skyport Logistics\n§r§l系列：Courier 轻型配送柜",
  "size_class": "S",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 1,
  "capacity": 50,
  "empty_mass": 16,
  "allowed_cargo_classes": [
    "agriculture",
    "aquatic",
    "general_supplies",
    "medical_supply",
    "electronics",
    "tools_equipment",
    "valuables"
  ],
  "special_designs": [],
  "design_defects": [],
  "tags": [
    "series.spl.courier"
  ]
}
```

## 基础运输权益

本型号同时作为云港物流集团的[初始基础货柜](<../../../05_基础货柜/spl_basic.md>)。注册终端领取的基础资产占 **0 调度点**；普通购买／制造的同型号仍占 1 点。型号 JSON 中的 `dispatch_points` 保持普通版本成本，豁免依据资产标记。
