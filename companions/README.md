# 配套包（companions）

ui-design-method 的方法主干不依赖这些包，但发散模式的风格语料检索、工艺底线校准和界面质量审查用到它们。每个包都是独立的 skill 目录，按需软链进宿主的 skills 目录即可；全部保留上游许可与版权声明，本仓库只做快照收录。

| 包 | 用途 | 上游 | 收录版本 | 许可 |
| --- | --- | --- | --- | --- |
| awesome-design-md | 74 个真实网站的 DESIGN.md 设计系统分析（色板、字阶、组件、Do/Don't），发散模式第 4 步按用户与任务检索品牌参考 | [VoltAgent/awesome-design-md](https://github.com/VoltAgent/awesome-design-md) | 提交 `8147538` | MIT |
| awesome-design-skills | 67 个设计风格技能包（SKILL.md + DESIGN.md，含调色板、字阶、组件、无障碍、质量门禁）与风格预览图，发散模式组气质卡时检索调性 | [bergside/awesome-design-skills](https://github.com/bergside/awesome-design-skills) | 提交 `f631a09` | MIT |
| oil-ui | 设计方向拆解、视觉语言、动效呼应与文案规则，收敛模式审计与工艺底线校准 | [oil-oil/oil-ui](https://github.com/oil-oil/oil-ui) | 2026-10 本地安装快照 | MIT |
| web-design-guidelines | Vercel 的 Web Interface Guidelines 审查封装，运行时拉取最新规则对代码做 `file:line` 级检查 | [vercel-labs/web-interface-guidelines](https://github.com/vercel-labs/web-interface-guidelines) | 封装 v1.0.0（metadata author: vercel） | MIT |

## 安装

```sh
# 以 Claude Code 为例；Codex 用 ~/.codex/skills，ZCode 用 ~/.zcode/skills
for s in awesome-design-md awesome-design-skills oil-ui web-design-guidelines; do
  ln -s "$PWD/companions/$s" ~/.claude/skills/$s
done
```

## 在方法里的位置

- 发散模式 → 研究参考（主文第 2 步、`references/mode-explore.md` 第 4 节）：从 awesome-design-md 挑 3 个品牌、从 awesome-design-skills 挑 3 种调性组成气质卡。只检索命中项，整库不装载。
- 收敛模式 → 审计路径（`references/mode-converge.md` A）：web-design-guidelines 做代码级规则审查，oil-ui 的方向拆解与文案规则做校准。
- 品牌与商业面（`references/surface-brand.md`）：工艺底线与 oil-ui 的视觉语言互为参照。

## 未收录但相关

- [impeccable](https://github.com/pbakaus/impeccable)：前端界面打磨与审计，依赖按平台下载的引擎二进制，仓库未附许可文件，请按上游说明自行安装。
- [finesse-skill](https://github.com/mouse-lin/finesse-skill)（MIT）：本方法的重要来源之一，其工作台定义、页型与五轴、AI 工作台层已吸收进 references；术语脚本与五册数据随本仓库 `scripts/term.mjs` 与 `data/*.json` 一并收录。

更新配套包时从上游重新快照并改写上表的收录版本；本地对上游的修改先提 PR 回上游。
