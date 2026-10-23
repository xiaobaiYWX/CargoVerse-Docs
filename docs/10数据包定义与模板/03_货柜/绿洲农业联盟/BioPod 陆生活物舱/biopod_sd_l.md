# VBS BioPod 陆生活物舱 L 型

> **【未实现／未开放制造】仅维护定义与设计目标；不提供该专项的完整运输、制造或交易能力。**

[绿洲农业联盟](<../README.md>) → [BioPod 陆生活物舱](<README.md>) → L 型

## 职责与使用边界

陆生活物的通风、空间与防逃逸舱；保留 S/M/L，等待明确的实体体型与环境规则。

- 目标形态：living 活物（明确陆生适配范围）。
- 当前 JSON 承载：未开放。
- 当前生效保护：无专用保护。
- 完整目标保护：防逃逸、通风、环境保温（目标）。
- 使用边界：不默认适合水生生物、所有实体或大体型；不作为普通干货柜。
- 典型内容：后续明确清单中的陆生小型与中型动物，按体型选 S/M/L。仅为例子，同形态同条件的物品不因行业或制造商被排除。
- 当前阶段：后续专项，未制造。

保护外观不等于程序效果。遮光、温控、生态维持和放射性屏蔽等未列入“当前生效保护”的部分只能作为后续结构预留，不能标成已经实装。

## 定义

| 项目 | 内容 |
| --- | --- |
| 资源 ID | `cargoverse:vbs/biopod_sd_l` |
| 定义文件 | [biopod_sd_l.json](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/vbs/biopod_sd_l.json>) |
| 制造商 | 绿洲农业联盟（`cargoverse:vbs`） |
| 系列 | BioPod 陆生活物舱 |
| 尺寸等级 | L |
| 普通调度点 | 4 |
| 结算单位 | `cargoverse:void_byte` |
| 标签 | `series.vbs.biopod`、`not_manufacturable`、`deferred_content` |

## 数值

| 指标 | 当前定义值 |
| --- | --- |
| 容量 | 未定义；专项计量待定，不是可用的 0 容量 |
| 空柜目标质量 | 150 Kpg |
| 分类容量修正 | 无，使用定义容量 |

空重为配置目标，实际基础质量取模板结构质量与配置空重的较大值；载货质量另算。型号 ID 的后缀不替代实际尺寸或接口。

## CargoClass 兼容与保护

当前不开放任何物品装载形态；目标载荷需等相应专项实现。

当前生效保护：无。

设计缺陷：无。未实现的目标保护不产生程序效果；准入与完整组件校验仍独立执行。

## 结构模板

| 项目 | 当前事实／制作目标 |
| --- | --- |
| 定义 | [cargoverse:vbs/biopod_sd_l](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/vbs/biopod_sd_l.json>) |
| 当前实际引用 | `cargoverse:cargo/aui/atlas/aui_atlas_sd_l` |
| 当前 NBT | [Atlas L 占位结构](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/aui/atlas/aui_atlas_sd_l.nbt>)；包络 13×6×6，体积 468；标准对接接口×6 |
| 专用路径建议 | `cargoverse:cargo/vbs/biopod/vbs_biopod_sd_l`；这是原候选／设计目标，不是已批准的分配结果 |
| 制作优先级 | 后续专项：先预留职责，不为未实现机制赶工 |
| 最终采用 | 待你分配；未切换运行引用 |

**原自用模板候选：** `cargoverse:cargo/vbs/biopod/vbs_biopod_sd_l` · [原 NBT 文件](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/vbs/biopod/vbs_biopod_sd_l.nbt>)。

只读结构检查：包络 11×6×7；标准对接接口×6；质量占位 2 个；分类占位 2 个；警示占位 10 个（槽号 0／1／2／3／4）；实体 0 个。这不是碰撞、实际质量、密封性或 Sable 连接验收。

## 制造与投放

当前无制造配方，不能把占位结构当作已开放产品。材料、费用、许可证和投放需在专项设计完成后明确，不从旧版成本或规格自动推导。

[统一制造与投放索引](<../../../08_货柜制造台/制造配方与投放总表.md>)。

## 当前 JSON

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/aui/atlas/aui_atlas_sd_l",
  "manufacturer": "cargoverse:vbs",
  "display_name": "VBS BioPod 陆生活物舱 L 型",
  "description": "临时使用对应规格 AUI 标准干柜结构；实际承载与保护以本定义为准。 本期未开放该内容形态。",
  "size_class": "L",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 4,
  "empty_mass": 150,
  "allowed_cargo_classes": [
    "living"
  ],
  "special_designs": [],
  "design_defects": [],
  "tags": [
    "series.vbs.biopod",
    "not_manufacturable",
    "deferred_content"
  ],
  "cargo_class_capacity_modifiers": {},
  "capacity": 0
}
```

## 验证边界

占位结构可加载不表示目标能力可用；专用模板、容量、保护、装卸和实机验证必须分别完成。已有物理货柜不因文档调整或重载自动换壳。

[返回系列](<README.md>) · [返回制造商](<../README.md>)
