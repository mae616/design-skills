# @mae616/design-skills

A collection of UI/UX design decision skills for Claude Code and AI agents. These skills automatically activate during design, implementation, and review tasks.

## Installation

```bash
npx skills add mae616/design-skills
```

## Included Skills

| Skill | Auto-triggers when... |
|-------|----------------------|
| `ui-designer` | Screen design, component design, design system, information architecture, visual hierarchy |
| `frontend-implementation` | Design-to-code, component implementation, responsive design, UI fixes |
| `creative-coder` | Animation, motion design, transitions, scroll effects, micro-UX, interaction design |
| `accessibility-engineer` | Any UI implementation, forms, interactive components, a11y concerns |
| `usability-psychologist` | UX review, user confusion, drop-off analysis, form usability, cognitive load issues |

## How It Works

1. **Install** the skills
2. **Add** the decision framework to your `CLAUDE.md` (see [Setup](#setup-add-to-your-claudemd) below)
3. Skills are applied **automatically** during relevant conversations—no explicit invocation needed

### Example Conversations

```
User: "Design a dashboard layout for analytics"
→ ui-designer skill activates

User: "Convert this Figma design to React"
→ frontend-implementation + accessibility-engineer skills activate

User: "Add a smooth page transition"
→ creative-coder skill activates

User: "Users keep abandoning our checkout form"
→ usability-psychologist skill activates

User: "Make this modal keyboard accessible"
→ accessibility-engineer skill activates
```

## Language Support

Skills support **English** and **Japanese** trigger keywords.

- English: "design", "implement", "animation", "accessibility", "usability"
- Japanese: 画面設計, UI実装, アニメーション, アクセシビリティ, 使いにくい

PRs welcome for additional language support!

## File Structure

```
design-skills/
├── skills/
│   ├── ui-designer/
│   │   └── SKILL.md
│   ├── frontend-implementation/
│   │   └── SKILL.md
│   ├── creative-coder/
│   │   └── SKILL.md
│   ├── accessibility-engineer/
│   │   └── SKILL.md
│   └── usability-psychologist/
│       └── SKILL.md
├── package.json
├── README.md
└── LICENSE
```

## Setup: Add to Your CLAUDE.md

To enable automatic skill activation, add the following to your `CLAUDE.md`, `agent.md`, or system prompt:

### English Version

```markdown
## Design Skills (Auto-apply)

When working on design or UI implementation tasks, apply the following decision frameworks from design-skills:

| Context | Skill | Focus |
|---------|-------|-------|
| Screen/component design | ui-designer | Information architecture → visual hierarchy → componentization |
| Design to code | frontend-implementation | Intent over pixels, structure over magic numbers, states are specs |
| Animation/interaction | creative-coder | Purpose-driven motion, a11y-safe, performance-aware |
| Any UI implementation | accessibility-engineer | Native elements first, minimal ARIA, keyboard baseline |
| UX review/friction | usability-psychologist | Cognitive load, error prevention, consistency |

Key principles:
- States (loading/error/empty/disabled) must be defined—not afterthoughts
- Use tokens/components/patterns instead of one-off solutions
- Accessibility is built-in, not bolted-on
```

### Japanese Version / 日本語版

```markdown
## デザインスキル（自動適用）

デザインやUI実装のタスクでは、以下の判断軸を適用すること：

| コンテキスト | スキル | 観点 |
|-------------|--------|------|
| 画面・コンポーネント設計 | ui-designer | 情報設計→視覚階層→コンポーネント化 |
| デザインから実装 | frontend-implementation | ピクセルより意図、マジックナンバーより構造、状態も仕様 |
| アニメーション・インタラクション | creative-coder | 目的ある動き、a11y安全、パフォーマンス意識 |
| UI実装全般 | accessibility-engineer | ネイティブ要素優先、ARIA最小、キーボード基本 |
| UXレビュー・離脱分析 | usability-psychologist | 認知負荷、エラー防止、一貫性 |

共通原則：
- 状態（loading/error/empty/disabled）は後付けではなく仕様として定義
- 場当たりではなくトークン・コンポーネント・パターンで統一
- アクセシビリティは最初から組み込む
```

## Skill Philosophy

These skills share common principles:

1. **Systematic over ad-hoc** - Use tokens, components, and patterns instead of one-off solutions
2. **States are specs** - Loading, error, empty, disabled states must be defined
3. **Accessibility by default** - Not an afterthought; built into every implementation
4. **Intent over pixels** - Understand purpose before translating to code

## Compatibility

- **Claude Code**: Fully supported
- **Other AI Agents**: Skills use standard markdown format, portable to similar systems

## Contributing

Contributions welcome!

- **Add language support**: Extend trigger keywords in "When to Apply" sections
- **Improve content**: Clarify explanations, add examples, fix issues
- **Report bugs**: Open an issue for problems or suggestions

### How to Contribute

1. Fork this repository
2. Create a branch (`git checkout -b feature/your-feature`)
3. Make changes and test
4. Submit a Pull Request

## License

MIT
