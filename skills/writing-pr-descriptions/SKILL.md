---
name: writing-pr-descriptions
description: "Writes pull request titles and PR descriptions that reviewers can understand in 30 seconds. Use when asked to create PRs, open PRs, or draft or update a PR description."
license: MIT
metadata:
  author: gomzkov
  version: "1.1.0"
---

# Writing PR Descriptions

The reviewer should understand the pull request in 30 seconds.

## Inspect first

1. Identify the base branch from the request, repository, or hosting service.
2. Read the complete diff from the base branch to the PR head, including any uncommitted changes intended for the PR.
3. Read every commit included in the PR.
4. Read the PR template, contribution guide, repository instructions, and existing PR body when updating one.
5. Collect the tests and manual checks that were actually performed. Do not infer testing from changed test files.

Typical local commands are:

```sh
git status --short
git diff --stat <base>...HEAD
git diff <base>...HEAD
git log --reverse --format='%h %s%n%b' <base>..HEAD
```

Use equivalent repository or hosting tools when needed. Include uncommitted changes only if they are intended for the PR. If the base branch or testing history cannot be established, say what is unknown instead of guessing.

## Write the title

Use Conventional Commits:

```text
{type}: {short imperative description}
```

Use `feat`, `fix`, `chore`, `refactor`, `docs`, `test`, `build`, or `ci`. Keep the description short, specific, imperative, and without a final period.

## Write the body

Begin with one sentence that states the outcome. Do not add a `Summary` heading.

Use this structure when the repository does not require a different one:

```markdown
One-sentence summary of the outcome.

## Changes

- Specific behavior change
- Important implementation or compatibility detail
- Relevant operational or user impact

## Testing

- `exact command that was run`
- Manual verification performed

## Notes

- Optional important caveat
```

- Include three to five `Changes` bullets about behavior, purpose, impact, and reviewer-relevant decisions. Do not narrate files or commits.
- List only tests that ran. Include exact commands and manual checks when known. State important untested areas honestly.
- Include `Notes` only for a meaningful caveat, rollout concern, or follow-up. Omit empty sections.
- Preserve required template headings and checklists. Add a ticket only when one is available.
- Use short sentences and bullets. Remove repetition, jargon, filler, and unsupported claims.

See [references/examples.md](references/examples.md) for one good and one bad example.

## Output

Return the title and body first. Explain a choice only when it needs context or the user asks.

If the user asked to create, open, or update the PR, use the final title and body with the available hosting tool, then report the resulting PR link or the exact blocker.
