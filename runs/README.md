# Runs

`runs/` stores Markdown logs for conversations or executions that are split by role.

Default AI_Office work should still happen in one conversation when that is enough. Use a run log only when a request is complex enough to benefit from explicit routing, handoffs, or later review.

## When to Create a Run Log

- The request uses multiple roles such as PM, Researcher, Engineer, or Reviewer.
- The work spans multiple sessions.
- Decisions, assumptions, risks, or handoffs need to be preserved.
- The user asks for an auditable record of the process.

## Suggested Format

Use:

- `templates/run.md` for the overall log
- `templates/routing.md` for role routing
- `templates/role-response.md` for individual role outputs

Suggested filename:

```text
YYYY-MM-DD-short-topic.md
```

Keep logs in Markdown. Do not add automation, external writes, or MCP behavior here unless the user explicitly asks for that in a future change.
