# 天空城综合市场 · 实际物品贸易表

> 已接入内置数据包。以新建贸易点实例验收。

编号：**S03**。归属：**云港物流集团（SPL）**。形态：**天空大站**。

资源 ID：`cargoverse:market/sky_station/skycity_market`。

对应数据路径：`data/cargoverse/trade_points/resource_tables/market/sky_station/skycity_market.json`。

## 业务定位

**居民消费与成品加工市场。** 集中消费食品、纺织、玻璃、装饰和日用品，出售书籍、灯具及精加工食品。收购玩家加工产品但逐项限制高价值消费，避免城市成为所有机器、矿物和遗物的万能出口。

## 报价口径

- 使用现行 `schema_version: 3`；价格为本站 `unit_price`，单位为 **VB／份**。库存、补货、限额及许可证经验均按份配置，物品每组为一份，活体每只为一份。
- 全部条目使用精确物品 ID，省略 `components`，只匹配默认完整状态；工具为全新默认状态，设备无嵌套库存。不接受标签通配或任意耐久、附魔、命名变体。
- 以下为基准报价。成交会应用行情与签约修正。许可证经验由当地收购条目按份配置。
- 所有出售条目都有有限 `stock`。收购列的 `0（不限）` 对应 `daily_limit: 0`；其余数值为同一站点实例所有玩家共享的每贸易日额度。
- 许可证经验按向自然生成目的地实际交付的份数和当地收购配置结算，适用于任意货源。繁荣度与制造商交付声望由独立物资供应结算。

## 出售目录

| rule_id | 物品 | 单价 VB | 初始库存 | 库存容量 | 每日补货 | 最低繁荣度 |
| --- | --- | ---: | ---: | ---: | ---: | ---: |
| `sell_minecraft_cookie` | 曲奇 · `minecraft:cookie` | 3 | 384 | 1024 | 256 | 0 |
| `sell_create_honeyed_apple` | 蜜渍苹果 · `create:honeyed_apple` | 15 | 256 | 768 | 192 | 0 |
| `sell_minecraft_book` | 书 · `minecraft:book` | 16 | 256 | 768 | 192 | 2 |
| `sell_minecraft_lantern` | 灯笼 · `minecraft:lantern` | 14 | 256 | 768 | 192 | 0 |
| `sell_create_sweet_roll` | 甜甜卷 · `create:sweet_roll` | 16 | 256 | 768 | 192 | 4 |
| `sell_create_builders_tea` | 建筑工茶饮 · `create:builders_tea` | 15 | 256 | 768 | 192 | 1 |
| `sell_minecraft_apple` | 苹果 · `minecraft:apple` | 4 | 256 | 768 | 192 | 0 |

## 收购目录

| rule_id | 物品 | 单价 VB | 每日限额 | 许可证经验／份 | 最低繁荣度 |
| --- | --- | ---: | ---: | ---: | ---: |
| `buy_minecraft_bread` | 面包 · `minecraft:bread` | 6 | 512 | 2 | 0 |
| `buy_minecraft_salmon` | 生鲑鱼 · `minecraft:salmon` | 9 | 256 | 3 | 0 |
| `buy_minecraft_white_wool` | 白色羊毛 · `minecraft:white_wool` | 9 | 256 | 3 | 0 |
| `buy_minecraft_glass` | 玻璃 · `minecraft:glass` | 10 | 512 | 2 | 0 |
| `buy_minecraft_painting` | 画 · `minecraft:painting` | 60 | 16 | 5 | 3 |
| `buy_create_cuckoo_clock` | 布谷鸟闹钟 · `create:cuckoo_clock` | 130 | 8 | 6 | 4 |
| `buy_minecraft_copper_ingot` | 铜锭 · `minecraft:copper_ingot` | 10 | 256 | 2 | 0 |
| `buy_minecraft_music_disc_13` | 音乐唱片 · `minecraft:music_disc_13` | 360 | 1 | 16 | 5 |
| `buy_minecraft_flower_pot` | 花盆 · `minecraft:flower_pot` | 16 | 32 | 3 | 1 |
| `buy_minecraft_baked_potato` | 烤马铃薯 · `minecraft:baked_potato` | 5 | 256 | 1 | 0 |
| `buy_create_polished_rose_quartz` | 磨制玫瑰石英 · `create:polished_rose_quartz` | 32 | 64 | 4 | 2 |

## 运输与落地依赖

货柜兼容按当前 solid／liquid／living 交付形态及保护需求判断；本站用途描述不产生额外分类。运输属性以[正式逐物品清单](<../../../../01运输物品/固体/README.md>)为准，不在每个报价设计中复制分类快照。

装柜前仍需按实际物品配置选择货柜与保护设计；本页不修改质量、固定组数损耗、冷链或易碎判定。不同货物未必能共用一个返程货柜。


报价目录在实例创建时保存快照。以新建经济实例验收；普通 reload 保留旧实例的报价快照。

[本站贸易网络](<../../../站点/market/天空城综合市场/定义设计/02_贸易网络设计.md>) · [总体设计](<../../../站点/设计总览.md>) · [现行格式与经验资格](<../../../../../04数据规范/贸易点/03_资源表定义.md>)
