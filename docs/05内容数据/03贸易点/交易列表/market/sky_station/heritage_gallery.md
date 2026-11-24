# 旧世珍品商馆 · 实际物品贸易表

> 已接入内置数据包。以新建贸易点实例验收。

编号：**R02**。归属：**遗民贸易协会（REX）**。形态：**天空大站**。

资源 ID：`cargoverse:market/sky_station/heritage_gallery`。

对应数据路径：`data/cargoverse/trade_points/resource_tables/market/sky_station/heritage_gallery.json`。

## 业务定位

**装饰交易与有限遗物鉴藏。** 以画、花盆、物品展示框构成常规装饰商品，仅把唱片作为一次性小批货源。稀有样本与收藏品限量收购；玩家探索取得的同类物品可以出售，但不会由此获得自然站运输经验。

## 报价口径

- 使用现行 `schema_version: 3`；价格为本站 `unit_price`，单位为 **VB／份**。库存、补货、限额及许可证经验均按份配置，物品每组为一份，活体每只为一份。
- 全部条目使用精确物品 ID，省略 `components`，只匹配默认完整状态；工具为全新默认状态，设备无嵌套库存。不接受标签通配或任意耐久、附魔、命名变体。
- 以下为基准报价。成交会应用行情与签约修正。许可证经验由当地收购条目按份配置。
- 所有出售条目都有有限 `stock`。收购列的 `0（不限）` 对应 `daily_limit: 0`；其余数值为同一站点实例所有玩家共享的每贸易日额度。
- 许可证经验按向自然生成目的地实际交付的份数和当地收购配置结算，适用于任意货源。繁荣度与制造商交付声望由独立物资供应结算。

## 出售目录

| rule_id | 物品 | 单价 VB | 初始库存 | 库存容量 | 每日补货 | 最低繁荣度 |
| --- | --- | ---: | ---: | ---: | ---: | ---: |
| `sell_minecraft_painting` | 画 · `minecraft:painting` | 45 | 24 | 64 | 12 | 0 |
| `sell_minecraft_flower_pot` | 花盆 · `minecraft:flower_pot` | 12 | 256 | 768 | 192 | 0 |
| `sell_minecraft_item_frame` | 物品展示框 · `minecraft:item_frame` | 25 | 256 | 768 | 192 | 0 |
| `sell_minecraft_music_disc_13` | 音乐唱片 · `minecraft:music_disc_13` | 300 | 1 | 1 | 0 | 3 |
| `sell_create_cuckoo_clock` | 布谷鸟闹钟 · `create:cuckoo_clock` | 110 | 24 | 64 | 12 | 1 |

## 收购目录

| rule_id | 物品 | 单价 VB | 每日限额 | 许可证经验／份 | 最低繁荣度 |
| --- | --- | ---: | ---: | ---: | ---: |
| `buy_minecraft_amethyst_shard` | 紫水晶碎片 · `minecraft:amethyst_shard` | 15 | 128 | 3 | 0 |
| `buy_minecraft_prismarine_crystals` | 海晶砂粒 · `minecraft:prismarine_crystals` | 26 | 64 | 4 | 3 |
| `buy_minecraft_nautilus_shell` | 鹦鹉螺壳 · `minecraft:nautilus_shell` | 140 | 8 | 6 | 4 |
| `buy_minecraft_echo_shard` | 回响碎片 · `minecraft:echo_shard` | 280 | 4 | 8 | 5 |
| `buy_minecraft_book` | 书 · `minecraft:book` | 20 | 64 | 3 | 1 |
| `buy_create_builders_tea` | 建筑工茶饮 · `create:builders_tea` | 18 | 64 | 3 | 0 |
| `buy_minecraft_bread` | 面包 · `minecraft:bread` | 6 | 128 | 2 | 0 |
| `buy_minecraft_paper` | 纸 · `minecraft:paper` | 6 | 128 | 2 | 0 |
| `buy_create_honeyed_apple` | 蜜渍苹果 · `create:honeyed_apple` | 18 | 64 | 3 | 0 |
| `buy_create_sweet_roll` | 甜甜卷 · `create:sweet_roll` | 20 | 64 | 3 | 2 |

## 运输与落地依赖

货柜兼容按当前 solid／liquid／living 交付形态及保护需求判断；本站用途描述不产生额外分类。运输属性以[正式逐物品清单](<../../../../01运输物品/固体/README.md>)为准，不在每个报价设计中复制分类快照。

装柜前仍需按实际物品配置选择货柜与保护设计；本页不修改质量、固定组数损耗、冷链或易碎判定。不同货物未必能共用一个返程货柜。


每日补货为 0 的条目是实例一次性批次，售空后不自动恢复；其他业务不因此停止。

报价目录在实例创建时保存快照。以新建经济实例验收；普通 reload 保留旧实例的报价快照。

[本站贸易网络](<../../../站点/market/旧世珍品商馆/定义设计/02_贸易网络设计.md>) · [总体设计](<../../../站点/设计总览.md>) · [现行格式与经验资格](<../../../../../04数据规范/贸易点/03_资源表定义.md>)
