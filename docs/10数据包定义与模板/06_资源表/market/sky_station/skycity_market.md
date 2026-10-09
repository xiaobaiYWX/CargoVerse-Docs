# 天空城综合市场资源表

> **已接入 · 2026-10-06：** 本页为本站当前出售库存、日补、逐商品报价与每日收购限额的唯一维护表。关联站点：[S03 天空城综合市场](<../../../07_贸易点/market/天空城综合市场/00_总体说明.md>)。新增目录仅自动用于新经济实例；已有实例保存资源目录快照。

| 项目 | 内容 |
| --- | --- |
| 资源 ID | `cargoverse:market/sky_station/skycity_market` |
| 目标 JSON | `src/main/resources/data/cargoverse/trade_points/resource_tables/market/sky_station/skycity_market.json` |
| schema_version | 1 |
| 匹配方式 | 每行独立规则；selector.match_mode 为 all；selector.tags 为该行唯一标签的单元素数组 |
| 数量单位 | t 是货物数量；完整贸易日为 24000 ticks |
| 报价方式 | 每条规则设置 price_multiplier；无站点总倍率 |

## 出售 sales

全部 create_inventory: true；初始量、容量、日补对应 initial_amount、capacity_per_good、daily_restock_per_good。价格倍率作用于基础价值，整笔结算后取整。

| 规则 ID | 货物 | 标签 | 初始量 | 容量 | 日补 | 价格倍率 |
| --- | --- | --- | ---: | ---: | ---: | ---: |
| `shelf_stable_rations` | [长效口粮](<../../../01_CargoGood/general_supplies/shelf_stable_rations.md>) | `ingredient.general_supplies.shelf_stable_rations` | 300 | 600 | 150 | 0.95 |
| `first_aid_medicines` | [急救药剂](<../../../01_CargoGood/medical_supply/first_aid_medicines.md>) | `ingredient.medical_supply.first_aid_medicines` | 100 | 200 | 50 | 0.95 |
| `kiln_dried_planks` | [烘干木板](<../../../01_CargoGood/processed_resource/kiln_dried_planks.md>) | `ingredient.processed_resource.kiln_dried_planks` | 200 | 400 | 100 | 0.95 |
| `sorted_packaging_scrap` | [分拣包装废料](<../../../01_CargoGood/processed_resource/sorted_packaging_scrap.md>) | `ingredient.processed_resource.sorted_packaging_scrap` | 100 | 200 | 50 | 0.5 |
| `dried_organic_residue` | [干化有机废料](<../../../01_CargoGood/processed_resource/dried_organic_residue.md>) | `ingredient.processed_resource.dried_organic_residue` | 80 | 160 | 40 | 0.5 |

## 收购 acquisitions

收购不建库存。true 写入 daily_limit_enabled: true 与 daily_limit_per_good；false 不写限额字段，表示不限额。额度由同一站点实例所有玩家共享，按贸易日重置、不累积；price_multiplier 对该商品独立生效。

| 规则 ID | 货物 | 标签 | 每日限额开关 | 每种货物每日上限（t） | 价格倍率 |
| --- | --- | --- | --- | ---: | ---: |
| `civilian_lighting_kits` | [民用照明器具](<../../../01_CargoGood/general_supplies/civilian_lighting_kits.md>) | `ingredient.general_supplies.civilian_lighting_kits` | false | 不限 | 1 |
| `greenhouse_fruit` | [温室鲜果](<../../../01_CargoGood/agriculture/greenhouse_fruit.md>) | `ingredient.agriculture.greenhouse_fruit` | false | 不限 | 1.1 |
| `hydroponic_leafy_greens` | [水培叶菜](<../../../01_CargoGood/agriculture/hydroponic_leafy_greens.md>) | `ingredient.agriculture.hydroponic_leafy_greens` | false | 不限 | 1.1 |
| `chilled_river_fish` | [冰鲜河鱼](<../../../01_CargoGood/aquatic/chilled_river_fish.md>) | `ingredient.aquatic.chilled_river_fish` | false | 不限 | 1.1 |
| `chilled_sea_shrimp` | [冰鲜海虾](<../../../01_CargoGood/aquatic/chilled_sea_shrimp.md>) | `ingredient.aquatic.chilled_sea_shrimp` | false | 不限 | 1.1 |
| `fresh_kelp` | [鲜采食用海带](<../../../01_CargoGood/aquatic/fresh_kelp.md>) | `ingredient.aquatic.fresh_kelp` | false | 不限 | 1.1 |
| `purified_shellfish` | [净化鲜贝](<../../../01_CargoGood/aquatic/purified_shellfish.md>) | `ingredient.aquatic.purified_shellfish` | false | 不限 | 1.1 |
| `aged_spirits` | [陈酿佳酿](<../../../01_CargoGood/valuables/aged_spirits.md>) | `ingredient.valuables.aged_spirits` | false | 不限 | 1.15 |
| `artisan_jewelry` | [精工饰品](<../../../01_CargoGood/valuables/artisan_jewelry.md>) | `ingredient.valuables.artisan_jewelry` | true | 200 | 1.15 |
| `restored_old_world_art` | [修复旧世艺术品](<../../../01_CargoGood/valuables/restored_old_world_art.md>) | `ingredient.valuables.restored_old_world_art` | true | 5 | 1.2 |
| `potable_water_crates` | [净水补给箱](<../../../01_CargoGood/general_supplies/potable_water_crates.md>) | `ingredient.general_supplies.potable_water_crates` | false | 不限 | 1 |
| `durable_workwear` | [耐用工装](<../../../01_CargoGood/general_supplies/durable_workwear.md>) | `ingredient.general_supplies.durable_workwear` | false | 不限 | 1 |
| `industrial_energy_cells` | [工业蓄能电池](<../../../01_CargoGood/energy_fuel/industrial_energy_cells.md>) | `ingredient.energy_fuel.industrial_energy_cells` | true | 100 | 1.05 |
| `industrial_cotton_cloth` | [工业棉布](<../../../01_CargoGood/processed_resource/industrial_cotton_cloth.md>) | `ingredient.processed_resource.industrial_cotton_cloth` | false | 不限 | 1.05 |

## 业务用途与维护

保持鲜货与珍品消费终点，新增常温口粮、急救与维修木板集散；包装与有机残料提供低价值回程。本站继续收购照明，不同时出售照明。

补货与收购独立运行，不依赖材料转化或邻站库存。5 / 5 / 0 的来源是每实例一次性批次，重复发现同型站会带来另一批库存；普通回收料不会刷新这些批次。

[本站网络职责与线路](<../../../07_贸易点/market/天空城综合市场/定义设计/02_贸易网络设计.md>) · [正式资源表目录](<../../README.md>) · [资源表目录](<../../README.md>)
