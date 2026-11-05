---
name: Vibecode UI 组件库
description: >-
  Vibecode / AI 写前端时想让界面更美观、选组件库或找视觉方向时用：按场景从 BoardUI、Bencho、HeroUI、beUI
  Pro、Libraries.dev、Watermelon UI 里选型并落地。
---
# Vibecode UI 组件库

给 AI / Vibecode 写 React 界面时，先按场景选库，再按该库的安装方式落地，避免从头造一套平庸 UI。

## 选型（先问场景，再动手）

| 想要的感觉 | 优先选 | 适合干什么 |
| --- | --- | --- |
| 苹果系干净克制、信息层级清楚 | [BoardUI](https://www.boardui.com/) | 后台、数据看板、多智能体 / Agent 界面 |
| 交互细腻、微动效 | [Bencho](https://bencho.dev/) | 打磨按钮、菜单、滑块、拖拽等小控件 |
| 精致成熟产品感、统一利落 | [HeroUI](https://heroui.com/) | 产品后台、个人工具等频繁操作的界面 |
| 品牌感强、渐变光影插画 | [beUI Pro](https://pro.beui.dev/) | 首屏展示、落地页、有辨识度的产品站 |
| 未来感 / AI 科技感特效 | [Libraries.dev](https://libraries.dev/) | AI 思考、聆听、生成中的状态表现 |
| 还没定视觉方向，要多逛 | [Watermelon UI](https://ui.watermelon.sh/) | 先找布局 / Dashboard / Blocks 当参考 |

一次主库 + 必要时一个特效库（例如 BoardUI / HeroUI 做骨架，Libraries.dev 补 AI 态）。不要六个全上。

## 各库要点

### BoardUI — 后台与 Agent
- React + Tailwind，组件以源码写入项目（可改），非运行时依赖。
- 图表、表格、App shell、Composer、流式任务、thinking 指示等适合看板与 Agent UI。
- 起步：`npx boardui@latest init`，再 `npx boardui@latest add <name>`；也可走 shadcn registry。
- Agent：MCP `https://www.boardui.com/mcp`；`npx boardui@latest skill` 可装其 SKILL。
- 规则：语义 token、不要硬编码 `dark:` 颜色。

### Bencho — 微交互
- 可在网页里试 Hover / Press / Drag / Slide 等交互后带走。
- 用来补「操作手感」，不做整站设计系统。
- 从 [bencho.dev](https://bencho.dev/) 挑组件，按页面说明拷进项目。

### HeroUI — 完整产品系统
- 基于 React Aria + Tailwind v4 的完整组件体系（Web + Native）。
- 默认打磨好边缘情况；适合要统一字体、间距、圆角、色板的生产界面。
- 优先读官方 Docs / LLM / MCP / Agent Skills，用其 CLI 或 MCP 安装，不要手抄半套。

### beUI Pro — 品牌与落地页
- 动画 Blocks、页面区块、插画、整站模板；源码进仓库可改。
- Web / Mobile（React Native）分许可；付费 Pro。落地前确认是否已有授权。
- Agent：Skill / MCP / 私有 registry；运动用共享 easing、注意 `prefers-reduced-motion`。

### Libraries.dev — AI 态特效
- MIT 免费包（如 `border-beam`、`thinking-orbs`、`liquid-gooey`、`metal-fx`、`img-fx`），偏视觉特效而非表单系统。
- 用法：复制站点上的「给 coding agent 的 prompt」，粘贴给 Agent 安装配置。
- 只加在真正需要「思考 / 聆听 / 生成」反馈的地方，避免整页特效堆叠。

### Watermelon UI — 灵感与布局
- 开源 React：Animated components、Blocks、Dashboards、Templates。
- 方向未定时先在站内找接近的布局，再决定是否迁到 BoardUI / HeroUI 等主库实现。
- 有 llms.txt、OpenAPI、MCP 入口时可让 Agent 按 docs 拉取。

## 落地步骤

1. 用一句话定场景（后台 / 工具 / 落地页 / AI 态 / 还没想好）。
2. 从上表选 **一个主库**；若有明显 AI 态需求，再加 Libraries.dev。
3. 打开对应官网（或 MCP / skill），用官方 init / add / prompt，不要凭印象重写组件。
4. 先装壳（layout / tokens），再装本页真正用到的组件；保持语义色与间距一致。
5. 交付前自检：信息层级、对比度、键盘可达、减少动画偏好、暗色是否不靠硬编码。

## 不要做的事

- 不要在同一屏混用多套互不兼容的设计 token。
- 不要把特效库当表单 / 表格方案。
- 不要在未授权时安装 beUI Pro 私有内容。
- 不要跳过官方 Agent 资源（MCP / skill / llms.txt）去凭截图瞎猜 API。
