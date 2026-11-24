# 云港民生集配站 · 实际物品贸易表

> 已接入内置数据包。以新建贸易点实例验收。

编号：**S01**。归属：**云港物流集团（SPL）**。形态：**天空大站**。

资源 ID：`cargoverse:market/sky_station/civic_distribution`。

对应数据路径：`data/cargoverse/trade_points/resource_tables/market/sky_station/civic_distribution.json`。

## 业务定位

**农产集购与常温生活补给主供。** 将居民常用面包、烤马铃薯、纸、火把和空瓶作为广覆盖货源，同时收购作物、鲜鱼、鲜肉与包装用品。Create 面粉作为真实中间产品出售，食品加工可由玩家工厂承接，不建立站内材料转化。

## 报价口径

- 使用现行 `schema_version: 3`；价格为本站 `unit_price`，单位为 **VB／份**。库存、补货、限额及许可证经验均按份配置，物品每组为一份，活体每只为一份。
- 固体条目使用精确物品 ID，省略 `components`，只匹配默认完整状态；工具为全新默认状态，设备无嵌套库存。不接受标签通配或任意耐久、附魔、命名变体。
- 以下为基准报价。成交会应用行情与签约修正。许可证经验由当地收购条目按份配置。
- 所有出售条目都有有限 `stock`。收购列的 `0（不限）` 对应 `daily_limit: 0`；其余数值为同一站点实例所有玩家共享的每贸易日额度。
- 许可证经验按向自然生成目的地实际交付的份数和当地收购配置结算，适用于任意货源。繁荣度与制造商交付声望由独立物资供应结算。

## 出售目录

| rule_id | 物品 | 单价 VB | 初始库存 | 库存容量 | 每日补货 | 最低繁荣度 |
| --- | --- | ---: | ---: | ---: | ---: | ---: |
| `sell_minecraft_bread` | 面包 · `minecraft:bread` | 5 | 1024 | 3072 | 768 | 1 |
| `sell_minecraft_baked_potato` | 烤马铃薯 · `minecraft:baked_potato` | 4 | 768 | 2048 | 512 | 0 |
| `sell_minecraft_paper` | 纸 · `minecraft:paper` | 5 | 768 | 2048 | 512 | 2 |
| `sell_minecraft_torch` | 火把 · `minecraft:torch` | 3 | 768 | 2048 | 512 | 0 |
| `sell_minecraft_glass_bottle` | 玻璃瓶 · `minecraft:glass_bottle` | 3 | 256 | 768 | 192 | 0 |
| `sell_create_wheat_flour` | 小麦面粉 · `create:wheat_flour` | 6 | 768 | 2048 | 512 | 4 |

## 收购目录

| rule_id | 物品 | 单价 VB | 每日限额 | 许可证经验／份 | 最低繁荣度 |
| --- | --- | ---: | ---: | ---: | ---: |
| `buy_minecraft_wheat` | 小麦 · `minecraft:wheat` | 4 | 0（不限） | 1 | 0 |
| `buy_minecraft_carrot` | 胡萝卜 · `minecraft:carrot` | 4 | 512 | 1 | 0 |
| `buy_minecraft_potato` | 马铃薯 · `minecraft:potato` | 3 | 512 | 1 | 0 |
| `buy_minecraft_cod` | 生鳕鱼 · `minecraft:cod` | 6 | 256 | 3 | 0 |
| `buy_minecraft_porkchop` | 生猪排 · `minecraft:porkchop` | 8 | 128 | 3 | 0 |
| `buy_create_cardboard` | 纸板 · `create:cardboard` | 5 | 256 | 1 | 0 |
| `buy_minecraft_barrel` | 木桶 · `minecraft:barrel` | 45 | 64 | 3 | 3 |
| `buy_minecraft_coal` | 煤炭 · `minecraft:coal` | 9 | 256 | 2 | 1 |
| `buy_create_andesite_funnel` | 安山漏斗 · `create:andesite_funnel` | 32 | 32 | 4 | 2 |
| `buy_minecraft_ink_sac` | 墨囊 · `minecraft:ink_sac` | 8 | 128 | 2 | 0 |
| `buy_living_cow` | 牛 · `minecraft:cow` | 120 | 4 | 6 | 5 |
| `buy_living_pig` | 猪 · `minecraft:pig` | 80 | 8 | 4 | 3 |
| `buy_living_sheep` | 羊 · `minecraft:sheep` | 90 | 6 | 5 | 4 |
| `buy_living_chicken` | 鸡 · `minecraft:chicken` | 26 | 16 | 2 | 1 |

## 运输与落地依赖

货柜兼容按当前 solid／liquid／living 交付形态及保护需求判断；本站用途描述不产生额外分类。运输属性以[正式逐物品清单](<../../../../01运输物品/固体/README.md>)为准，不在每个报价设计中复制分类快照。

装柜前仍需按实际物品配置选择货柜与保护设计；本页不修改质量、固定组数损耗、冷链或易碎判定。不同货物未必能共用一个返程货柜。


报价目录在实例创建时保存快照。以新建经济实例验收；普通 reload 保留旧实例的报价快照。

[本站贸易网络](<../../../站点/market/云港民生集配站/定义设计/02_贸易网络设计.md>) · [总体设计](<../../../站点/设计总览.md>) · [现行格式与经验资格](<../../../../../04数据规范/贸易点/03_资源表定义.md>)

## 活体交易

已接入首轮陆生活体交易，按只结算，与上文固体按组报价分开。物种、价格、有限库存／日限额和每只经验见[自然站活体交易](../../../自然站活体交易.md)。运行数据为本站同名资源表中的 `type: living` 条目。
