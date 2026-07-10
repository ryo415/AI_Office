# AI_Office Usage

This repository is the configuration and working memory for a personal AI office.

Use it as a Markdown-first operating system. The user talks to the Chief of Staff, and the Chief of Staff chooses the smallest useful workflow, role, skill, and template.

## Basic Rule

Start from `AI_OFFICE.md`.

`AI_OFFICE.md` defines the operating policy, role routing, file responsibilities, and confirmation rules. When another file conflicts with `AI_OFFICE.md`, treat `AI_OFFICE.md` as the source of truth.

## Daily Flow

1. Put rough ideas in `inbox/`.
2. Ask the Chief of Staff to clarify the request.
3. Use a workflow only when the request is complex enough to benefit from repeatable steps.
4. Use supporting agents only when their responsibility is needed.
5. Use a template when the output should be saved, reused, pasted into Notion, or converted into a GitHub issue later.
6. Save active project details in `projects/`.
7. Keep durable preferences, decisions, and project indexes in `memory/`.

## Directory Responsibilities

| Path | Purpose | Edit When |
|---|---|---|
| `AI_OFFICE.md` | Operating policy and routing rules | The whole system behavior should change |
| `README.md` | Short overview of the repository | The public-facing explanation changes |
| `agents/` | Role definitions | A role's responsibility needs clarification |
| `workflows/` | Repeatable process steps | A recurring work process needs improvement |
| `skills/` | Reusable task-specific execution rules | A capability needs better rules or output expectations |
| `templates/` | Output formats | A reusable document shape is needed |
| `memory/` | Durable user context and indexes | A preference, decision, profile fact, or active project index changes |
| `projects/` | Active or planned project documents | A project is created or updated |
| `inbox/` | Rough notes and unstructured ideas | An idea is not ready to become a project |

## How To Ask AI_Office For Help

Use the Chief of Staff as the default interface.

Good request examples:

- "Chief of Staff, turn this rough idea into a small project."
- "Review this plan for risks and missing assumptions."
- "Research options for this tool and recommend one."
- "Create a GitHub issue draft from this task."
- "Convert these notes into Notion-ready Markdown."
- "Update the active project index after this project changed."

For small questions, the Chief of Staff should answer directly.

For larger requests, the Chief of Staff should identify:

1. Goal
2. Assumptions
3. Workflow
4. Supporting roles
5. Skill or template
6. Next action

## When To Use Each Workflow

| Workflow | Use For | Typical Output |
|---|---|---|
| `workflows/intake.md` | Vague or ambiguous requests | Clarified request and next workflow |
| `workflows/project-planning.md` | Turning an idea into a project | Project document using `templates/project.md` |
| `workflows/research.md` | Comparisons, current information, decision support | Research report using `templates/research-report.md` |
| `workflows/development.md` | Code, config, debugging, technical planning | Technical plan, file list, verification steps, GitHub issue draft |
| `workflows/review.md` | Important outputs, risks, assumptions, quality check | Review report using `templates/review-report.md` |
| `workflows/output.md` | Formatting for Markdown, Notion, GitHub, or task lists | Copy-pasteable output using a template |

## When To Use Each Agent

| Agent | Use When |
|---|---|
| Chief of Staff | Always as the main interface, router, and final synthesizer |
| PM | A goal needs scope, milestones, tasks, blockers, or next actions |
| Researcher | A topic needs evidence, comparison, sources, or current information |
| Engineer | A request involves code, config, debugging, technical design, or validation |
| Secretary | Notes, task lists, summaries, and external-output-ready Markdown are needed |
| Reviewer | The result may affect decisions, systems, cost, security, privacy, or publication |

Use the minimum necessary roles. Do not run every request through every agent.

## Common Operations

### Capture A Rough Idea

1. Add it to `inbox/ideas.md` or create a new file from `templates/inbox-item.md`.
2. Keep it rough. Do not force structure too early.
3. Later, ask the Chief of Staff whether it should become a project, task, research item, decision, or archive.

### Create A Project

1. Start with the Chief of Staff.
2. Use `workflows/project-planning.md`.
3. Create a project file from `templates/project.md` under `projects/`.
4. Add the project to `memory/active-projects.md` if it is active.

### Track A Decision

1. Use `templates/decision-log.md`.
2. Add durable decisions to `memory/decisions.md`.
3. Keep one decision entry focused on one decision.

### Prepare A GitHub Issue Draft

1. Use `templates/github-issue.md`.
2. Keep it as Markdown unless the user explicitly approves creating or updating a GitHub issue.
3. Add related files and acceptance criteria so it can become an issue later.

### Prepare Notion-Ready Markdown

1. Use `skills/notion-output.md`.
2. Keep headings and properties stable.
3. Do not write to Notion unless the user explicitly approves it.

### Review Important Output

1. Use `workflows/review.md`.
2. Use `templates/review-report.md` if the review should be saved.
3. Focus on material risks, missing assumptions, and concrete fixes.

## External Action Policy

The repository is Markdown-first. External integrations are future extensions.

Allowed without confirmation:

- Summarizing
- Brainstorming
- Planning
- Reviewing
- Drafting Markdown
- Creating Notion-ready text
- Creating GitHub issue drafts

Requires confirmation:

- Writing to Notion
- Creating or updating GitHub issues or pull requests
- Editing actual files outside the requested scope
- Running destructive commands
- Sending emails
- Creating calendar events
- Publishing content

## Maintenance Guidelines

- Keep files small and readable.
- Prefer stable headings over clever structure.
- Avoid duplicating the same project details in both `memory/` and `projects/`.
- Treat `memory/active-projects.md` as an index, not a full project tracker.
- Keep one active or planned project per file in `projects/`.
- Keep templates generic enough to reuse.
- Add fields for Notion, GitHub, or MCP only when they are useful as plain Markdown.

## Recommended Weekly Review

Once a week:

1. Review `memory/active-projects.md`.
2. Update active project files in `projects/`.
3. Move stale inbox items forward or archive them.
4. Add important decisions to `memory/decisions.md`.
5. Update `memory/preferences.md` if a stable preference changed.
6. Use `templates/weekly-review.md` if the review should be saved.

