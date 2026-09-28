# 货柜制造台定义设计

> 制造投放已调整为固定品牌中心＋概率工坊，部分贸易点不再提供制造服务；[查看分布与模板生成方案](<制造服务分布与模块生成方案.md>)。原型号材料与加工费保持不变。

货柜制造台采用 v2 实体材料制造：玩家从主背包与快捷栏提供材料，并支付 VB 加工费；贸易点负责制造目录、繁荣门槛与生成位置，不提供制造材料库存。

## 本轮完整目录

[60 款统一配方与 站点制造功能规划](<制造配方与投放总表.md>)：已给出材料、加工费、许可、繁荣与各站完整 v2 JSON。系统已实现，新增内容仍待接入；当前实装定义见页末。各贸易点内的 `货柜制造台定义.md` 已替换旧纯 VB 出售草案。

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
| [cargoverse:resource/general/default](resource/general/default.md) | 基础货柜制造台 | 1 |

[字段与运行规则](../../02贸易点系统/05_货柜制造台定义.md) · [实体物品制造方案](实体物品制造方案.md) · [后续配方设计依据](后续配方设计依据.md)
