# 重工材料与矿机厂 · 实际物品贸易表

> 已接入内置数据包。以新建贸易点实例验收。

编号：**D03**。归属：**深岩矿业集团（DMC）**。形态：**天空大站**。

资源 ID：`cargoverse:factory/sky_station/heavy_works`。

对应数据路径：`data/cargoverse/trade_points/resource_tables/factory/sky_station/heavy_works.json`。

## 业务定位

**金属板材与矿业重机供应。** 将普通压片材料、坚固板和重型矿机组合，服务航空、防务和采矿站。高价设备小批补货；金属原料与矿物压板材料为较大宗需求，避免用同一库存规模覆盖板材和整机。

## 报价口径

- 使用现行 `schema_version: 3`；价格为本站 `unit_price`，单位为 **VB／份**。库存、补货、限额及许可证经验均按份配置，物品每组为一份，活体每只为一份。
- 全部条目使用精确物品 ID，省略 `components`，只匹配默认完整状态；工具为全新默认状态，设备无嵌套库存。不接受标签通配或任意耐久、附魔、命名变体。
- 以下为基准报价。成交会应用行情与签约修正。许可证经验由当地收购条目按份配置。
- 所有出售条目都有有限 `stock`。收购列的 `0（不限）` 对应 `daily_limit: 0`；其余数值为同一站点实例所有玩家共享的每贸易日额度。
- 许可证经验按向自然生成目的地实际交付的份数和当地收购配置结算，适用于任意货源。繁荣度与制造商交付声望由独立物资供应结算。

## 出售目录

| rule_id | 物品 | 单价 VB | 初始库存 | 库存容量 | 每日补货 | 最低繁荣度 |
| --- | --- | ---: | ---: | ---: | ---: | ---: |
| `sell_create_iron_sheet` | 铁板 · `create:iron_sheet` | 16 | 256 | 768 | 192 | 0 |
| `sell_create_brass_sheet` | 黄铜板 · `create:brass_sheet` | 28 | 256 | 768 | 192 | 0 |
| `sell_create_sturdy_sheet` | 坚固板 · `create:sturdy_sheet` | 70 | 24 | 64 | 12 | 0 |
| `sell_create_mechanical_drill` | 动力钻头 · `create:mechanical_drill` | 190 | 24 | 64 | 12 | 2 |
| `sell_create_crushing_wheel` | 粉碎轮 · `create:crushing_wheel` | 220 | 24 | 64 | 12 | 4 |
| `sell_create_rope_pulley` | 绳索滑轮 · `create:rope_pulley` | 140 | 24 | 64 | 12 | 1 |

## 收购目录

| rule_id | 物品 | 单价 VB | 每日限额 | 许可证经验／份 | 最低繁荣度 |
| --- | --- | ---: | ---: | ---: | ---: |
| `buy_minecraft_iron_ingot` | 铁锭 · `minecraft:iron_ingot` | 15 | 0（不限） | 3 | 0 |
| `buy_create_brass_ingot` | 黄铜锭 · `create:brass_ingot` | 26 | 256 | 3 | 3 |
| `buy_minecraft_obsidian` | 黑曜石 · `minecraft:obsidian` | 16 | 256 | 3 | 1 |
| `buy_create_andesite_alloy` | 安山合金 · `create:andesite_alloy` | 16 | 256 | 3 | 2 |
| `buy_create_precision_mechanism` | 精密构件 · `create:precision_mechanism` | 190 | 64 | 5 | 4 |
| `buy_minecraft_bread` | 面包 · `minecraft:bread` | 6 | 256 | 2 | 0 |
| `buy_minecraft_coal` | 煤炭 · `minecraft:coal` | 9 | 512 | 2 | 0 |
| `buy_minecraft_cobblestone` | 圆石 · `minecraft:cobblestone` | 2 | 512 | 1 | 0 |

## 运输与落地依赖

货柜兼容按当前 solid／liquid／living 交付形态及保护需求判断；本站用途描述不产生额外分类。运输属性以[正式逐物品清单](<../../../../01运输物品/固体/README.md>)为准，不在每个报价设计中复制分类快照。

装柜前仍需按实际物品配置选择货柜与保护设计；本页不修改质量、固定组数损耗、冷链或易碎判定。不同货物未必能共用一个返程货柜。

报价目录在实例创建时保存快照。以新建经济实例验收；普通 reload 保留旧实例的报价快照。

[本站贸易网络](<../../../站点/factory/重工材料与矿机厂/定义设计/02_贸易网络设计.md>) · [总体设计](<../../../站点/设计总览.md>) · [现行格式与经验资格](<../../../../../04数据规范/贸易点/03_资源表定义.md>)
