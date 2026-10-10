# HEC Apollo 燃料化工柜 S 型


[赫利俄斯能源集团](<../README.md>) → [Apollo 燃料化工柜](<README.md>) → S 型

面向燃料与工业化学材料供应，使用防火、防潮和固定设计满足能源运输需求。

## 定义

| 项目 | 内容 |
| --- | --- |
| 完整型号 | `HEC-Apollo-SD-S` |
| 资源 ID | `cargoverse:hec/apollo_sd_s` |
| 定义文件 | [apollo_sd_s.json](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/hec/apollo_sd_s.json>) |
| 制造商 | 赫利俄斯能源集团 / Helios Energy Corporation（`cargoverse:hec`） |
| 系列全称 | Apollo 燃料化工柜 |
| 尺寸等级 | S |
| 调度点 | 1 |
| 结算单位 | `cargoverse:void_byte` |
| 标签 | `series.hec.apollo` |

## 结构模板

**正式模板已接入。** 当前引用：`cargoverse:cargo/hec/apollo/hec_apollo_sd_s`。

包络尺寸（X × Y × Z）：**6 × 5 × 5** 方块；体积 150 方块³。

模板中的连接部件：`cargoverse:cargo_docking_port` ×2。已校验压缩 NBT、尺寸、方块位置与调色板索引；游戏内连接、碰撞和实际质量尚未重新实测。

[当前 NBT 文件](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/hec/apollo/hec_apollo_sd_s.nbt>) · [模板接入与缺失清单](<../../缺失结构模板.md>)

## 数值

| 指标 | 定义基础值 | 实际值 |
| --- | ---: | ---: |
| 容量（t） | 50 | 50 |
| 空柜目标质量（Kpg） | 28 | 28 |

未配置 CargoClass 容量修正，所有允许分类均使用基础容量。

容量、空重、防护与缺陷均由本货柜型号直接定义；未列出的允许分类使用基础容量。指定分类容量在最终乘算后一次向下取整。目标空重仍受结构中非货柜方块质量下限约束。

## CargoClass 兼容

| 分类 | CargoClass | 当前 CargoGood 数 |
| --- | --- | --- |
| 能源燃料 | `energy_fuel` | 4 |
| 化工原料 | `chemical_material` | 5 |

仅允许上表分类，`none` 与其他未列出分类均不可装载。同一允许分类下的货物均可选择，但不能混装不同 CargoGood。

## 防护与运输要求

消除：易燃、勿倒置、防潮。对应 `cargoverse:flammable`、`cargoverse:keep_upright`、`cargoverse:moisture_proof`。

设计缺陷：无。未被消除的货物运输要求继续生效；所有型号保留 `time_limit`。御寒不代表恒温冷藏，防潮不代表抗腐蚀。

## 制造与投放

| 项目 | v2 实体材料设计 |
| --- | --- |
| 加工费 | 110 VB |
| 实体材料 | 铁锭 ×16、铜锭 ×8、玻璃 ×4、红石 ×2 |
| 最低许可证 | S |
| 最低繁荣等级 | 0 |
| 材料最少占格 | 4 格，按每种物品 64 堆叠 |
| 当前配方状态 | 配方设计完成，尚未写入运行时制造定义 |

正式提供节点：[E01 赫利俄斯燃料供应站](<../../../07_贸易点/factory/赫利俄斯燃料供应站/定义设计/01_货柜制造台定义.md>)（固定配套制造台）、[E02 工业化学品供应站](<../../../07_贸易点/factory/工业化学品供应站/定义设计/01_货柜制造台定义.md>)（固定专业工坊）、[V03 绿洲生物工程站](<../../../07_贸易点/factory/绿洲生物工程站/定义设计/01_货柜制造台定义.md>)（固定专业工坊）。同型号跨站使用同一实体配方、加工费和门槛；玩家背包供料，不扣贸易点库存。普通资产按当前型号占用调度点，基础领取独立处理。

[统一配方与定价依据](<../../../08_货柜制造台/制造配方与投放总表.md>)。数值为首轮设计目标，尚未完成实机平衡。

## 当前 JSON

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/hec/apollo/hec_apollo_sd_s",
  "manufacturer": "cargoverse:hec",
  "display_name": "HEC Apollo 燃料化工柜 S 型",
  "description": "§lHEC Apollo 燃料化工柜 S 型\n§r§7面向燃料与工业化学材料供应，使用防火、防潮和固定设计满足能源运输需求。\n§r§l制造商：赫利俄斯能源集团 / Helios Energy Corporation\n§r§l系列：Apollo 燃料化工柜",
  "size_class": "S",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 1,
  "capacity": 50,
  "empty_mass": 28,
  "allowed_cargo_classes": [
    "energy_fuel",
    "chemical_material"
  ],
  "special_designs": [
    "cargoverse:flammable",
    "cargoverse:keep_upright",
    "cargoverse:moisture_proof"
  ],
  "design_defects": [],
  "tags": [
    "series.hec.apollo"
  ]
}
```

## 基础运输权益

本型号同时作为赫利俄斯能源集团的[初始基础货柜](<../../../05_基础货柜/hec_basic.md>)。注册终端领取的基础资产占 **0 调度点**；普通购买／制造的同型号仍占 1 点。型号 JSON 中的 `dispatch_points` 保持普通版本成本，豁免依据资产标记。
