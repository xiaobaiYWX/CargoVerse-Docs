# 云港民生集配站 · 实际物品贸易表

> **待落数据 · 2026-10-20 首轮设计。** 运行数据仍为空表，以下商品与数值尚未发布、未经过实机平衡。

编号：**S01**。归属：**云港物流集团（SPL）**。形态：**天空大站**。

资源 ID：`cargoverse:market/sky_station/civic_distribution`。

对应数据路径：`data/cargoverse/trade_points/resource_tables/market/sky_station/civic_distribution.json`。

## 业务定位

**农产集购与常温生活补给主供。** 将居民常用面包、烤马铃薯、纸、火把和空瓶作为广覆盖货源，同时收购作物、鲜鱼、鲜肉与包装用品。Create 面粉作为真实中间产品出售，食品加工可由玩家工厂承接，不建立站内材料转化。

## 报价口径

- 使用现行 `schema_version: 3`；价格为本站 `unit_price`，单位为 **VB／个实际物品**。数量均为实际件数，不是栈数、旧货物数量或现实吨数。
- 全部条目使用精确物品 ID，省略 `components`，只匹配默认完整状态；工具为全新默认状态，设备无嵌套库存。不接受标签通配或任意耐久、附魔、命名变体。
- 以下为基准报价，不含行情与签约修正。经验是本站收购条目的每件奖励，不属于物品属性，也不根据价格自动推导。
- 所有出售条目都有有限 `stock`。收购列的 `0（不限）` 对应 `daily_limit: 0`；其余数值为同一站点实例所有玩家共享的每贸易日额度。
- 许可证／繁荣度经验只按自然生成收购目的地和实际成交件数计算；玩家工厂或玩家仓库来源同样按本地收购配置奖励。玩家目的地、手动普通目的地及出发购买不奖励。

## 出售目录

| rule_id | 物品 | 单价 VB | 初始件数 | 库存容量 | 每日补货 |
| --- | --- | ---: | ---: | ---: | ---: |
| `sell_minecraft_bread` | 面包 · `minecraft:bread` | 5 | 1024 | 3072 | 768 |
| `sell_minecraft_baked_potato` | 烤马铃薯 · `minecraft:baked_potato` | 4 | 768 | 2048 | 512 |
| `sell_minecraft_paper` | 纸 · `minecraft:paper` | 5 | 768 | 2048 | 512 |
| `sell_minecraft_torch` | 火把 · `minecraft:torch` | 3 | 768 | 2048 | 512 |
| `sell_minecraft_glass_bottle` | 玻璃瓶 · `minecraft:glass_bottle` | 3 | 256 | 768 | 192 |
| `sell_create_wheat_flour` | 小麦面粉 · `create:wheat_flour` | 6 | 768 | 2048 | 512 |

## 收购目录

| rule_id | 物品 | 单价 VB | 每日限额 | 许可证经验／件 | 繁荣度经验／件 |
| --- | --- | ---: | ---: | ---: | ---: |
| `buy_minecraft_wheat` | 小麦 · `minecraft:wheat` | 4 | 0（不限） | 1 | 1 |
| `buy_minecraft_carrot` | 胡萝卜 · `minecraft:carrot` | 4 | 512 | 1 | 1 |
| `buy_minecraft_potato` | 马铃薯 · `minecraft:potato` | 3 | 512 | 1 | 1 |
| `buy_minecraft_cod` | 生鳕鱼 · `minecraft:cod` | 6 | 256 | 3 | 3 |
| `buy_minecraft_porkchop` | 生猪排 · `minecraft:porkchop` | 8 | 128 | 3 | 3 |
| `buy_create_cardboard` | 纸板 · `create:cardboard` | 5 | 256 | 1 | 1 |
| `buy_minecraft_barrel` | 木桶 · `minecraft:barrel` | 45 | 64 | 3 | 3 |
| `buy_minecraft_coal` | 煤炭 · `minecraft:coal` | 9 | 256 | 2 | 2 |
| `buy_create_andesite_funnel` | 安山漏斗 · `create:andesite_funnel` | 32 | 32 | 4 | 3 |
| `buy_minecraft_ink_sac` | 墨囊 · `minecraft:ink_sac` | 8 | 128 | 2 | 2 |

## 运输与落地依赖

货柜兼容按当前 solid／liquid／gas／living 交付形态及保护需求判断；本站用途描述不产生额外分类。运输属性以[正式逐物品清单](<../../../../14运输分类统计/README.md>)为准，不在每个报价设计中复制分类快照。

装柜前仍需按实际物品配置选择货柜与保护设计；本页不修改质量、固定件数损耗、冷链或易碎判定。不同货物未必能共用一个返程货柜。


报价目录在实例创建时保存快照。未来落入 JSON 后，应以新建经济实例验收；普通 reload 不会替换旧实例的空目录。

[本站贸易网络](<../../../07_贸易点/market/云港民生集配站/定义设计/02_贸易网络设计.md>) · [总体设计](<../../../07_贸易点/设计总览.md>) · [现行格式与经验资格](<../../../../02贸易点系统/03_资源表定义.md>)
