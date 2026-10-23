# HRI Crucible 衬层液体罐柜 L 型

> **【基础液体业务已接入】专用结构及液体材料保护仍待完善，当前使用 AUI 占位结构。**

[地平线研究院](<../README.md>) → [Crucible 衬层液体罐柜](<README.md>) → L 型

## 职责与使用边界

HRI 以接触材料研究和异常样本封存形成衬层液体罐；面向所有明确兼容介质，与 SPL Cistern 竞争普通液体，同时处理指定腐蚀介质。

- 目标形态：liquid 液体（明确衬层适配范围）。
- 当前 JSON 承载：仅 liquid 液体。
- 当前生效保护：无专用保护。
- 完整目标保护：液密、指定接触材质兼容、防冻结（目标）。
- 使用边界：当前与 Cistern 同样按液体介质准入，未实现衬层材料白名单或腐蚀保护；目标耐受范围须另行设计，不作为气体罐。
- 典型内容：明确已适配的腐蚀性液体，普通水等兼容介质亦可。仅为例子，同形态同条件的物品不因行业或制造商被排除。
- 当前阶段：可制造及装卸；M/L 容量暂定120/240桶。

保护外观不等于程序效果。遮光、温控、生态维持和放射性屏蔽等未列入“当前生效保护”的部分只能作为后续结构预留，不能标成已经实装。

## 定义

| 项目 | 内容 |
| --- | --- |
| 资源 ID | `cargoverse:hri/crucible_si_l` |
| 定义文件 | [crucible_si_l.json](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/hri/crucible_si_l.json>) |
| 制造商 | 地平线研究院（`cargoverse:hri`） |
| 系列 | Crucible 衬层液体罐柜 |
| 尺寸等级 | L |
| 普通调度点 | 4 |
| 结算单位 | `cargoverse:void_byte` |
| 标签 | `series.hri.crucible` |

## 数值

| 指标 | 当前定义值 |
| --- | --- |
| 容量 | 定义 240，实际 240000mB（暂定） |
| 空柜目标质量 | 170 Kpg |
| 分类容量修正 | 无，使用定义容量 |

空重为配置目标，实际基础质量取模板结构质量与配置空重的较大值；载货质量另算。型号 ID 的后缀不替代实际尺寸或接口。

## CargoClass 兼容与保护

只允许液体，不装固体、气体或活体；完整组件变体不可混装。

当前生效保护：无。

设计缺陷：无。未实现的目标保护不产生程序效果；准入与完整组件校验仍独立执行。

## 结构模板

| 项目 | 当前事实／制作目标 |
| --- | --- |
| 定义 | [cargoverse:hri/crucible_si_l](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/hri/crucible_si_l.json>) |
| 当前实际引用 | `cargoverse:cargo/aui/atlas/aui_atlas_sd_l` |
| 当前 NBT | [Atlas L 占位结构](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/aui/atlas/aui_atlas_sd_l.nbt>)；包络 13×6×6，体积 468；标准对接接口×6 |
| 专用路径建议 | `cargoverse:cargo/hri/crucible/hri_crucible_si_l`；这是原候选／设计目标，不是已批准的分配结果 |
| 制作优先级 | 后续专项：先预留职责，不为未实现机制赶工 |
| 最终采用 | 待你分配；未切换运行引用 |

**无本型号原专用 NBT。** 当前能引用 Atlas 只表示占位可加载，不能当作粉料柜／封存柜／罐体等职责已经在模型中完成。

## 制造与投放

测试全型号制造目录已添加同规格基线配方；正式投放和费用仍待平衡。占位结构不等于专用罐体模型已完成。

[统一制造与投放索引](<../../../08_货柜制造台/制造配方与投放总表.md>)。

## 当前 JSON

```json
{
  "schema_version": 1,
  "manufacturer": "cargoverse:hri",
  "trade_currency": "cargoverse:void_byte",
  "template": "cargoverse:cargo/aui/atlas/aui_atlas_sd_l",
  "display_name": "HRI Crucible 衬层液体罐柜 L 型",
  "description": "液体运输罐柜；容量按1000mB为一个单位，实际载荷与保护由数据包定义。",
  "size_class": "L",
  "dispatch_points": 4,
  "empty_mass": 170,
  "allowed_cargo_classes": [
    "liquid"
  ],
  "cargo_class_capacity_modifiers": {},
  "special_designs": [],
  "design_defects": [],
  "tags": [
    "series.hri.crucible"
  ],
  "capacity": 240
}
```

## 验证边界

占位结构可加载不表示目标能力可用；基础容量与装卸已落地；专用模板、材料保护和实机验证仍分别推进。已有物理货柜不因文档调整或重载自动换壳。

[返回系列](<README.md>) · [返回制造商](<../README.md>)
