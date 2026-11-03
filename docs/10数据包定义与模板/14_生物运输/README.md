# 生物基础运输配置

现行路径：`data/<实体命名空间>/cargoverse_entity_properties/living/<实体路径>.json`。每个EntityType一份文件，schema_version固定为3、form固定为living。字段、示例及识别边界统一见[生物打包机](../../11玩家贸易点/07_生物打包机.md#运输json)，本目录不重复维护配置副本。

| 陆生实体 ID | Kpg／只 | 舱位／只 | 冲击耐受 |
| --- | ---: | ---: | ---: |
| minecraft:chicken | 0.5 | 1 | 12 |
| minecraft:cow | 8 | 4 | 16 |
| minecraft:goat | 3 | 3 | 20 |
| minecraft:mooshroom | 8 | 4 | 16 |
| minecraft:pig | 4 | 3 | 16 |
| minecraft:rabbit | 0.5 | 1 | 10 |
| minecraft:sheep | 3 | 3 | 16 |
| minecraft:zombie | 4 | 3 | 16 |

牲畜适温 5～50 TU、适压 0.7～1.3。单项持续超限 240 秒后每只扣 1 HP，此后每分钟扣 1 HP。僵尸要求光照 ≤5，持续超限 20 秒后每 10 秒扣 1 HP。冲击事件独立扣 1 HP。

## living_chamber

生物货柜在原定义中额外声明：

```json
"capacity": 16,
"living_chamber": {
  "environment": "land",
  "max_entity_bytes": 65536,
  "max_total_bytes": 1048576
}
```

`capacity`为总舱位，不是只数；大体型物种在实体JSON中配置更高的`space_units`，不另配长宽高。不再配置`max_entities`，只数由舱位计算；单体字节上限1024～262144，默认65536；整柜按包含UUID、生命等包装的个体记录累计计费；总字节上限不小于单体上限，最大4194304，默认1048576。环境必填，未知字段拒绝。非生物柜不允许声明舱室。装载后冻结舱室及实体规则，重载不追改在途载荷。

具体装卸、贸易、生命周期和验证柜参数见[生物运输](../../01货柜系统/01核心系统/17_生物运输.md)。水生环境与其他后续项目见[统一待办](../../设计草案/待完成事项清单.md#生物专项)。
