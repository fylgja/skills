# Fylgja Skills

Agent skills for building UI with [Fylgja CSS](https://fylgja.dev/), a modular CSS library built around plain HTML. They teach your AI assistant how Fylgja is put together, so it reaches for native elements, design tokens, and dynamic utilities instead of inventing classes.

| Skill | Use for |
| --- | --- |
| `fylgja-css` | The rules, setup, and a reference for Base, Tokens, Utilities, and Components |
| `create-fylgja-accordion` | Accordions and FAQ lists on `<details>` |
| `create-fylgja-menu` | Dropdown and action menus on the Popover API |
| `create-fylgja-modal` | Modals and confirmations on `<dialog>` |
| `create-fylgja-offcanvas` | Drawers and side panels on `<dialog>` |

## Install

### Claude Code

```text
/plugin marketplace add fylgja/skills
/plugin install fylgja@fylgja
```

### Other agents

Copy a skill folder into your project. The `fylgja-css` skill has reference files, so download the whole folder, not only the `SKILL.md`:

```bash
# Replace .agents with your AI agent folder, e.g. .claude, .cursor, .github or .codex
mkdir -p .agents/skills
curl -L https://codeload.github.com/fylgja/skills/tar.gz/main | tar -xz -C .agents/skills --strip-components=2 skills-main/skills/fylgja-css
```

## Contributing

The skills describe the published packages. Run `npm install`, then `npm test` checks that every CSS variable and `@fylgja/*` path in a skill exists in those packages. There is no lockfile on purpose, so the weekly check also catches a new release that breaks a skill.

When you change a skill, raise `version` in `.claude-plugin/plugin.json`.

## License

Fylgja Skills is licensed under the [MIT License](https://github.com/fylgja/skills/blob/main/LICENSE).
