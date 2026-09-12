# 基础货柜制造台

| 项目 | 内容 |
| --- | --- |
| 资源 ID | `cargoverse:resource/general/default` |
| JSON 文件 | `src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/resource/general/default.json` |
| Schema 版本 | 1 |
| 显示名称 | 基础货柜制造台 |
| 配方数量 | 2 |

## 配方

### `atlas_sd_l`

| 货柜 | 最低繁荣 | 最低许可证 | 价格 | 结算单位 |
| --- | ---: | --- | ---: | --- |
| `cargoverse:aui/atlas_sd_l` | 3 | L | 320 VB | `cargoverse:void_byte` |

| match_mode | 标签 | 数量 |
| --- | --- | ---: |
| `any` | ingredient.chemical_material.compound_fertilizer | 8t |
| `any` | ingredient.energy_fuel.biomass_briquettes | 10t |

### `atlas_sd_s`

| 货柜 | 最低繁荣 | 最低许可证 | 价格 | 结算单位 |
| --- | ---: | --- | ---: | --- |
| `cargoverse:aui/atlas_sd_s` | 1 | S | 80 VB | `cargoverse:void_byte` |

| match_mode | 标签 | 数量 |
| --- | --- | ---: |
| `any` | ingredient.construction_material.bagged_cement | 8t |
| `any` | ingredient.raw_resource.hematite_ore | 10t |

## 设计说明

加工费与等级门槛已同步货柜 v3：Atlas S 为起步型号，Atlas L 需要 L 级许可及繁荣 3 级。库存材料沿用现有示例，尚未完成工业用料平衡。

当前仅这两个示例配方已配置，其余现役货柜的材料配方与节点投放仍待编制；参见[货柜目录](../../../03_货柜/README.md)。
