# 资源表正式定义

40 个正式站点各有一份资源表，2026-10-07 小站扩展已接入：104 种正式货物、212 条出售规则、375 条收购规则。每商品独立 price_multiplier；出售有限库存、收购无库存，按条目选择每日限额。4 种 NONE 预留货物不参与贸易。

各页是库存、日补、倍率与额度的正式维护入口，站点目录只保留用途和线路。规则 schema_version 为 1，唯一标签匹配，不做同站同货物双向贸易。字段约束见[资源表定义](<../../02贸易点系统/03_资源表定义.md>)。

## 天空站资源表

| 编号 | 资源表 | 出售条目 | 收购条目 |
| --- | --- | ---: | ---: |
| A01 | [标准建材装配港](<factory/sky_station/standard_assembly.md>) | 8 | 14 |
| A02 | [通用机电装备厂](<factory/sky_station/modular_equipment.md>) | 8 | 15 |
| A03 | [飞艇总装与航修港](<factory/sky_station/airship_yard.md>) | 10 | 15 |
| S01 | [云港民生集配站](<market/sky_station/civic_distribution.md>) | 4 | 11 |
| S02 | [远航货运枢纽](<market/sky_station/longhaul_port.md>) | 9 | 16 |
| S03 | [天空城综合市场](<market/sky_station/skycity_market.md>) | 5 | 14 |
| D01 | [深岩露天矿站](<resource/sky_station/deepcore_mine.md>) | 6 | 14 |
| D02 | [矿物分选精炼站](<factory/sky_station/mineral_refinery.md>) | 6 | 13 |
| D03 | [重工材料与矿机厂](<factory/sky_station/heavy_works.md>) | 10 | 13 |
| V01 | [梯田农林站](<resource/sky_station/terrace_farm.md>) | 11 | 17 |
| V02 | [云泽水产与育种站](<resource/sky_station/aquaculture_station.md>) | 11 | 10 |
| V03 | [绿洲生物工程站](<factory/sky_station/biosystems_station.md>) | 8 | 12 |
| E01 | [赫利俄斯燃料供应站](<factory/sky_station/fuel_depot.md>) | 8 | 10 |
| E02 | [工业化学品供应站](<factory/sky_station/chemical_works.md>) | 9 | 9 |
| E03 | [净水与环境处理站](<factory/sky_station/reclamation_station.md>) | 3 | 15 |
| H01 | [地平线野外科考站](<resource/sky_station/field_station.md>) | 9 | 13 |
| H02 | [精密电子与测绘中心](<factory/sky_station/precision_center.md>) | 9 | 11 |
| H03 | [虚空相位研究站](<resource/sky_station/phase_station.md>) | 4 | 16 |
| B01 | [铁壁防务装备站](<factory/sky_station/defense_arsenal.md>) | 6 | 9 |
| B02 | [安防设施集成厂](<factory/sky_station/security_works.md>) | 6 | 13 |
| B03 | [边境驻防补给港](<market/sky_station/frontier_garrison.md>) | 6 | 18 |
| R01 | [遗民打捞交换所](<resource/sky_station/remnant_exchange.md>) | 6 | 10 |
| R02 | [旧世珍品商馆](<market/sky_station/heritage_gallery.md>) | 5 | 8 |
| R03 | [远界异常交换站](<resource/sky_station/far_reach_exchange.md>) | 4 | 9 |

## 地面小站资源表

| 编号 | 资源表 | 出售条目 | 收购条目 |
| --- | --- | ---: | ---: |
| G01 | [浅层矿务前哨](<resource/ground_station/shallow_mining_outpost.md>) | 4 | 4 |
| G02 | [林缘采运站](<resource/ground_station/woodland_logging_station.md>) | 3 | 3 |
| G03 | [独立农圃](<resource/ground_station/independent_farmstead.md>) | 4 | 4 |
| G04 | [河岸渔站](<resource/ground_station/river_fishing_station.md>) | 3 | 3 |
| G05 | [地层采样站](<resource/ground_station/stratigraphic_sampling_station.md>) | 2 | 4 |
| G06 | [遗迹清理营](<resource/ground_station/ruin_clearance_camp.md>) | 2 | 4 |
| G07 | [野地居民点](<market/ground_station/wilderness_settlement.md>) | 2 | 5 |
| G08 | [航路巡防哨站](<market/ground_station/route_watchpost.md>) | 1 | 5 |
| G09 | [路畔货运驿站](<market/ground_station/roadside_freight_inn.md>) | 3 | 4 |
| G10 | [乡野机修所](<factory/ground_station/rural_repair_shop.md>) | 3 | 4 |
| G11 | [泉源净水所](<factory/ground_station/spring_water_station.md>) | 2 | 4 |
| G12 | [林间制材所](<factory/ground_station/woodland_processing_yard.md>) | 3 | 4 |
| G13 | [野外救护所](<market/ground_station/field_aid_station.md>) | 2 | 5 |
| G14 | [气象观测哨](<market/ground_station/weather_observation_post.md>) | 2 | 6 |
| G15 | [旧件回收铺](<market/ground_station/salvage_parts_shop.md>) | 3 | 5 |
| G16 | [边路施工营](<market/ground_station/wayside_construction_camp.md>) | 2 | 6 |

小站全部收购规则设每日上限；G07、G08 已加入回收出售，使用现有预留设备。首次创建实例时保存目录快照，普通 reload 不替换已存在实例的目录和报价。

## 指令测试资源表

[测试 A](<market/test_station/a.md>)与[测试 B](<market/test_station/b.md>)互为买卖方，合计覆盖 104 种正式商品；每站的出售与收购互斥。出售初始 10000 t、上限 20000 t、日补 10000 t；收购不限额，出售倍率 0.9、收购倍率 1.1。两表不计入上方正式贸易网络的条目数。
