# Examples

## Good

```markdown
Title: fix: preserve filters during pagination

Keeps active search and status filters applied when users move between result pages.

## Changes

- Carries the current query parameters into previous and next page links.
- Leaves unfiltered pagination URLs unchanged for existing bookmarks and integrations.
- Prevents filtered result sets from resetting after the first page.

## Testing

- `npm test -- pagination.test.ts`
- Manually paginated results with one filter, multiple filters, and no filters.
```

This example states the user-visible outcome, gives the reviewer three concrete facts, and names the checks that were run. It omits `Notes` because there is no meaningful caveat.

## Bad

```markdown
Title: enhanced: comprehensive pagination improvements

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

This example uses an unsupported title type, filler words, file narration, vague changes, an unverifiable testing claim, and an empty `Notes` section.
