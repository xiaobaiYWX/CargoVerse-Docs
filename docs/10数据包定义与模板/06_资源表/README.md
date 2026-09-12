# 资源表设计

## 基本信息

| 项目 | 内容 |
| --- | --- |
| 资源 ID |  |
| JSON 文件 | `src/main/resources/data/<namespace>/trade_points/resource_tables/<type>/<category>/<name>.json` |
| Schema 版本 | 1 |
| 用途 |  |

## 出售规则

| 规则 ID | match_mode | 标签 | 创建库存 | 初始量 | 每种货物容量 | 每日补货 |
| --- | --- | --- | --- | ---: | ---: | ---: |
|  |  |  |  |  |  |  |

## 收购规则

| 规则 ID | match_mode | 标签 | 创建库存 | 初始量 | 每种货物容量 | 每日消耗 | 满库继续收购 |
| --- | --- | --- | --- | ---: | ---: | ---: | --- |
|  |  |  |  |  |  |  |  |

`create_inventory: false` 的规则只填写 ID、匹配方式、标签和库存开关，其余库存字段留空。每种匹配货物独享表中容量和周转量，不与同规则的其他货物共享。

## 当前定义

| 资源表 | 出售规则 | 收购规则 |
| --- | ---: | ---: |
| [cargoverse:resource/agriculture/default](resource/agriculture/default.md) | 1 | 0 |
| [cargoverse:resource/general/default](resource/general/default.md) | 3 | 2 |

字段规则见[资源表定义](../../02贸易点系统/03_资源表定义.md)。

## 新增定义（已同步，结构待补）

24 个贸易点及其资源表已同步数据包；当前共 25 个贸易点定义（含 1 个测试点）、26 份资源表（含 2 份示例）。新节点的自然结构与生成绑定尚未接入。

[整体设计与制造商定位](<../07_贸易点/设计总览.md>) · [100 项货物供需校核](<../07_贸易点/供需覆盖与数值校核.md>) · [起步航线与投放顺序](<../07_贸易点/起步航线与投放顺序.md>)

| 编号 | 资源表 | 出售规则 | 收购规则 |
| --- | --- | ---: | ---: |
| A01 | [标准建材装配港](<factory/construction/standard_assembly.md>) | 6 | 4 |
| A02 | [通用机电装备厂](<factory/machinery/modular_equipment.md>) | 7 | 4 |
| A03 | [飞艇总装与航修港](<factory/aviation/airship_yard.md>) | 5 | 5 |
| S01 | [云港民生集配站](<market/logistics/civic_distribution.md>) | 3 | 6 |
| S02 | [远航货运枢纽](<market/logistics/longhaul_port.md>) | 0 | 9 |
| S03 | [天空城综合市场](<market/settlement/skycity_market.md>) | 0 | 10 |
| D01 | [深岩露天矿站](<resource/mining/deepcore_mine.md>) | 4 | 4 |
| D02 | [矿物分选精炼站](<factory/mineral/mineral_refinery.md>) | 3 | 3 |
| D03 | [重工材料与矿机厂](<factory/heavy/heavy_works.md>) | 7 | 5 |
| V01 | [梯田农林站](<resource/agriculture/terrace_farm.md>) | 8 | 8 |
| V02 | [云泽水产与育种站](<resource/ecology/aquaculture_station.md>) | 8 | 2 |
| V03 | [绿洲生物工程站](<factory/biology/biosystems_station.md>) | 7 | 3 |
| E01 | [赫利俄斯燃料供应站](<factory/energy/fuel_depot.md>) | 5 | 1 |
| E02 | [工业化学品供应站](<factory/chemical/chemical_works.md>) | 6 | 0 |
| E03 | [净水与环境处理站](<factory/environment/reclamation_station.md>) | 2 | 5 |
| H01 | [地平线野外科考站](<resource/research/field_station.md>) | 5 | 3 |
| H02 | [精密电子与测绘中心](<factory/electronics/precision_center.md>) | 6 | 3 |
| H03 | [虚空相位研究站](<resource/anomaly/phase_station.md>) | 2 | 6 |
| B01 | [铁壁防务装备站](<factory/defense/defense_arsenal.md>) | 4 | 0 |
| B02 | [安防设施集成厂](<factory/security/security_works.md>) | 4 | 3 |
| B03 | [边境驻防补给港](<market/defense/frontier_garrison.md>) | 0 | 11 |
| R01 | [遗民打捞交换所](<resource/salvage/remnant_exchange.md>) | 3 | 2 |
| R02 | [旧世珍品商馆](<market/valuables/heritage_gallery.md>) | 3 | 1 |
| R03 | [远界异常交换站](<resource/anomaly/far_reach_exchange.md>) | 2 | 2 |

## 生成设计补充

[结构生成规则与概率](<../07_贸易点/结构生成规则与概率.md>) · [生成密度与库存校核](<../07_贸易点/生成密度与库存校核.md>)。24 个新结构均采用一个世界结构对应一个贸易点定义，绑定概率 100%；世界出现频率由结构集控制。
