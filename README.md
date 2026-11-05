# Vibecode UI 组件库

Agent Skill（[`SKILL.md`](./SKILL.md)）：Vibecode / AI 写前端时，按场景从 6 个高质量 UI 组件库选型并落地。

同一份 `SKILL.md` 兼容 [Cursor](https://cursor.com/)、[Claude Code](https://code.claude.com/docs/en/skills)、[Codex](https://learn.chatgpt.com/docs/build-skills)（以及 Grok Bot）。

## 覆盖的库

| 感觉 | 库 |
| --- | --- |
| 苹果系干净克制 | [BoardUI](https://www.boardui.com/) |
| 微交互细腻 | [Bencho](https://bencho.dev/) |
| 成熟产品感 | [HeroUI](https://heroui.com/) |
| 品牌落地页 | [beUI Pro](https://pro.beui.dev/) |
| AI 科技感特效 | [Libraries.dev](https://libraries.dev/) |
| 多逛找方向 | [Watermelon UI](https://ui.watermelon.sh/) |

选型规则、安装命令与落地步骤见 [`SKILL.md`](./SKILL.md)。

## Cursor

放到项目的 `.cursor/skills/vibecode-ui/`（或用户 skills 目录），对话里 `@` 或提到「选 UI 组件库 / Vibecode 界面好看」即可触发。

```bash
mkdir -p .cursor/skills/vibecode-ui
curl -fsSL https://raw.githubusercontent.com/lageev/vibecode-ui/main/SKILL.md \
  -o .cursor/skills/vibecode-ui/SKILL.md
```

## Claude Code

放到个人或项目 skills 目录；Claude 会按 `description` 自动选用，也可直接 `/vibecode-ui`。

**个人（所有项目）：**

```bash
mkdir -p ~/.claude/skills/vibecode-ui
curl -fsSL https://raw.githubusercontent.com/lageev/vibecode-ui/main/SKILL.md \
  -o ~/.claude/skills/vibecode-ui/SKILL.md
```

**仅当前仓库（可提交给团队）：**

```bash
mkdir -p .claude/skills/vibecode-ui
curl -fsSL https://raw.githubusercontent.com/lageev/vibecode-ui/main/SKILL.md \
  -o .claude/skills/vibecode-ui/SKILL.md
```

用法示例：

- 直接说：「用 vibecode-ui 帮我给后台选一套组件库」
- 或输入：`/vibecode-ui`

说明见 [Extend Claude with skills](https://code.claude.com/docs/en/skills)。

## Codex（CLI / IDE / ChatGPT）

放到用户或仓库的 `.agents/skills/`；可用 `$vibecode-ui` 显式调用，或在任务匹配 `description` 时自动加载。列表里可用 `/skills` 查看。

**个人（所有项目）：**

```bash
mkdir -p ~/.agents/skills/vibecode-ui
curl -fsSL https://raw.githubusercontent.com/lageev/vibecode-ui/main/SKILL.md \
  -o ~/.agents/skills/vibecode-ui/SKILL.md
```

**仅当前仓库（可提交给团队）：**

```bash
mkdir -p .agents/skills/vibecode-ui
curl -fsSL https://raw.githubusercontent.com/lageev/vibecode-ui/main/SKILL.md \
  -o .agents/skills/vibecode-ui/SKILL.md
```

用法示例：

- 显式：`$vibecode-ui` 或「用 vibecode-ui 给落地页选型」
- 查看已装技能：`/skills`
- 也可在 Codex 里用 `$skill-installer` 从其他仓库安装技能

说明见 [Build skills](https://learn.chatgpt.com/docs/build-skills)。

## License

MIT
