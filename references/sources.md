# 来源与恢复位置

## 2026-10-19 统一版谱系

本版按用户裁决把三代内容合成一套主干加分册：发散与收敛是按任务轨道分的两种模式；沉淀分产品级与通用级，风格跟产品走；术语库降为工具，平台差异落成参数包；分册按判定结果渐进加载。

| 来源 | 吸收进本版的内容 | 当前位置 |
| --- | --- | --- |
| design-methodology-workflow（六层编排器） | 战略层四问与退出条件、旅程与流失点、信息架构与线框、风格语料组气质卡、A11Y 四项、5 秒测试与漏斗指标、用户要跳步的处理、归档约定 | mode-explore.md |
| product-design-workflow（改写自 Anshu Chimala 文章） | 身份假设卡、同条件候选、随机引子、独立评审包与提示、收敛每元素说明价值、批准稿落地 C1–C5、三个结论、分级沉淀口径 | mode-explore.md、mode-converge.md、主文第 8 步 |
| ui-design-workflow（用户 2026-09-15 认可） | 规范先行一次定死、同功能一套实现、静态候选稿人选、性能分开治、交付前清单 | mode-converge.md |
| finesse-brief（finesse-skill） | 后台/工作台分叉、两问定义法、十一种结构表、钩子字段与写入方、冷启动、spec 结构 | surface-product.md |
| finesse-ui（finesse-skill） | 页型决定结构、五轴组合、工艺底线、素材授权门、商业面骨架、读页/操作页、AI 工作台层、四拍与效果族→路线、八状态组件流、H5 固定框与成对处理 | surface-brand.md、surface-product.md、motion.md、component-flow.md、params-h5.json |
| finesse-term（finesse-skill） | 原话转执行单、术语按需检索 | communication.md、scripts/term.mjs、data 五册 |
| 全局 6 步「UI 设计流程」分支（10-04 至 10-12） | 已确认设计的 1:1 约束、组件设计与复用、整页组件与风格审计、效果图确认制 | 主文第 5–6 步、component-flow.md、component-system-audit.md |
| 仓库 9 步「执行手册」（10-05） | 功能映射表、参考拆解六项、字体样张、图标流程、色值布局材质参数、动作表、真实操作验收 | 主文第 1–7 步、visual.md、icons.md、interaction.md、definition.md、implementation.md、verification.md |

本次恢复快照（维护者私有仓库内）：`design/research/ui-method-unify-20261019/`（全局 6 步分支完整文件、六份原始 skill 主文、`recovery-manifest.json`，提交 `e25a9a88`）；仓库 9 步版恢复点为提交 `ef8a71b6`。

## 整页组件审计补充

`component-system-audit.md` 来自全局分支 2026-10-12 的整理，针对榜单、目录、动态、报告类页面的板块任务、材质层次与分类 Tab 做出图前审计；本版在收敛模式路径 A 与主文第 4 步引用，参数沿用 visual / icons / interaction。

## 更早的原始资料（维护者私有仓库记录）

- 2026-10-04 六份原始 skill 归档：`git show 0a8dae3a:design/research/ui-skill-unification-20261004/original-skills-recovery.tar.gz`（归档包已于 2026-10-16 从工作区删除，Git 历史保留），manifest 见 `design/research/ui-skill-unification-20261004/recovery-manifest.json`，删除前提交 `df4d2c129`。
- 2026-10-05 执行手册重写前快照：`git show 0a8dae3a:design/research/ui-method-executable-20261005/ui-design-method-before.tar.gz`，重写前提交 `9c80b2db2`。

恢复时先提取到独立临时目录，核对 manifest 里的哈希，再按需恢复具体文件。

## 外部来源与许可

- [Anshu Chimala, How to turn your AI into a world-class designer](https://www.lennysnewsletter.com/p/how-to-turn-your-ai-into-a-world)（Lenny's Newsletter，2026-09-01）：身份假设、人的品味引导、独立评审、参考校准、删减无效元素；作者在 Apple 带软件工程与设计团队 12 年。
- [finesse-skill](https://github.com/mouse-lin/finesse-skill)（MIT，西瓜同学）：finesse-brief / finesse-ui / finesse-term 的原始仓库，术语脚本与五册数据亦出自此；许可保留在根目录 LICENSE。
- [Oil UI](https://github.com/oil-oil/oil-ui)（复查版本 `b7004ab8`）：参考拆解、图标光学校准、点击到结果的反馈链。
- 风格语料：[awesome-design-md](https://github.com/VoltAgent/awesome-design-md)（74 个品牌 DESIGN.md）、[awesome-design-skills](https://github.com/bergside/awesome-design-skills)（67 种风格），只检索命中项。
- 可访问性：[W3C 对比度](https://www.w3.org/WAI/WCAG22/Understanding/contrast-minimum.html)、[W3C 目标尺寸](https://www.w3.org/WAI/WCAG22/Understanding/target-size-minimum.html)。
- 字体与图标来源见 visual.md 与 icons.md；MiSans 用其官方协议，开源字体按各自名称与修改条款处理。

参数包与分册里的数字是设计比较的起始配方，由项目规范和用户确认值覆盖。
