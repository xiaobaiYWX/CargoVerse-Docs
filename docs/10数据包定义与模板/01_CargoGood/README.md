# CargoGood 正式定义

现有数据包含 **104 项正式货物＋4 项 none 预留定义**，23 个正式分类每类至少 4 项。每项文档与对应 JSON 同步；具体交易目录、库存与周转由资源表逐贸易点设计。

## 空白模板

每项包含资源 ID、JSON 路径、显示名、科技、结算单位、质量、价值、两种经验、基础完整度、运输要求及来源／去向。可复制任一条目按相同表格填写。字段约束见[货物类型](../../01货柜系统/01核心系统/05_货物类型.md)。

## 本批数值与资源规则

- none 预留定义为 0 VB/t、0 经验，不接入普通资源表；其余基础价值以各货物文档为准。
- 常规货物许可证经验 T1～T5 为 **4／6／8／12／16 exp/t**，繁荣经验为 **2／3／4／6／8 exp/t**；整数化时门槛同步 ×4，本次数量扩量再 ×5。基础完整度统一 **200**，完整度损耗同步 ×2。108 项单位质量均为整数；当前容量、单价与门槛以[50 t 数量基线](<数量与运力基线.md>)为准；详见[整数数值基线](<整数数值基线.md>)。
- 2026-10-06 新增四种普通回收料，许可证／繁荣经验均为 1/单位，作为低价值回程业务的明确例外；无新增 CargoClass。
- 资源表、商店和制造台均通过完整 CargoGood ID 显式引用货物；CargoGood 不再维护自动匹配标签。
- 普通限时 48000 ticks，宽松限时 96000 ticks；其他词条使用各文档列明的温和参数，每货物最多 2 项。本批不启用 cold_chain；异常候选约束不自动生效。
- 全部 108 项已配置独立 `icon`，使用 32×32 透明 PNG；CargoClass 贴花和缺图问号回退保留各自用途。
- 稀缺遗物和 none 只登记定义，没有新加订单、鉴定或转运系统。贸易点是否交易及是否创建库存全部由资源表决定。

## 当前定义

当前 108 项定义与正式文档字段一致，23 个正式分类均有可用货柜。资源表、制造台及商店参加统一数据加载校验；仍需在游戏内验证运输表现与数值平衡。

| CargoGood | 名称 | 分类 | 科技 | 基础价值 VB/t | 单位质量 Kpg/t | 许可证经验 exp/t | 繁荣经验 exp/t |
| --- | --- | --- | ---: | ---: | ---: | ---: | ---: |
| [cargoverse:agriculture/bagged_wheat](agriculture/bagged_wheat.md) | 袋装麦粒 | agriculture | 1 | 8 | 2 | 4 | 2 |
| [cargoverse:agriculture/cotton_bales](agriculture/cotton_bales.md) | 纤维棉包 | agriculture | 1 | 12 | 1 | 4 | 2 |
| [cargoverse:agriculture/greenhouse_fruit](agriculture/greenhouse_fruit.md) | 温室鲜果 | agriculture | 2 | 14 | 2 | 6 | 3 |
| [cargoverse:agriculture/hydroponic_leafy_greens](agriculture/hydroponic_leafy_greens.md) | 水培叶菜 | agriculture | 2 | 14 | 1 | 6 | 3 |
| [cargoverse:agriculture/sealed_seed_grain](agriculture/sealed_seed_grain.md) | 密封种粮 | agriculture | 2 | 28 | 2 | 6 | 3 |
| [cargoverse:anomalous_cargo/contained_void_mixture](anomalous_cargo/contained_void_mixture.md) | 桶装虚空混合物 | anomalous_cargo | 5 | 202 | 4 | 16 | 8 |
| [cargoverse:anomalous_cargo/memory_echo_media](anomalous_cargo/memory_echo_media.md) | 记忆回声介质 | anomalous_cargo | 4 | 1800 | 1 | 12 | 6 |
| [cargoverse:anomalous_cargo/non_euclidean_components](anomalous_cargo/non_euclidean_components.md) | 非欧几何构件 | anomalous_cargo | 5 | 4400 | 3 | 16 | 8 |
| [cargoverse:anomalous_cargo/temporal_lag_clusters](anomalous_cargo/temporal_lag_clusters.md) | 时滞晶簇 | anomalous_cargo | 5 | 4800 | 2 | 16 | 8 |
| [cargoverse:aquatic/chilled_river_fish](aquatic/chilled_river_fish.md) | 冰鲜河鱼 | aquatic | 1 | 16 | 2 | 4 | 2 |
| [cargoverse:aquatic/chilled_sea_shrimp](aquatic/chilled_sea_shrimp.md) | 冰鲜海虾 | aquatic | 2 | 32 | 2 | 6 | 3 |
| [cargoverse:aquatic/fresh_kelp](aquatic/fresh_kelp.md) | 鲜采食用海带 | aquatic | 1 | 7 | 2 | 4 | 2 |
| [cargoverse:aquatic/purified_shellfish](aquatic/purified_shellfish.md) | 净化鲜贝 | aquatic | 2 | 14 | 2 | 6 | 3 |
| [cargoverse:chemical_material/compound_fertilizer](chemical_material/compound_fertilizer.md) | 复合肥料 | chemical_material | 2 | 14 | 3 | 6 | 3 |
| [cargoverse:chemical_material/culture_medium](chemical_material/culture_medium.md) | 培养基原液 | chemical_material | 3 | 40 | 3 | 8 | 4 |
| [cargoverse:chemical_material/hydroponic_nutrient_solution](chemical_material/hydroponic_nutrient_solution.md) | 水培营养液 | chemical_material | 2 | 16 | 3 | 6 | 3 |
| [cargoverse:chemical_material/industrial_lubricant](chemical_material/industrial_lubricant.md) | 工业润滑油 | chemical_material | 2 | 20 | 3 | 6 | 3 |
| [cargoverse:chemical_material/sealing_resin](chemical_material/sealing_resin.md) | 密封树脂 | chemical_material | 2 | 22 | 3 | 6 | 3 |
| [cargoverse:construction_material/bagged_cement](construction_material/bagged_cement.md) | 袋装水泥 | construction_material | 1 | 6 | 5 | 4 | 2 |
| [cargoverse:construction_material/insulation_panels](construction_material/insulation_panels.md) | 保温板材 | construction_material | 2 | 52 | 1 | 6 | 3 |
| [cargoverse:construction_material/structural_steel_beams](construction_material/structural_steel_beams.md) | 标准钢梁 | construction_material | 2 | 126 | 6 | 6 | 3 |
| [cargoverse:construction_material/tempered_glass_panels](construction_material/tempered_glass_panels.md) | 钢化玻璃板 | construction_material | 2 | 24 | 3 | 6 | 3 |
| [cargoverse:electronics/avionics_controllers](electronics/avionics_controllers.md) | 航电控制器 | electronics | 3 | 90 | 1 | 8 | 4 |
| [cargoverse:electronics/communication_relays](electronics/communication_relays.md) | 通信中继器 | electronics | 3 | 124 | 1 | 8 | 4 |
| [cargoverse:electronics/data_storage_arrays](electronics/data_storage_arrays.md) | 封装数据存储阵列 | electronics | 4 | 146 | 2 | 12 | 6 |
| [cargoverse:electronics/industrial_sensors](electronics/industrial_sensors.md) | 工业传感器 | electronics | 3 | 108 | 1 | 8 | 4 |
| [cargoverse:electronics/perimeter_security_systems](electronics/perimeter_security_systems.md) | 周界警戒系统 | electronics | 3 | 142 | 1 | 8 | 4 |
| [cargoverse:electronics/precursor_navigation_cores](electronics/precursor_navigation_cores.md) | 前文明导航核心 | electronics | 5 | 3600 | 1 | 16 | 8 |
| [cargoverse:energy_fuel/aviation_fuel_drums](energy_fuel/aviation_fuel_drums.md) | 桶装航空燃油 | energy_fuel | 3 | 40 | 3 | 8 | 4 |
| [cargoverse:energy_fuel/biomass_briquettes](energy_fuel/biomass_briquettes.md) | 压制生物燃料 | energy_fuel | 1 | 5 | 2 | 4 | 2 |
| [cargoverse:energy_fuel/coke_fuel](energy_fuel/coke_fuel.md) | 煤焦燃料 | energy_fuel | 2 | 10 | 3 | 6 | 3 |
| [cargoverse:energy_fuel/industrial_energy_cells](energy_fuel/industrial_energy_cells.md) | 工业蓄能电池 | energy_fuel | 3 | 114 | 3 | 8 | 4 |
| [cargoverse:general_supplies/civilian_lighting_kits](general_supplies/civilian_lighting_kits.md) | 民用照明器具 | general_supplies | 2 | 56 | 2 | 6 | 3 |
| [cargoverse:general_supplies/durable_workwear](general_supplies/durable_workwear.md) | 耐用工装 | general_supplies | 2 | 72 | 1 | 6 | 3 |
| [cargoverse:general_supplies/potable_water_crates](general_supplies/potable_water_crates.md) | 净水补给箱 | general_supplies | 1 | 5 | 3 | 4 | 2 |
| [cargoverse:general_supplies/shelf_stable_rations](general_supplies/shelf_stable_rations.md) | 长效口粮 | general_supplies | 1 | 20 | 2 | 4 | 2 |
| [cargoverse:hazardous_material/contaminated_adsorbent](hazardous_material/contaminated_adsorbent.md) | 污染吸附剂 | hazardous_material | 3 | 8 | 3 | 8 | 4 |
| [cargoverse:hazardous_material/heavy_metal_filter_cake](hazardous_material/heavy_metal_filter_cake.md) | 重金属滤渣 | hazardous_material | 2 | 3 | 5 | 6 | 3 |
| [cargoverse:hazardous_material/spent_acid_drums](hazardous_material/spent_acid_drums.md) | 废酸回收桶 | hazardous_material | 2 | 4 | 3 | 6 | 3 |
| [cargoverse:hazardous_material/spent_isotope_sources](hazardous_material/spent_isotope_sources.md) | 失效同位素源 | hazardous_material | 4 | 80 | 4 | 12 | 6 |
| [cargoverse:livestock/breeding_poultry](livestock/breeding_poultry.md) | 家禽种群 | livestock | 1 | 24 | 2 | 4 | 2 |
| [cargoverse:livestock/breeding_sheep](livestock/breeding_sheep.md) | 育成绵羊 | livestock | 1 | 36 | 2 | 4 | 2 |
| [cargoverse:livestock/hatchery_fry](livestock/hatchery_fry.md) | 养殖鱼苗 | livestock | 2 | 28 | 2 | 6 | 3 |
| [cargoverse:livestock/pollinator_colonies](livestock/pollinator_colonies.md) | 授粉蜂群 | livestock | 2 | 48 | 1 | 6 | 3 |
| [cargoverse:machinery/automated_cargo_handlers](machinery/automated_cargo_handlers.md) | 自动装卸机 | machinery | 3 | 188 | 4 | 8 | 4 |
| [cargoverse:machinery/industrial_pump_sets](machinery/industrial_pump_sets.md) | 工业水泵机组 | machinery | 2 | 140 | 5 | 6 | 3 |
| [cargoverse:machinery/ore_crushers](machinery/ore_crushers.md) | 矿石破碎机 | machinery | 2 | 204 | 6 | 6 | 3 |
| [cargoverse:machinery/precision_machine_tools](machinery/precision_machine_tools.md) | 精密机床 | machinery | 3 | 196 | 5 | 8 | 4 |
| [cargoverse:mechanical_parts/hydraulic_cylinders](mechanical_parts/hydraulic_cylinders.md) | 液压执行缸 | mechanical_parts | 3 | 136 | 3 | 8 | 4 |
| [cargoverse:mechanical_parts/precision_bearings](mechanical_parts/precision_bearings.md) | 精密轴承 | mechanical_parts | 3 | 152 | 3 | 8 | 4 |
| [cargoverse:mechanical_parts/propulsion_impellers](mechanical_parts/propulsion_impellers.md) | 推进器叶轮 | mechanical_parts | 3 | 152 | 3 | 8 | 4 |
| [cargoverse:mechanical_parts/scrapped_electronic_components](mechanical_parts/scrapped_electronic_components.md) | 报废电子组件 | mechanical_parts | 1 | 14 | 2 | 1 | 1 |
| [cargoverse:mechanical_parts/standard_container_couplings](mechanical_parts/standard_container_couplings.md) | 标准货柜接口总成 | mechanical_parts | 2 | 128 | 3 | 6 | 3 |
| [cargoverse:mechanical_parts/transmission_gears](mechanical_parts/transmission_gears.md) | 标准传动齿轮 | mechanical_parts | 2 | 134 | 3 | 6 | 3 |
| [cargoverse:medical_supply/first_aid_medicines](medical_supply/first_aid_medicines.md) | 急救药剂 | medical_supply | 2 | 30 | 1 | 6 | 3 |
| [cargoverse:medical_supply/regenerative_culture_fluid](medical_supply/regenerative_culture_fluid.md) | 再生培养液 | medical_supply | 4 | 164 | 2 | 12 | 6 |
| [cargoverse:medical_supply/sterile_dressings](medical_supply/sterile_dressings.md) | 无菌敷料 | medical_supply | 2 | 80 | 1 | 6 | 3 |
| [cargoverse:medical_supply/vaccine_preparations](medical_supply/vaccine_preparations.md) | 疫苗制剂 | medical_supply | 3 | 112 | 1 | 8 | 4 |
| [cargoverse:none/unidentified_fragments](none/unidentified_fragments.md) | 未鉴定残件 | none | 2 | 0 | 3 | 0 | 0 |
| [cargoverse:none/unlabelled_warehouse_crates](none/unlabelled_warehouse_crates.md) | 失标仓储货箱 | none | 1 | 0 | 3 | 0 | 0 |
| [cargoverse:none/unprovenanced_sealed_crates](none/unprovenanced_sealed_crates.md) | 来源不明封存箱 | none | 2 | 0 | 3 | 0 | 0 |
| [cargoverse:none/unsorted_salvage_lots](none/unsorted_salvage_lots.md) | 未分拣打捞包 | none | 1 | 0 | 3 | 0 | 0 |
| [cargoverse:prefab_structure/airship_keel_modules](prefab_structure/airship_keel_modules.md) | 飞艇龙骨模块 | prefab_structure | 3 | 208 | 10 | 8 | 4 |
| [cargoverse:prefab_structure/closed_loop_hydroponic_modules](prefab_structure/closed_loop_hydroponic_modules.md) | 循环水培舱 | prefab_structure | 3 | 200 | 8 | 8 | 4 |
| [cargoverse:prefab_structure/containerized_water_stations](prefab_structure/containerized_water_stations.md) | 集装式净水站 | prefab_structure | 3 | 214 | 8 | 8 | 4 |
| [cargoverse:prefab_structure/greenhouse_frame_modules](prefab_structure/greenhouse_frame_modules.md) | 温室骨架模块 | prefab_structure | 2 | 138 | 5 | 6 | 3 |
| [cargoverse:prefab_structure/prefab_defensive_positions](prefab_structure/prefab_defensive_positions.md) | 预制防御工事 | prefab_structure | 3 | 122 | 8 | 8 | 4 |
| [cargoverse:prefab_structure/prefab_habitat_pods](prefab_structure/prefab_habitat_pods.md) | 预制居住舱 | prefab_structure | 2 | 116 | 8 | 6 | 3 |
| [cargoverse:processed_resource/copper_concentrate](processed_resource/copper_concentrate.md) | 铜精矿 | processed_resource | 2 | 34 | 2 | 6 | 3 |
| [cargoverse:processed_resource/dried_organic_residue](processed_resource/dried_organic_residue.md) | 干化有机废料 | processed_resource | 1 | 3 | 2 | 1 | 1 |
| [cargoverse:processed_resource/industrial_cotton_cloth](processed_resource/industrial_cotton_cloth.md) | 工业棉布 | processed_resource | 2 | 38 | 1 | 6 | 3 |
| [cargoverse:processed_resource/iron_concentrate](processed_resource/iron_concentrate.md) | 铁精矿 | processed_resource | 2 | 26 | 2 | 6 | 3 |
| [cargoverse:processed_resource/kiln_dried_planks](processed_resource/kiln_dried_planks.md) | 烘干木板 | processed_resource | 1 | 24 | 2 | 4 | 2 |
| [cargoverse:processed_resource/recyclable_metal_scrap](processed_resource/recyclable_metal_scrap.md) | 可回收金属废料 | processed_resource | 1 | 6 | 4 | 1 | 1 |
| [cargoverse:processed_resource/sorted_packaging_scrap](processed_resource/sorted_packaging_scrap.md) | 分拣包装废料 | processed_resource | 1 | 4 | 1 | 1 | 1 |
| [cargoverse:raw_resource/conifer_logs](raw_resource/conifer_logs.md) | 针叶原木 | raw_resource | 1 | 8 | 3 | 4 | 2 |
| [cargoverse:raw_resource/copper_ore](raw_resource/copper_ore.md) | 含铜原矿 | raw_resource | 1 | 9 | 5 | 4 | 2 |
| [cargoverse:raw_resource/hematite_ore](raw_resource/hematite_ore.md) | 赤铁原矿 | raw_resource | 1 | 6 | 5 | 4 | 2 |
| [cargoverse:raw_resource/quartz_sand](raw_resource/quartz_sand.md) | 石英原砂 | raw_resource | 1 | 5 | 4 | 4 | 2 |
| [cargoverse:refined_resource/high_purity_silicon_wafers](refined_resource/high_purity_silicon_wafers.md) | 高纯硅片 | refined_resource | 3 | 54 | 1 | 8 | 4 |
| [cargoverse:refined_resource/optical_glass_blanks](refined_resource/optical_glass_blanks.md) | 光学玻璃坯 | refined_resource | 3 | 42 | 3 | 8 | 4 |
| [cargoverse:refined_resource/precision_copper_wire](refined_resource/precision_copper_wire.md) | 精密铜线 | refined_resource | 3 | 102 | 4 | 8 | 4 |
| [cargoverse:refined_resource/structural_steel_ingots](refined_resource/structural_steel_ingots.md) | 结构钢锭 | refined_resource | 2 | 66 | 5 | 6 | 3 |
| [cargoverse:research_sample/end_environment_samples](research_sample/end_environment_samples.md) | 末地环境样本 | research_sample | 4 | 320 | 2 | 12 | 6 |
| [cargoverse:research_sample/ruin_material_sections](research_sample/ruin_material_sections.md) | 遗迹材料切片 | research_sample | 3 | 140 | 2 | 8 | 4 |
| [cargoverse:research_sample/stratigraphic_core_samples](research_sample/stratigraphic_core_samples.md) | 地层岩芯 | research_sample | 2 | 50 | 2 | 6 | 3 |
| [cargoverse:research_sample/upper_air_microbe_samples](research_sample/upper_air_microbe_samples.md) | 高空微生物样本 | research_sample | 3 | 54 | 1 | 8 | 4 |
| [cargoverse:special_resource/amethyst_resonator_plates](special_resource/amethyst_resonator_plates.md) | 紫水晶谐振片 | special_resource | 3 | 80 | 2 | 8 | 4 |
| [cargoverse:special_resource/glowstone_luminant](special_resource/glowstone_luminant.md) | 萤石发光粉 | special_resource | 2 | 40 | 2 | 6 | 3 |
| [cargoverse:special_resource/nether_quartz_clusters](special_resource/nether_quartz_clusters.md) | 下界石英晶簇 | special_resource | 3 | 64 | 2 | 8 | 4 |
| [cargoverse:special_resource/old_world_alloy_fragments](special_resource/old_world_alloy_fragments.md) | 旧世合金残片 | special_resource | 4 | 800 | 5 | 12 | 6 |
| [cargoverse:special_resource/stabilized_ender_grains](special_resource/stabilized_ender_grains.md) | 稳相末影晶粒 | special_resource | 4 | 90 | 2 | 12 | 6 |
| [cargoverse:tools_equipment/aviation_maintenance_toolkits](tools_equipment/aviation_maintenance_toolkits.md) | 航修工具箱 | tools_equipment | 2 | 96 | 2 | 6 | 3 |
| [cargoverse:tools_equipment/field_sampling_kits](tools_equipment/field_sampling_kits.md) | 野外采样器 | tools_equipment | 3 | 96 | 2 | 8 | 4 |
| [cargoverse:tools_equipment/mining_hand_tools](tools_equipment/mining_hand_tools.md) | 矿务手工具 | tools_equipment | 1 | 22 | 2 | 4 | 2 |
| [cargoverse:tools_equipment/precision_measuring_instruments](tools_equipment/precision_measuring_instruments.md) | 精密测量仪 | tools_equipment | 3 | 122 | 2 | 8 | 4 |
| [cargoverse:valuables/aged_spirits](valuables/aged_spirits.md) | 陈酿佳酿 | valuables | 2 | 44 | 1 | 6 | 3 |
| [cargoverse:valuables/artisan_jewelry](valuables/artisan_jewelry.md) | 精工饰品 | valuables | 3 | 192 | 1 | 8 | 4 |
| [cargoverse:valuables/cut_gemstones](valuables/cut_gemstones.md) | 切磨宝石 | valuables | 2 | 180 | 1 | 6 | 3 |
| [cargoverse:valuables/restored_old_world_art](valuables/restored_old_world_art.md) | 修复旧世艺术品 | valuables | 3 | 1200 | 1 | 8 | 4 |
| [cargoverse:vehicle/light_patrol_boats](vehicle/light_patrol_boats.md) | 轻型巡逻艇 | vehicle | 3 | 152 | 6 | 8 | 4 |
| [cargoverse:vehicle/mining_haulers](vehicle/mining_haulers.md) | 矿用运输车 | vehicle | 2 | 158 | 8 | 6 | 3 |
| [cargoverse:vehicle/port_tractors](vehicle/port_tractors.md) | 港区牵引车 | vehicle | 2 | 134 | 6 | 6 | 3 |
| [cargoverse:vehicle/survey_drones](vehicle/survey_drones.md) | 测绘无人机 | vehicle | 4 | 204 | 1 | 12 | 6 |
| [cargoverse:weapon_armor/garrison_ammunition_crates](weapon_armor/garrison_ammunition_crates.md) | 驻防弹药箱 | weapon_armor | 3 | 76 | 4 | 8 | 4 |
| [cargoverse:weapon_armor/guard_armor](weapon_armor/guard_armor.md) | 护卫护甲 | weapon_armor | 2 | 96 | 3 | 6 | 3 |
| [cargoverse:weapon_armor/service_crossbows](weapon_armor/service_crossbows.md) | 制式弩机 | weapon_armor | 2 | 84 | 4 | 6 | 3 |
| [cargoverse:weapon_armor/ship_defense_gun_sets](weapon_armor/ship_defense_gun_sets.md) | 舰载防御炮组 | weapon_armor | 3 | 140 | 6 | 8 | 4 |

## 图标资源

本批图标验证：104 个独立 32×32 透明 PNG，JSON、正式文档、打包资源引用一致；完整工作区测试通过 565 项。未进行游戏内视觉验证。虚空混合物采用通过透明通道检查的深紫色收容罐图标。

所有图标位于 `assets/cargoverse/textures/gui/cargo_goods/<class>/<good>.png`。统一 32×32、透明底、像素风；原始生成提示和总览位于工作区 `CargoVerse-Assets/texetures/GUI/cargo_good_icons/`。本批通过内置 image_gen 逐项生成，导出只做透明边裁切、最近邻缩放与有限色 PNG 编码。

## 内容设计依据

[货物分类、显式引用与经济设计口径](<设计口径.md>) · [贸易点详细设计](<../07_贸易点/设计总览.md>)
