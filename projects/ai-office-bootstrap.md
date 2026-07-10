# Project: AI_Office

## Status

Active

## Owner

User

## Goal

Build a personal AI office that helps with thinking, research, planning, development, task management, review, and structured output.

## Background

The user wants a role-based AI support system. Instead of calling it an AI company, the system is called AI_Office because it supports both business and non-business topics.

The initial system should be file-based and editable with Codex.

## Success Criteria

- [x] Base directory structure exists
- [x] Core role files exist
- [x] Core workflow files exist
- [x] Core skill files exist
- [x] Output templates exist
- [x] Memory files exist
- [ ] A real request can be processed using the structure
- [ ] Codex can modify and improve the files

## Scope

### In Scope

- Markdown-based role definitions
- Markdown-based workflows
- Markdown-based skills
- Markdown templates
- User memory files
- Project tracking
- Inbox for rough ideas

### Out of Scope

- Full autonomous multi-agent execution
- Automatic Notion writing
- Automatic GitHub issue creation
- Calendar or email integration
- Production-ready MCP integration

## Milestones

### Milestone 1: Base System

- [x] Create directory structure
- [x] Add initial Markdown files
- [x] Review files with Codex
- [x] Clarify file responsibilities

### Milestone 2: First Real Use

- [ ] Add a rough idea to `inbox/ideas.md`
- [ ] Convert it into a project using Project Planning Workflow
- [ ] Save result under `projects/`

### Milestone 3: External Output Preparation

- [x] Add GitHub issue draft template
- [ ] Improve Notion-ready output after first real use
- [ ] Decide how to connect MCP later

## Risks

- Too many roles may create unnecessary complexity.
- Workflows may become too rigid.
- Memory files may become stale.
- External write actions may be risky if automated too early.

## Decisions

- Use `AI_Office` as the project name.
- Use `~/AI_Office` as the directory.
- Start with file-based Markdown management.
- Use Chief of Staff as the main interface.

## Next Action

- [ ] Test the system with one real request through Chief of Staff.

## Notes

This project should evolve gradually. The first goal is repeatability, not full automation.

## External Links

- Notion:
- GitHub:
- MCP:
