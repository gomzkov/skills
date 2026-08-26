# Agent skills

Reusable skills for AI agents.

## Install

Choose skills and target agents interactively:

```sh
npx skills@latest add gomzkov/skills
```

Install one skill globally for Codex:

```sh
npx skills@latest add gomzkov/skills --skill say-it-normally -g -a codex
```

Each skill follows the open [Agent Skills specification](https://agentskills.io/specification).

## Skills

| Skill | What it does |
| --- | --- |
| [`say-it-normally`](skills/say-it-normally/SKILL.md) | Makes agent responses clear, direct, and natural. |
| [`writing-pr-descriptions`](skills/writing-pr-descriptions/SKILL.md) | Writes reviewer-friendly PR titles and descriptions from the full change. |

## Contributing

Issues and pull requests are welcome. Read [CONTRIBUTING.md](CONTRIBUTING.md) before changing a skill.

## License

[MIT](LICENSE)
