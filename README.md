# @mae616/design-skills

A collection of UI/UX design skills for Claude Code and other AI agents.

## Installation

```bash
npx skills add mae616/design-skills
```

## Included Skills

| Skill | Description |
|-------|-------------|
| `ui-designer` | Design UI as information architecture + interaction + visual tone, translate into implementable specs |
| `creative-coder` | Translate motion/interaction quality into implementable constraints while preserving a11y and performance |
| `frontend-implementation` | Translate design tools (Figma/Pencil) to robust, extensible implementations |
| `usability-psychologist` | Evaluate UI/flows from cognitive load, error prevention, and accessibility perspectives |
| `accessibility-engineer` | Apply semantic HTML and WAI-ARIA correctly and minimally |

## When Skills Apply

These skills have `user-invocable: false`, meaning they activate automatically based on context rather than being called directly.

### Trigger Examples

- **ui-designer**: screen design, UI design, component design, design system, information architecture
- **creative-coder**: animation, interaction, motion design, transitions, micro-UX
- **frontend-implementation**: UI implementation, design-to-code, Figma to code, responsive design
- **usability-psychologist**: hard to use, high drop-off, confusing, accessibility issues
- **accessibility-engineer**: accessibility, a11y, WAI-ARIA, semantic HTML, keyboard navigation

**Note:** Skills currently support English and Japanese trigger keywords only. PRs welcome for other languages!

## Usage Examples

After installation, these skills automatically activate when you ask relevant questions:

```
# Triggers ui-designer skill
"Design a dashboard layout for analytics"

# Triggers frontend-implementation skill
"Convert this Figma design to React components"

# Triggers accessibility-engineer skill
"Make this form accessible"

# Triggers creative-coder skill
"Add a smooth page transition animation"

# Triggers usability-psychologist skill
"Users are dropping off at the checkout form"
```

## Compatibility

- **Claude Code**: Tested with Claude Code CLI
- **Other AI Agents**: Skills follow standard markdown format, compatible with agents that support similar skill/rule systems

## File Structure

```
design-skills/
├── package.json
├── README.md
├── LICENSE
└── skills/
    ├── ui-designer/SKILL.md
    ├── creative-coder/SKILL.md
    ├── frontend-implementation/SKILL.md
    ├── usability-psychologist/SKILL.md
    └── accessibility-engineer/SKILL.md
```

## Contributing

Contributions are welcome! Here's how you can help:

1. **Add language support**: Add trigger keywords in your language to the "When to Apply" section of each skill
2. **Improve content**: Fix typos, clarify explanations, add examples
3. **Report issues**: Open an issue if you find problems or have suggestions

### How to Contribute

1. Fork this repository
2. Create a branch (`git checkout -b feature/your-feature`)
3. Make your changes
4. Submit a Pull Request

## License

MIT
