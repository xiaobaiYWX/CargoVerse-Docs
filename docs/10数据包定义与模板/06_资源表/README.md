# 自然贸易点货物交易表

**设计状态（2026-10-20）：** 40 个自然站已完成首轮实际物品贸易表，覆盖 149 种物品、189 条出售、315 条收购；全部标记为“待落数据”。商品包括原版、Create、航空学及随附的 Simulated。A／B 测试表另按这 149 种商品互补分组并已接入，用于指令测试，不计入自然经济统计。

**运行状态：** `schema_version: 3` 已支持实际物品及完整组件报价，40 张自然站 JSON 仍为空；A／B 两张测试 JSON 已更新，分别出售 75／74 种，收购对方目录。站点结构、制造、商店及注册等功能保留。旧抽象货物、schema 2 参数不迁移。

每个站表维护精确物品、规则 ID、每件 VB 单价、有限库存、日补、每日收购额度与两种每件经验。价格和经验属于本站报价，既不写回物品，也不写进运输配置。只要在自然生成目的地成功收购，就按成交件数和当地收购配置产生两种经验，包括玩家自产物品；玩家目的地不奖励。

先读[贸易网络与定价设计](../07_贸易点/设计总览.md)，再查看各站表。字段语义见[现行报价与运输经验规则](../../02贸易点系统/03_资源表定义.md)。各站用途及线路直接维护在本站 `定义设计/02_贸易网络设计.md`，不另建集中商品参数表。

- [乡野机修所资源表](factory/ground_station/rural_repair_shop.md)
- [云泽水产与育种站资源表](resource/sky_station/aquaculture_station.md)
- [云港民生集配站资源表](market/sky_station/civic_distribution.md)
- [净水与环境处理站资源表](factory/sky_station/reclamation_station.md)
- [地层采样站资源表](resource/ground_station/stratigraphic_sampling_station.md)
- [地平线野外科考站资源表](resource/sky_station/field_station.md)
- [天空城综合市场资源表](market/sky_station/skycity_market.md)
- [安防设施集成厂资源表](factory/sky_station/security_works.md)
- [工业化学品供应站资源表](factory/sky_station/chemical_works.md)
- [旧世珍品商馆资源表](market/sky_station/heritage_gallery.md)
- [旧件回收铺资源表](market/ground_station/salvage_parts_shop.md)
- [林缘采运站资源表](resource/ground_station/woodland_logging_station.md)
- [林间制材所资源表](factory/ground_station/woodland_processing_yard.md)
- [标准建材装配港资源表](factory/sky_station/standard_assembly.md)
- [梯田农林站资源表](resource/sky_station/terrace_farm.md)
- [气象观测哨资源表](market/ground_station/weather_observation_post.md)
- [河岸渔站资源表](resource/ground_station/river_fishing_station.md)
- [泉源净水所资源表](factory/ground_station/spring_water_station.md)
- [浅层矿务前哨资源表](resource/ground_station/shallow_mining_outpost.md)
- [测试贸易点 A · 资源表](market/test_station/a.md)
- [测试贸易点 B · 资源表](market/test_station/b.md)
- [深岩露天矿站资源表](resource/sky_station/deepcore_mine.md)
- [独立农圃资源表](resource/ground_station/independent_farmstead.md)
- [矿物分选精炼站资源表](factory/sky_station/mineral_refinery.md)
- [精密电子与测绘中心资源表](factory/sky_station/precision_center.md)
- [绿洲生物工程站资源表](factory/sky_station/biosystems_station.md)
- [航路巡防哨站资源表](market/ground_station/route_watchpost.md)
- [虚空相位研究站资源表](resource/sky_station/phase_station.md)
- [赫利俄斯燃料供应站资源表](factory/sky_station/fuel_depot.md)
- [路畔货运驿站资源表](market/ground_station/roadside_freight_inn.md)
- [边境驻防补给港资源表](market/sky_station/frontier_garrison.md)
- [边路施工营资源表](market/ground_station/wayside_construction_camp.md)
- [远界异常交换站资源表](resource/sky_station/far_reach_exchange.md)
- [远航货运枢纽资源表](market/sky_station/longhaul_port.md)
- [通用机电装备厂资源表](factory/sky_station/modular_equipment.md)
- [遗民打捞交换所资源表](resource/sky_station/remnant_exchange.md)
- [遗迹清理营资源表](resource/ground_station/ruin_clearance_camp.md)
- [重工材料与矿机厂资源表](factory/sky_station/heavy_works.md)
- [野地居民点资源表](market/ground_station/wilderness_settlement.md)
- [野外救护所资源表](market/ground_station/field_aid_station.md)
- [铁壁防务装备站资源表](factory/sky_station/defense_arsenal.md)
- [飞艇总装与航修港资源表](factory/sky_station/airship_yard.md)

[实际物品与运输配置](../01_物品运输/README.md)
