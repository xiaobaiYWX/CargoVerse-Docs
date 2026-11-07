# Levitite 混合液

> 当前内置数据，2026-11-07 专项细化。数值已写入数据包；实机航程平衡仍待验证。

## 身份与质量

| 项目 | 当前配置 |
| --- | --- |
| 源流体 | `aeronautics:levitite_blend` |
| 流动变体 | `aeronautics:flowing_levitite_blend` |
| 定位 | 轻质工业混合液 |
| 每桶质量 | 0.8 Kpg／1000 mB |
| 120 桶货重 | 96 Kpg |
| 240 桶货重 | 192 Kpg |
| 货类贴花 | `cargoverse:decal_processed_resource` |

两种注册身份参数相同，仍各有一份属性文件；不等于可以将不同 ID 混装。货重不含柜体，整批最终向上保留一位小数。

## 运输条件

无特殊运输条件。`transport_conditions` 明确为空；温度、压力、光照不产生本流体的条件损耗。

## 选柜与调整依据

Cistern 已满足本轮需求。

沿用每桶 0.8 Kpg 的正质量；不凭航空用途推导负质量、易爆、挥发或气压需求。

通用液体柜允许装载本流体，选柜差异通过保护效果体现。柜型的模板缺失状态以各型号文档为准，本页不替代模板验收。

## 当前配置

[源流体 JSON](<../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/aeronautics/cargoverse_fluid_properties/liquid/levitite_blend.json>) · [流动变体 JSON](<../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/aeronautics/cargoverse_fluid_properties/liquid/flowing_levitite_blend.json>)

```json
{
  "schema_version": 3,
  "form": "liquid",
  "mass_per_bucket": 0.8,
  "decal": "cargoverse:decal_processed_resource",
  "transport_conditions": {}
}
```

[流体总览](README.md) · [配置格式](<../../../04数据规范/运输属性/02_流体.md>)
