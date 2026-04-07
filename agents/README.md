# Agents

This directory is the canonical home for **in-repo** AI agent instructions and profiles for the paper-agent project.

## Layout

| Path | Purpose |
|------|---------|
| [`AGENTS.md`](./AGENTS.md) | Default instructions for any agent working in this repository. |
| [`cursor/`](./cursor/README.md) | Optional Cursor rules; see README for how this relates to `.cursor/rules/`. |
| `<role>/AGENTS.md` | Optional per-role overrides (for example `agents/review/AGENTS.md`). Add subfolders as the team grows. |

## Migration note

At the time this folder was introduced, the repository had **no** existing agent definition files under version control (no `.cursor/rules`, Codex plugin configs, or other agent markdown in-tree). Nothing was moved; this structure is the baseline for future additions.

Point local adapters (Cursor, Paperclip, Codex, and so on) at `agents/AGENTS.md` or a role-specific file under `agents/` using each tool’s `instructionsFilePath` (or equivalent) setting.
