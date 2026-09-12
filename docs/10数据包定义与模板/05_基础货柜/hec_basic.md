# 赫利俄斯能源集团基础货柜

Helios Energy Corporation（HEC）

[返回基础货柜目录](<README.md>)

| 项目 | 内容 |
| --- | --- |
| 基础权益 ID | `cargoverse:starter_containers/hec_basic` |
| 基础定义 JSON | [hec_basic.json](<../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/starter_containers/hec_basic.json>) |
| 货柜定义 | [HEC Apollo 燃料化工柜 S 型](<../03_货柜/赫利俄斯能源集团/Apollo 燃料化工柜/apollo_sd_s.md>) |
| 完整型号 | `HEC-Apollo-SD-S` |
| 尺寸等级 | S |
| 领取占用调度点 | **0**（仅基础货柜资产） |
| 默认容量 / 空重 / 耐久 | 10 / 28 / 130（t / Kpg / 点） |
| 普通同型号调度点 | 1 |
| 起步用途 | 燃料与化工小批补给 |
| 注册点 | [赫利俄斯能源集团](<../10_注册点/hec_energy.md>) |
| 投放状态 | 注册点定义已提供，待同制造商贸易点绑定 |
| 结构状态 | 正式模板已接入 |

每名玩家同时仅有一份当前注册机构的基础货柜权益。货柜通过注册终端领取，带 `starterContainer` 资产标记，不收取制造费用、库存材料或调度点。普通购买／制造的同型号不享受免点。旧存档中带此标记的资产也立即免点，设备快照仍保留当时型号参数。

## 当前 JSON

```json
{
  "schema_version": 1,
  "container_definition": "cargoverse:hec/apollo_sd_s"
}
```
