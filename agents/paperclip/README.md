# Paperclip agent mirrors

This directory mirrors each Paperclip company agent's **full instruction bundle** (`AGENTS.md`, `SOUL.md`, `TOOLS.md`, …) under `<urlKey>/`, so every agent managed in the Paperclip instance also has a corresponding in-repo copy.

## Status

Not yet populated. No company agent bundles have been copied into this tree yet — see the migration note in [`../README.md`](../README.md#migration-note) for the intended population process.

## Layout (once populated)

```
paperclip/
  <urlKey>/
    AGENTS.md
    SOUL.md
    TOOLS.md
    ...
```

Each `<urlKey>/` folder should mirror that agent's managed instructions from the Paperclip instance verbatim — this directory is a read-through copy, not a place to hand-author agent instructions (use `agents/_template/AGENTS.md` for new custom profiles instead).
