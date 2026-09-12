# 遗民贸易协会基础货柜

Remnant Exchange（REX）

[返回基础货柜目录](<README.md>)

| 项目 | 内容 |
| --- | --- |
| 基础权益 ID | `cargoverse:starter_containers/rex_basic` |
| 基础定义 JSON | [rex_basic.json](<../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/starter_containers/rex_basic.json>) |
| 货柜定义 | [REX Salvage 旧世打捞柜 S 型](<../03_货柜/遗民贸易协会/Salvage 旧世打捞柜/salvage_lm_s.md>) |
| 完整型号 | `REX-Salvage-LM-S` |
| 尺寸等级 | S |
| 领取占用调度点 | **0**（仅基础货柜资产） |
| 默认容量 / 空重 / 耐久 | 9 / 22 / 80（t / Kpg / 点） |
| 普通同型号调度点 | 1 |
| 起步用途 | 旧世遗物与稀材运输 |
| 注册点 | [遗民贸易协会](<../10_注册点/rex_exchange.md>) |
| 投放状态 | 注册点定义已提供，待同制造商贸易点绑定 |
| 结构状态 | 沿用已提供的正式结构 |

每名玩家同时仅有一份当前注册机构的基础货柜权益。货柜通过注册终端领取，带 `starterContainer` 资产标记，不收取制造费用、库存材料或调度点。普通购买／制造的同型号不享受免点。旧存档中带此标记的资产也立即免点，设备快照仍保留当时型号参数。

## 当前 JSON

```json
{
  "schema_version": 1,
  "container_definition": "cargoverse:rex/salvage_lm_s"
}
```
