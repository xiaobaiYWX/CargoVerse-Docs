# 天穹联合工业基础货柜

Aether Union Industries（AUI）

[返回基础货柜目录](<README.md>)

| 项目             | 内容                                                                                                                              |
| -------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| 基础权益 ID        | `cargoverse:starter_containers/aui_basic`                                                                                       |
| 基础定义 JSON      | [aui_basic.json](<../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/starter_containers/aui_basic.json>) |
| 货柜定义           | [AUI Atlas 标准干货柜 S 型](<../03_货柜/天穹联合工业/Atlas 标准干货柜/atlas_sd_s.md>)                                                              |
| 完整型号           | `AUI-Atlas-SD-S`                                                                                                                |
| 尺寸等级           | S                                                                                                                               |
| 领取占用调度点        | **0**（仅基础货柜资产）                                                                                                                  |
| 默认容量 / 空重 / 耐久 | 11 / 20 / 100（t / Kpg / 点）                                                                                                      |
| 普通同型号调度点       | 1                                                                                                                               |
| 起步用途           | 通用工业与航运起步                                                                                                                       |
| 注册点            | [天穹联合工业](<../10_注册点/aui_industry.md>)                                                                                           |
| 投放状态           | 注册点定义已提供，待同制造商贸易点绑定                                                                                                             |
| 结构状态           | 沿用已提供的正式结构                                                                                                                      |

每名玩家同时仅有一份当前注册机构的基础货柜权益。货柜通过注册终端领取，带 `starterContainer` 资产标记，不收取制造费用、库存材料或调度点。普通购买／制造的同型号不享受免点。旧存档中带此标记的资产也立即免点，设备快照仍保留当时型号参数。

## 当前 JSON

```json
{
  "schema_version": 1,
  "container_definition": "cargoverse:aui/atlas_sd_s"
}
```
