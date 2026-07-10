# AI_Office

AI_Office is a personal AI office for organizing thoughts, projects, research, development, tasks, and outputs.

The system is centered around a Chief of Staff role. The user talks to the Chief of Staff, and the Chief of Staff chooses the appropriate workflow, role, skill, and output format.

## Purpose

- Organize vague ideas into actionable projects
- Support research, technical design, development, and review
- Manage personal projects, learning, automation, and side-business ideas
- Produce reusable outputs such as Markdown, Notion-ready documents, GitHub issues, and task lists
- Keep decisions, preferences, and active projects in a structured format

## Core Concept

The user is the owner and final decision maker.

AI_Office does not act as an autonomous company. It acts as a personal office, with multiple roles and workflows that support the user.

## Main Roles

- Chief of Staff: Main interface, intent clarification, routing, and final synthesis
- PM: Project planning, task breakdown, progress management
- Researcher: Investigation, comparison, source checking, uncertainty handling
- Engineer: Technical design, implementation planning, code review support
- Secretary: Notes, tasks, schedules, Notion-ready output
- Reviewer: Risk review, assumptions, omissions, quality check

## Directory Structure

```text
AI_OFFICE.md  Operating policy and routing rules
agents/       Role definitions
workflows/    Repeatable work processes
skills/       Reusable task-specific capabilities
templates/    Output formats
prompts/      Chat prompts for Chief of Staff and role-specific conversations
exports/      Integrated prompts for ChatGPT or other external AI environments
runs/         Markdown logs for role-routed conversations or executions
memory/       Durable user context, preferences, decisions, and project index
projects/     Active or planned project files
inbox/        Unstructured ideas and rough notes
```

## Operating Model

1. The user talks to the Chief of Staff by default.
2. The Chief of Staff selects the smallest useful workflow, role, skill, and template.
3. Supporting roles contribute only when their responsibility is needed.
4. Outputs stay in Markdown unless the user explicitly asks for external publishing.
5. Notion, GitHub, and MCP integrations should consume these Markdown files later instead of replacing them.

## Prompt Exports

- `prompts/chief-chat.md` is the Codex Chief of Staff prompt for repository-aware work.
- `exports/chatgpt-chief-of-staff.md` is the ChatGPT / Custom GPT Chief of Staff export.
- `prompts/export-chatgpt-chief-of-staff.md` is the Codex prompt for refreshing the ChatGPT export from current AI_Office files.

## Using AI_Office From Other Projects

`~/AI_Office` is the source of truth for AI_Office operating policy, roles, workflows, skills, templates, and memory.

For another project repository, use this lightweight structure:

```text
some-project/
|-- AGENTS.md
`-- .ai-office.md
```

The intended reference chain is:

```text
AGENTS.md -> .ai-office.md -> ~/AI_Office
```

- `AGENTS.md` stays short and holds project-specific instructions.
- `.ai-office.md` is a bridge that tells Codex which `~/AI_Office` files to read when relevant.
- AI_Office details stay in `~/AI_Office`; do not copy the full system into each project.

Copy the project templates into the target project:

```sh
cp ~/AI_Office/templates/project-agents.md /path/to/project/AGENTS.md
cp ~/AI_Office/templates/project-ai-office.md /path/to/project/.ai-office.md
```

Start Codex from the target project directory:

```sh
cd /path/to/project
codex
```
