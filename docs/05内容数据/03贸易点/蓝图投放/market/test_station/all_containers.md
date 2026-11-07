# A／B测试贸易点蓝图目录

A／B 指令测试站共用`cargoverse:market/test_station/all_containers`，当前覆盖62款可制造货柜。大型终端按此表收取打印费；材料不在打印阶段扣除。货柜结构、容量、质量与能力见[现行货柜定义](<../../../../02货柜/README.md>)，材料见[独立制造配方](<../../../../../04数据规范/货柜/02_制造配方.md>)。

单方块蓝图测试工具不使用此表；它自动枚举全部有效制造配方，供创造玩家或管理员免费领取。

| 货柜定义 | 打印许可 | 最低繁荣 | 打印费 VB（配方投影） |
| --- | --- | ---: | ---: |
| `cargoverse:aui/atlas_sd_l` | L | 2 | 320 |
| `cargoverse:aui/atlas_sd_m` | M | 1 | 160 |
| `cargoverse:aui/atlas_sd_s` | S | 0 | 80 |
| `cargoverse:aui/atlas_sd_x` | X | 3 | 560 |
| `cargoverse:aui/hermes_mc_l` | L | 2 | 440 |
| `cargoverse:aui/hermes_mc_m` | M | 1 | 220 |
| `cargoverse:aui/hermes_mc_s` | S | 0 | 110 |
| `cargoverse:aui/titan_hd_l` | L | 2 | 400 |
| `cargoverse:aui/titan_hd_x` | X | 3 | 700 |
| `cargoverse:aui/titan_hd_xl` | XL | 4 | 1200 |
| `cargoverse:aui/vulcan_sd_l` | L | 2 | 560 |
| `cargoverse:aui/vulcan_sd_m` | M | 0 | 280 |
| `cargoverse:aui/vulcan_sd_x` | X | 3 | 980 |
| `cargoverse:bds/bastion_mc_l` | L | 2 | 680 |
| `cargoverse:bds/bastion_mc_x` | X | 3 | 1190 |
| `cargoverse:bds/fortress_hd_xl` | XL | 4 | 2520 |
| `cargoverse:bds/sentinel_mc_m` | M | 1 | 320 |
| `cargoverse:bds/sentinel_mc_s` | S | 0 | 160 |
| `cargoverse:dmc/boreal_sd_l` | L | 2 | 400 |
| `cargoverse:dmc/boreal_sd_m` | M | 0 | 200 |
| `cargoverse:dmc/corevault_sd_m` | M | 1 | 300 |
| `cargoverse:dmc/corevault_sd_s` | S | 0 | 150 |
| `cargoverse:dmc/silo_sd_l` | L | 2 | 320 |
| `cargoverse:dmc/silo_sd_x` | X | 3 | 980 |
| `cargoverse:dmc/silo_sd_xl` | XL | 4 | 1680 |
| `cargoverse:dmc/titanhaul_hd_x` | X | 3 | 1050 |
| `cargoverse:dmc/titanhaul_hd_xl` | XL | 4 | 1800 |
| `cargoverse:hec/apollo_sd_l` | X | 2 | 510 |
| `cargoverse:hec/apollo_sd_m` | L | 1 | 260 |
| `cargoverse:hec/apollo_sd_s` | M | 0 | 130 |
| `cargoverse:hec/boreas_hd_l` | L | 2 | 400 |
| `cargoverse:hec/boreas_hd_m` | M | 1 | 200 |
| `cargoverse:hri/crucible_si_l` | L | 2 | 440 |
| `cargoverse:hri/crucible_si_m` | M | 1 | 220 |
| `cargoverse:hri/explorer_si_l` | L | 2 | 920 |
| `cargoverse:hri/explorer_si_m` | M | 1 | 460 |
| `cargoverse:hri/explorer_si_s` | S | 0 | 230 |
| `cargoverse:rex/reliquary_lm_m` | M | 1 | 200 |
| `cargoverse:rex/reliquary_lm_s` | S | 0 | 100 |
| `cargoverse:rex/salvage_lm_l` | L | 2 | 320 |
| `cargoverse:rex/salvage_lm_m` | M | 1 | 160 |
| `cargoverse:rex/salvage_lm_s` | S | 0 | 80 |
| `cargoverse:spl/cargo_mc_l` | L | 2 | 280 |
| `cargoverse:spl/cistern_sd_l` | L | 2 | 360 |
| `cargoverse:spl/cistern_sd_m` | M | 1 | 180 |
| `cargoverse:spl/courier_mc_m` | M | 1 | 120 |
| `cargoverse:spl/courier_mc_s` | S | 0 | 60 |
| `cargoverse:spl/express_mc_s` | S | 0 | 110 |
| `cargoverse:vbs/biopod_sd_l` | L | 2 | 640 |
| `cargoverse:vbs/biopod_sd_m` | M | 1 | 320 |
| `cargoverse:vbs/biopod_sd_s` | S | 0 | 160 |
| `cargoverse:vbs/harvest_lm_l` | L | 2 | 400 |
| `cargoverse:vbs/harvest_lm_m` | M | 1 | 200 |
| `cargoverse:vbs/harvest_lm_s` | S | 0 | 100 |
| `cargoverse:aui/starter_atlas_sd_s` | S | 0 | 0 |
| `cargoverse:bds/starter_sentinel_mc_s` | S | 0 | 0 |
| `cargoverse:dmc/starter_boreal_sd_m` | M | 0 | 0 |
| `cargoverse:hec/starter_apollo_sd_s` | M | 0 | 0 |
| `cargoverse:hri/starter_explorer_si_s` | S | 0 | 0 |
| `cargoverse:rex/starter_salvage_lm_s` | S | 0 | 0 |
| `cargoverse:spl/starter_courier_mc_s` | S | 0 | 0 |
| `cargoverse:vbs/starter_harvest_lm_s` | S | 0 | 0 |
