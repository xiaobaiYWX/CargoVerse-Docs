# VBS Aquarium 水生运输舱 L 型

> **缺失本系列模板：vbs_aquarium_sd_l.nbt。** 属性和制造配方已配置，禁止制造／出售，待结构补齐后开放。不得引用 Atlas、BioPod 或其他系列替代。

| 项目 | 配置 |
| --- | --- |
| 定义 ID | `cargoverse:vbs/aquarium_sd_l` |
| 制造商／系列／接口 | 绿洲农业联盟 VBS／Aquarium／SD |
| 必须补齐的模板 ID | `cargoverse:cargo/vbs/aquarium/vbs_aquarium_sd_l` |
| 文件位置 | `data/cargoverse/structure/cargo/vbs/aquarium/vbs_aquarium_sd_l.nbt` |
| 舱位 | 48 |
| 配置空重 | 36 Kpg |
| 调度点 | 4 |
| 舱室 | water；单体 65536 B，整柜 1048576 B |
| 蓝图许可证／价格 | L／840 VB（待开放） |
| 制造时间 | 400 tick，20 秒 |

## 装载能力

只接收 water 生活环境的生物，一柜一种 EntityType。当前 12 种水生生物均能至少装入一只；不接收 land BioPod 对应生物，也不是流体运输罐。

| 代表生物 | 每只舱位 | 满柜只数 |
| --- | ---: | ---: |
| 鳕鱼、热带鱼、蝌蚪 | 1 | 48 |
| 美西螈、鲑鱼、河豚 | 2 | 24 |
| 溺尸 | 3 | 16 |
| 海豚、鱿鱼、发光鱿鱼 | 4 | 12 |
| 守卫者 | 5 | 9 |
| 远古守卫者 | 12 | 4 |

质量为柜体有效空重加实际生物货重；配置空重按水生维持结构的简化固定预算设计，不另扣水、不按真实容积计算水重。**结构未完成，实际结构质量下限尚未核定**，不能宣称最终空柜就只有 36 Kpg。

## 保护与设备

气密 2；缓冲 2（速度变化耐受 +5）；隔热 240 秒；双向调温 5～40 TU、0.3 TU/s；双向稳压 0.5～1.5、0.02/s；遮光减 15。设备默认沿当前自动控制规则工作，按货物需求取目标；普通水生目标温度 20、气压 1。

不虚构溶氧、水质或耗材模拟。遮光可保护溺尸；调温稳压不等于装载瞬间达到安全值，冲击保护也非绝对免伤。M／L 保护相同，以容量和质量区分。

## 制造与投放

[制造配方](<../../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_manufacturing_recipes/vbs/aquarium_sd_l.json>) 已配置。材料为铁锭、玻璃、蓝冰、流体管道、储罐与羊毛，具体数量以文件为准。蓝图费用为图纸定影价格，不是运输属性中的价格。

模板缺失期间保留 `not_manufacturable` 与 `missing_template`，不加入 A／B 或自然站的在售目录，防止售出无法施工的蓝图。模板补齐并核定结构质量后，解除两项标记，接入 A／B 全型号目录；正式渠道安排水产养殖站与生态系统研究站，许可证和繁荣等级按 L 型要求接入。

## 结构搭建要求

制作独立 Aquarium 系列水生舱：可辨认的玻璃水舱、承压框架、循环水管、维护舱和 SD 接口。外观使用 VBS 生态设备风格，避免复制其他系列并改名。无需在 NBT 中预放动物，动物保存在原生载荷中；水体外观不替代 living_chamber=water。参考现有货柜制作规范布置必须的标记，导出后再核定结构质量、物理碰撞和搭建材料。

[工程定义](<../../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/vbs/aquarium_sd_l.json>) · [系列总览](README.md)
