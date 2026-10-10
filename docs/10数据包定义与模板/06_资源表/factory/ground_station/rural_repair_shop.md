# 乡野机修所资源表

> **已接入（2026-10-07）：** 完整整站 NBT、贸易点定义、资源表、结构绑定与自然生成配置已发布；设备静态核对通过，地形、货柜装卸与营业流程仍待实机验收。

| 项目 | 设计内容 |
| --- | --- |
| 关联站点 | [G10 乡野机修所](<../../../07_贸易点/factory/乡野机修所/00_总体说明.md>) |
| 资源 ID | `cargoverse:factory/ground_station/rural_repair_shop` |
| 发布 JSON | `src/main/resources/data/cargoverse/trade_points/resource_tables/factory/ground_station/rural_repair_shop.json` |
| schema_version | 2 |
| 引用方式 | 每行直接填写一个 CargoGood 完整 ID |
| 数量单位 | t 为数量符号；每日按 24000 ticks 计算 |
| 报价与库存 | 逐商品 price_multiplier；出售有限库存，收购无库存且全部设每日限额 |

## 出售 sales

全部使用有限 `inventory`；初始量、容量、日补分别对应 `initial`、`capacity`、`daily_restock`。当前均为持续补货，不增加一次性遗物来源。

| CargoGood ID | 货物 | 初始量 | 容量 | 日补 | 价格倍率 |
| --- | --- | ---: | ---: | ---: | ---: |
| `cargoverse:tools_equipment/mining_hand_tools` | [矿务手工具](<../../../01_CargoGood/tools_equipment/mining_hand_tools.md>) | 50 | 100 | 25 | 0.95 |
| `cargoverse:mechanical_parts/transmission_gears` | [标准传动齿轮](<../../../01_CargoGood/mechanical_parts/transmission_gears.md>) | 20 | 40 | 10 | 0.95 |
| `cargoverse:processed_resource/recyclable_metal_scrap` | [可回收金属废料](<../../../01_CargoGood/processed_resource/recyclable_metal_scrap.md>) | 30 | 60 | 15 | 0.5 |

## 收购 acquisitions

全部填写 `daily_limit`，额度由同一实例的所有玩家按每种货物共享，跨日恢复但不累计。不创建收购库存、不扣除材料来驱动出售。

| CargoGood ID | 货物 | 每日限额 | 价格倍率 |
| --- | --- | ---: | ---: |
| `cargoverse:refined_resource/structural_steel_ingots` | [结构钢锭](<../../../01_CargoGood/refined_resource/structural_steel_ingots.md>) | 30 | 1 |
| `cargoverse:chemical_material/industrial_lubricant` | [工业润滑油](<../../../01_CargoGood/chemical_material/industrial_lubricant.md>) | 30 | 1 |
| `cargoverse:general_supplies/shelf_stable_rations` | [长效口粮](<../../../01_CargoGood/general_supplies/shelf_stable_rations.md>) | 60 | 1 |
| `cargoverse:energy_fuel/industrial_energy_cells` | [工业蓄能电池](<../../../01_CargoGood/energy_fuel/industrial_energy_cells.md>) | 10 | 1 |

## 数值依据

| 方向 | 货物 | 数量的业务依据 |
| --- | --- | --- |
| 出售 | [矿务手工具](<../../../01_CargoGood/tools_equipment/mining_hand_tools.md>) | 工具整修与本地备件周转，服务 G01、G02 和制材作业 |
| 出售 | [标准传动齿轮](<../../../01_CargoGood/mechanical_parts/transmission_gears.md>) | 小批标准传动件，不形成完整机器货架 |
| 出售 | [可回收金属废料](<../../../01_CargoGood/processed_resource/recyclable_metal_scrap.md>) | 经除油分拣的维修边角料 |
| 收购 | [结构钢锭](<../../../01_CargoGood/refined_resource/structural_steel_ingots.md>) | 工具与通用金属件的维修用料 |
| 收购 | [工业润滑油](<../../../01_CargoGood/chemical_material/industrial_lubricant.md>) | 台架、轴承和工器具保养 |
| 收购 | [长效口粮](<../../../01_CargoGood/general_supplies/shelf_stable_rations.md>) | 作业人员日常补给 |
| 收购 | [工业蓄能电池](<../../../01_CargoGood/energy_fuel/industrial_energy_cells.md>) | 台式机具电源替换，设备需求故意小于生活用品 |

普通来源初始两日量、容量四日量，让初见站点有可装运库存，持续补货仍受本站用途约束。生活和低价原料按整柜或数柜组织，专业设备使用小批替换额度，不为了装满 S 柜而夸大每日仪器需求。

数量与价格为待实机平衡设计。新增站点数量会叠加区域供给和共享额度，不以单站看似很小就忽略总量；结算取整、签约修正、防护损耗和实际航程仍需验证。

[站点总览](<../../../07_贸易点/factory/乡野机修所/00_总体说明.md>) · [资源表目录](<../../README.md>) · [贸易点目录](<../../../07_贸易点/README.md>)
