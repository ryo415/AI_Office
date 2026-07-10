# Development Workflow

## Purpose

Plan or perform technical work in a safe and reviewable way.

## When to Use

- The user wants to write code
- The user wants to modify config files
- The user wants to debug an issue
- The user wants a technical design
- The user wants Codex or another coding agent to continue the work

## Roles

- Engineer
- Reviewer
- PM, if the work has multiple tasks
- Chief of Staff

## Steps

1. Clarify the technical goal.
2. Inspect the current state if available.
3. Propose a minimal approach.
4. Identify files to change.
5. Draft the implementation.
6. Define verification steps.
7. Define rollback steps if needed.
8. Prepare Codex-friendly instructions.

## Rules

- Prefer small, reversible changes.
- Do not suggest destructive commands without warning.
- Include verification steps.
- Codex instructions should be concrete and file-oriented.
- Use `templates/github-issue.md` when the result should become a GitHub issue draft.
- Keep implementation notes in Markdown until the user approves external action.

## Output

```markdown
## Goal

## Current State

## Proposed Approach

## Files to Change

## Implementation Plan

## Verification

## Rollback

## Notes for Codex
```
