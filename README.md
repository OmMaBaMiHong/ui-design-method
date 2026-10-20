# ui-design-method

给 AI 编码代理用的 UI 设计方法论 Skill。**一套主干、两种模式、分册按需加载**：先判定任务（发散 / 收敛 × 品牌面 / 产品面 × 桌面 / H5 / 小程序），再按八步主干执行——理解内容、研究参考、出设计图、打磨图稿与交互、用户审阅确认、页面开发、对照验收、分级沉淀。

适用于 Claude Code、Codex CLI、ZCode 等支持 `SKILL.md` 目录约定的代理宿主。

## 它解决什么

- **风格漂移**：没有约束时代理每次自由发挥，改版越改越乱。本方法要求规范一次定死、同条件出候选、由人选版，再 1:1 落地。
- **发散与收敛混在一起**：新品牌需要放开想，原功能上的小修需要克制。这里按任务轨道分成两种模式，各有各的步骤与禁区。
- **验收靠感觉**：以同视口、同主题、同状态的并排对照和真实页面操作为证据，视觉、任务、工程三个结论分开给。
- **平台差异写进方法里**：方法主干平台无关，桌面、手机、小程序的差异全部落在参数包里按需加载。

## 结构

```
SKILL.md                      一级：判定五件事 → 八步主干 × 两种模式 → 分级沉淀
references/
  mode-explore.md             发散模式：战略、旅程、结构、身份假设、气质卡、令牌候选、人选、独立评审
  mode-converge.md            收敛模式：审计、小修、批准稿落地（1:1 约束、迁移方式、对照验收）
  surface-brand.md            品牌与商业面：页型定结构、五轴组合、工艺底线、商详/列表/结算骨架
  surface-product.md          产品面：后台/工作台分叉、工作台定义法与十一种结构、读页/操作页、AI 工作台层
  motion.md                   动效编排：四拍、效果族 → 实现路线、减少动效
  component-flow.md           单组件流程：八状态、复用规则、组件与数据分工、缺字段追链
  component-system-audit.md   整页组件与风格审计清单
  definition / visual / icons / interaction / implementation / verification / communication
  sources.md                  谱系、外部来源与许可
data/
  params-web.json             桌面 Web 起始配方：栅格、首屏预算、字阶、间距、圆角阴影、对比、动效时长
  params-h5.json              手机 H5：390×844 框、安全区、原生件尺寸、拇指区、触控、成对处理、转场
  params-mp.json              小程序：rpx 换算、胶囊避让、TabBar、平台限制
  base/web/h5/mp/motion.json  界面术语库（供 scripts/term.mjs 检索）
assets/execution-sheet.md     执行表：基准、功能映射、参考拆解、字体、图标、配色、尺寸、动作、操作记录
scripts/term.mjs              用用户原话反查界面术语
companions/                   配套包（公开仓库内）：awesome-design-md、awesome-design-skills、oil-ui、web-design-guidelines
```

渐进式加载：主文每次读；模式册、表面册、横切册按第 0 步的判定各读一本；参数包按平台读一个；术语库与风格语料只检索命中项。

## 安装

把本目录放进宿主的 skills 目录（复制或软链均可）：

```sh
git clone https://github.com/OmMaBaMiHong/ui-design-method.git
ln -s "$PWD/ui-design-method" ~/.claude/skills/ui-design-method   # Claude Code
ln -s "$PWD/ui-design-method" ~/.codex/skills/ui-design-method    # Codex CLI
ln -s "$PWD/ui-design-method" ~/.zcode/skills/ui-design-method    # ZCode
```

术语检索需要 Node 18+：`node scripts/term.mjs find --q "底部按钮被黑杠挡住了" --surface h5`。

## 配套包

`companions/` 收录四个配套 skill 的快照（均为 MIT，保留上游许可与版权）：**awesome-design-md**（74 个品牌 DESIGN.md）、**awesome-design-skills**（67 种风格技能包与预览图）、**oil-ui**（方向拆解、视觉语言、动效与文案规则）、**web-design-guidelines**（Vercel 界面规则审查）。发散模式用前两者检索风格语料组气质卡，收敛模式用后两者做审计校准。各自软链进 skills 目录即可启用：

```sh
for s in awesome-design-md awesome-design-skills oil-ui web-design-guidelines; do
  ln -s "$PWD/ui-design-method/companions/$s" ~/.claude/skills/$s
done
```

出处、收录版本与安装细节见 [companions/README.md](https://github.com/OmMaBaMiHong/ui-design-method/tree/main/companions)。

## 用法

在对话里描述 UI 任务即可触发，例如「给作品库页面做一轮品牌升级」「把这张批准稿 1:1 落地到 /settings」「审计一下首页的组件和配色」。代理会先读项目、规范与历史对话，判定模式与平台，再按八步交付：功能映射表、参考拆解表、参数表与图稿、批准记录、组件修改、操作记录、规范更新。

数值全部是起始配方：项目已有 token 与用户确认值优先，出图前收敛成单值写进执行表。

## 来源与许可

本方法整合自多份工作流与研究，详见 [references/sources.md](references/sources.md)：

- Anshu Chimala, [How to turn your AI into a world-class designer](https://www.lennysnewsletter.com/p/how-to-turn-your-ai-into-a-world)（身份假设、人的品味引导、独立评审、删减无效元素）
- [finesse-skill](https://github.com/mouse-lin/finesse-skill)（MIT，西瓜同学）：工作台定义、页型与五轴、AI 工作台层、术语库与检索脚本
- [Oil UI](https://github.com/oil-oil/oil-ui)、[awesome-design-md](https://github.com/VoltAgent/awesome-design-md)、[awesome-design-skills](https://github.com/bergside/awesome-design-skills)、[Web Interface Guidelines](https://github.com/vercel-labs/web-interface-guidelines)

许可：MIT，见 [LICENSE](LICENSE)（保留 finesse-skill 原作者版权声明）。

---

## English

A UI design methodology skill for AI coding agents (Claude Code, Codex CLI, ZCode and any host that reads a `SKILL.md` directory). One spine, two modes, progressive loading: the agent first classifies the task — **explore** (new product, rebrand, new direction) vs **converge** (audit, small fix, implementing an approved mockup), brand/commerce vs product surface, desktop / mobile H5 / mini-program — then runs an eight-step spine: understand → reference → design → refine → user approval → build 1:1 → side-by-side verification → tiered codification (product-level identity stays with the product; only generic components go to the shared library). Platform differences live in `data/params-*.json`, not in the method. Install by cloning into your host's skills directory. MIT.
