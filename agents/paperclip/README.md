# Paperclip agent mirrors

This folder contains **verbatim copies** of each **WAR** company agent’s full managed **instructions root** from the local Paperclip instance (`instructionsRootPath`: `…/companies/<companyId>/agents/<agentId>/instructions/`). That includes `AGENTS.md` plus companion files such as **`SOUL.md`**, **`TOOLS.md`**, **`HEARTBEAT.md`** (when present), and any subfolders (for example `memory/`).

| Folder | Agent (Paperclip `urlKey`) |
|--------|----------------------------|
| [`ceo/`](./ceo/AGENTS.md) | CEO |
| [`cto/`](./cto/AGENTS.md) | CTO |
| [`python-engineer/`](./python-engineer/AGENTS.md) | Python Engineer |
| [`using-superpowers/`](./using-superpowers/AGENTS.md) | Using Superpowers |
| [`receiving-code-review/`](./receiving-code-review/AGENTS.md) | Receiving Code Review |
| [`brainstorming/`](./brainstorming/AGENTS.md) | Brainstorming |
| [`systematic-debugging/`](./systematic-debugging/AGENTS.md) | Systematic Debugging |
| [`requesting-code-review/`](./requesting-code-review/AGENTS.md) | Requesting Code Review |
| [`test-driven-development/`](./test-driven-development/AGENTS.md) | Test-Driven Development |
| [`executing-plans/`](./executing-plans/AGENTS.md) | Executing Plans |
| [`writing-skills/`](./writing-skills/AGENTS.md) | Writing Skills |
| [`routine-operations/`](./routine-operations/AGENTS.md) | Routine Operations |

**Canonical for runtime:** Paperclip still loads instructions from the managed bundle on disk or via the control plane. Treat these files as a **repo-local snapshot** for search, review, and onboarding—not as the source of truth for adapter `instructionsFilePath` unless you intentionally repoint adapters.

**Refreshing:** Re-run the recursive copy from a machine that can read each agent’s `instructionsRootPath` (see Paperclip agent `adapterConfig` in the API).
