# 虚空相位研究站 · 实际物品贸易表

> 已接入内置数据包。以新建贸易点实例验收。

编号：**H03**。归属：**地平线研究院（HRI）**。形态：**天空大站**。

资源 ID：`cargoverse:resource/sky_station/phase_station`。

对应数据路径：`data/cargoverse/trade_points/resource_tables/resource/sky_station/phase_station.json`。

## 业务定位

**末地材料与浮空相位研究供应。** 用实际末地粉料、末影珍珠及两种浮空材料构成研究业务；不将旧虚空混合物抽象货物直接映射为不存在的物品。采购末地石、黑曜石粉、控制件和陀螺仪，维持少量高技术专线。

## 报价口径

- 使用现行 `schema_version: 3`；价格为本站 `unit_price`，单位为 **VB／份**。库存、补货、限额及许可证经验均按份配置，物品每组为一份，活体每只为一份。
- 全部条目使用精确物品 ID，省略 `components`，只匹配默认完整状态；工具为全新默认状态，设备无嵌套库存。不接受标签通配或任意耐久、附魔、命名变体。
- 以下为基准报价。成交会应用行情与签约修正。许可证经验由当地收购条目按份配置。
- 所有出售条目都有有限 `stock`。收购列的 `0（不限）` 对应 `daily_limit: 0`；其余数值为同一站点实例所有玩家共享的每贸易日额度。
- 许可证经验按向自然生成目的地实际交付的份数和当地收购配置结算，适用于任意货源。繁荣度与制造商交付声望由独立物资供应结算。

## 出售目录

| rule_id | 物品 | 单价 VB | 初始库存 | 库存容量 | 每日补货 | 最低繁荣度 |
| --- | --- | ---: | ---: | ---: | ---: | ---: |
| `sell_aeronautics_end_stone_powder` | 末地石粉末 · `aeronautics:end_stone_powder` | 28 | 256 | 768 | 192 | 0 |
| `sell_minecraft_ender_pearl` | 末影珍珠 · `minecraft:ender_pearl` | 60 | 16 | 48 | 8 | 1 |
| `sell_aeronautics_levitite` | 浮空水晶 · `aeronautics:levitite` | 42 | 24 | 64 | 12 | 0 |
| `sell_aeronautics_pearlescent_levitite` | 珠光浮空水晶 · `aeronautics:pearlescent_levitite` | 120 | 4 | 12 | 2 | 3 |

## 收购目录

| rule_id | 物品 | 单价 VB | 每日限额 | 许可证经验／份 | 最低繁荣度 |
| --- | --- | ---: | ---: | ---: | ---: |
| `buy_minecraft_end_stone` | 末地石 · `minecraft:end_stone` | 10 | 256 | 3 | 0 |
| `buy_create_powdered_obsidian` | 黑曜石粉末 · `create:powdered_obsidian` | 15 | 128 | 4 | 0 |
| `buy_minecraft_quartz` | 下界石英 · `minecraft:quartz` | 12 | 128 | 3 | 0 |
| `buy_simulated_gyroscopic_mechanism` | 陀螺仪构件 · `simulated:gyroscopic_mechanism` | 340 | 16 | 8 | 4 |
| `buy_create_redstone_link` | 无线红石信号终端 · `create:redstone_link` | 115 | 32 | 5 | 2 |
| `buy_minecraft_blaze_powder` | 烈焰粉 · `minecraft:blaze_powder` | 36 | 64 | 4 | 1 |
| `buy_minecraft_bread` | 面包 · `minecraft:bread` | 6 | 256 | 2 | 0 |

## 运输与落地依赖

货柜兼容按当前 solid／liquid／living 交付形态及保护需求判断；本站用途描述不产生额外分类。运输属性以[正式逐物品清单](<../../../../01运输物品/固体/README.md>)为准，不在每个报价设计中复制分类快照。

装柜前仍需按实际物品配置选择货柜与保护设计；本页不修改质量、固定组数损耗、冷链或易碎判定。不同货物未必能共用一个返程货柜。


报价目录在实例创建时保存快照。以新建经济实例验收；普通 reload 保留旧实例的报价快照。

[本站贸易网络](<../../../站点/resource/虚空相位研究站/定义设计/02_贸易网络设计.md>) · [总体设计](<../../../站点/设计总览.md>) · [现行格式与经验资格](<../../../../../04数据规范/贸易点/03_资源表定义.md>)
