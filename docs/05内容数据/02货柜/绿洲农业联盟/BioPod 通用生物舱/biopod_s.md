# VBS BioPod 通用生物舱 S 型

## 货柜介绍

BioPod用调温、稳压与基础缓冲照看VBS的生物货运。克隆培养站让出货名单迅速变长，饲养员也逐渐改用批次号区分那些过于相像的乘客。为小规模育种与安置准备。第一次迎来新成员的聚居地，常比运输人员更早守在卸货区。

## 型号与承载

| 项目 | 现行值 |
| --- | --- |
| 系列 | BioPod 通用生物舱 |
| 文档型号代号 | `vbs/biopod_s` |
| 规格 | S |
| 运输介质 | living |
| 容量 | 16 舱位 |
| 定义空重 | 6 Kpg |
| 调度点 | 1 |
| 接口 | 统一标准接口；型号代号不再包含接口缩写 |

容量按物种舱位占用计算，不直接等于可运输只数；所有已支持生物共用同一生物柜准入规则。

实际空重取定义空重与结构质量的较大值。表中数值不是结构实测质量，起吊与满载运输仍需实机验收。

## 保护能力

| 能力 | 配置 ID | 完整参数 |
| --- | --- | --- |
| 密封结构 | `cargoverse:sealing` | `{"level":1}` |
| 缓冲衬垫 | `cargoverse:cushioning` | `{"level":1,"velocity_change_bonus":2}` |
| 主动调温 | `cargoverse:thermal_control` | `{"level":1}` |
| 真空隔层 | `cargoverse:vacuum_insulation` | `{"level":1}` |
| 气压调节 | `cargoverse:pressure_control` | `{"level":1}` |
| 遮光结构 | `cargoverse:light_blocking` | `{"level":1,"reduction":15}` |

生物舱室：`{"max_entity_bytes":65536,"max_total_bytes":1048576}`。字节上限属于载荷保存约束，不是额外舱位。

容量修正：`{}`。运输条件与能力的对应规则见[能力规范](../../../../04数据规范/货柜/能力/README.md)。

## 模板与制作状态

| 项目 | 现行值 |
| --- | --- |
| 模板状态 | 已接入；发布文件存在，无缺失模板 |
| 模板资源 ID | `cargoverse:cargo/vbs/biopod_g2/vbs_biopod_g2_s` |
| 导出相对路径 | `generated/cargoverse/structures/cargo/g2/vbs/biopod/biopod_s.nbt` |
| 尺寸 X×Y×Z | 4×5×5 格 |
| 发布结构文件 | [NBT](../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/vbs/biopod_g2/vbs_biopod_g2_s.nbt) |

G2模板按本系列命名，不使用其他系列作占位。尺寸沿现有模板记录；对接、结构质量和满载表现仍按[实运验收](../../制作与实运验收.md)检查。

## 蓝图获取与制造

测试贸易点 A、测试贸易点 B

| 项目 | 当前要求 |
| --- | --- |
| 许可证 | S |
| 制造商声望 | cargoverse:vbs／0级 |
| 蓝图打印费 | 160 VB |
| 施工时间 | 400 tick（20 TPS时20秒） |

材料按实体物品件数消耗，打印阶段不扣材料。蓝图获取仍需满足所列许可证及声望要求。

| 层次 | 材料 | 件数 |
| --- | --- | ---: |
| 主材料 | 铁锭（`minecraft:iron_ingot`） | 32 |
| 辅材料 | 标准紧固件箱（`cargoverse:standard_fasteners`） | 8 |
| 辅材料 | 工业构件箱（`cargoverse:industrial_components`） | 4 |
| 特殊材料 | 生命维持组件（`cargoverse:life_support_module`） | 2 |

[产业物资获取与生产](../../../01运输物品/04_产业物资.md) · [共用制造规则](../../../03贸易点/蓝图投放/制造配方与投放总表.md)

## 运行资源对应

文档型号代号用于统一查阅和制作命名，**不是已注册的新资源ID**。本轮未迁移运行资源；指令、配方和数据包引用仍使用下列实际ID。旧名称不表示第二个产品系列或不同接口。

| 资源 | 当前 ID／来源 |
| --- | --- |
| 实际货柜定义 ID | `cargoverse:vbs/biopod_sd_s` · [JSON](../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/vbs/biopod_sd_s.json) |
| 制造配方 ID | `cargoverse:vbs/biopod_sd_s` · [JSON](../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_manufacturing_recipes/vbs/biopod_sd_s.json) |

<details>
<summary>完整现行货柜定义</summary>

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/vbs/biopod_g2/vbs_biopod_g2_s",
  "manufacturer": "cargoverse:vbs",
  "display_name": "VBS BioPod 通用生物舱 S 型",
  "description": "BioPod用调温、稳压与基础缓冲照看VBS的生物货运。克隆培养站让出货名单迅速变长，饲养员也逐渐改用批次号区分那些过于相像的乘客。为小规模育种与安置准备。第一次迎来新成员的聚居地，常比运输人员更早守在卸货区。",
  "size_class": "S",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 1,
  "empty_mass": 6,
  "allowed_cargo_classes": [
    "living"
  ],
  "tags": [
    "series.vbs.biopod",
    "validation_content"
  ],
  "cargo_class_capacity_modifiers": {},
  "capacity": 16,
  "living_chamber": {
    "max_entity_bytes": 65536,
    "max_total_bytes": 1048576
  },
  "abilities": {
    "cargoverse:sealing": {
      "level": 1
    },
    "cargoverse:cushioning": {
      "level": 1,
      "velocity_change_bonus": 2
    },
    "cargoverse:thermal_control": {
      "level": 1
    },
    "cargoverse:vacuum_insulation": {
      "level": 1
    },
    "cargoverse:pressure_control": {
      "level": 1
    },
    "cargoverse:light_blocking": {
      "level": 1,
      "reduction": 15
    }
  }
}
```

</details>

[本系列](README.md) · [制造商目录](../README.md)
