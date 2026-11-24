# 矿物分选精炼站 · 实际物品贸易表

> 已接入内置数据包。以新建贸易点实例验收。

编号：**D02**。归属：**深岩矿业集团（DMC）**。形态：**天空大站**。

资源 ID：`cargoverse:factory/sky_station/mineral_refinery`。

对应数据路径：`data/cargoverse/trade_points/resource_tables/factory/sky_station/mineral_refinery.json`。

## 业务定位

**金属冶炼与基础合金供应。** 主要收购粗铁、粗铜、粗锌及燃料，出售铁铜锌锭、黄铜锭和安山合金。矿物与锭的报价是独立区域供需，不承诺站内真实生产，也不规定玩家必须从矿站取得原料。

## 报价口径

- 使用现行 `schema_version: 3`；价格为本站 `unit_price`，单位为 **VB／份**。库存、补货、限额及许可证经验均按份配置，物品每组为一份，活体每只为一份。
- 全部条目使用精确物品 ID，省略 `components`，只匹配默认完整状态；工具为全新默认状态，设备无嵌套库存。不接受标签通配或任意耐久、附魔、命名变体。
- 以下为基准报价。成交会应用行情与签约修正。许可证经验由当地收购条目按份配置。
- 所有出售条目都有有限 `stock`。收购列的 `0（不限）` 对应 `daily_limit: 0`；其余数值为同一站点实例所有玩家共享的每贸易日额度。
- 许可证经验按向自然生成目的地实际交付的份数和当地收购配置结算，适用于任意货源。繁荣度与制造商交付声望由独立物资供应结算。

## 出售目录

| rule_id | 物品 | 单价 VB | 初始库存 | 库存容量 | 每日补货 | 最低繁荣度 |
| --- | --- | ---: | ---: | ---: | ---: | ---: |
| `sell_minecraft_iron_ingot` | 铁锭 · `minecraft:iron_ingot` | 12 | 1024 | 3072 | 512 | 0 |
| `sell_minecraft_copper_ingot` | 铜锭 · `minecraft:copper_ingot` | 8 | 1024 | 3072 | 512 | 0 |
| `sell_create_zinc_ingot` | 锌锭 · `create:zinc_ingot` | 12 | 768 | 2048 | 512 | 0 |
| `sell_create_brass_ingot` | 黄铜锭 · `create:brass_ingot` | 22 | 256 | 768 | 192 | 3 |
| `sell_create_andesite_alloy` | 安山合金 · `create:andesite_alloy` | 13 | 768 | 2048 | 512 | 1 |

## 收购目录

| rule_id | 物品 | 单价 VB | 每日限额 | 许可证经验／份 | 最低繁荣度 |
| --- | --- | ---: | ---: | ---: | ---: |
| `buy_minecraft_raw_iron` | 粗铁 · `minecraft:raw_iron` | 10 | 0（不限） | 2 | 1 |
| `buy_minecraft_raw_copper` | 粗铜 · `minecraft:raw_copper` | 6 | 0（不限） | 1 | 0 |
| `buy_create_raw_zinc` | 粗锌 · `create:raw_zinc` | 9 | 0（不限） | 2 | 0 |
| `buy_minecraft_coal` | 煤炭 · `minecraft:coal` | 9 | 0（不限） | 2 | 0 |
| `buy_minecraft_sand` | 沙子 · `minecraft:sand` | 4 | 512 | 1 | 0 |
| `buy_create_shaft` | 传动杆 · `create:shaft` | 12 | 128 | 3 | 2 |
| `buy_create_mechanical_press` | 动力冲压机 · `create:mechanical_press` | 215 | 16 | 6 | 4 |
| `buy_minecraft_bread` | 面包 · `minecraft:bread` | 6 | 256 | 2 | 0 |
| `buy_create_blaze_cake` | 烈焰蛋糕 · `create:blaze_cake` | 125 | 64 | 5 | 3 |

## 运输与落地依赖

货柜兼容按当前 solid／liquid／living 交付形态及保护需求判断；本站用途描述不产生额外分类。运输属性以[正式逐物品清单](<../../../../01运输物品/固体/README.md>)为准，不在每个报价设计中复制分类快照。

装柜前仍需按实际物品配置选择货柜与保护设计；本页不修改质量、固定组数损耗、冷链或易碎判定。不同货物未必能共用一个返程货柜。

报价目录在实例创建时保存快照。以新建经济实例验收；普通 reload 保留旧实例的报价快照。

[本站贸易网络](<../../../站点/factory/矿物分选精炼站/定义设计/02_贸易网络设计.md>) · [总体设计](<../../../站点/设计总览.md>) · [现行格式与经验资格](<../../../../../04数据规范/贸易点/03_资源表定义.md>)
