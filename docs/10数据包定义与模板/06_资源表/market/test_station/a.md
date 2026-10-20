# 测试贸易点 A · 实际物品交易表

> **已接入 · 2026-10-20 · 指令测试专用。** 本站出售 75 种、收购 74 种，与 B 站互补；两站覆盖本轮自然贸易设计的全部 149 种商品，不等于覆盖全部已注册或可运输物品。

资源 ID：`cargoverse:market/test_station/a`。

数据源：`data/cargoverse/trade_points/resource_tables/market/test_station/a.json`。

## 测试规则

- 按当前运输类别、物品 ID 排序整个商品清单后连续交替分组，A 取偶数索引，B 取奇数索引；默认运输属性物品按 general_supplies 排序。分类仅用于分组，不在报价中增加分类字段。
- 使用 schema 3；全部省略 components，仅交易默认完整变体，同站无同品买卖重叠。所有物品在恰好一站出售、另一站收购。
- 出售初始库存 **2048 件**、容量 **4096 件**、每日补货 **1024 件**，用于验证扣减与补货；收购 daily_limit 为 **0（不限）**。
- 本轮测试报价取设计目录中的最低出售价与最高收购价，便于测出往返价差；这是生成本次测试表的取值方法，不是全局价格，也不是运行时动态关联自然站。后续修改仍须同步测试 JSON 与本页。
- 收购经验取设计中对应物品的最大每件配置。**指令测试站作为目的地不具备自然生成身份，即使配置经验，A／B 往返仍不奖励许可证或繁荣度经验**；该配置可用于确认目的地自然生成身份校验没有被非零奖励绕过。
- 不改变制造、注册、货柜权限或自然生成设置。所有 60 款货柜仍由两站共用制造定义提供。
- 当前 14 种商品仍使用默认运输配置，详见[总体设计](../../../07_贸易点/设计总览.md)。测试表不擅自修订其质量和分类。

## 出售目录

以下每项 stock 均采用上述 2048／4096／1024 件设置。

| rule_id | 物品 | unit_price（VB／件） |
| --- | --- | ---: |
| `sell_create_tree_fertilizer` | 树木肥料 · `create:tree_fertilizer` | 10 |
| `sell_minecraft_kelp` | 海带 · `minecraft:kelp` | 2 |
| `sell_minecraft_wheat` | 小麦 · `minecraft:wheat` | 3 |
| `sell_aeronautics_end_stone_powder` | 末地石粉末 · `aeronautics:end_stone_powder` | 28 |
| `sell_create_super_glue` | 强力胶 · `create:super_glue` | 70 |
| `sell_minecraft_glowstone_dust` | 荧石粉 · `minecraft:glowstone_dust` | 12 |
| `sell_minecraft_slime_ball` | 黏液球 · `minecraft:slime_ball` | 10 |
| `sell_create_metal_girder` | 金属梁 · `create:metal_girder` | 22 |
| `sell_minecraft_glass` | 玻璃 · `minecraft:glass` | 8 |
| `sell_minecraft_iron_door` | 铁门 · `minecraft:iron_door` | 40 |
| `sell_minecraft_spruce_planks` | 云杉木板 · `minecraft:spruce_planks` | 3 |
| `sell_minecraft_white_wool` | 白色羊毛 · `minecraft:white_wool` | 6 |
| `sell_create_redstone_link` | 无线红石信号终端 · `create:redstone_link` | 95 |
| `sell_minecraft_redstone` | 红石粉 · `minecraft:redstone` | 8 |
| `sell_simulated_altitude_sensor` | 高度传感器 · `simulated:altitude_sensor` | 180 |
| `sell_create_blaze_cake` | 烈焰蛋糕 · `create:blaze_cake` | 100 |
| `sell_minecraft_coal` | 煤炭 · `minecraft:coal` | 7 |
| `sell_create_honeyed_apple` | 蜜渍苹果 · `create:honeyed_apple` | 15 |
| `sell_create_wheat_flour` | 小麦面粉 · `create:wheat_flour` | 6 |
| `sell_minecraft_baked_potato` | 烤马铃薯 · `minecraft:baked_potato` | 4 |
| `sell_minecraft_carrot` | 胡萝卜 · `minecraft:carrot` | 3 |
| `sell_minecraft_cooked_beef` | 牛排 · `minecraft:cooked_beef` | 12 |
| `sell_minecraft_dried_kelp` | 干海带 · `minecraft:dried_kelp` | 3 |
| `sell_minecraft_golden_carrot` | 金胡萝卜 · `minecraft:golden_carrot` | 28 |
| `sell_minecraft_porkchop` | 生猪排 · `minecraft:porkchop` | 6 |
| `sell_minecraft_salmon` | 生鲑鱼 · `minecraft:salmon` | 6 |
| `sell_create_cuckoo_clock` | 布谷鸟闹钟 · `create:cuckoo_clock` | 110 |
| `sell_minecraft_bone` | 骨头 · `minecraft:bone` | 3 |
| `sell_minecraft_compass` | 指南针 · `minecraft:compass` | 75 |
| `sell_minecraft_ender_pearl` | 末影珍珠 · `minecraft:ender_pearl` | 60 |
| `sell_minecraft_glass_bottle` | 玻璃瓶 · `minecraft:glass_bottle` | 3 |
| `sell_minecraft_item_frame` | 物品展示框 · `minecraft:item_frame` | 25 |
| `sell_minecraft_map` | 空地图 · `minecraft:map` | 40 |
| `sell_minecraft_music_disc_13` | 音乐唱片 · `minecraft:music_disc_13` | 300 |
| `sell_minecraft_painting` | 画 · `minecraft:painting` | 45 |
| `sell_minecraft_sponge` | 海绵 · `minecraft:sponge` | 100 |
| `sell_minecraft_torch` | 火把 · `minecraft:torch` | 3 |
| `sell_create_belt_connector` | 传送带 · `create:belt_connector` | 24 |
| `sell_create_filter` | 列表过滤器 · `create:filter` | 24 |
| `sell_create_fluid_tank` | 流体储罐 · `create:fluid_tank` | 70 |
| `sell_minecraft_barrel` | 木桶 · `minecraft:barrel` | 35 |
| `sell_create_mechanical_drill` | 动力钻头 · `create:mechanical_drill` | 190 |
| `sell_create_mechanical_mixer` | 动力搅拌器 · `create:mechanical_mixer` | 200 |
| `sell_create_mechanical_press` | 动力冲压机 · `create:mechanical_press` | 180 |
| `sell_create_mechanical_saw` | 动力锯 · `create:mechanical_saw` | 190 |
| `sell_create_cogwheel` | 齿轮 · `create:cogwheel` | 14 |
| `sell_create_precision_mechanism` | 精密构件 · `create:precision_mechanism` | 160 |
| `sell_simulated_gyroscopic_mechanism` | 陀螺仪构件 · `simulated:gyroscopic_mechanism` | 280 |
| `sell_create_brass_ingot` | 黄铜锭 · `create:brass_ingot` | 22 |
| `sell_create_cardboard` | 纸板 · `create:cardboard` | 4 |
| `sell_create_polished_rose_quartz` | 磨制玫瑰石英 · `create:polished_rose_quartz` | 26 |
| `sell_create_sturdy_sheet` | 坚固板 · `create:sturdy_sheet` | 70 |
| `sell_minecraft_brick` | 红砖 · `minecraft:brick` | 2 |
| `sell_minecraft_copper_ingot` | 铜锭 · `minecraft:copper_ingot` | 7 |
| `sell_minecraft_iron_ingot` | 铁锭 · `minecraft:iron_ingot` | 12 |
| `sell_minecraft_leather` | 皮革 · `minecraft:leather` | 10 |
| `sell_minecraft_stick` | 木棍 · `minecraft:stick` | 2 |
| `sell_aeronautics_pearlescent_levitite` | 珠光浮空水晶 · `aeronautics:pearlescent_levitite` | 120 |
| `sell_minecraft_amethyst_shard` | 紫水晶碎片 · `minecraft:amethyst_shard` | 10 |
| `sell_minecraft_calcite` | 方解石 · `minecraft:calcite` | 6 |
| `sell_minecraft_end_stone` | 末地石 · `minecraft:end_stone` | 8 |
| `sell_minecraft_gravel` | 沙砾 · `minecraft:gravel` | 1 |
| `sell_minecraft_oak_log` | 橡木原木 · `minecraft:oak_log` | 10 |
| `sell_minecraft_prismarine_crystals` | 海晶砂粒 · `minecraft:prismarine_crystals` | 20 |
| `sell_minecraft_quartz` | 下界石英 · `minecraft:quartz` | 10 |
| `sell_minecraft_raw_iron` | 粗铁 · `minecraft:raw_iron` | 7 |
| `sell_minecraft_spruce_log` | 云杉原木 · `minecraft:spruce_log` | 10 |
| `sell_create_goggles` | 工程师护目镜 · `create:goggles` | 90 |
| `sell_create_wrench` | 扳手 · `create:wrench` | 75 |
| `sell_minecraft_fishing_rod` | 钓鱼竿 · `minecraft:fishing_rod` | 24 |
| `sell_minecraft_iron_hoe` | 铁锄 · `minecraft:iron_hoe` | 60 |
| `sell_minecraft_shield` | 盾牌 · `minecraft:shield` | 75 |
| `sell_aeronautics_propeller_bearing` | 螺旋桨轴承 · `aeronautics:propeller_bearing` | 160 |
| `sell_aeronautics_wooden_propeller` | 木制螺旋桨 · `aeronautics:wooden_propeller` | 100 |
| `sell_simulated_rope_connector` | 绳索连接器 · `simulated:rope_connector` | 40 |

## 收购目录

以下每项 daily_limit 均为 0（不限）。经验配置不代表指令站实际获得奖励。

| rule_id | 物品 | unit_price（VB／件） | 许可证经验／件 | 繁荣度经验／件 |
| --- | --- | ---: | ---: | ---: |
| `buy_minecraft_bone_meal` | 骨粉 · `minecraft:bone_meal` | 5 | 1 | 1 |
| `buy_minecraft_sugar_cane` | 甘蔗 · `minecraft:sugar_cane` | 4 | 1 | 1 |
| `buy_minecraft_wheat_seeds` | 小麦种子 · `minecraft:wheat_seeds` | 3 | 1 | 1 |
| `buy_create_cinder_flour` | 余烬面粉 · `create:cinder_flour` | 10 | 3 | 3 |
| `buy_minecraft_blaze_powder` | 烈焰粉 · `minecraft:blaze_powder` | 36 | 4 | 3 |
| `buy_minecraft_gunpowder` | 火药 · `minecraft:gunpowder` | 20 | 4 | 3 |
| `buy_create_andesite_casing` | 安山机壳 · `create:andesite_casing` | 40 | 4 | 3 |
| `buy_minecraft_cracked_stone_bricks` | 裂纹石砖 · `minecraft:cracked_stone_bricks` | 5 | 1 | 1 |
| `buy_minecraft_iron_bars` | 铁栏杆 · `minecraft:iron_bars` | 16 | 3 | 3 |
| `buy_minecraft_oak_planks` | 橡木木板 · `minecraft:oak_planks` | 4 | 1 | 1 |
| `buy_minecraft_stone_bricks` | 石砖 · `minecraft:stone_bricks` | 5 | 1 | 1 |
| `buy_create_electron_tube` | 电子管 · `create:electron_tube` | 60 | 5 | 4 |
| `buy_minecraft_observer` | 侦测器 · `minecraft:observer` | 85 | 4 | 3 |
| `buy_minecraft_redstone_lamp` | 红石灯 · `minecraft:redstone_lamp` | 55 | 4 | 3 |
| `buy_simulated_laser_sensor` | 激光传感器 · `simulated:laser_sensor` | 260 | 6 | 5 |
| `buy_minecraft_charcoal` | 木炭 · `minecraft:charcoal` | 8 | 2 | 2 |
| `buy_create_builders_tea` | 建筑工茶饮 · `create:builders_tea` | 18 | 3 | 2 |
| `buy_create_sweet_roll` | 甜甜卷 · `create:sweet_roll` | 20 | 3 | 2 |
| `buy_minecraft_apple` | 苹果 · `minecraft:apple` | 5 | 1 | 1 |
| `buy_minecraft_bread` | 面包 · `minecraft:bread` | 6 | 2 | 2 |
| `buy_minecraft_cod` | 生鳕鱼 · `minecraft:cod` | 6 | 3 | 3 |
| `buy_minecraft_cookie` | 曲奇 · `minecraft:cookie` | 4 | 1 | 1 |
| `buy_minecraft_egg` | 鸡蛋 · `minecraft:egg` | 3 | 1 | 1 |
| `buy_minecraft_honey_bottle` | 蜂蜜瓶 · `minecraft:honey_bottle` | 16 | 3 | 2 |
| `buy_minecraft_potato` | 马铃薯 · `minecraft:potato` | 3 | 1 | 1 |
| `buy_minecraft_sugar` | 糖 · `minecraft:sugar` | 5 | 1 | 1 |
| `buy_minecraft_arrow` | 箭 · `minecraft:arrow` | 8 | 3 | 3 |
| `buy_minecraft_book` | 书 · `minecraft:book` | 20 | 3 | 3 |
| `buy_minecraft_echo_shard` | 回响碎片 · `minecraft:echo_shard` | 280 | 8 | 6 |
| `buy_minecraft_flower_pot` | 花盆 · `minecraft:flower_pot` | 16 | 3 | 2 |
| `buy_minecraft_ink_sac` | 墨囊 · `minecraft:ink_sac` | 8 | 2 | 2 |
| `buy_minecraft_lantern` | 灯笼 · `minecraft:lantern` | 18 | 3 | 2 |
| `buy_minecraft_mossy_cobblestone` | 苔石 · `minecraft:mossy_cobblestone` | 5 | 1 | 1 |
| `buy_minecraft_nautilus_shell` | 鹦鹉螺壳 · `minecraft:nautilus_shell` | 140 | 6 | 4 |
| `buy_minecraft_rotten_flesh` | 腐肉 · `minecraft:rotten_flesh` | 2 | 0 | 1 |
| `buy_minecraft_spyglass` | 望远镜 · `minecraft:spyglass` | 100 | 5 | 4 |
| `buy_create_andesite_funnel` | 安山漏斗 · `create:andesite_funnel` | 32 | 4 | 3 |
| `buy_create_chute` | 溜槽 · `create:chute` | 25 | 3 | 3 |
| `buy_create_fluid_pipe` | 流体管道 · `create:fluid_pipe` | 12 | 3 | 3 |
| `buy_create_item_vault` | 物品保险库 · `create:item_vault` | 100 | 4 | 3 |
| `buy_create_crushing_wheel` | 粉碎轮 · `create:crushing_wheel` | 270 | 8 | 6 |
| `buy_create_mechanical_harvester` | 动力收割机 · `create:mechanical_harvester` | 230 | 6 | 5 |
| `buy_create_mechanical_plough` | 动力犁 · `create:mechanical_plough` | 170 | 6 | 5 |
| `buy_create_mechanical_pump` | 动力泵 · `create:mechanical_pump` | 110 | 5 | 4 |
| `buy_create_rope_pulley` | 绳索滑轮 · `create:rope_pulley` | 170 | 6 | 4 |
| `buy_create_gearbox` | 十字齿轮箱 · `create:gearbox` | 75 | 4 | 4 |
| `buy_create_shaft` | 传动杆 · `create:shaft` | 12 | 3 | 3 |
| `buy_create_andesite_alloy` | 安山合金 · `create:andesite_alloy` | 16 | 3 | 3 |
| `buy_create_brass_sheet` | 黄铜板 · `create:brass_sheet` | 34 | 4 | 3 |
| `buy_create_iron_sheet` | 铁板 · `create:iron_sheet` | 20 | 4 | 3 |
| `buy_create_powdered_obsidian` | 黑曜石粉末 · `create:powdered_obsidian` | 15 | 4 | 3 |
| `buy_create_zinc_ingot` | 锌锭 · `create:zinc_ingot` | 15 | 3 | 3 |
| `buy_minecraft_clay_ball` | 黏土球 · `minecraft:clay_ball` | 4 | 1 | 1 |
| `buy_minecraft_feather` | 羽毛 · `minecraft:feather` | 4 | 1 | 1 |
| `buy_minecraft_iron_nugget` | 铁粒 · `minecraft:iron_nugget` | 2 | 0 | 1 |
| `buy_minecraft_paper` | 纸 · `minecraft:paper` | 6 | 2 | 2 |
| `buy_aeronautics_levitite` | 浮空水晶 · `aeronautics:levitite` | 48 | 5 | 4 |
| `buy_create_raw_zinc` | 粗锌 · `create:raw_zinc` | 9 | 2 | 2 |
| `buy_minecraft_andesite` | 安山岩 · `minecraft:andesite` | 7 | 1 | 1 |
| `buy_minecraft_cobblestone` | 圆石 · `minecraft:cobblestone` | 2 | 1 | 1 |
| `buy_minecraft_flint` | 燧石 · `minecraft:flint` | 3 | 0 | 1 |
| `buy_minecraft_netherrack` | 下界岩 · `minecraft:netherrack` | 2 | 0 | 1 |
| `buy_minecraft_obsidian` | 黑曜石 · `minecraft:obsidian` | 16 | 3 | 3 |
| `buy_minecraft_prismarine_shard` | 海晶碎片 · `minecraft:prismarine_shard` | 19 | 3 | 3 |
| `buy_minecraft_raw_copper` | 粗铜 · `minecraft:raw_copper` | 6 | 1 | 1 |
| `buy_minecraft_sand` | 沙子 · `minecraft:sand` | 4 | 1 | 1 |
| `buy_create_copper_backtank` | 铜背罐 · `create:copper_backtank` | 300 | 6 | 5 |
| `buy_create_sand_paper` | 砂纸 · `create:sand_paper` | 6 | 1 | 1 |
| `buy_minecraft_brush` | 刷子 · `minecraft:brush` | 45 | 4 | 3 |
| `buy_minecraft_iron_axe` | 铁斧 · `minecraft:iron_axe` | 115 | 5 | 4 |
| `buy_minecraft_iron_pickaxe` | 铁镐 · `minecraft:iron_pickaxe` | 115 | 5 | 4 |
| `buy_aeronautics_andesite_propeller` | 安山螺旋桨 · `aeronautics:andesite_propeller` | 220 | 6 | 5 |
| `buy_aeronautics_white_envelope` | 气球蒙皮 · `aeronautics:white_envelope` | 38 | 4 | 3 |
| `buy_simulated_docking_connector` | 对接连接器 · `simulated:docking_connector` | 195 | 6 | 4 |

## 使用新实例验证

报价随实例保存快照，普通 reload 不替换旧站目录。更新资源并重载后，使用 `/place structure cargoverse:trade_point/market/test_station/a` 在新位置创建站点；已有空表站点不会自动补齐。两站指令、注册及许可证准备见各自生成规则页。

[返回资源表](../../README.md) · [现行报价与经验资格](../../../../02贸易点系统/03_资源表定义.md)
