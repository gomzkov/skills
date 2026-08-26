---
name: writing-pr-descriptions
description: "Writes concise pull request titles and PR descriptions after inspecting the full diff, included commits, repository guidance, and actual testing. Use for requests to create PRs, open PRs, or draft or update a PR description."
license: MIT
metadata:
  author: gomzkov
  version: "1.0.0"
---

# Writing PR Descriptions

Write a pull request that a reviewer can understand in 30 seconds.

## Gather the evidence

Before drafting:

1. Identify the base branch from the request, repository metadata, or hosting service.
2. Inspect the complete diff from the base branch's merge base to the PR head. Read the full diff, not only the file list or summary.
3. Read every commit included in the PR.
4. Read the repository's PR template, contribution guide, and relevant repository instructions.
5. Collect evidence of tests and manual checks that were actually performed. Do not infer testing from changed test files.
6. When updating an existing PR, read its current title and body before replacing them.

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

Choose the type that best describes the main outcome: `feat`, `fix`, `chore`, `refactor`, `docs`, `test`, `build`, or `ci`.

Keep the description short, specific, and imperative. Do not end it with a period.

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

- Include three to five specific `Changes` bullets. Cover behavior, purpose, impact, and decisions that help the reviewer.
- List only tests that were run. Use exact commands when they are known.
- Describe manual verification plainly. If an important area was not tested, say so and explain why when useful.
- Include `Notes` only for a meaningful caveat, rollout concern, or follow-up. Omit it otherwise.
- Add a ticket link only when one is available. Never invent one.
- Preserve required template headings, checklists, and repository-specific instructions. Apply this writing style within that structure.
- Omit empty or irrelevant optional sections.

## Keep it useful

- Focus on what changed, why it matters, and what the reviewer should pay attention to.
- Mention implementation details only when they affect behavior, compatibility, risk, or review.
- Do not narrate files, restate commit messages, or explain obvious code changes.
- Prefer short sentences and scannable bullets over long paragraphs.
- Remove repetition, corporate jargon, and filler such as "comprehensive," "robust," "enhanced," and "seamless."
- Do not claim results, coverage, compatibility, or safety that the evidence does not support.

See [references/examples.md](references/examples.md) for one good and one bad example.

## Output

Return the proposed title and body first. Explain a choice only when it needs reviewer context or the user asks.

If the user asked to create, open, or update the PR, use the final title and body with the available hosting tool, then report the resulting PR link or the exact blocker.
