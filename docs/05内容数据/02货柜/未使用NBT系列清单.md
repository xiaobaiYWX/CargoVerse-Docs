# 未使用 NBT：按模板真实系列分组

核对：2026-11-06。范围为项目 `data/cargoverse/structure/cargo` 下 66 份 NBT 与全部 81 个货柜定义。**未使用仅指没有任何定义的 template 引用，包含已关闭定义在内一起查找；不代表文件无价值或可以删除。**

**20 份未引用 NBT，分属 8 个系列。** 下表系列直接从 NBT 路径与文件名读取。

| 制造商 | NBT 系列 | 未引用规格与接口 | 文件 | 状态说明 |
| --- | --- | --- | --- | --- |
| 天穹联合工业 AUI | nomad | L / HD、M / HD、X / HD | [aui_nomad_hd_l.nbt](<../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/aui/nomad/aui_nomad_hd_l.nbt>)<br>[aui_nomad_hd_m.nbt](<../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/aui/nomad/aui_nomad_hd_m.nbt>)<br>[aui_nomad_hd_x.nbt](<../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/aui/nomad/aui_nomad_hd_x.nbt>) | 未接入对应系列；不因历史合并转归其他系列。 |
| 赫利俄斯能源集团 HEC | apollo | L / SD、M / SD、S / SD | [hec_apollo_sd_l.nbt](<../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/hec/apollo/hec_apollo_sd_l.nbt>)<br>[hec_apollo_sd_m.nbt](<../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/hec/apollo/hec_apollo_sd_m.nbt>)<br>[hec_apollo_sd_s.nbt](<../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/hec/apollo/hec_apollo_sd_s.nbt>) | M／L 可供现行 Apollo 同规格核对；S 当前无正式规格。SD 接口不可冒称 HD。 |
| 赫利俄斯能源集团 HEC | cryovault | L / SD、M / SD、S / SD | [hec_cryovault_sd_l.nbt](<../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/hec/cryovault/hec_cryovault_sd_l.nbt>)<br>[hec_cryovault_sd_m.nbt](<../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/hec/cryovault/hec_cryovault_sd_m.nbt>)<br>[hec_cryovault_sd_s.nbt](<../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/hec/cryovault/hec_cryovault_sd_s.nbt>) | 未接入对应系列；不因历史合并转归其他系列。 |
| 赫利俄斯能源集团 HEC | reclaimer | L / SD、M / SD | [hec_reclaimer_sd_l.nbt](<../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/hec/reclaimer/hec_reclaimer_sd_l.nbt>)<br>[hec_reclaimer_sd_m.nbt](<../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/hec/reclaimer/hec_reclaimer_sd_m.nbt>) | 未接入对应系列；不因历史合并转归其他系列。 |
| 地平线研究院 HRI | archive | M / SI、S / SI | [hri_archive_si_m.nbt](<../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/hri/archive/hri_archive_si_m.nbt>)<br>[hri_archive_si_s.nbt](<../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/hri/archive/hri_archive_si_s.nbt>) | 未接入对应系列；不因历史合并转归其他系列。 |
| 云港物流集团 SPL | courier | M / MC、S / MC | [spl_courier_mc_m.nbt](<../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/spl/courier/spl_courier_mc_m.nbt>)<br>[spl_courier_mc_s.nbt](<../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/spl/courier/spl_courier_mc_s.nbt>) | S／M 已有正确模板，当前定义错误引用 Cargo。 |
| 绿洲农业联盟 VBS | biopod | L / SD、M / SD、S / SD | [vbs_biopod_sd_l.nbt](<../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/vbs/biopod/vbs_biopod_sd_l.nbt>)<br>[vbs_biopod_sd_m.nbt](<../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/vbs/biopod/vbs_biopod_sd_m.nbt>)<br>[vbs_biopod_sd_s.nbt](<../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/vbs/biopod/vbs_biopod_sd_s.nbt>) | 测试验证内容，不列正式产品。 |
| 绿洲农业联盟 VBS | eden | X / HD、XL / HD | [vbs_eden_hd_x.nbt](<../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/vbs/eden/vbs_eden_hd_x.nbt>)<br>[vbs_eden_hd_xl.nbt](<../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/vbs/eden/vbs_eden_hd_xl.nbt>) | 未接入对应系列；不因历史合并转归其他系列。 |

## 被跨系列借用的 NBT：不是未引用文件

这些文件有实际引用，因此不能列入上面的“未使用”数；但借用不能改变模板系列归属。

| NBT 真实系列 | 被跨系列引用的规格 | 当前借用它的设计系列 |
| --- | --- | --- |
| aui/atlas | L、M、S、X、XL | aui/vulcan、dmc/boreal、hec/boreas、hec/cryovault、hec/apollo、hec/reclaimer、hri/crucible、spl/cistern、vbs/biopod、hri/explorer、spl/courier、vbs/harvest |
| bds/bastion | L、X | bds/sentinel |
| dmc/titanhaul | L、X、XL | dmc/silo |
| hec/reactor | L、M、X | hec/apollo |
| rex/recycle | M、S | rex/reliquary |
| spl/cargo | L、M、S | spl/courier |

Atlas XL 虽无正式 Atlas XL 型号，仍被旧 Eden 定义引用，所以不属于“零引用文件”。同理 Cargo、Reactor、TitanHaul、Bastion、Recycle 都仍被错误引用，不计入 20 份未使用 NBT。

[正式产品目录](README.md) · [非正式内容](<../../90设计草案/货柜/预留与验证/README.md>)
