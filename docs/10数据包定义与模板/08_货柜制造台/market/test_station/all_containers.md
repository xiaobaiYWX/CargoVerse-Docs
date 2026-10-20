# 测试全型号货柜制造目录

A、B 共用 `cargoverse:market/test_station/all_containers`，覆盖全部 60 个 cargo_containers 定义。逐型号的材料、加工费、许可证和繁荣门槛完整取自正式天空站配方，重复型号须完全一致才允许合并。测试点初始繁荣为满级，材料、资金、许可证、调度点与净空校验正常执行。

| 货柜定义 | 配方 ID | 许可证 | 最低繁荣 | 加工费（VB） |
| --- | --- | --- | --- | --- |
| `cargoverse:aui/atlas_sd_l` | `aui_atlas_sd_l` | L | 2 | 320 |
| `cargoverse:aui/atlas_sd_m` | `aui_atlas_sd_m` | M | 1 | 160 |
| `cargoverse:aui/atlas_sd_s` | `aui_atlas_sd_s` | S | 0 | 80 |
| `cargoverse:aui/atlas_sd_x` | `aui_atlas_sd_x` | X | 3 | 560 |
| `cargoverse:aui/hermes_mc_l` | `aui_hermes_mc_l` | L | 2 | 400 |
| `cargoverse:aui/hermes_mc_m` | `aui_hermes_mc_m` | M | 1 | 200 |
| `cargoverse:aui/hermes_mc_s` | `aui_hermes_mc_s` | S | 0 | 100 |
| `cargoverse:aui/nomad_hd_l` | `aui_nomad_hd_l` | L | 2 | 560 |
| `cargoverse:aui/nomad_hd_m` | `aui_nomad_hd_m` | M | 0 | 280 |
| `cargoverse:aui/nomad_hd_x` | `aui_nomad_hd_x` | X | 3 | 980 |
| `cargoverse:aui/titan_hd_l` | `aui_titan_hd_l` | L | 2 | 400 |
| `cargoverse:aui/titan_hd_x` | `aui_titan_hd_x` | X | 3 | 700 |
| `cargoverse:aui/titan_hd_xl` | `aui_titan_hd_xl` | XL | 4 | 1200 |
| `cargoverse:aui/vulcan_sd_l` | `aui_vulcan_sd_l` | L | 2 | 480 |
| `cargoverse:aui/vulcan_sd_m` | `aui_vulcan_sd_m` | M | 0 | 240 |
| `cargoverse:aui/vulcan_sd_x` | `aui_vulcan_sd_x` | X | 3 | 840 |
| `cargoverse:bds/bastion_mc_l` | `bds_bastion_mc_l` | L | 2 | 600 |
| `cargoverse:bds/bastion_mc_x` | `bds_bastion_mc_x` | X | 3 | 1050 |
| `cargoverse:bds/fortress_hd_xl` | `bds_fortress_hd_xl` | XL | 4 | 2280 |
| `cargoverse:bds/sentinel_mc_m` | `bds_sentinel_mc_m` | M | 1 | 280 |
| `cargoverse:bds/sentinel_mc_s` | `bds_sentinel_mc_s` | S | 0 | 140 |
| `cargoverse:dmc/boreal_sd_l` | `dmc_boreal_sd_l` | L | 2 | 360 |
| `cargoverse:dmc/boreal_sd_m` | `dmc_boreal_sd_m` | M | 0 | 180 |
| `cargoverse:dmc/corevault_sd_m` | `dmc_corevault_sd_m` | M | 1 | 280 |
| `cargoverse:dmc/corevault_sd_s` | `dmc_corevault_sd_s` | S | 0 | 140 |
| `cargoverse:dmc/titanhaul_hd_l` | `dmc_titanhaul_hd_l` | L | 2 | 560 |
| `cargoverse:dmc/titanhaul_hd_x` | `dmc_titanhaul_hd_x` | X | 3 | 980 |
| `cargoverse:dmc/titanhaul_hd_xl` | `dmc_titanhaul_hd_xl` | XL | 4 | 1680 |
| `cargoverse:hec/apollo_sd_l` | `hec_apollo_sd_l` | L | 2 | 440 |
| `cargoverse:hec/apollo_sd_m` | `hec_apollo_sd_m` | M | 1 | 220 |
| `cargoverse:hec/apollo_sd_s` | `hec_apollo_sd_s` | S | 0 | 110 |
| `cargoverse:hec/cryovault_sd_l` | `hec_cryovault_sd_l` | L | 2 | 560 |
| `cargoverse:hec/cryovault_sd_m` | `hec_cryovault_sd_m` | M | 1 | 280 |
| `cargoverse:hec/cryovault_sd_s` | `hec_cryovault_sd_s` | S | 0 | 140 |
| `cargoverse:hec/reactor_hd_l` | `hec_reactor_hd_l` | L | 2 | 800 |
| `cargoverse:hec/reactor_hd_m` | `hec_reactor_hd_m` | M | 0 | 400 |
| `cargoverse:hec/reactor_hd_x` | `hec_reactor_hd_x` | X | 3 | 1400 |
| `cargoverse:hec/reclaimer_sd_l` | `hec_reclaimer_sd_l` | L | 2 | 360 |
| `cargoverse:hec/reclaimer_sd_m` | `hec_reclaimer_sd_m` | M | 0 | 180 |
| `cargoverse:hri/archive_si_m` | `hri_archive_si_m` | M | 1 | 400 |
| `cargoverse:hri/archive_si_s` | `hri_archive_si_s` | S | 0 | 200 |
| `cargoverse:hri/explorer_si_l` | `hri_explorer_si_l` | L | 2 | 720 |
| `cargoverse:hri/explorer_si_m` | `hri_explorer_si_m` | M | 1 | 360 |
| `cargoverse:hri/explorer_si_s` | `hri_explorer_si_s` | S | 0 | 180 |
| `cargoverse:rex/salvage_lm_l` | `rex_salvage_lm_l` | L | 2 | 280 |
| `cargoverse:rex/salvage_lm_m` | `rex_salvage_lm_m` | M | 1 | 140 |
| `cargoverse:rex/salvage_lm_s` | `rex_salvage_lm_s` | S | 0 | 70 |
| `cargoverse:spl/cargo_mc_l` | `spl_cargo_mc_l` | L | 2 | 280 |
| `cargoverse:spl/cargo_mc_m` | `spl_cargo_mc_m` | M | 1 | 140 |
| `cargoverse:spl/courier_mc_m` | `spl_courier_mc_m` | M | 1 | 120 |
| `cargoverse:spl/courier_mc_s` | `spl_courier_mc_s` | S | 0 | 60 |
| `cargoverse:spl/express_mc_s` | `spl_express_mc_s` | S | 0 | 90 |
| `cargoverse:vbs/biopod_sd_l` | `vbs_biopod_sd_l` | L | 2 | 480 |
| `cargoverse:vbs/biopod_sd_m` | `vbs_biopod_sd_m` | M | 1 | 240 |
| `cargoverse:vbs/biopod_sd_s` | `vbs_biopod_sd_s` | S | 0 | 120 |
| `cargoverse:vbs/eden_hd_x` | `vbs_eden_hd_x` | X | 3 | 1050 |
| `cargoverse:vbs/eden_hd_xl` | `vbs_eden_hd_xl` | XL | 4 | 1800 |
| `cargoverse:vbs/harvest_lm_l` | `vbs_harvest_lm_l` | L | 2 | 360 |
| `cargoverse:vbs/harvest_lm_m` | `vbs_harvest_lm_m` | M | 1 | 180 |
| `cargoverse:vbs/harvest_lm_s` | `vbs_harvest_lm_s` | S | 0 | 90 |

实体材料的唯一运行定义为 `trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/market/test_station/all_containers.json`，对应正式设计见[制造配方总表](<../../制造配方与投放总表.md>)。该目录只供测试，两站各显示完整 60 款，不计入正式站点的 93 条配方统计。

增加货柜型号或配方后，同步维护本目录 JSON 与本文档，并运行制造资源回归检查；调整测试商品则维护两站 schema 3 资源表与对应文档。旧抽象货物测试站生成器已移除，不再从 `cargo_goods` 重建目录，也不自动改写正式站点、原始模板或自然结构集。

[测试 A](<../../../07_贸易点/market/测试贸易点A/00_总体说明.md>) · [测试 B](<../../../07_贸易点/market/测试贸易点B/00_总体说明.md>)
