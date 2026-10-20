# 飞艇总装与航修港 · 实际物品贸易表

> **待落数据 · 2026-10-20 首轮设计。** 本页已替换旧抽象货物方案；运行数据仍为空表，以下商品与数值尚未发布、未经过实机平衡。

编号：**A03**。归属：**天穹联合工业（AUI）**。形态：**天空大站**。

资源 ID：`cargoverse:factory/sky_station/airship_yard`。

对应数据路径：`data/cargoverse/trade_points/resource_tables/factory/sky_station/airship_yard.json`。

## 业务定位

**航空蒙皮、推进与系泊部件专业供应。** 直接引入航空学气囊与螺旋桨，配合 Simulated 系泊和绳索连接部件。采购蒙皮纤维、金属板、精密构件、陀螺仪构件和浮空材料；只售实际部件，不将整艘载具或结构当作物品。

## 报价口径

- 使用现行 `schema_version: 3`；价格为本站 `unit_price`，单位为 **VB／个实际物品**。数量均为实际件数，不是栈数、旧货物数量或现实吨数。
- 全部条目使用精确物品 ID，省略 `components`，只匹配默认完整状态；工具为全新默认状态，设备无嵌套库存。不接受标签通配或任意耐久、附魔、命名变体。
- 以下为基准报价，不含行情与签约修正。经验是本站收购条目的每件奖励，不属于物品属性，也不根据价格自动推导。
- 所有出售条目都有有限 `stock`。收购列的 `0（不限）` 对应 `daily_limit: 0`；其余数值为同一站点实例所有玩家共享的每贸易日额度。
- 许可证／繁荣度经验只按自然生成收购目的地和实际成交件数计算；玩家工厂或玩家仓库来源同样按本地收购配置奖励。玩家目的地、手动普通目的地及出发购买不奖励。

## 出售目录

| rule_id | 物品 | 单价 VB | 初始件数 | 库存容量 | 每日补货 |
| --- | --- | ---: | ---: | ---: | ---: |
| `sell_aeronautics_white_envelope` | 气球蒙皮 · `aeronautics:white_envelope` | 30 | 128 | 384 | 64 |
| `sell_aeronautics_wooden_propeller` | 木制螺旋桨 · `aeronautics:wooden_propeller` | 100 | 24 | 64 | 12 |
| `sell_aeronautics_andesite_propeller` | 安山螺旋桨 · `aeronautics:andesite_propeller` | 180 | 24 | 64 | 12 |
| `sell_aeronautics_propeller_bearing` | 螺旋桨轴承 · `aeronautics:propeller_bearing` | 160 | 24 | 64 | 12 |
| `sell_simulated_docking_connector` | 对接连接器 · `simulated:docking_connector` | 160 | 24 | 64 | 12 |
| `sell_simulated_rope_connector` | 绳索连接器 · `simulated:rope_connector` | 40 | 256 | 768 | 192 |

## 收购目录

| rule_id | 物品 | 单价 VB | 每日限额 | 许可证经验／件 | 繁荣度经验／件 |
| --- | --- | ---: | ---: | ---: | ---: |
| `buy_minecraft_white_wool` | 白色羊毛 · `minecraft:white_wool` | 9 | 512 | 3 | 3 |
| `buy_create_brass_sheet` | 黄铜板 · `create:brass_sheet` | 34 | 256 | 4 | 3 |
| `buy_create_sturdy_sheet` | 坚固板 · `create:sturdy_sheet` | 85 | 64 | 5 | 4 |
| `buy_create_precision_mechanism` | 精密构件 · `create:precision_mechanism` | 190 | 64 | 5 | 4 |
| `buy_simulated_gyroscopic_mechanism` | 陀螺仪构件 · `simulated:gyroscopic_mechanism` | 330 | 16 | 8 | 6 |
| `buy_aeronautics_levitite` | 浮空水晶 · `aeronautics:levitite` | 48 | 128 | 5 | 4 |
| `buy_minecraft_coal` | 煤炭 · `minecraft:coal` | 9 | 256 | 2 | 2 |
| `buy_minecraft_bread` | 面包 · `minecraft:bread` | 6 | 256 | 2 | 2 |
| `buy_create_super_glue` | 强力胶 · `create:super_glue` | 85 | 64 | 4 | 3 |
| `buy_create_sand_paper` | 砂纸 · `create:sand_paper` | 6 | 128 | 1 | 1 |
| `buy_create_blaze_cake` | 烈焰蛋糕 · `create:blaze_cake` | 125 | 32 | 5 | 4 |

## 运输与落地依赖

已命中专用配置的运输类别包括：化工与药剂、建筑构件、燃料与能源、食品与食材、机械零件、加工材料、原料资源、工具与装备、载具与部件。类别只用于货柜兼容，不能代替本页精确报价目录。

装柜前仍需按实际物品配置选择货柜与保护设计；本页不修改质量、固定件数损耗、冷链或易碎判定。不同货物未必能共用一个返程货柜。

报价目录在实例创建时保存快照。未来落入 JSON 后，应以新建经济实例验收；普通 reload 不会替换旧实例的空目录。

[本站贸易网络](<../../../07_贸易点/factory/飞艇总装与航修港/定义设计/02_贸易网络设计.md>) · [总体设计](<../../../07_贸易点/设计总览.md>) · [现行格式与经验资格](<../../../../02贸易点系统/03_资源表定义.md>)
