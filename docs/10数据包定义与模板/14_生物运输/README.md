# 生物基础运输配置

现行路径：`data/<实体命名空间>/cargoverse_entity_properties/living/<实体路径>.json`。每个EntityType一份文件，schema_version固定为3、form固定为living。字段、示例及识别边界统一见[生物打包机](../../11玩家贸易点/07_生物打包机.md#运输json)，本目录不重复维护配置副本。

| 实体ID | 单只质量Kpg | 成年舱位 |
| --- | ---: | ---: |
| minecraft:chicken | 2 | 1 |
| minecraft:cow | 50 | 4 |
| minecraft:sheep | 20 | 3 |
| minecraft:pig | 25 | 3 |
| minecraft:zombie | 30 | 3 |

以上为已落入运行资源的识别验证参数，尚非正式平衡。五份配置暂不声明特殊运输条件，贴花使用decal_none。物种键只由EntityType确定，毛色、年龄、名字、生命和归属保留为个体状态，不另建属性文件或库存栏位。

无JSON不进入识别库存；配置有效不代表已支持捕获和原样恢复。运输尺寸、生活环境、携带内容与特殊适配尚待专项落地，后续工作见[生物运输设计](../../设计草案/生物运输设计.md)和[统一待办](../../设计草案/待完成事项清单.md#生物专项)。
