# 遗迹清理营 · 实际物品贸易表

> **待落数据 · 2026-10-20 首轮设计。** 运行数据仍为空表，以下商品与数值尚未发布、未经过实机平衡。

编号：**G06**。归属：**遗民贸易协会（REX）**。形态：**地面小站**。

资源 ID：`cargoverse:resource/ground_station/ruin_clearance_camp`。

对应数据路径：`data/cargoverse/trade_points/resource_tables/resource/ground_station/ruin_clearance_camp.json`。

## 业务定位

**遗址普通材料整理。** REX 清理队出售苔石、裂纹石砖、砖和少量紫水晶；遗迹特色体现在材料与清理工具，不以日补复制全部稀有战利品。

## 报价口径

- 使用现行 `schema_version: 3`；价格为本站 `unit_price`，单位为 **VB／个实际物品**。数量均为实际件数，不是栈数、旧货物数量或现实吨数。
- 全部条目使用精确物品 ID，省略 `components`，只匹配默认完整状态；工具为全新默认状态，设备无嵌套库存。不接受标签通配或任意耐久、附魔、命名变体。
- 以下为基准报价，不含行情与签约修正。经验是本站收购条目的每件奖励，不属于物品属性，也不根据价格自动推导。
- 所有出售条目都有有限 `stock`。收购列的 `0（不限）` 对应 `daily_limit: 0`；其余数值为同一站点实例所有玩家共享的每贸易日额度。
- 许可证／繁荣度经验只按自然生成收购目的地和实际成交件数计算；玩家工厂或玩家仓库来源同样按本地收购配置奖励。玩家目的地、手动普通目的地及出发购买不奖励。

## 出售目录

| rule_id | 物品 | 单价 VB | 初始件数 | 库存容量 | 每日补货 |
| --- | --- | ---: | ---: | ---: | ---: |
| `sell_minecraft_mossy_cobblestone` | 苔石 · `minecraft:mossy_cobblestone` | 4 | 96 | 256 | 64 |
| `sell_minecraft_cracked_stone_bricks` | 裂纹石砖 · `minecraft:cracked_stone_bricks` | 4 | 96 | 256 | 64 |
| `sell_minecraft_brick` | 红砖 · `minecraft:brick` | 2 | 32 | 96 | 16 |
| `sell_minecraft_amethyst_shard` | 紫水晶碎片 · `minecraft:amethyst_shard` | 10 | 32 | 96 | 16 |
| `sell_minecraft_rotten_flesh` | 腐肉 · `minecraft:rotten_flesh` | 1 | 32 | 96 | 16 |

## 收购目录

| rule_id | 物品 | 单价 VB | 每日限额 | 许可证经验／件 | 繁荣度经验／件 |
| --- | --- | ---: | ---: | ---: | ---: |
| `buy_minecraft_brush` | 刷子 · `minecraft:brush` | 45 | 4 | 4 | 3 |
| `buy_minecraft_paper` | 纸 · `minecraft:paper` | 6 | 64 | 2 | 2 |
| `buy_minecraft_iron_pickaxe` | 铁镐 · `minecraft:iron_pickaxe` | 115 | 4 | 5 | 4 |
| `buy_minecraft_bread` | 面包 · `minecraft:bread` | 6 | 64 | 2 | 2 |
| `buy_minecraft_lantern` | 灯笼 · `minecraft:lantern` | 18 | 16 | 3 | 2 |

## 运输与落地依赖

货柜兼容按当前 solid／liquid／gas／living 交付形态及保护需求判断；本站用途描述不产生额外分类。运输属性以[正式逐物品清单](<../../../../14运输分类统计/README.md>)为准，不在每个报价设计中复制分类快照。

装柜前仍需按实际物品配置选择货柜与保护设计；本页不修改质量、固定件数损耗、冷链或易碎判定。不同货物未必能共用一个返程货柜。


本站不增加货柜制造、注册或领柜功能；所有收购条目设正数限额。设备采购额度通常低于一柜，属于地方更新需求。

报价目录在实例创建时保存快照。未来落入 JSON 后，应以新建经济实例验收；普通 reload 不会替换旧实例的空目录。

[本站贸易网络](<../../../07_贸易点/resource/遗迹清理营/定义设计/02_贸易网络设计.md>) · [总体设计](<../../../07_贸易点/设计总览.md>) · [现行格式与经验资格](<../../../../02贸易点系统/03_资源表定义.md>)
