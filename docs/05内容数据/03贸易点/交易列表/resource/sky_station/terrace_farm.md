# 梯田农林站 · 实际物品贸易表

> 已接入内置数据包。以新建贸易点实例验收。

编号：**V01**。归属：**绿洲农业联盟（VBS）**。形态：**天空大站**。

资源 ID：`cargoverse:resource/sky_station/terrace_farm`。

对应数据路径：`data/cargoverse/trade_points/resource_tables/resource/sky_station/terrace_farm.json`。

## 业务定位

**谷物、林木与农场补给主供。** 供给小麦、甘蔗、原木和种子，同时提供基础面包以增加非城市地区的口粮来源。农业设备、肥料与维护件有明确需求；不包办养殖、水产或生物工程的全部产品。

## 报价口径

- 使用现行 `schema_version: 3`；价格为本站 `unit_price`，单位为 **VB／份**。库存、补货、限额及许可证经验均按份配置，物品每组为一份，活体每只为一份。
- 固体条目使用精确物品 ID，省略 `components`，只匹配默认完整状态；工具为全新默认状态，设备无嵌套库存。不接受标签通配或任意耐久、附魔、命名变体。
- 以下为基准报价。成交会应用行情与签约修正。许可证经验由当地收购条目按份配置。
- 所有出售条目都有有限 `stock`。收购列的 `0（不限）` 对应 `daily_limit: 0`；其余数值为同一站点实例所有玩家共享的每贸易日额度。
- 许可证经验按向自然生成目的地实际交付的份数和当地收购配置结算，适用于任意货源。繁荣度与制造商交付声望由独立物资供应结算。

## 出售目录

| rule_id | 物品 | 单价 VB | 初始库存 | 库存容量 | 每日补货 | 最低繁荣度 |
| --- | --- | ---: | ---: | ---: | ---: | ---: |
| `sell_minecraft_wheat` | 小麦 · `minecraft:wheat` | 3 | 1536 | 4096 | 768 | 0 |
| `sell_minecraft_sugar_cane` | 甘蔗 · `minecraft:sugar_cane` | 3 | 768 | 2048 | 512 | 0 |
| `sell_minecraft_oak_log` | 橡木原木 · `minecraft:oak_log` | 12 | 768 | 2048 | 512 | 1 |
| `sell_minecraft_wheat_seeds` | 小麦种子 · `minecraft:wheat_seeds` | 2 | 256 | 768 | 192 | 0 |
| `sell_minecraft_bread` | 面包 · `minecraft:bread` | 5 | 512 | 1536 | 384 | 0 |
| `sell_minecraft_porkchop` | 生猪排 · `minecraft:porkchop` | 6 | 256 | 768 | 192 | 0 |
| `sell_living_cow` | 牛 · `minecraft:cow` | 96 | 4 | 12 | 2 | 4 |
| `sell_living_pig` | 猪 · `minecraft:pig` | 64 | 6 | 18 | 3 | 2 |
| `sell_living_sheep` | 羊 · `minecraft:sheep` | 72 | 6 | 18 | 3 | 3 |

## 收购目录

| rule_id | 物品 | 单价 VB | 每日限额 | 许可证经验／份 | 最低繁荣度 |
| --- | --- | ---: | ---: | ---: | ---: |
| `buy_minecraft_bone_meal` | 骨粉 · `minecraft:bone_meal` | 5 | 512 | 1 | 0 |
| `buy_create_tree_fertilizer` | 树木肥料 · `create:tree_fertilizer` | 12 | 128 | 3 | 0 |
| `buy_create_mechanical_harvester` | 动力收割机 · `create:mechanical_harvester` | 230 | 16 | 6 | 4 |
| `buy_create_mechanical_plough` | 动力犁 · `create:mechanical_plough` | 170 | 16 | 6 | 3 |
| `buy_create_shaft` | 传动杆 · `create:shaft` | 12 | 128 | 3 | 0 |
| `buy_minecraft_dried_kelp` | 干海带 · `minecraft:dried_kelp` | 4 | 256 | 1 | 0 |
| `buy_create_builders_tea` | 建筑工茶饮 · `create:builders_tea` | 18 | 128 | 3 | 1 |
| `buy_create_fluid_tank` | 流体储罐 · `create:fluid_tank` | 85 | 32 | 4 | 2 |
| `buy_minecraft_gravel` | 沙砾 · `minecraft:gravel` | 3 | 256 | 1 | 0 |

## 运输与落地依赖

货柜兼容按当前 solid／liquid／living 交付形态及保护需求判断；本站用途描述不产生额外分类。运输属性以[正式逐物品清单](<../../../../01运输物品/固体/README.md>)为准，不在每个报价设计中复制分类快照。

装柜前仍需按实际物品配置选择货柜与保护设计；本页不修改质量、固定组数损耗、冷链或易碎判定。不同货物未必能共用一个返程货柜。

报价目录在实例创建时保存快照。以新建经济实例验收；普通 reload 保留旧实例的报价快照。

[本站贸易网络](<../../../站点/resource/梯田农林站/定义设计/02_贸易网络设计.md>) · [总体设计](<../../../站点/设计总览.md>) · [现行格式与经验资格](<../../../../../04数据规范/贸易点/03_资源表定义.md>)

## 活体交易

已接入首轮陆生活体交易，按只结算，与上文固体按组报价分开。物种、价格、有限库存／日限额和每只经验见[自然站活体交易](../../../自然站活体交易.md)。运行数据为本站同名资源表中的 `type: living` 条目。
