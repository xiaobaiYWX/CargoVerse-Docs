# 云港民生集配站资源表

> **已接入 · 2026-10-06：** 本页为本站当前出售库存、日补、逐商品报价与每日收购限额的唯一维护表。关联站点：[S01 云港民生集配站](<../../../07_贸易点/market/云港民生集配站/00_总体说明.md>)。新增目录仅自动用于新经济实例；已有实例保存资源目录快照。

| 项目 | 内容 |
| --- | --- |
| 资源 ID | `cargoverse:market/sky_station/civic_distribution` |
| 目标 JSON | `src/main/resources/data/cargoverse/trade_points/resource_tables/market/sky_station/civic_distribution.json` |
| schema_version | 1 |
| 匹配方式 | 每行独立规则；selector.match_mode 为 all；selector.tags 为该行唯一标签的单元素数组 |
| 数量单位 | t 是货物数量；完整贸易日为 24000 ticks |
| 报价方式 | 每条规则设置 price_multiplier；无站点总倍率 |

## 出售 sales

全部 create_inventory: true；初始量、容量、日补对应 initial_amount、capacity_per_good、daily_restock_per_good。价格倍率作用于基础价值，整笔结算后取整。

| 规则 ID | 货物 | 标签 | 初始量 | 容量 | 日补 | 价格倍率 |
| --- | --- | --- | ---: | ---: | ---: | ---: |
| `shelf_stable_rations` | [长效口粮](<../../../01_CargoGood/general_supplies/shelf_stable_rations.md>) | `ingredient.general_supplies.shelf_stable_rations` | 800 | 1600 | 400 | 0.9 |
| `durable_workwear` | [耐用工装](<../../../01_CargoGood/general_supplies/durable_workwear.md>) | `ingredient.general_supplies.durable_workwear` | 200 | 400 | 100 | 0.9 |
| `civilian_lighting_kits` | [民用照明器具](<../../../01_CargoGood/general_supplies/civilian_lighting_kits.md>) | `ingredient.general_supplies.civilian_lighting_kits` | 200 | 400 | 100 | 0.9 |
| `mining_hand_tools` | [矿务手工具](<../../../01_CargoGood/tools_equipment/mining_hand_tools.md>) | `ingredient.tools_equipment.mining_hand_tools` | 100 | 200 | 50 | 1 |

## 收购 acquisitions

收购不建库存。true 写入 daily_limit_enabled: true 与 daily_limit_per_good；false 不写限额字段，表示不限额。额度由同一站点实例所有玩家共享，按贸易日重置、不累积；price_multiplier 对该商品独立生效。

| 规则 ID | 货物 | 标签 | 每日限额开关 | 每种货物每日上限（t） | 价格倍率 |
| --- | --- | --- | --- | ---: | ---: |
| `prefab_habitat_pods` | [预制居住舱](<../../../01_CargoGood/prefab_structure/prefab_habitat_pods.md>) | `ingredient.prefab_structure.prefab_habitat_pods` | false | 不限 | 1.1 |
| `bagged_wheat` | [袋装麦粒](<../../../01_CargoGood/agriculture/bagged_wheat.md>) | `ingredient.agriculture.bagged_wheat` | false | 不限 | 1.1 |
| `industrial_cotton_cloth` | [工业棉布](<../../../01_CargoGood/processed_resource/industrial_cotton_cloth.md>) | `ingredient.processed_resource.industrial_cotton_cloth` | false | 不限 | 1.1 |
| `biomass_briquettes` | [压制生物燃料](<../../../01_CargoGood/energy_fuel/biomass_briquettes.md>) | `ingredient.energy_fuel.biomass_briquettes` | false | 不限 | 1.1 |
| `glowstone_luminant` | [萤石发光粉](<../../../01_CargoGood/special_resource/glowstone_luminant.md>) | `ingredient.special_resource.glowstone_luminant` | false | 不限 | 1.1 |
| `potable_water_crates` | [净水补给箱](<../../../01_CargoGood/general_supplies/potable_water_crates.md>) | `ingredient.general_supplies.potable_water_crates` | false | 不限 | 1 |
| `first_aid_medicines` | [急救药剂](<../../../01_CargoGood/medical_supply/first_aid_medicines.md>) | `ingredient.medical_supply.first_aid_medicines` | false | 不限 | 1 |
| `kiln_dried_planks` | [烘干木板](<../../../01_CargoGood/processed_resource/kiln_dried_planks.md>) | `ingredient.processed_resource.kiln_dried_planks` | false | 不限 | 1 |
| `standard_container_couplings` | [标准货柜接口总成](<../../../01_CargoGood/mechanical_parts/standard_container_couplings.md>) | `ingredient.mechanical_parts.standard_container_couplings` | true | 100 | 1.05 |
| `industrial_energy_cells` | [工业蓄能电池](<../../../01_CargoGood/energy_fuel/industrial_energy_cells.md>) | `ingredient.energy_fuel.industrial_energy_cells` | true | 100 | 1.05 |
| `sorted_packaging_scrap` | [分拣包装废料](<../../../01_CargoGood/processed_resource/sorted_packaging_scrap.md>) | `ingredient.processed_resource.sorted_packaging_scrap` | false | 不限 | 1 |

## 业务用途与维护

保持日用品主供，承接麦粒、棉布与生活物资；增加劳动工具和包装回收，服务周边工厂、乡间和居民点。

补货与收购独立运行，不依赖材料转化或邻站库存。5 / 5 / 0 的来源是每实例一次性批次，重复发现同型站会带来另一批库存；普通回收料不会刷新这些批次。

[本站网络职责与线路](<../../../07_贸易点/market/云港民生集配站/定义设计/02_贸易网络设计.md>) · [正式资源表目录](<../../README.md>) · [资源表目录](<../../README.md>)
