# 边境驻防补给港资源表

> **已接入 · 2026-10-06：** 本页为本站当前出售库存、日补、逐商品报价与每日收购限额的唯一维护表。关联站点：[B03 边境驻防补给港](<../../../07_贸易点/market/边境驻防补给港/00_总体说明.md>)。新增目录仅自动用于新经济实例；已有实例保存资源目录快照。

| 项目 | 内容 |
| --- | --- |
| 资源 ID | `cargoverse:market/sky_station/frontier_garrison` |
| 目标 JSON | `src/main/resources/data/cargoverse/trade_points/resource_tables/market/sky_station/frontier_garrison.json` |
| schema_version | 1 |
| 匹配方式 | 每行独立规则；selector.match_mode 为 all；selector.tags 为该行唯一标签的单元素数组 |
| 数量单位 | t 是货物数量；完整贸易日为 24000 ticks |
| 报价方式 | 每条规则设置 price_multiplier；无站点总倍率 |

## 出售 sales

全部 create_inventory: true；初始量、容量、日补对应 initial_amount、capacity_per_good、daily_restock_per_good。价格倍率作用于基础价值，整笔结算后取整。

| 规则 ID | 货物 | 标签 | 初始量 | 容量 | 日补 | 价格倍率 |
| --- | --- | --- | ---: | ---: | ---: | ---: |
| `potable_water_crates` | [净水补给箱](<../../../01_CargoGood/general_supplies/potable_water_crates.md>) | `ingredient.general_supplies.potable_water_crates` | 200 | 400 | 100 | 0.95 |
| `durable_workwear` | [耐用工装](<../../../01_CargoGood/general_supplies/durable_workwear.md>) | `ingredient.general_supplies.durable_workwear` | 100 | 200 | 50 | 0.95 |
| `industrial_energy_cells` | [工业蓄能电池](<../../../01_CargoGood/energy_fuel/industrial_energy_cells.md>) | `ingredient.energy_fuel.industrial_energy_cells` | 100 | 200 | 50 | 1 |
| `sorted_packaging_scrap` | [分拣包装废料](<../../../01_CargoGood/processed_resource/sorted_packaging_scrap.md>) | `ingredient.processed_resource.sorted_packaging_scrap` | 100 | 200 | 50 | 0.5 |
| `dried_organic_residue` | [干化有机废料](<../../../01_CargoGood/processed_resource/dried_organic_residue.md>) | `ingredient.processed_resource.dried_organic_residue` | 80 | 160 | 40 | 0.5 |
| `scrapped_electronic_components` | [报废电子组件](<../../../01_CargoGood/mechanical_parts/scrapped_electronic_components.md>) | `ingredient.mechanical_parts.scrapped_electronic_components` | 40 | 80 | 20 | 0.5 |

## 收购 acquisitions

收购不建库存。true 写入 daily_limit_enabled: true 与 daily_limit_per_good；false 不写限额字段，表示不限额。额度由同一站点实例所有玩家共享，按贸易日重置、不累积；price_multiplier 对该商品独立生效。

| 规则 ID | 货物 | 标签 | 每日限额开关 | 每种货物每日上限（t） | 价格倍率 |
| --- | --- | --- | --- | ---: | ---: |
| `shelf_stable_rations` | [长效口粮](<../../../01_CargoGood/general_supplies/shelf_stable_rations.md>) | `ingredient.general_supplies.shelf_stable_rations` | false | 不限 | 1 |
| `first_aid_medicines` | [急救药剂](<../../../01_CargoGood/medical_supply/first_aid_medicines.md>) | `ingredient.medical_supply.first_aid_medicines` | false | 不限 | 1 |
| `sterile_dressings` | [无菌敷料](<../../../01_CargoGood/medical_supply/sterile_dressings.md>) | `ingredient.medical_supply.sterile_dressings` | false | 不限 | 1.1 |
| `vaccine_preparations` | [疫苗制剂](<../../../01_CargoGood/medical_supply/vaccine_preparations.md>) | `ingredient.medical_supply.vaccine_preparations` | false | 不限 | 1.15 |
| `garrison_ammunition_crates` | [驻防弹药箱](<../../../01_CargoGood/weapon_armor/garrison_ammunition_crates.md>) | `ingredient.weapon_armor.garrison_ammunition_crates` | false | 不限 | 1.1 |
| `guard_armor` | [护卫护甲](<../../../01_CargoGood/weapon_armor/guard_armor.md>) | `ingredient.weapon_armor.guard_armor` | false | 不限 | 1.1 |
| `service_crossbows` | [制式弩机](<../../../01_CargoGood/weapon_armor/service_crossbows.md>) | `ingredient.weapon_armor.service_crossbows` | false | 不限 | 1.1 |
| `ship_defense_gun_sets` | [舰载防御炮组](<../../../01_CargoGood/weapon_armor/ship_defense_gun_sets.md>) | `ingredient.weapon_armor.ship_defense_gun_sets` | false | 不限 | 1.15 |
| `perimeter_security_systems` | [周界警戒系统](<../../../01_CargoGood/electronics/perimeter_security_systems.md>) | `ingredient.electronics.perimeter_security_systems` | false | 不限 | 1.1 |
| `prefab_defensive_positions` | [预制防御工事](<../../../01_CargoGood/prefab_structure/prefab_defensive_positions.md>) | `ingredient.prefab_structure.prefab_defensive_positions` | false | 不限 | 1.1 |
| `light_patrol_boats` | [轻型巡逻艇](<../../../01_CargoGood/vehicle/light_patrol_boats.md>) | `ingredient.vehicle.light_patrol_boats` | false | 不限 | 1.1 |
| `civilian_lighting_kits` | [民用照明器具](<../../../01_CargoGood/general_supplies/civilian_lighting_kits.md>) | `ingredient.general_supplies.civilian_lighting_kits` | false | 不限 | 1 |
| `kiln_dried_planks` | [烘干木板](<../../../01_CargoGood/processed_resource/kiln_dried_planks.md>) | `ingredient.processed_resource.kiln_dried_planks` | false | 不限 | 1 |
| `aviation_fuel_drums` | [桶装航空燃油](<../../../01_CargoGood/energy_fuel/aviation_fuel_drums.md>) | `ingredient.energy_fuel.aviation_fuel_drums` | false | 不限 | 1.05 |
| `aviation_maintenance_toolkits` | [航修工具箱](<../../../01_CargoGood/tools_equipment/aviation_maintenance_toolkits.md>) | `ingredient.tools_equipment.aviation_maintenance_toolkits` | false | 不限 | 1.05 |
| `standard_container_couplings` | [标准货柜接口总成](<../../../01_CargoGood/mechanical_parts/standard_container_couplings.md>) | `ingredient.mechanical_parts.standard_container_couplings` | true | 100 | 1.05 |
| `structural_steel_ingots` | [结构钢锭](<../../../01_CargoGood/refined_resource/structural_steel_ingots.md>) | `ingredient.refined_resource.structural_steel_ingots` | true | 100 | 1.05 |
| `containerized_water_stations` | [集装式净水站](<../../../01_CargoGood/prefab_structure/containerized_water_stations.md>) | `ingredient.prefab_structure.containerized_water_stations` | true | 100 | 1.05 |

## 业务用途与维护

保留完整军需消费，新增净水、通用工装与储能电池的后勤经销；采购修缮钢材和驻点净水设施，连接丘陵重工与冻河处理站。继续收购口粮、药品和武器，不将军用品改为倒卖目录。

补货与收购独立运行，不依赖材料转化或邻站库存。5 / 5 / 0 的来源是每实例一次性批次，重复发现同型站会带来另一批库存；普通回收料不会刷新这些批次。

[本站网络职责与线路](<../../../07_贸易点/market/边境驻防补给港/定义设计/02_贸易网络设计.md>) · [正式资源表目录](<../../README.md>) · [资源表目录](<../../README.md>)
