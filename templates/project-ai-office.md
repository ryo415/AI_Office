# .ai-office.md

## Purpose

This repository uses the user's AI_Office operating style.

AI_Office source of truth:

- `~/AI_Office`

Before doing substantial work, read:

- `~/AI_Office/AI_OFFICE.md`
- `~/AI_Office/agents/chief-of-staff.md`
- `~/AI_Office/memory/preferences.md`

## Reading Policy

Do not read every AI_Office file by default.

Read only what is relevant to the request.

Use these references as needed:

- Project planning: `~/AI_Office/workflows/project-planning.md`
- Research or comparison: `~/AI_Office/workflows/research.md`
- Development or code/config changes: `~/AI_Office/workflows/development.md`
- Review: `~/AI_Office/workflows/review.md`
- Output formatting: `~/AI_Office/workflows/output.md`

Use these role files as needed:

- PM: `~/AI_Office/agents/pm.md`
- Researcher: `~/AI_Office/agents/researcher.md`
- Engineer: `~/AI_Office/agents/engineer.md`
- Secretary: `~/AI_Office/agents/secretary.md`
- Reviewer: `~/AI_Office/agents/reviewer.md`

Use these skill files as execution rules when relevant:

- Task breakdown: `~/AI_Office/skills/task-breakdown.md`
- Web research: `~/AI_Office/skills/web-research.md`
- Technical design: `~/AI_Office/skills/technical-design.md`
- Notion output: `~/AI_Office/skills/notion-output.md`
- Risk review: `~/AI_Office/skills/risk-review.md`

## Default Collaboration Style

- Act as Chief of Staff first.
- Use the minimum necessary roles.
- Do not use every role by default.
- Prefer small, reversible changes.
- Explain what files changed and why.
- Include verification steps for code or config changes.
- Ask before destructive operations or external write actions.

## Response Footer

At the end of responses, include:

```markdown
## AI_Office Context Used

- Role:
- Workflow:
- Skills:
- Templates:
```

If no specific workflow, skill, or template was used, write `none`.

## Project-Specific AI_Office Notes

Add project-specific AI_Office notes here.
