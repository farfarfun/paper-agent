# Agents

This directory is the canonical home for **in-repo** AI agent instructions and profiles for the paper-agent project.

## Layout

| Path | Purpose |
|------|---------|
| [`AGENTS.md`](./AGENTS.md) | Default instructions for any agent working in this repository. |
| [`paperclip/`](./paperclip/README.md) | Per-agent **full instruction bundle** for each Paperclip company agent (`<urlKey>/…` — `AGENTS.md`, `SOUL.md`, `TOOLS.md`, etc.). |
| [`cursor/`](./cursor/README.md) | Optional Cursor rules; see README for how this relates to `.cursor/rules/`. |
| [`_template/`](./_template/AGENTS.md) | Starter file for new per-agent folders. |
| `<role>/AGENTS.md` | Optional per-role overrides (for example `agents/review/AGENTS.md`). Add subfolders as the team grows. |

## Migration note

The repository had **no** legacy in-tree agent markdown (no `.cursor/rules`, Codex plugin configs, etc.). The **`paperclip/`** tree is populated by **copying** each company agent’s managed `AGENTS.md` from the Paperclip instance so every agent has a corresponding folder under `agents/` (see [`paperclip/README.md`](./paperclip/README.md)).

Point local adapters (Cursor, Paperclip, Codex, and so on) at `agents/AGENTS.md`, a file under `agents/paperclip/<urlKey>/`, or another role-specific path using each tool’s `instructionsFilePath` (or equivalent) setting.
