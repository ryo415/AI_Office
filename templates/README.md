# Templates

Reusable Markdown templates for AI_Office outputs and project setup.

## Project Bridge Templates

- `project-agents.md`: Short `AGENTS.md` template for each project repository.
- `project-ai-office.md`: `.ai-office.md` template that points Codex back to `~/AI_Office` as the source of truth.

## Role Execution Templates

- `run.md`: Overall Markdown log for a role-routed conversation or execution.
- `routing.md`: Routing plan for choosing Default, Delegated, or Agent Mode and assigning roles.
- `role-response.md`: Standard response shape for PM, Researcher, Engineer, or Reviewer handoffs.

## Usage

Copy these files into the target project:

```sh
cp ~/AI_Office/templates/project-agents.md /path/to/project/AGENTS.md
cp ~/AI_Office/templates/project-ai-office.md /path/to/project/.ai-office.md
```

Then start Codex from the target project:

```sh
cd /path/to/project
codex
```

Keep project-specific instructions in the target project's `AGENTS.md`. Keep AI_Office collaboration and routing instructions in `.ai-office.md`, which should remain a bridge to `~/AI_Office` instead of copying the full AI_Office system into each project.
