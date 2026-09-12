# 失标仓储货箱

状态：正式 CargoGood 定义；数据同步批次 2026-09-10。数值为首轮基线，后续按实际航运测试校准。

## 定义

| 项目 | 内容 |
| --- | --- |
| 资源 ID | `cargoverse:none/unlabelled_warehouse_crates` |
| JSON 文件 | `src/main/resources/data/cargoverse/cargo_goods/none/unlabelled_warehouse_crates.json` |
| Schema 版本 | 1 |
| CargoClass | `none` |
| 显示名称 | 失标仓储货箱 |
| UI 图标 | `cargoverse:textures/gui/cargo_goods/none/unlabelled_warehouse_crates.png`（32×32 RGBA PNG） |
| 科技等级 | 1 |
| 标签 | `ingredient.none.unlabelled_warehouse_crates`、`reserved_unidentified` |
| 结算单位 | `cargoverse:void_byte` |

## 数值

| 项目 | 数值 | 单位 |
| --- | ---: | --- |
| 单位质量 | 3 | Kpg/t |
| 单位基础价值 | 0 | VB/t |
| 单位许可证经验 | 0 | exp/t |
| 单位繁荣经验 | 0 | exp/t |
| 基础完整度 | 100 | 点 |

## 运输要求

无。

## 内容定位与投放

废弃仓储→鉴定站；单证与标记遗失；常规

- 本轮不安排常规出售或收购节点；保留为未鉴定／特殊事件内容。投放范围见[资源表版贸易点设计](<../../07_贸易点/设计总览.md>)。
- 未识别预留货物：本批注册但不加入普通供货池，基础价值与经验为 0。当前没有寄运身份或鉴定限制机制，不能把预留标签当作运行时权限。
- 基础估值沿用已评审目录的参考值；质量按物流定位区分，经验按科技层级分档，不按货价线性增长。
- 货物专属标签仅匹配本货物；资源表、商店或制造台需要其他候选货物时应显式列出。

[返回 CargoGood 目录](../README.md)

图标采用统一像素风格的独立实物轮廓，由内置 image_gen 生成并导出为 32×32；透明底、最近邻缩放，无文字标签。
