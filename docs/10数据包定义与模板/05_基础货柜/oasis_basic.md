# 绿洲农业联盟基础货柜

Verdant BioSystems（VBS）

[返回基础货柜目录](<README.md>)

| 项目 | 内容 |
| --- | --- |
| 基础权益 ID | `cargoverse:starter_containers/oasis_basic` |
| 基础定义 JSON | [oasis_basic.json](<../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/starter_containers/oasis_basic.json>) |
| 货柜定义 | [VBS Harvest 农鲜周转柜 S 型](<../03_货柜/绿洲农业联盟/Harvest 农鲜周转柜/harvest_lm_s.md>) |
| 完整型号 | `VBS-Harvest-LM-S` |
| 尺寸等级 | S |
| 领取占用调度点 | **0**（仅基础货柜资产） |
| 默认容量 / 空重 / 耐久 | 12 / 24 / 85（t / Kpg / 点） |
| 普通同型号调度点 | 1 |
| 起步用途 | 农业与农鲜周转 |
| 注册点 | [绿洲农业联盟](<../10_注册点/oasis_agriculture.md>) |
| 投放状态 | 已绑定现有默认资源贸易点 |
| 结构状态 | 正式模板已接入 |

每名玩家同时仅有一份当前注册机构的基础货柜权益。货柜通过注册终端领取，带 `starterContainer` 资产标记，不收取制造费用、库存材料或调度点。普通购买／制造的同型号不享受免点。旧存档中带此标记的资产也立即免点，设备快照仍保留当时型号参数。

## 当前 JSON

```json
{
  "schema_version": 1,
  "container_definition": "cargoverse:vbs/harvest_lm_s"
}
```
