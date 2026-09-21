# Agents

This directory is the canonical home for **in-repo** AI agent instructions and profiles for the paper-agent project.

## Layout

| Path | Purpose |
|------|---------|
| [`AGENTS.md`](./AGENTS.md) | Default instructions for any agent working in this repository. |
| [`paperclip/`](./paperclip/README.md) | Per-agent **full instruction bundle** for each Paperclip company agent (`<urlKey>/…` — `AGENTS.md`, `SOUL.md`, `TOOLS.md`, etc.). |
| [`_template/`](./_template/AGENTS.md) | Starter file for new per-agent folders. |
| `<role>/AGENTS.md` | Optional per-role overrides (for example `agents/review/AGENTS.md`). Add subfolders as the team grows. |

## Migration note

The repository has **no** legacy in-tree agent markdown (no `.cursor/rules`, Codex plugin configs, etc.). The **`paperclip/`** tree is reserved for copies of each company agent’s managed instructions from the Paperclip instance; it is currently empty (see [`paperclip/README.md`](./paperclip/README.md)).

Point local adapters (Cursor, Paperclip, Codex, and so on) at `agents/AGENTS.md`, a file under `agents/paperclip/<urlKey>/`, or another role-specific path using each tool’s `instructionsFilePath` (or equivalent) setting.
