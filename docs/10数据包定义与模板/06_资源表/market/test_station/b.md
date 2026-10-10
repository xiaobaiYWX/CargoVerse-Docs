# 测试贸易点 B · 资源表

仅供指令测试，不计入正式贸易网络。定义 ID：`cargoverse:market/test_station/b`。数量单位 t 是数量符号；每贸易日 24000 ticks。

## 出售 sales

50 项；每项均填写有限 `inventory`：初始 10000、容量 20000、日补 10000，`price_multiplier=0.9`。

| 货物 | CargoGood ID |
| --- | --- |
| 纤维棉包 | `cargoverse:agriculture/cotton_bales` |
| 水培叶菜 | `cargoverse:agriculture/hydroponic_leafy_greens` |
| 记忆回声介质 | `cargoverse:anomalous_cargo/memory_echo_media` |
| 时滞晶簇 | `cargoverse:anomalous_cargo/temporal_lag_clusters` |
| 冰鲜海虾 | `cargoverse:aquatic/chilled_sea_shrimp` |
| 净化鲜贝 | `cargoverse:aquatic/purified_shellfish` |
| 培养基原液 | `cargoverse:chemical_material/culture_medium` |
| 工业润滑油 | `cargoverse:chemical_material/industrial_lubricant` |
| 保温板材 | `cargoverse:construction_material/insulation_panels` |
| 钢化玻璃板 | `cargoverse:construction_material/tempered_glass_panels` |
| 通信中继器 | `cargoverse:electronics/communication_relays` |
| 工业传感器 | `cargoverse:electronics/industrial_sensors` |
| 前文明导航核心 | `cargoverse:electronics/precursor_navigation_cores` |
| 压制生物燃料 | `cargoverse:energy_fuel/biomass_briquettes` |
| 工业蓄能电池 | `cargoverse:energy_fuel/industrial_energy_cells` |
| 耐用工装 | `cargoverse:general_supplies/durable_workwear` |
| 长效口粮 | `cargoverse:general_supplies/shelf_stable_rations` |
| 重金属滤渣 | `cargoverse:hazardous_material/heavy_metal_filter_cake` |
| 失效同位素源 | `cargoverse:hazardous_material/spent_isotope_sources` |
| 育成绵羊 | `cargoverse:livestock/breeding_sheep` |
| 授粉蜂群 | `cargoverse:livestock/pollinator_colonies` |
| 工业水泵机组 | `cargoverse:machinery/industrial_pump_sets` |
| 精密机床 | `cargoverse:machinery/precision_machine_tools` |
| 精密轴承 | `cargoverse:mechanical_parts/precision_bearings` |
| 报废电子组件 | `cargoverse:mechanical_parts/scrapped_electronic_components` |
| 标准传动齿轮 | `cargoverse:mechanical_parts/transmission_gears` |
| 再生培养液 | `cargoverse:medical_supply/regenerative_culture_fluid` |
| 疫苗制剂 | `cargoverse:medical_supply/vaccine_preparations` |
| 循环水培舱 | `cargoverse:prefab_structure/closed_loop_hydroponic_modules` |
| 温室骨架模块 | `cargoverse:prefab_structure/greenhouse_frame_modules` |
| 预制居住舱 | `cargoverse:prefab_structure/prefab_habitat_pods` |
| 干化有机废料 | `cargoverse:processed_resource/dried_organic_residue` |
| 铁精矿 | `cargoverse:processed_resource/iron_concentrate` |
| 可回收金属废料 | `cargoverse:processed_resource/recyclable_metal_scrap` |
| 含铜原矿 | `cargoverse:raw_resource/copper_ore` |
| 石英原砂 | `cargoverse:raw_resource/quartz_sand` |
| 光学玻璃坯 | `cargoverse:refined_resource/optical_glass_blanks` |
| 结构钢锭 | `cargoverse:refined_resource/structural_steel_ingots` |
| 遗迹材料切片 | `cargoverse:research_sample/ruin_material_sections` |
| 高空微生物样本 | `cargoverse:research_sample/upper_air_microbe_samples` |
| 萤石发光粉 | `cargoverse:special_resource/glowstone_luminant` |
| 旧世合金残片 | `cargoverse:special_resource/old_world_alloy_fragments` |
| 野外采样器 | `cargoverse:tools_equipment/field_sampling_kits` |
| 精密测量仪 | `cargoverse:tools_equipment/precision_measuring_instruments` |
| 精工饰品 | `cargoverse:valuables/artisan_jewelry` |
| 修复旧世艺术品 | `cargoverse:valuables/restored_old_world_art` |
| 矿用运输车 | `cargoverse:vehicle/mining_haulers` |
| 测绘无人机 | `cargoverse:vehicle/survey_drones` |
| 护卫护甲 | `cargoverse:weapon_armor/guard_armor` |
| 舰载防御炮组 | `cargoverse:weapon_armor/ship_defense_gun_sets` |

## 收购 acquisitions

54 项；无库存、无每日限额，price_multiplier=1.1。每项直接引用对应 CargoGood ID。

| 货物 | CargoGood ID |
| --- | --- |
| 袋装麦粒 | `cargoverse:agriculture/bagged_wheat` |
| 温室鲜果 | `cargoverse:agriculture/greenhouse_fruit` |
| 密封种粮 | `cargoverse:agriculture/sealed_seed_grain` |
| 桶装虚空混合物 | `cargoverse:anomalous_cargo/contained_void_mixture` |
| 非欧几何构件 | `cargoverse:anomalous_cargo/non_euclidean_components` |
| 冰鲜河鱼 | `cargoverse:aquatic/chilled_river_fish` |
| 鲜采食用海带 | `cargoverse:aquatic/fresh_kelp` |
| 复合肥料 | `cargoverse:chemical_material/compound_fertilizer` |
| 水培营养液 | `cargoverse:chemical_material/hydroponic_nutrient_solution` |
| 密封树脂 | `cargoverse:chemical_material/sealing_resin` |
| 袋装水泥 | `cargoverse:construction_material/bagged_cement` |
| 标准钢梁 | `cargoverse:construction_material/structural_steel_beams` |
| 航电控制器 | `cargoverse:electronics/avionics_controllers` |
| 封装数据存储阵列 | `cargoverse:electronics/data_storage_arrays` |
| 周界警戒系统 | `cargoverse:electronics/perimeter_security_systems` |
| 桶装航空燃油 | `cargoverse:energy_fuel/aviation_fuel_drums` |
| 煤焦燃料 | `cargoverse:energy_fuel/coke_fuel` |
| 民用照明器具 | `cargoverse:general_supplies/civilian_lighting_kits` |
| 净水补给箱 | `cargoverse:general_supplies/potable_water_crates` |
| 污染吸附剂 | `cargoverse:hazardous_material/contaminated_adsorbent` |
| 废酸回收桶 | `cargoverse:hazardous_material/spent_acid_drums` |
| 家禽种群 | `cargoverse:livestock/breeding_poultry` |
| 养殖鱼苗 | `cargoverse:livestock/hatchery_fry` |
| 自动装卸机 | `cargoverse:machinery/automated_cargo_handlers` |
| 矿石破碎机 | `cargoverse:machinery/ore_crushers` |
| 液压执行缸 | `cargoverse:mechanical_parts/hydraulic_cylinders` |
| 推进器叶轮 | `cargoverse:mechanical_parts/propulsion_impellers` |
| 标准货柜接口总成 | `cargoverse:mechanical_parts/standard_container_couplings` |
| 急救药剂 | `cargoverse:medical_supply/first_aid_medicines` |
| 无菌敷料 | `cargoverse:medical_supply/sterile_dressings` |
| 飞艇龙骨模块 | `cargoverse:prefab_structure/airship_keel_modules` |
| 集装式净水站 | `cargoverse:prefab_structure/containerized_water_stations` |
| 预制防御工事 | `cargoverse:prefab_structure/prefab_defensive_positions` |
| 铜精矿 | `cargoverse:processed_resource/copper_concentrate` |
| 工业棉布 | `cargoverse:processed_resource/industrial_cotton_cloth` |
| 烘干木板 | `cargoverse:processed_resource/kiln_dried_planks` |
| 分拣包装废料 | `cargoverse:processed_resource/sorted_packaging_scrap` |
| 针叶原木 | `cargoverse:raw_resource/conifer_logs` |
| 赤铁原矿 | `cargoverse:raw_resource/hematite_ore` |
| 高纯硅片 | `cargoverse:refined_resource/high_purity_silicon_wafers` |
| 精密铜线 | `cargoverse:refined_resource/precision_copper_wire` |
| 末地环境样本 | `cargoverse:research_sample/end_environment_samples` |
| 地层岩芯 | `cargoverse:research_sample/stratigraphic_core_samples` |
| 紫水晶谐振片 | `cargoverse:special_resource/amethyst_resonator_plates` |
| 下界石英晶簇 | `cargoverse:special_resource/nether_quartz_clusters` |
| 稳相末影晶粒 | `cargoverse:special_resource/stabilized_ender_grains` |
| 航修工具箱 | `cargoverse:tools_equipment/aviation_maintenance_toolkits` |
| 矿务手工具 | `cargoverse:tools_equipment/mining_hand_tools` |
| 陈酿佳酿 | `cargoverse:valuables/aged_spirits` |
| 切磨宝石 | `cargoverse:valuables/cut_gemstones` |
| 轻型巡逻艇 | `cargoverse:vehicle/light_patrol_boats` |
| 港区牵引车 | `cargoverse:vehicle/port_tractors` |
| 驻防弹药箱 | `cargoverse:weapon_armor/garrison_ammunition_crates` |
| 制式弩机 | `cargoverse:weapon_armor/service_crossbows` |

[站点总览](<../../../07_贸易点/market/测试贸易点B/00_总体说明.md>)
