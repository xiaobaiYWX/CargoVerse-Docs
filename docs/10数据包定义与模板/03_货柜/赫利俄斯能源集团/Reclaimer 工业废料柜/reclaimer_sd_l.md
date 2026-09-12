# HEC Reclaimer 工业废料柜 L 型

[赫利俄斯能源集团](<../README.md>) → [Reclaimer 工业废料柜](<README.md>) → L 型

承运工业回收料与低单价大宗废物，提供固定设计及经济的大容量周转方案。

## 定义

| 项目 | 内容 |
| --- | --- |
| 完整型号 | `HEC-Reclaimer-SD-L` |
| 资源 ID | `cargoverse:hec/reclaimer_sd_l` |
| 定义文件 | [reclaimer_sd_l.json](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/hec/reclaimer_sd_l.json>) |
| 制造商 | 赫利俄斯能源集团 / Helios Energy Corporation（`cargoverse:hec`） |
| 系列全称 | Reclaimer 工业废料柜 |
| 尺寸等级 | L |
| 调度点 | 4 |
| 结算单位 | `cargoverse:void_byte` |
| 标签 | `series.hec.reclaimer` |

## 结构模板

**正式模板已接入。** 当前引用：`cargoverse:cargo/hec/reclaimer/hec_reclaimer_sd_l`。

包络尺寸（X × Y × Z）：**13 × 7 × 7** 方块；体积 637 方块³。

模板中的连接部件：`cargoverse:cargo_docking_port` ×6。已校验压缩 NBT、尺寸、方块位置与调色板索引；游戏内连接、碰撞和实际质量尚未重新实测。

[当前 NBT 文件](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/hec/reclaimer/hec_reclaimer_sd_l.nbt>) · [模板接入与缺失清单](<../../缺失结构模板.md>)

## 数值

| 指标 | 定义基础值 | 默认实际值（含厂商通用倍率） |
| --- | --- | --- |
| 容量（t） | 48 | 48 |
| 空柜目标质量（Kpg） | 128 | 128 |
| 最大耐久 | 130 | 130 |

本厂商当前无额外数值修正。 指定货物容量按所有适用倍率相乘后一次向下取整，不能先取整默认容量再乘专项倍率。目标空重仍受结构中非货柜方块质量下限约束。

## CargoClass 兼容

| 分类 | CargoClass | 当前 CargoGood 数 |
| --- | --- | --- |
| 环境危害材料 | `hazardous_material` | 4 |

仅允许上表分类，`none` 与其他未列出分类均不可装载。同一允许分类下的货物均可选择，但不能混装不同 CargoGood。

## 防护与运输要求

消除：勿倒置。对应 `cargoverse:keep_upright`。

设计缺陷：无。未被消除的货物运输要求继续生效；所有型号保留 `time_limit`。御寒不代表恒温冷藏，防潮不代表抗腐蚀。

## 制造与投放

| 项目 | 值 |
| --- | --- |
| 规划加工费 | 360 VB（不含库存材料） |
| 最低许可证 | L |
| 最低繁荣等级 | 3 |
| 规划节点类型 | 工业废物回收站、净化厂 |
| 当前配方状态 | 待编制材料配方、绑定制造台与供应节点 |

货柜定义已注册，可供系统引用；规划加工费与门槛尚未写入制造配方，不代表现有制造台可购买该型号。

## 当前 JSON

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/hec/reclaimer/hec_reclaimer_sd_l",
  "manufacturer": "cargoverse:hec",
  "display_name": "HEC Reclaimer 工业废料柜 L 型",
  "description": "§lHEC Reclaimer 工业废料柜 L 型\n§r§7承运工业回收料与低单价大宗废物，提供固定设计及经济的大容量周转方案。\n§r§l制造商：赫利俄斯能源集团 / Helios Energy Corporation\n§r§l系列：Reclaimer 工业废料柜",
  "size_class": "L",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 4,
  "capacity": 48,
  "empty_mass": 128,
  "max_durability": 130,
  "allowed_cargo_classes": [
    "hazardous_material"
  ],
  "special_designs": [
    "cargoverse:keep_upright"
  ],
  "design_defects": [],
  "tags": [
    "series.hec.reclaimer"
  ]
}
```
