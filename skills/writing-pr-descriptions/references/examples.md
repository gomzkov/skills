# Examples

## Good

Title: `fix: preserve filters during pagination`

```markdown
Keeps active search and status filters applied when users move between result pages.

## Changes

- Carries the current query parameters into previous and next page links.
- Leaves unfiltered pagination URLs unchanged for existing bookmarks and integrations.
- Prevents filtered result sets from resetting after the first page.

## Testing

- `npm test -- pagination.test.ts`
- Manually paginated results with one filter, multiple filters, and no filters.
```

Why it works: the outcome is clear, the changes are specific, and the checks are exact. `Notes` is omitted because there is no caveat.

## Bad

Title: `enhanced: comprehensive pagination improvements`

```markdown
This PR provides a robust and enhanced pagination experience.

## Changes

- Updated the pagination component.
- Modified the relevant files.
- Made several improvements.

## Testing

- Testing completed successfully.

## Notes

- N/A
```

Why it fails: unsupported title type, filler, file narration, vague changes, an unverifiable test claim, and an empty `Notes` section.
