# 生物基础运输配置

现行路径：`data/<实体命名空间>/cargoverse_entity_properties/living/<实体路径>.json`。每个EntityType一份文件，schema_version固定为3、form固定为living。字段、示例及识别边界统一见[生物打包机](../../11玩家贸易点/07_生物打包机.md#运输json)，本目录不重复维护配置副本。

| 实体ID | 单只质量Kpg | 成年舱位 |
| --- | ---: | ---: |
| minecraft:chicken | 2 | 1 |
| minecraft:cow | 50 | 4 |
| minecraft:sheep | 20 | 3 |
| minecraft:pig | 25 | 3 |
| minecraft:zombie | 30 | 3 |

以上为已落入运行资源的装卸验证参数，尚非正式平衡。五份配置暂不声明特殊运输条件，贴花使用decal_none。物种键只由EntityType确定，毛色、年龄、名字、生命和归属保留为个体状态，不另建属性文件或库存栏位。

无JSON不进入识别库存；已有配置仍须通过原生保存恢复、当前实体结构和权限检查，不能仅增加JSON便承诺任意模组兼容。`environment`默认`land`，可声明`water`，当前内置五种均为陆生。

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
