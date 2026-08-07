# Installer notes

This repository uses the shared `skills` CLI instead of publishing its own npm package.

## Decision

Keep each skill under `skills/<name>/SKILL.md`. The CLI discovers that layout directly from a GitHub repository, lets the user choose a skill and agent, and supports global or project installation.

That gives this repository the same install path used by other public skill libraries:

```sh
npx skills@latest add gomzkov/skills
```

No `package.json`, generated installer, or copied CLI code is needed here.

## Sources

- [The `skills` CLI README](https://github.com/vercel-labs/skills/blob/main/README.md) documents GitHub shorthand, selective installs, local installs, and supported agents.
- [Matt Pocock's skills repository](https://github.com/mattpocock/skills) uses `npx skills@latest add mattpocock/skills` for Codex and other agents.
- [The Agent Skills specification](https://agentskills.io/specification) defines the `SKILL.md` format, naming rules, optional folders, and validation.
- [OpenAI's skill documentation](https://developers.openai.com/codex/skills) explains Codex skill discovery, activation, and optional `agents/openai.yaml` metadata.

Checked on 2026-08-07.
