# 航路巡防哨站 · 实际物品贸易表

> 已接入内置数据包。以新建贸易点实例验收。

编号：**G08**。归属：**铁壁防务集团（BDS）**。形态：**地面小站**。

资源 ID：`cargoverse:market/ground_station/route_watchpost`。

对应数据路径：`data/cargoverse/trade_points/resource_tables/market/ground_station/route_watchpost.json`。

## 业务定位

**巡防消耗与少量回程材料。** BDS 派驻哨提供少量羽毛、燧石和金属零料，需求集中在箭、盾、通信和生活补给。零料低值低经验，不冒称损坏装备被自动拆解。

## 报价口径

- 使用现行 `schema_version: 3`；价格为本站 `unit_price`，单位为 **VB／份**。库存、补货、限额及许可证经验均按份配置，物品每组为一份，活体每只为一份。
- 全部条目使用精确物品 ID，省略 `components`，只匹配默认完整状态；工具为全新默认状态，设备无嵌套库存。不接受标签通配或任意耐久、附魔、命名变体。
- 以下为基准报价。成交会应用行情与签约修正。许可证经验由当地收购条目按份配置。
- 所有出售条目都有有限 `stock`。收购列的 `0（不限）` 对应 `daily_limit: 0`；其余数值为同一站点实例所有玩家共享的每贸易日额度。
- 许可证经验按向自然生成目的地实际交付的份数和当地收购配置结算，适用于任意货源。繁荣度与制造商交付声望由独立物资供应结算。

## 出售目录

| rule_id | 物品 | 单价 VB | 初始库存 | 库存容量 | 每日补货 | 最低繁荣度 |
| --- | --- | ---: | ---: | ---: | ---: | ---: |
| `sell_minecraft_feather` | 羽毛 · `minecraft:feather` | 3 | 32 | 96 | 16 | 1 |
| `sell_minecraft_flint` | 燧石 · `minecraft:flint` | 2 | 32 | 96 | 16 | 0 |
| `sell_minecraft_iron_nugget` | 铁粒 · `minecraft:iron_nugget` | 1 | 32 | 96 | 16 | 0 |

## 收购目录

| rule_id | 物品 | 单价 VB | 每日限额 | 许可证经验／份 | 最低繁荣度 |
| --- | --- | ---: | ---: | ---: | ---: |
| `buy_minecraft_arrow` | 箭 · `minecraft:arrow` | 8 | 128 | 3 | 0 |
| `buy_minecraft_bread` | 面包 · `minecraft:bread` | 6 | 64 | 2 | 0 |
| `buy_minecraft_coal` | 煤炭 · `minecraft:coal` | 9 | 64 | 2 | 0 |
| `buy_create_redstone_link` | 无线红石信号终端 · `create:redstone_link` | 115 | 4 | 5 | 4 |
| `buy_minecraft_shield` | 盾牌 · `minecraft:shield` | 90 | 4 | 5 | 2 |
| `buy_create_builders_tea` | 建筑工茶饮 · `create:builders_tea` | 18 | 32 | 3 | 1 |

## 运输与落地依赖

货柜兼容按当前 solid／liquid／living 交付形态及保护需求判断；本站用途描述不产生额外分类。运输属性以[正式逐物品清单](<../../../../01运输物品/固体/README.md>)为准，不在每个报价设计中复制分类快照。

装柜前仍需按实际物品配置选择货柜与保护设计；本页不修改质量、固定组数损耗、冷链或易碎判定。不同货物未必能共用一个返程货柜。


本站不增加货柜制造、注册或领柜功能；所有收购条目设正数限额。设备采购额度通常低于一柜，属于地方更新需求。

报价目录在实例创建时保存快照。以新建经济实例验收；普通 reload 保留旧实例的报价快照。

[本站贸易网络](<../../../站点/market/航路巡防哨站/定义设计/02_贸易网络设计.md>) · [总体设计](<../../../站点/设计总览.md>) · [现行格式与经验资格](<../../../../../04数据规范/贸易点/03_资源表定义.md>)
