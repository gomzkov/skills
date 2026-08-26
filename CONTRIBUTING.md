# Contributing

Keep each skill focused on one job. Its name and description should make that job clear.

## Add or update a skill

1. Put the skill in `skills/<skill-name>/`.
2. Follow the [Agent Skills specification](https://agentskills.io/specification).
3. Keep `SKILL.md` short. Add supporting files only when they change how the skill works.
4. Remove private data, credentials, client details, and personal examples.
5. Validate the skill, update the skill table in `README.md`, then check installer discovery:

```sh
npx skills@latest add . --list
```

## Commits

Use [Conventional Commits](https://www.conventionalcommits.org/) with a short, specific subject. Add a commit body only when the reason is not clear from the diff.
