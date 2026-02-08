# Changelog / Diff Summary

Code diffs and changelogs are often cryptic — a wall of changes with no narrative. This prompt translates raw changes into human-readable summaries that explain what changed and why it matters. Essential for release notes, PR descriptions, or helping reviewers understand the intent behind changes.

---

## The Prompt

Summarize what changed between this version and the previous state. Write for someone who needs to understand the changes without reading every line.

Structure your summary as:

### Summary
2-3 sentences: What's the overall theme or purpose of these changes?

### What's New
- Features, capabilities, or files that didn't exist before

### What Changed
- Modifications to existing behavior, logic, or structure
- For each: what it was → what it is now → why

### What's Removed
- Anything deleted, deprecated, or disabled
- Note if removal is breaking (affects existing users/code)

### Breaking Changes
- Anything that requires action from users or downstream code
- Migration steps if applicable

### Technical Notes
- Performance implications
- Dependency changes
- Things reviewers/maintainers should pay attention to

Be specific — reference file names, function names, and line numbers where helpful.
