# 林间制材所资源表

> **已接入（2026-10-07）：** 完整整站 NBT、贸易点定义、资源表、结构绑定与自然生成配置已发布；设备静态核对通过，地形、货柜装卸与营业流程仍待实机验收。

| 项目 | 设计内容 |
| --- | --- |
| 关联站点 | [G12 林间制材所](<../../../07_贸易点/factory/林间制材所/00_总体说明.md>) |
| 资源 ID | `cargoverse:factory/ground_station/woodland_processing_yard` |
| 发布 JSON | `src/main/resources/data/cargoverse/trade_points/resource_tables/factory/ground_station/woodland_processing_yard.json` |
| schema_version | 2 |
| 引用方式 | 每行直接填写一个 CargoGood 完整 ID |
| 数量单位 | t 为数量符号；每日按 24000 ticks 计算 |
| 报价与库存 | 逐商品 price_multiplier；出售有限库存，收购无库存且全部设每日限额 |

## 出售 sales

全部使用有限 `inventory`；初始量、容量、日补分别对应 `initial`、`capacity`、`daily_restock`。当前均为持续补货，不增加一次性遗物来源。

| CargoGood ID | 货物 | 初始量 | 容量 | 日补 | 价格倍率 |
| --- | --- | ---: | ---: | ---: | ---: |
| `cargoverse:processed_resource/kiln_dried_planks` | [烘干木板](<../../../01_CargoGood/processed_resource/kiln_dried_planks.md>) | 120 | 240 | 60 | 0.95 |
| `cargoverse:energy_fuel/biomass_briquettes` | [压制生物燃料](<../../../01_CargoGood/energy_fuel/biomass_briquettes.md>) | 160 | 320 | 80 | 0.95 |
| `cargoverse:processed_resource/dried_organic_residue` | [干化有机废料](<../../../01_CargoGood/processed_resource/dried_organic_residue.md>) | 30 | 60 | 15 | 0.5 |

## 收购 acquisitions

全部填写 `daily_limit`，额度由同一实例的所有玩家按每种货物共享，跨日恢复但不累计。不创建收购库存、不扣除材料来驱动出售。

| CargoGood ID | 货物 | 每日限额 | 价格倍率 |
| --- | --- | ---: | ---: |
| `cargoverse:raw_resource/conifer_logs` | [针叶原木](<../../../01_CargoGood/raw_resource/conifer_logs.md>) | 100 | 1 |
| `cargoverse:tools_equipment/mining_hand_tools` | [矿务手工具](<../../../01_CargoGood/tools_equipment/mining_hand_tools.md>) | 30 | 1 |
| `cargoverse:general_supplies/durable_workwear` | [耐用工装](<../../../01_CargoGood/general_supplies/durable_workwear.md>) | 25 | 1 |
| `cargoverse:general_supplies/potable_water_crates` | [净水补给箱](<../../../01_CargoGood/general_supplies/potable_water_crates.md>) | 80 | 1 |

## 数值依据

| 方向 | 货物 | 数量的业务依据 |
| --- | --- | --- |
| 出售 | [烘干木板](<../../../01_CargoGood/processed_resource/kiln_dried_planks.md>) | 维修木板主货，连接居民、驿站与施工点 |
| 出售 | [压制生物燃料](<../../../01_CargoGood/energy_fuel/biomass_briquettes.md>) | 林业剩余物形成的普通燃料来源 |
| 出售 | [干化有机废料](<../../../01_CargoGood/processed_resource/dried_organic_residue.md>) | 干燥封装的植物残料，排除未经处理的腐败物 |
| 收购 | [针叶原木](<../../../01_CargoGood/raw_resource/conifer_logs.md>) | 与 G02 等采运来源形成短途交付 |
| 收购 | [矿务手工具](<../../../01_CargoGood/tools_equipment/mining_hand_tools.md>) | 通用手工具用于搬运、切分与维护 |
| 收购 | [耐用工装](<../../../01_CargoGood/general_supplies/durable_workwear.md>) | 作业人员劳保 |
| 收购 | [净水补给箱](<../../../01_CargoGood/general_supplies/potable_water_crates.md>) | 值守和日常作业补给 |

普通来源初始两日量、容量四日量，让初见站点有可装运库存，持续补货仍受本站用途约束。生活和低价原料按整柜或数柜组织，专业设备使用小批替换额度，不为了装满 S 柜而夸大每日仪器需求。

数量与价格为待实机平衡设计。新增站点数量会叠加区域供给和共享额度，不以单站看似很小就忽略总量；结算取整、签约修正、防护损耗和实际航程仍需验证。

[站点总览](<../../../07_贸易点/factory/林间制材所/00_总体说明.md>) · [资源表目录](<../../README.md>) · [贸易点目录](<../../../07_贸易点/README.md>)
