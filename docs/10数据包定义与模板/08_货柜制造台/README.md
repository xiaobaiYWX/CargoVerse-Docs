# 货柜制造台定义设计

> 24 个天空大站及 A／B 测试点固定配置制造台与一处生成点；地面小站不设制造服务，目录按专业生产和运输配套区分。[查看制造与运输设计](<制造服务分布与模块生成方案.md>)。原配方成本和门槛保留，24 个正式站点的目录及模块已同步数据包。

货柜制造台采用 v2 实体材料制造：玩家从主背包与快捷栏提供材料，并支付 VB 加工费；贸易点负责制造目录、繁荣门槛与生成位置，不提供制造材料库存。

## 本轮完整目录

[60 款配方与站点制造规划](<制造配方与投放总表.md>)给出材料、加工费、许可和繁荣基线；24 个正式制造站与两个测试点均附非空制造目录与 v2 JSON 定义，测试点单独计数。具体业务关系见[制造服务设计](<制造服务分布与模块生成方案.md>)和[100 项货物备柜路径](<运输任务与制造配套.md>)。系统已实现，24 站共 93 条配方已接入；A／B 测试点共用一份全 60 型号目录，正常保留材料、加工费与许可条件。

## 设计模板

```json
{
  "schema_version": 2,
  "display_name": "制造台名称",
  "recipes": [
    {
      "id": "recipe_id",
      "min_prosperity_level": 0,
      "required_license_level": "S",
      "cargo_container_definition": "namespace:path/to/container",
      "currency_cost": {
        "currency": "cargoverse:void_byte",
        "amount": 0
      },
      "item_costs": [
        {
          "ingredient": {
            "item": "minecraft:iron_ingot"
          },
          "count": 1
        }
      ]
    }
  ]
}
```

材料也可使用物品标签：

```json
{
  "ingredient": {
    "tag": "minecraft:planks"
  },
  "count": 8
}
```

## 配方设计表

| recipe ID | 货柜 ID | 最低繁荣 | 最低许可证 | VB 加工费 | 实体材料 |
| --- | --- | ---: | --- | ---: | --- |
|  |  |  |  |  | 物品／标签 × 数量 |

同一制造台定义内，一个货柜型号只能出现一次。每条配方必须填写 1～8 项材料；不设置纯 VB 或空材料入口。

## 当前实现定义

| 制造台 | 名称 | 配方数 |
| --- | --- | ---: |
| [cargoverse:market/test_station/all_containers](market/test_station/all_containers.md) | 测试全型号货柜制造目录（A／B 共用） | 60 |

[字段与运行规则](../../02贸易点系统/05_货柜制造台定义.md) · [实体物品制造方案](实体物品制造方案.md) · [后续配方设计依据](后续配方设计依据.md)
