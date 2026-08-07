# Contributing

Keep each skill focused on one job. A person should be able to understand what it does from the name and description alone.

## Adding or changing a skill

1. Put the skill in `skills/<skill-name>/`.
2. Follow the [Agent Skills specification](https://agentskills.io/specification).
3. Keep detailed examples and background in `references/` so the main `SKILL.md` stays short.
4. Do not include private data, client details, credentials, or examples that depend on personal context.
5. Update the skill list in `README.md`.
6. Check that the installer can find it:

```sh
npx skills@latest add . --list
```

## Commits

Use [Conventional Commits](https://www.conventionalcommits.org/):

- `feat:` for a new skill or capability
- `fix:` for a behavior correction
- `docs:` for documentation only
- `chore:` for maintenance

Keep the subject short and explain the reason in the commit body when it is not obvious from the diff.
