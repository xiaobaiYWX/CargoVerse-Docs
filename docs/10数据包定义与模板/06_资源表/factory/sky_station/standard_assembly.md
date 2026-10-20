# 标准建材装配港 · 实际物品贸易表

> **待落数据 · 2026-10-20 首轮设计。** 本页已替换旧抽象货物方案；运行数据仍为空表，以下商品与数值尚未发布、未经过实机平衡。

编号：**A01**。归属：**天穹联合工业（AUI）**。形态：**天空大站**。

资源 ID：`cargoverse:factory/sky_station/standard_assembly`。

对应数据路径：`data/cargoverse/trade_points/resource_tables/factory/sky_station/standard_assembly.json`。

## 业务定位

**标准建筑构件供应与大宗建材集散。** 采购砂石、金属与机壳材料，出售可直接搭建工厂和聚居区的标准构件。建材来自站点独立补货；收进砂石不会触发配方产出。重型石材形成低单价大宗业务，玻璃与金属构件提供较高附加值。

## 报价口径

- 使用现行 `schema_version: 3`；价格为本站 `unit_price`，单位为 **VB／个实际物品**。数量均为实际件数，不是栈数、旧货物数量或现实吨数。
- 全部条目使用精确物品 ID，省略 `components`，只匹配默认完整状态；工具为全新默认状态，设备无嵌套库存。不接受标签通配或任意耐久、附魔、命名变体。
- 以下为基准报价，不含行情与签约修正。经验是本站收购条目的每件奖励，不属于物品属性，也不根据价格自动推导。
- 所有出售条目都有有限 `stock`。收购列的 `0（不限）` 对应 `daily_limit: 0`；其余数值为同一站点实例所有玩家共享的每贸易日额度。
- 许可证／繁荣度经验只按自然生成收购目的地和实际成交件数计算；玩家工厂或玩家仓库来源同样按本地收购配置奖励。玩家目的地、手动普通目的地及出发购买不奖励。

## 出售目录

| rule_id | 物品 | 单价 VB | 初始件数 | 库存容量 | 每日补货 |
| --- | --- | ---: | ---: | ---: | ---: |
| `sell_minecraft_stone_bricks` | 石砖 · `minecraft:stone_bricks` | 4 | 768 | 2048 | 512 |
| `sell_minecraft_glass` | 玻璃 · `minecraft:glass` | 8 | 768 | 2048 | 512 |
| `sell_minecraft_iron_bars` | 铁栏杆 · `minecraft:iron_bars` | 12 | 256 | 768 | 192 |
| `sell_create_metal_girder` | 金属梁 · `create:metal_girder` | 22 | 256 | 768 | 192 |
| `sell_create_andesite_casing` | 安山机壳 · `create:andesite_casing` | 32 | 256 | 768 | 192 |

## 收购目录

| rule_id | 物品 | 单价 VB | 每日限额 | 许可证经验／件 | 繁荣度经验／件 |
| --- | --- | ---: | ---: | ---: | ---: |
| `buy_minecraft_cobblestone` | 圆石 · `minecraft:cobblestone` | 2 | 0（不限） | 1 | 1 |
| `buy_minecraft_sand` | 沙子 · `minecraft:sand` | 4 | 0（不限） | 1 | 1 |
| `buy_minecraft_gravel` | 沙砾 · `minecraft:gravel` | 3 | 0（不限） | 1 | 1 |
| `buy_minecraft_clay_ball` | 黏土球 · `minecraft:clay_ball` | 4 | 512 | 1 | 1 |
| `buy_minecraft_iron_ingot` | 铁锭 · `minecraft:iron_ingot` | 15 | 512 | 3 | 3 |
| `buy_create_andesite_alloy` | 安山合金 · `create:andesite_alloy` | 16 | 256 | 3 | 3 |
| `buy_minecraft_bread` | 面包 · `minecraft:bread` | 6 | 256 | 2 | 2 |
| `buy_minecraft_coal` | 煤炭 · `minecraft:coal` | 9 | 256 | 2 | 2 |
| `buy_minecraft_paper` | 纸 · `minecraft:paper` | 6 | 128 | 2 | 2 |
| `buy_minecraft_prismarine_shard` | 海晶碎片 · `minecraft:prismarine_shard` | 19 | 128 | 3 | 3 |
| `buy_minecraft_andesite` | 安山岩 · `minecraft:andesite` | 7 | 512 | 1 | 1 |
| `buy_minecraft_brick` | 红砖 · `minecraft:brick` | 3 | 256 | 1 | 1 |

## 运输与落地依赖

已命中专用配置的运输类别包括：建筑构件、燃料与能源、食品与食材、加工材料、原料资源。类别只用于货柜兼容，不能代替本页精确报价目录。

装柜前仍需按实际物品配置选择货柜与保护设计；本页不修改质量、固定件数损耗、冷链或易碎判定。不同货物未必能共用一个返程货柜。

报价目录在实例创建时保存快照。未来落入 JSON 后，应以新建经济实例验收；普通 reload 不会替换旧实例的空目录。

[本站贸易网络](<../../../07_贸易点/factory/标准建材装配港/定义设计/02_贸易网络设计.md>) · [总体设计](<../../../07_贸易点/设计总览.md>) · [现行格式与经验资格](<../../../../02贸易点系统/03_资源表定义.md>)
