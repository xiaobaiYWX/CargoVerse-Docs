# 工业化学品供应站 · 实际物品贸易表

> **待落数据 · 2026-10-20 首轮设计。** 本页已替换旧抽象货物方案；运行数据仍为空表，以下商品与数值尚未发布、未经过实机平衡。

编号：**E02**。归属：**赫利俄斯能源集团（HEC）**。形态：**天空大站**。

资源 ID：`cargoverse:factory/sky_station/chemical_works`。

对应数据路径：`data/cargoverse/trade_points/resource_tables/factory/sky_station/chemical_works.json`。

## 业务定位

**化工粉料、黏合与危险物资供应。** 以余烬面粉、黑曜石粉、黏液、荧石粉和火药替代旧抽象化学品；强力胶只交易默认全新状态。采购基础试剂、容器和搅拌设备，不出售空名词的润滑油或虚构电池。

## 报价口径

- 使用现行 `schema_version: 3`；价格为本站 `unit_price`，单位为 **VB／个实际物品**。数量均为实际件数，不是栈数、旧货物数量或现实吨数。
- 全部条目使用精确物品 ID，省略 `components`，只匹配默认完整状态；工具为全新默认状态，设备无嵌套库存。不接受标签通配或任意耐久、附魔、命名变体。
- 以下为基准报价，不含行情与签约修正。经验是本站收购条目的每件奖励，不属于物品属性，也不根据价格自动推导。
- 所有出售条目都有有限 `stock`。收购列的 `0（不限）` 对应 `daily_limit: 0`；其余数值为同一站点实例所有玩家共享的每贸易日额度。
- 许可证／繁荣度经验只按自然生成收购目的地和实际成交件数计算；玩家工厂或玩家仓库来源同样按本地收购配置奖励。玩家目的地、手动普通目的地及出发购买不奖励。

## 出售目录

| rule_id | 物品 | 单价 VB | 初始件数 | 库存容量 | 每日补货 |
| --- | --- | ---: | ---: | ---: | ---: |
| `sell_create_cinder_flour` | 余烬面粉 · `create:cinder_flour` | 8 | 256 | 768 | 192 |
| `sell_create_powdered_obsidian` | 黑曜石粉末 · `create:powdered_obsidian` | 12 | 256 | 768 | 192 |
| `sell_minecraft_slime_ball` | 黏液球 · `minecraft:slime_ball` | 10 | 256 | 768 | 192 |
| `sell_minecraft_glowstone_dust` | 荧石粉 · `minecraft:glowstone_dust` | 12 | 256 | 768 | 192 |
| `sell_minecraft_gunpowder` | 火药 · `minecraft:gunpowder` | 16 | 256 | 768 | 192 |
| `sell_create_super_glue` | 强力胶 · `create:super_glue` | 70 | 24 | 64 | 12 |

## 收购目录

| rule_id | 物品 | 单价 VB | 每日限额 | 许可证经验／件 | 繁荣度经验／件 |
| --- | --- | ---: | ---: | ---: | ---: |
| `buy_minecraft_netherrack` | 下界岩 · `minecraft:netherrack` | 2 | 0（不限） | 0 | 1 |
| `buy_minecraft_redstone` | 红石粉 · `minecraft:redstone` | 10 | 256 | 3 | 3 |
| `buy_minecraft_sugar` | 糖 · `minecraft:sugar` | 5 | 256 | 1 | 1 |
| `buy_minecraft_glass_bottle` | 玻璃瓶 · `minecraft:glass_bottle` | 4 | 256 | 1 | 1 |
| `buy_create_mechanical_mixer` | 动力搅拌器 · `create:mechanical_mixer` | 240 | 16 | 6 | 5 |
| `buy_minecraft_bread` | 面包 · `minecraft:bread` | 6 | 256 | 2 | 2 |
| `buy_minecraft_coal` | 煤炭 · `minecraft:coal` | 9 | 256 | 2 | 2 |
| `buy_minecraft_obsidian` | 黑曜石 · `minecraft:obsidian` | 16 | 256 | 3 | 3 |

## 运输与落地依赖

已命中专用配置的运输类别包括：化工与药剂、红石与控制、燃料与能源、食品与食材、机械设备、加工材料、原料资源。类别只用于货柜兼容，不能代替本页精确报价目录。

装柜前仍需按实际物品配置选择货柜与保护设计；本页不修改质量、固定件数损耗、冷链或易碎判定。不同货物未必能共用一个返程货柜。

**运输属性待补：** 玻璃瓶（`minecraft:glass_bottle`）。当前这些物品使用通用默认配置，并非不能装柜，但分类与质量尚未按用途专门确认；不能把默认轻量当作已平衡结果。

报价目录在实例创建时保存快照。未来落入 JSON 后，应以新建经济实例验收；普通 reload 不会替换旧实例的空目录。

[本站贸易网络](<../../../07_贸易点/factory/工业化学品供应站/定义设计/02_贸易网络设计.md>) · [总体设计](<../../../07_贸易点/设计总览.md>) · [现行格式与经验资格](<../../../../02贸易点系统/03_资源表定义.md>)
