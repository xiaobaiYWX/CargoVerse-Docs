# VBS Aquarium 加强缓冲生物舱 M 型

## 货柜介绍

Aquarium在生物舱的温压调节之外安排了更充分的缓冲。绿洲农业联盟接受较少的舱位，换取运输中对颠簸的更多照顾；这个名字也被沿用至今。面向需要谨慎转运的小批生物。接收者关心的第一件事，通常不是这趟航程有没有准点。

## 型号与承载

| 项目 | 现行值 |
| --- | --- |
| 系列 | Aquarium 加强缓冲生物舱 |
| 文档型号代号 | `vbs/aquarium_m` |
| 规格 | M |
| 运输介质 | living |
| 容量 | 16 舱位 |
| 定义空重 | 17 Kpg |
| 调度点 | 2 |
| 接口 | 统一标准接口；型号代号不再包含接口缩写 |

容量按物种舱位占用计算，不直接等于可运输只数；所有已支持生物共用同一生物柜准入规则。

实际空重取定义空重与结构质量的较大值。表中数值不是结构实测质量，起吊与满载运输仍需实机验收。

## 保护能力

| 能力 | 配置 ID | 完整参数 |
| --- | --- | --- |
| 密封结构 | `cargoverse:sealing` | `{"level":1}` |
| 缓冲衬垫 | `cargoverse:cushioning` | `{"level":2,"velocity_change_bonus":5}` |
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
| 模板资源 ID | `cargoverse:cargo/vbs/aquarium_g2/vbs_aquarium_g2_m` |
| 导出相对路径 | `generated/cargoverse/structures/cargo/g2/vbs/aquarium/aquarium_m.nbt` |
| 尺寸 X×Y×Z | 8×5×5 格 |
| 发布结构文件 | [NBT](../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/vbs/aquarium_g2/vbs_aquarium_g2_m.nbt) |

G2模板按本系列命名，不使用其他系列作占位。尺寸沿现有模板记录；对接、结构质量和满载表现仍按[实运验收](../../制作与实运验收.md)检查。

## 蓝图获取与制造

测试贸易点 A、测试贸易点 B

| 项目 | 当前要求 |
| --- | --- |
| 许可证 | M |
| 制造商声望 | cargoverse:vbs／1级 |
| 蓝图打印费 | 420 VB |
| 施工时间 | 400 tick（20 TPS时20秒） |

材料按实体物品件数消耗，打印阶段不扣材料。蓝图获取仍需满足所列许可证及声望要求。

| 层次 | 材料 | 件数 |
| --- | --- | ---: |
| 主材料 | 铁锭（`minecraft:iron_ingot`） | 64 |
| 辅材料 | 标准紧固件箱（`cargoverse:standard_fasteners`） | 16 |
| 辅材料 | 工业构件箱（`cargoverse:industrial_components`） | 8 |
| 特殊材料 | 生命维持组件（`cargoverse:life_support_module`） | 4 |
| 特殊材料 | 缓冲组件（`cargoverse:cushioning_module`） | 2 |

[产业物资获取与生产](../../../01运输物品/04_产业物资.md) · [共用制造规则](../../../03贸易点/蓝图投放/制造配方与投放总表.md)

## 运行资源对应

文档型号代号用于统一查阅和制作命名，**不是已注册的新资源ID**。本轮未迁移运行资源；指令、配方和数据包引用仍使用下列实际ID。旧名称不表示第二个产品系列或不同接口。

| 资源 | 当前 ID／来源 |
| --- | --- |
| 实际货柜定义 ID | `cargoverse:vbs/aquarium_sd_m` · [JSON](../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/vbs/aquarium_sd_m.json) |
| 制造配方 ID | `cargoverse:vbs/aquarium_sd_m` · [JSON](../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_manufacturing_recipes/vbs/aquarium_sd_m.json) |

<details>
<summary>完整现行货柜定义</summary>

```json
{
  "schema_version": 1,
  "manufacturer": "cargoverse:vbs",
  "trade_currency": "cargoverse:void_byte",
  "template": "cargoverse:cargo/vbs/aquarium_g2/vbs_aquarium_g2_m",
  "display_name": "VBS Aquarium 加强缓冲生物舱 M 型",
  "description": "Aquarium在生物舱的温压调节之外安排了更充分的缓冲。绿洲农业联盟接受较少的舱位，换取运输中对颠簸的更多照顾；这个名字也被沿用至今。面向需要谨慎转运的小批生物。接收者关心的第一件事，通常不是这趟航程有没有准点。",
  "size_class": "M",
  "dispatch_points": 2,
  "empty_mass": 17,
  "allowed_cargo_classes": [
    "living"
  ],
  "cargo_class_capacity_modifiers": {},
  "tags": [
    "series.vbs.aquarium"
  ],
  "capacity": 16,
  "abilities": {
    "cargoverse:sealing": {
      "level": 1
    },
    "cargoverse:cushioning": {
      "level": 2,
      "velocity_change_bonus": 5
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
  },
  "living_chamber": {
    "max_entity_bytes": 65536,
    "max_total_bytes": 1048576
  }
}
```

</details>

[本系列](README.md) · [制造商目录](../README.md)
