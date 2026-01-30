# @mae616/design-skills

A collection of UI/UX design decision skills for Claude Code and AI agents. These skills automatically activate during design, implementation, and review tasks.

## Installation

### Claude Code (Plugin)

```bash
/plugin add mae616/design-skills
```

### npx (Alternative)

```bash
npx skills add mae616/design-skills
```

## Included Skills

| Skill | Auto-triggers when... |
|-------|----------------------|
| `ui-designer` | Screen design, component design, design system, information architecture, visual hierarchy |
| `frontend-implementation` | Design-to-code, Figma/Sketch conversion, component implementation, responsive design, UI fixes |
| `creative-coder` | Animation, motion design, transitions, scroll effects, micro-UX, interaction design |
| `accessibility-engineer` | Any UI implementation, forms, interactive components, a11y concerns |
| `usability-psychologist` | UX review, user confusion, drop-off analysis, form usability, cognitive load issues |

## How It Works

All skills have `user-invocable: false`, meaning they activate **automatically** based on conversation context rather than requiring explicit invocation.

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
├── .claude-plugin/
│   └── plugin.json           # Plugin manifest
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

## Skill Philosophy

These skills share common principles:

1. **Systematic over ad-hoc** - Use tokens, components, and patterns instead of one-off solutions
2. **States are specs** - Loading, error, empty, disabled states must be defined
3. **Accessibility by default** - Not an afterthought; built into every implementation
4. **Intent over pixels** - Understand purpose before translating to code

## Compatibility

- **Claude Code**: Fully supported (plugin format)
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
