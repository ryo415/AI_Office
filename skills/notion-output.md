# Notion Output Skill

## Purpose

Convert content into Notion-ready Markdown or database-friendly fields.

## Input

- Source content
- Destination database or page type
- Desired format

## Rules

- Do not write to Notion without confirmation.
- Keep property names stable.
- Use checkboxes for tasks when useful.
- Make output easy to paste into Notion.
- Keep Markdown readable even without Notion.
- Do not introduce Notion-only structure unless the user asks for it.

## Output

```markdown
## Title

## Summary

## Properties

- Status:
- Priority:
- Area:
- Project:
- Due:
- Tags:

## Body

## Tasks

## Decisions

## Next Actions
```
