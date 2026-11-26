# A／B测试贸易点蓝图目录

A／B 指令测试站共用`cargoverse:market/test_station/all_containers`，当前覆盖65款普通货柜，8款初始货柜改由注册赠图。大型终端按此表收取打印费；材料不在打印阶段扣除。货柜结构、容量、质量与能力见[现行货柜定义](<../../../../02货柜/README.md>)，材料见[独立制造配方](<../../../../../04数据规范/货柜/02_制造配方.md>)。

单方块蓝图测试工具不使用此表；它自动枚举全部有效普通制造配方（排除初始型号），供创造玩家或管理员免费领取。

| 货柜定义 | 打印许可 | 制造商声望要求 | 打印费 VB（配方投影） |
| --- | --- | ---: | ---: |
| `cargoverse:aui/atlas_sd_l` | L | cargoverse:aui ≥ 2级 | 320 |
| `cargoverse:aui/atlas_sd_m` | M | cargoverse:aui ≥ 1级 | 160 |
| `cargoverse:aui/atlas_sd_s` | S | cargoverse:aui ≥ 0级 | 80 |
| `cargoverse:aui/atlas_sd_x` | X | cargoverse:aui ≥ 3级 | 560 |
| `cargoverse:aui/hermes_mc_l` | L | cargoverse:aui ≥ 2级 | 440 |
| `cargoverse:aui/hermes_mc_m` | M | cargoverse:aui ≥ 1级 | 220 |
| `cargoverse:aui/hermes_mc_s` | S | cargoverse:aui ≥ 0级 | 110 |
| `cargoverse:aui/titan_hd_l` | L | cargoverse:aui ≥ 2级 | 400 |
| `cargoverse:aui/titan_hd_x` | X | cargoverse:aui ≥ 3级 | 700 |
| `cargoverse:aui/titan_hd_xl` | XL | cargoverse:aui ≥ 4级 | 1200 |
| `cargoverse:aui/vulcan_sd_l` | L | cargoverse:aui ≥ 2级 | 560 |
| `cargoverse:aui/vulcan_sd_m` | M | cargoverse:aui ≥ 0级 | 280 |
| `cargoverse:aui/vulcan_sd_x` | X | cargoverse:aui ≥ 3级 | 980 |
| `cargoverse:bds/bastion_mc_l` | L | cargoverse:bds ≥ 2级 | 680 |
| `cargoverse:bds/bastion_mc_x` | X | cargoverse:bds ≥ 3级 | 1190 |
| `cargoverse:bds/fortress_hd_xl` | XL | cargoverse:bds ≥ 4级 | 2520 |
| `cargoverse:bds/sentinel_mc_m` | M | cargoverse:bds ≥ 1级 | 320 |
| `cargoverse:bds/sentinel_mc_s` | S | cargoverse:bds ≥ 0级 | 160 |
| `cargoverse:dmc/boreal_sd_l` | L | cargoverse:dmc ≥ 2级 | 400 |
| `cargoverse:dmc/boreal_sd_m` | M | cargoverse:dmc ≥ 0级 | 200 |
| `cargoverse:dmc/corevault_sd_m` | M | cargoverse:dmc ≥ 1级 | 300 |
| `cargoverse:dmc/corevault_sd_s` | S | cargoverse:dmc ≥ 0级 | 150 |
| `cargoverse:dmc/silo_sd_l` | L | cargoverse:dmc ≥ 2级 | 320 |
| `cargoverse:dmc/silo_sd_x` | X | cargoverse:dmc ≥ 3级 | 980 |
| `cargoverse:dmc/silo_sd_xl` | XL | cargoverse:dmc ≥ 4级 | 1680 |
| `cargoverse:dmc/titanhaul_hd_x` | X | cargoverse:dmc ≥ 3级 | 1050 |
| `cargoverse:dmc/titanhaul_hd_xl` | XL | cargoverse:dmc ≥ 4级 | 1800 |
| `cargoverse:hec/apollo_sd_l` | X | cargoverse:hec ≥ 2级 | 510 |
| `cargoverse:hec/apollo_sd_m` | L | cargoverse:hec ≥ 1级 | 260 |
| `cargoverse:hec/apollo_sd_s` | M | cargoverse:hec ≥ 0级 | 130 |
| `cargoverse:hec/boreas_hd_l` | L | cargoverse:hec ≥ 2级 | 400 |
| `cargoverse:hec/boreas_hd_m` | M | cargoverse:hec ≥ 1级 | 200 |
| `cargoverse:hec/boreas_hd_s` | S | cargoverse:hec ≥ 0级 | 100 |
| `cargoverse:hri/crucible_si_l` | L | cargoverse:hri ≥ 2级 | 440 |
| `cargoverse:hri/crucible_si_m` | M | cargoverse:hri ≥ 1级 | 220 |
| `cargoverse:hri/explorer_si_l` | L | cargoverse:hri ≥ 2级 | 920 |
| `cargoverse:hri/explorer_si_m` | M | cargoverse:hri ≥ 1级 | 460 |
| `cargoverse:hri/explorer_si_s` | S | cargoverse:hri ≥ 0级 | 230 |
| `cargoverse:rex/reliquary_lm_m` | M | cargoverse:rex ≥ 1级 | 200 |
| `cargoverse:rex/reliquary_lm_s` | S | cargoverse:rex ≥ 0级 | 100 |
| `cargoverse:rex/salvage_lm_l` | L | cargoverse:rex ≥ 2级 | 320 |
| `cargoverse:rex/salvage_lm_m` | M | cargoverse:rex ≥ 1级 | 160 |
| `cargoverse:rex/salvage_lm_s` | S | cargoverse:rex ≥ 0级 | 80 |
| `cargoverse:spl/cargo_mc_l` | L | cargoverse:spl ≥ 2级 | 280 |
| `cargoverse:spl/cistern_sd_l` | L | cargoverse:spl ≥ 2级 | 360 |
| `cargoverse:spl/cistern_sd_m` | M | cargoverse:spl ≥ 1级 | 180 |
| `cargoverse:spl/courier_mc_m` | M | cargoverse:spl ≥ 1级 | 120 |
| `cargoverse:spl/courier_mc_s` | S | cargoverse:spl ≥ 0级 | 60 |
| `cargoverse:spl/express_mc_s` | S | cargoverse:spl ≥ 0级 | 110 |
| `cargoverse:vbs/biopod_sd_l` | L | cargoverse:vbs ≥ 2级 | 640 |
| `cargoverse:vbs/biopod_sd_m` | M | cargoverse:vbs ≥ 1级 | 320 |
| `cargoverse:vbs/biopod_sd_s` | S | cargoverse:vbs ≥ 0级 | 160 |
| `cargoverse:vbs/harvest_lm_l` | L | cargoverse:vbs ≥ 2级 | 400 |
| `cargoverse:vbs/harvest_lm_m` | M | cargoverse:vbs ≥ 1级 | 200 |
| `cargoverse:vbs/harvest_lm_s` | S | cargoverse:vbs ≥ 0级 | 100 |
| `cargoverse:hec/boreas_hd_x` | X | cargoverse:hec ≥ 3级 | 800 |
| `cargoverse:hec/boreas_hd_xl` | XL | cargoverse:hec ≥ 4级 | 1400 |
| `cargoverse:spl/cistern_sd_x` | X | cargoverse:spl ≥ 3级 | 720 |
| `cargoverse:spl/cistern_sd_xl` | XL | cargoverse:spl ≥ 4级 | 1260 |
| `cargoverse:vbs/aquarium_sd_l` | L | cargoverse:vbs ≥ 2级 | 840 |
| `cargoverse:vbs/aquarium_sd_m` | M | cargoverse:vbs ≥ 1级 | 420 |
| `cargoverse:vbs/aquarium_sd_x` | X | cargoverse:vbs ≥ 3级 | 1680 |
| `cargoverse:vbs/aquarium_sd_xl` | XL | cargoverse:vbs ≥ 4级 | 2940 |
| `cargoverse:vbs/biopod_sd_x` | X | cargoverse:vbs ≥ 3级 | 1280 |
| `cargoverse:vbs/biopod_sd_xl` | XL | cargoverse:vbs ≥ 4级 | 2240 |
