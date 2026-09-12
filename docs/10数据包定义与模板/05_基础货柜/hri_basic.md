# 地平线研究院基础货柜

Horizon Research Institute（HRI）

[返回基础货柜目录](<README.md>)

| 项目 | 内容 |
| --- | --- |
| 基础权益 ID | `cargoverse:starter_containers/hri_basic` |
| 基础定义 JSON | [hri_basic.json](<../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/starter_containers/hri_basic.json>) |
| 货柜定义 | [HRI Explorer 科考样本舱 S 型](<../03_货柜/地平线研究院/Explorer 科考样本舱/explorer_si_s.md>) |
| 完整型号 | `HRI-Explorer-SI-S` |
| 尺寸等级 | S |
| 领取占用调度点 | **0**（仅基础货柜资产） |
| 默认容量 / 空重 / 耐久 | 6 / 26.4 / 162.5（t / Kpg / 点） |
| 普通同型号调度点 | 1 |
| 起步用途 | 样本与采样器材运输 |
| 注册点 | [地平线研究院](<../10_注册点/hri_research.md>) |
| 投放状态 | 注册点定义已提供，待同制造商贸易点绑定 |
| 结构状态 | 沿用已提供的正式结构 |

每名玩家同时仅有一份当前注册机构的基础货柜权益。货柜通过注册终端领取，带 `starterContainer` 资产标记，不收取制造费用、库存材料或调度点。普通购买／制造的同型号不享受免点。旧存档中带此标记的资产也立即免点，设备快照仍保留当时型号参数。

## 当前 JSON

```json
{
  "schema_version": 1,
  "container_definition": "cargoverse:hri/explorer_si_s"
}
```
