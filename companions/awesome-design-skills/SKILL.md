---
name: awesome-design-skills
description: 设计风格复刻。67 个 AI 编码代理可用的设计系统技能（每个含 SKILL.md + DESIGN.md，定义调色板/字阶/组件/无障碍/质量门禁），读取即可让 AI 复刻该视觉风格。来源 bergside/awesome-design-skills，MIT 许可。
version: 1.0.0
license: MIT
---

# Awesome Design Skills · 设计风格复刻

> 用途：当你需要「用某种设计风格（如极简、玻璃拟态、企业级）来构建 UI」时，读取对应风格的 `SKILL.md` + `DESIGN.md`，AI 即按该风格的设计令牌与规则生成界面。本技能是**风格复刻引擎**——提供可组合的视觉风格。

## 如何使用
1. 在下方索引选风格（如 `minimal`、`glassmorphism`、`corporate`）。
2. 读取 `skills/<风格>/SKILL.md`（面向 AI 的指令）与 `skills/<风格>/DESIGN.md`（设计意图说明）。
3. 对 AI 说：「用 `skills/minimal/` 的设计系统，为我们做一套页面」。
4. 可搭配 `awesome-design-md` 品牌模板库：先用风格定调性，再参考某真实品牌做细节。

每个风格目录均包含：
- `SKILL.md` —— 面向 AI 代理的指令（品牌使命、样式基础、组件、无障碍、Do/Don't、质量门禁）
- `DESIGN.md` —— 面向人类的设计说明（概览、理由、引用）

## 安全说明
- 纯 Markdown 文档集合，无可执行脚本/钩子/依赖（已审计：skills/ 下仅 .md 文件，无 .sh/package.json/js）。
- MIT 许可。

## 风格索引（67 个）

### 极简 / 干净 / 高级（推荐用于 C 端品牌）
minimal · clean · flat · mono · modern · contemporary · refined · sleek · spacious · basic

### 大胆 / 表现力 / 鲜艳
bold · dramatic · expressive · vibrant · colorful · neon · gradient · cosmic · futuristic · immersive · power · levels · lingo

### 材质 / 质感 / 深度
glassmorphism · neumorphism · claymorphism · skeumorphism · material · paper · sketch · dithered · riso · terracotta

### 复古 / 趣味 / 玩味
retro · vintage · neobrutalism · brutalism · doodle · pacman · sega · tetris · square · roku · cafe · storytelling · fiction · fantasy · artistic · creative

### 企业 / 专业 / 平台
corporate · enterprise · professional · premium · shadcn · ant · claude · codex · stitch · agentic · geometric · editorial · matrix · perspective · bento · friendly

## 与本项目（热点追踪 / 社媒榜单 C 端）最契合的风格
- **minimal** —— 极简高级，留白克制，最适合做有品牌感的 C 端榜单站
- **clean / modern / refined / sleek** —— 干净现代，信息密度友好
- **glassmorphism** —— 若想要更「潮」的玻璃质感榜卡片
- **premium / editorial** —— 偏杂志/高端叙事感

路径示例：`skills/minimal/SKILL.md`、`skills/minimal/DESIGN.md`
