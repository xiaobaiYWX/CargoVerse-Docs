# HRI Explorer 环境样品柜 M 型

## 货柜介绍

Explorer为研究院样品调节温压并遮光。运单常把保存条件写得很细，项目名称却只有编号；有时接收它的研究员也没有权限知道更多。用于将一处调查区域的样品集中送回。样品编号彼此相邻，结论却未必相同。

## 型号与承载

| 项目 | 现行值 |
| --- | --- |
| 系列 | Explorer 环境样品柜 |
| 文档型号代号 | `hri/explorer_m` |
| 规格 | M |
| 运输介质 | solid |
| 容量 | 4096 件 |
| 定义空重 | 60 Kpg |
| 调度点 | 2 |
| 接口 | 统一标准接口；型号代号不再包含接口缩写 |

容量按单件计数，组只决定装卸步长。最大堆叠64时满载为64组；每件0.1 Kpg的货物装满后货重409.6 Kpg，不含柜体。

实际空重取定义空重与结构质量的较大值。表中数值不是结构实测质量，起吊与满载运输仍需实机验收。

## 保护能力

| 能力 | 配置 ID | 完整参数 |
| --- | --- | --- |
| 气压调节 | `cargoverse:pressure_control` | `{"level":1}` |
| 主动调温 | `cargoverse:thermal_control` | `{"level":1}` |
| 遮光结构 | `cargoverse:light_blocking` | `{"level":1,"reduction":15}` |

容量修正：`{}`。运输条件与能力的对应规则见[能力规范](../../../../04数据规范/货柜/能力/README.md)。

## 模板与制作状态

| 项目 | 现行值 |
| --- | --- |
| 模板状态 | 已接入；发布文件存在，无缺失模板 |
| 模板资源 ID | `cargoverse:cargo/hri/explorer_g2/hri_explorer_g2_m` |
| 导出相对路径 | `generated/cargoverse/structures/cargo/g2/gri/explorer/explorer_m.nbt` |
| 尺寸 X×Y×Z | 8×5×5 格 |
| 发布结构文件 | [NBT](../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/hri/explorer_g2/hri_explorer_g2_m.nbt) |

G2模板按本系列命名，不使用其他系列作占位。尺寸沿现有模板记录；对接、结构质量和满载表现仍按[实运验收](../../制作与实运验收.md)检查。

## 蓝图获取与制造

地平线科研贸易港；测试贸易点 A、测试贸易点 B

| 项目 | 当前要求 |
| --- | --- |
| 许可证 | M |
| 制造商声望 | cargoverse:hri／1级 |
| 蓝图打印费 | 460 VB |
| 施工时间 | 400 tick（20 TPS时20秒） |

材料按实体物品件数消耗，打印阶段不扣材料。蓝图获取仍需满足所列许可证及声望要求。

| 层次 | 材料 | 件数 |
| --- | --- | ---: |
| 主材料 | 铁锭（`minecraft:iron_ingot`） | 64 |
| 辅材料 | 标准紧固件箱（`cargoverse:standard_fasteners`） | 16 |
| 辅材料 | 工业构件箱（`cargoverse:industrial_components`） | 8 |
| 特殊材料 | 调温机组（`cargoverse:thermal_control_unit`） | 2 |
| 特殊材料 | 稳压组件（`cargoverse:pressure_regulator`） | 2 |

[产业物资获取与生产](../../../01运输物品/04_产业物资.md) · [共用制造规则](../../../03贸易点/蓝图投放/制造配方与投放总表.md)

## 运行资源对应

文档型号代号用于统一查阅和制作命名，**不是已注册的新资源ID**。本轮未迁移运行资源；指令、配方和数据包引用仍使用下列实际ID。旧名称不表示第二个产品系列或不同接口。

| 资源 | 当前 ID／来源 |
| --- | --- |
| 实际货柜定义 ID | `cargoverse:hri/explorer_si_m` · [JSON](../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/hri/explorer_si_m.json) |
| 制造配方 ID | `cargoverse:hri/explorer_si_m` · [JSON](../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_manufacturing_recipes/hri/explorer_si_m.json) |

<details>
<summary>完整现行货柜定义</summary>

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/hri/explorer_g2/hri_explorer_g2_m",
  "manufacturer": "cargoverse:hri",
  "display_name": "HRI Explorer 环境样品柜 M 型",
  "description": "Explorer为研究院样品调节温压并遮光。运单常把保存条件写得很细，项目名称却只有编号；有时接收它的研究员也没有权限知道更多。用于将一处调查区域的样品集中送回。样品编号彼此相邻，结论却未必相同。",
  "size_class": "M",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 2,
  "capacity": 4096,
  "empty_mass": 60,
  "allowed_cargo_classes": [
    "solid"
  ],
  "tags": [
    "series.hri.explorer"
  ],
  "cargo_class_capacity_modifiers": {},
  "abilities": {
    "cargoverse:pressure_control": {
      "level": 1
    },
    "cargoverse:thermal_control": {
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
