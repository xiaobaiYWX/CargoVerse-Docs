# DMC CoreVault 干燥精矿柜 M 型

## 货柜介绍

CoreVault用于运送值得单独登记的精矿。深岩矿业为它配置密封与防雨结构；采样员则坚持在封柜前，再抄一遍矿脉编号。为集中转运精选矿料准备。深岩的验收员先核对产地记录，随后才肯在重量一栏签字。

## 型号与承载

| 项目 | 现行值 |
| --- | --- |
| 系列 | CoreVault 干燥精矿柜 |
| 文档型号代号 | `dmc/corevault_m` |
| 规格 | M |
| 运输介质 | solid |
| 容量 | 4096 件 |
| 定义空重 | 72 Kpg |
| 调度点 | 2 |
| 接口 | 统一标准接口；型号代号不再包含接口缩写 |

容量按单件计数，组只决定装卸步长。最大堆叠64时满载为64组；每件0.1 Kpg的货物装满后货重409.6 Kpg，不含柜体。

实际空重取定义空重与结构质量的较大值。表中数值不是结构实测质量，起吊与满载运输仍需实机验收。

## 保护能力

| 能力 | 配置 ID | 完整参数 |
| --- | --- | --- |
| 围护结构 | `cargoverse:containment` | `{"level":1}` |
| 防水柜体 | `cargoverse:waterproof_body` | `{}` |
| 密封结构 | `cargoverse:sealing` | `{"level":1}` |

容量修正：`{}`。运输条件与能力的对应规则见[能力规范](../../../../04数据规范/货柜/能力/README.md)。

## 模板与制作状态

| 项目 | 现行值 |
| --- | --- |
| 模板状态 | 已接入；发布文件存在，无缺失模板 |
| 模板资源 ID | `cargoverse:cargo/dmc/corevault_g2/dmc_corevault_g2_m` |
| 导出相对路径 | `generated/cargoverse/structures/cargo/g2/dmc/corevault/corevault_m.nbt` |
| 尺寸 X×Y×Z | 8×5×5 格 |
| 发布结构文件 | [NBT](../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/dmc/corevault_g2/dmc_corevault_g2_m.nbt) |

G2模板按本系列命名，不使用其他系列作占位。尺寸沿现有模板记录；对接、结构质量和满载表现仍按[实运验收](../../制作与实运验收.md)检查。

## 蓝图获取与制造

深岩矿业贸易港；测试贸易点 A、测试贸易点 B

| 项目 | 当前要求 |
| --- | --- |
| 许可证 | M |
| 制造商声望 | cargoverse:dmc／1级 |
| 蓝图打印费 | 300 VB |
| 施工时间 | 400 tick（20 TPS时20秒） |

材料按实体物品件数消耗，打印阶段不扣材料。蓝图获取仍需满足所列许可证及声望要求。

| 层次 | 材料 | 件数 |
| --- | --- | ---: |
| 主材料 | 铁锭（`minecraft:iron_ingot`） | 64 |
| 辅材料 | 标准紧固件箱（`cargoverse:standard_fasteners`） | 16 |
| 辅材料 | 工业构件箱（`cargoverse:industrial_components`） | 12 |
| 辅材料 | 密封接头组（`cargoverse:sealing_joints`） | 4 |

[产业物资获取与生产](../../../01运输物品/04_产业物资.md) · [共用制造规则](../../../03贸易点/蓝图投放/制造配方与投放总表.md)

## 运行资源对应

文档型号代号用于统一查阅和制作命名，**不是已注册的新资源ID**。本轮未迁移运行资源；指令、配方和数据包引用仍使用下列实际ID。旧名称不表示第二个产品系列或不同接口。

| 资源 | 当前 ID／来源 |
| --- | --- |
| 实际货柜定义 ID | `cargoverse:dmc/corevault_sd_m` · [JSON](../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/dmc/corevault_sd_m.json) |
| 制造配方 ID | `cargoverse:dmc/corevault_sd_m` · [JSON](../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_manufacturing_recipes/dmc/corevault_sd_m.json) |

<details>
<summary>完整现行货柜定义</summary>

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/dmc/corevault_g2/dmc_corevault_g2_m",
  "manufacturer": "cargoverse:dmc",
  "display_name": "DMC CoreVault 干燥精矿柜 M 型",
  "description": "CoreVault用于运送值得单独登记的精矿。深岩矿业为它配置密封与防雨结构；采样员则坚持在封柜前，再抄一遍矿脉编号。为集中转运精选矿料准备。深岩的验收员先核对产地记录，随后才肯在重量一栏签字。",
  "size_class": "M",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 2,
  "capacity": 4096,
  "empty_mass": 72,
  "allowed_cargo_classes": [
    "solid"
  ],
  "tags": [
    "series.dmc.corevault"
  ],
  "cargo_class_capacity_modifiers": {},
  "abilities": {
    "cargoverse:containment": {
      "level": 1
    },
    "cargoverse:waterproof_body": {},
    "cargoverse:sealing": {
      "level": 1
    }
  }
}
```

</details>

[本系列](README.md) · [制造商目录](../README.md)
