# Agent skills

A collection of reusable skills for AI agents.

## Install

Pick the skills and agents interactively:

```sh
npx skills@latest add gomzkov/skills
```

Install one skill globally for Codex:

```sh
npx skills@latest add gomzkov/skills --skill say-it-normally -g -a codex
```

The repo follows the open [Agent Skills specification](https://agentskills.io/specification). The installer also supports Claude Code, Cursor, and many other agents.

## Skills

### `say-it-normally`

Writes any agent response in plain, natural language without flattening its meaning or voice.

[Read the skill](skills/say-it-normally/SKILL.md)

### `writing-pr-descriptions`

Drafts Conventional Commit PR titles and concise descriptions from the full change and actual testing.

[Read the skill](skills/writing-pr-descriptions/SKILL.md)

## Contributing

Issues and pull requests are welcome. See [CONTRIBUTING.md](CONTRIBUTING.md) before adding or changing a skill.

## License

[MIT](LICENSE)
