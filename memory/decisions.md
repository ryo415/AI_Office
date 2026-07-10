# Decisions

## 2026-07-08: Name the system AI_Office

### Decision

Use `AI_Office` as the project name.

### Reason

The system is not limited to business topics. It supports many areas of the user's life and work, so "Office" is more appropriate than "Company".

### Consequences

- Use `AI_Office` as the project name.
- Use `~/AI_Office` as the local directory.
- Use office-like roles such as Chief of Staff, PM, Researcher, Engineer, Secretary, and Reviewer.

## 2026-07-08: Keep AI_Office Markdown-first

### Decision

Use Markdown files as the source of truth before adding Notion, GitHub, or MCP integrations.

### Reason

Markdown keeps the system inspectable, editable with Codex, and easy to version. Future integrations can consume the files later without changing the operating model.

### Consequences

- Keep operating policy in `AI_OFFICE.md`.
- Keep role definitions in `agents/`.
- Keep reusable processes in `workflows/`.
- Keep output formats in `templates/`.
- Keep rough ideas in `inbox/`.
- Keep active project details in `projects/`.
- Keep durable cross-project context in `memory/`.
- Do not automate external writes until the user explicitly approves that capability.
