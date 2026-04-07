# Cursor

Optional home for **Cursor-specific** rules that you want versioned next to other agent assets.

Cursor’s default path is `.cursor/rules/` (often `.mdc` files). This repo did not ship with any rules before the `agents/` migration.

**Options when you add rules:**

- Author under `agents/cursor/rules/` and copy or symlink into `.cursor/rules/` if Cursor must read that path, or  
- Keep a single source of truth here and document the copy step in your local setup.

Do not commit secrets or machine-specific paths.
