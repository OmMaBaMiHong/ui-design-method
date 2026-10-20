---
name: awesome-design-md
description: 品牌模板库。精选 74 个真实网站的 DESIGN.md 设计系统分析文档（含色板/字阶/组件/Do-Don't），复制到项目即可让 AI 生成同款品牌风格 UI。来源 VoltAgent/awesome-design-md，MIT 许可。
version: 1.0.0
license: MIT
---

# Awesome DESIGN.md · 品牌模板库

> 用途：当你需要「复刻某个真实品牌的视觉风格」时，读取对应站点的 `DESIGN.md`，把它作为设计约束交给 AI，即可生成高度一致、有真实设计深度的 UI。本技能是**品牌模板库**——提供现成可参考的设计文档。

## 如何使用
1. 在下方索引找到目标品牌（如 `notion`、`airbnb`、`linear.app`）。
2. 读取 `design-md/<站点>/DESIGN.md`（设计令牌 + 规则）以及 `design-md/<站点>/preview.html`（视觉参考）。
3. 对 AI 说：「参考 `design-md/notion/DESIGN.md` 的设计令牌与规则，为我们的页面生成同风格 UI」。
4. 可直接把该 `DESIGN.md` 复制到你的项目根目录，AI 会自动读取并保持一致。

每个站点目录均包含：
- `DESIGN.md` —— 设计系统文档（调色板/字体/组件/布局/Do-Don't/响应式/代理提示）
- `preview.html` / `preview-dark.html` —— 色板、字阶、按钮、卡片的可视化目录

## 安全说明
- 纯 Markdown + HTML 文档集合，无任何可执行脚本、钩子或依赖（已审计：无 .sh / package.json / postinstall）。
- MIT 许可；内容为公开网站 CSS 的提取分析，不主张任何网站视觉标识，仅供 AI 生成 UI 参考。

## 站点索引（74 个，按类别）

### 1. AI & LLM 平台（12）
claude · cohere · elevenlabs · minimax · mistral.ai · ollama · opencode.ai · replicate · runwayml · together.ai · voltagent · x.ai

### 2. 开发者工具 & IDE（7）
cursor · expo · lovable · raycast · superhuman · vercel · warp

### 3. 后端 / 数据库 / DevOps（8）
clickhouse · composio · hashicorp · mongodb · posthog · sanity · sentry · supabase

### 4. 生产力 & SaaS（8）
cal · intercom · linear.app · mintlify · notion · resend · slack · zapier

### 5. 设计 & 创意工具（6）
airtable · clay · figma · framer · miro · webflow

### 6. 金融科技 & 加密（7）
binance · coinbase · kraken · mastercard · revolut · stripe · wise

### 7. 电商 & 零售（5）
airbnb · meta · · nike · shopify · starbucks
> 注：meta 归类于社媒/消费科技，亦可作为电商参考。

### 8. 媒体 & 消费科技（12）
apple · hp · ibm · nvidia · pinterest · playstation · spacex · spotify · theverge · uber · vodafone · wired

### 9. 汽车（7）
bmw · bmw-m · bugatti · ferrari · lamborghini · renault · tesla

### 10. 复古网页（2）
dell-1996 · nintendo-2001

## 推荐用于「C 端极简高级品牌」的参考站点
- `notion`（克制、留白、插画品牌感）
- `linear.app`（极简、精密、暗色高级）
- `airbnb`（温暖、清晰、强信任感）
- `stripe`（精致、专业、渐变质感）
- `apple`（极致极简、大留白）
- `spotify`（活力但不杂乱）
- `framer` / `webflow`（设计工具自身的高完成度 UI）

路径示例：`design-md/notion/DESIGN.md`、`design-md/linear.app/DESIGN.md`
