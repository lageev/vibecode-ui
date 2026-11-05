# Vibecode UI 组件库

Cursor / Grok Bot skill：Vibecode（AI 写前端）时按场景从 6 个高质量 UI 组件库选型并落地。

## 怎么用

### 作为 Cursor Skill

把本仓库放到项目的 `.cursor/skills/vibecode-ui/`（或你的 skills 目录），确保其中有 `SKILL.md`。在对话里 `@` 或提到「选 UI 组件库 / Vibecode 界面好看」时即可触发。

```bash
mkdir -p .cursor/skills/vibecode-ui
curl -fsSL https://raw.githubusercontent.com/lageev/vibecode-ui/main/SKILL.md \
  -o .cursor/skills/vibecode-ui/SKILL.md
```

### 覆盖的库

| 感觉 | 库 |
| --- | --- |
| 苹果系干净克制 | [BoardUI](https://www.boardui.com/) |
| 微交互细腻 | [Bencho](https://bencho.dev/) |
| 成熟产品感 | [HeroUI](https://heroui.com/) |
| 品牌落地页 | [beUI Pro](https://pro.beui.dev/) |
| AI 科技感特效 | [Libraries.dev](https://libraries.dev/) |
| 多逛找方向 | [Watermelon UI](https://ui.watermelon.sh/) |

细节、安装命令与落地步骤见 [`SKILL.md`](./SKILL.md)。

## License

MIT
