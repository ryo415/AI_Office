# Export ChatGPT Chief of Staff Prompt

Use this prompt with Codex to update `exports/chatgpt-chief-of-staff.md` from the current AI_Office source files.

## Purpose

Reflect the latest AI_Office operating style, roles, workflows, skills, templates, and preferences in a single ChatGPT-ready Chief of Staff prompt.

The output should help ChatGPT act as AI_Office's Chief of Staff without assuming local repository access.

## Input Files

Read these files:

- `AI_OFFICE.md`
- `README.md`
- `agents/*.md`
- `workflows/*.md`
- `skills/*.md`
- `templates/*.md`
- `memory/preferences.md`

Read only the relevant parts of this file:

- `memory/user-profile.md`

## Output File

Update:

- `exports/chatgpt-chief-of-staff.md`

## Update Policy

- Do not mechanically concatenate the source files.
- Summarize and integrate the current AI_Office rules into one prompt that is easy to paste into ChatGPT or a Custom GPT.
- Keep the prompt self-contained.
- Do not assume ChatGPT can directly read local files.
- Avoid overloading the export with Codex-only implementation steps.
- Keep Codex-specific editing, repository inspection, and verification instructions in `prompts/chief-chat.md`, not in the ChatGPT export.
- Reflect the latest rules for roles, workflows, Markdown-first output, external write confirmation, and destructive-operation confirmation.
- Keep Notion, GitHub, and MCP as optional or future integration targets unless current AI_Office policy says otherwise.
- Reduce duplication.
- Remove stale wording and references to files that no longer exist.
- Keep the export concise enough to paste into a Custom GPT instruction or normal ChatGPT conversation.

## Verification

After updating, verify:

- Referenced file names exist when they are local AI_Office source files.
- Markdown code fences are closed.
- The export does not rely on ChatGPT reading local files directly.
- Codex-specific language is not mixed into the ChatGPT prompt except where needed to explain limitations.
- `prompts/chief-chat.md` remains the Codex-specific Chief of Staff prompt.
- `exports/chatgpt-chief-of-staff.md` remains the ChatGPT/Custom GPT prompt.
- No Notion, GitHub, MCP, or other external integration implementation was added.

## Report

End with:

```markdown
## Summary

## Files Changed

## Verification

## Notes / Next Actions
```
