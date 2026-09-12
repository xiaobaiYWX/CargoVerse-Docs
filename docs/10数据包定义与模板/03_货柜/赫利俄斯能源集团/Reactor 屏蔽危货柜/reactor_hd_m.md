# HEC Reactor 屏蔽危货柜 M 型

[赫利俄斯能源集团](<../README.md>) → [Reactor 屏蔽危货柜](<README.md>) → M 型

以屏蔽与固定结构承运退役放射源等危险货物，较低容量换取高耐久与放射性防护。

## 定义

| 项目 | 内容 |
| --- | --- |
| 完整型号 | `HEC-Reactor-HD-M` |
| 资源 ID | `cargoverse:hec/reactor_hd_m` |
| 定义文件 | [reactor_hd_m.json](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/hec/reactor_hd_m.json>) |
| 制造商 | 赫利俄斯能源集团 / Helios Energy Corporation（`cargoverse:hec`） |
| 系列全称 | Reactor 屏蔽危货柜 |
| 尺寸等级 | M |
| 调度点 | 2 |
| 结算单位 | `cargoverse:void_byte` |
| 标签 | `series.hec.reactor` |

## 结构模板

**正式模板已接入。** 当前引用：`cargoverse:cargo/hec/reactor/hec_reactor_hd_m`。

包络尺寸（X × Y × Z）：**10 × 6 × 5** 方块；体积 300 方块³。

模板中的连接部件：`cargoverse:heavy_connection_point` ×4。已校验压缩 NBT、尺寸、方块位置与调色板索引；游戏内连接、碰撞和实际质量尚未重新实测。

[当前 NBT 文件](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/hec/reactor/hec_reactor_hd_m.nbt>) · [模板接入与缺失清单](<../../缺失结构模板.md>)

## 数值

| 指标 | 定义基础值 | 默认实际值（含厂商通用倍率） |
| --- | --- | --- |
| 容量（t） | 12 | 12 |
| 空柜目标质量（Kpg） | 60 | 60 |
| 最大耐久 | 190 | 190 |

本厂商当前无额外数值修正。 指定货物容量按所有适用倍率相乘后一次向下取整，不能先取整默认容量再乘专项倍率。目标空重仍受结构中非货柜方块质量下限约束。

## CargoClass 兼容

| 分类 | CargoClass | 当前 CargoGood 数 |
| --- | --- | --- |
| 环境危害材料 | `hazardous_material` | 4 |

仅允许上表分类，`none` 与其他未列出分类均不可装载。同一允许分类下的货物均可选择，但不能混装不同 CargoGood。

## 防护与运输要求

消除：放射性、勿倒置。对应 `cargoverse:radioactive`、`cargoverse:keep_upright`。

设计缺陷：无。未被消除的货物运输要求继续生效；所有型号保留 `time_limit`。御寒不代表恒温冷藏，防潮不代表抗腐蚀。

## 制造与投放

| 项目 | 值 |
| --- | --- |
| 规划加工费 | 400 VB（不含库存材料） |
| 最低许可证 | M |
| 最低繁荣等级 | 2 |
| 规划节点类型 | 危险物接收站、退役源处置站 |
| 当前配方状态 | 待编制材料配方、绑定制造台与供应节点 |

货柜定义已注册，可供系统引用；规划加工费与门槛尚未写入制造配方，不代表现有制造台可购买该型号。

## 当前 JSON

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/hec/reactor/hec_reactor_hd_m",
  "manufacturer": "cargoverse:hec",
  "display_name": "HEC Reactor 屏蔽危货柜 M 型",
  "description": "§lHEC Reactor 屏蔽危货柜 M 型\n§r§7以屏蔽与固定结构承运退役放射源等危险货物，较低容量换取高耐久与放射性防护。\n§r§l制造商：赫利俄斯能源集团 / Helios Energy Corporation\n§r§l系列：Reactor 屏蔽危货柜",
  "size_class": "M",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 2,
  "capacity": 12,
  "empty_mass": 60,
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
