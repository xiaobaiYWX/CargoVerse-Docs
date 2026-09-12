# 深岩矿业集团基础货柜

Deepcore Mining Corporation（DMC）

[返回基础货柜目录](<README.md>)

| 项目 | 内容 |
| --- | --- |
| 基础权益 ID | `cargoverse:starter_containers/dmc_basic` |
| 基础定义 JSON | [dmc_basic.json](<../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/starter_containers/dmc_basic.json>) |
| 货柜定义 | [DMC Boreal 矿冶散料柜 M 型](<../03_货柜/深岩矿业集团/Boreal 矿冶散料柜/boreal_sd_m.md>) |
| 完整型号 | `DMC-Boreal-SD-M` |
| 尺寸等级 | M |
| 领取占用调度点 | **0**（仅基础货柜资产） |
| 默认容量 / 空重 / 耐久 | 24 / 57.2 / 195（t / Kpg / 点） |
| 普通同型号调度点 | 2 |
| 起步用途 | 原矿与冶炼材料运输 |
| 注册点 | [深岩矿业集团](<../10_注册点/dmc_mining.md>) |
| 投放状态 | 注册点定义已提供，待同制造商贸易点绑定 |
| 结构状态 | 沿用已提供的正式结构 |

DMC 是唯一 M 级例外：沿用 Boreal M 的矿冶定位，基础领取不经过普通制造许可门槛。它比 S 级初始柜更重，需要足够的生成空间与载具承载；初始许可证仍为 S。

每名玩家同时仅有一份当前注册机构的基础货柜权益。货柜通过注册终端领取，带 `starterContainer` 资产标记，不收取制造费用、库存材料或调度点。普通购买／制造的同型号不享受免点。旧存档中带此标记的资产也立即免点，设备快照仍保留当时型号参数。

## 当前 JSON

```json
{
  "schema_version": 1,
  "container_definition": "cargoverse:dmc/boreal_sd_m"
}
```
