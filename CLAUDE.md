# CLAUDE.md — instructions for AI assistants

This is Ben Reeve's personal site at https://benreeve.dev. Sister repo for standalone tools is at https://github.com/benreeve1984/tools.benreeve.dev.

## Conventions

- One HTML file per page, dropped in the repo root. No subdirectories for content.
- All CSS lives in a single inline `<style>` block per file. Copy the block from `index.html` for consistency — same colour variables, same fonts, same spacing.
- Every new page must (a) use the shared serif style, (b) include the favicon link + theme-color + open-graph meta block from `index.html`, and (c) get an entry added to `colophon.html` linking to its source-history URL on GitHub.
- `CNAME` configures GH Pages — do not delete or edit it.

## Don'ts

- No frameworks, no build step, no bundler, no JSX, no TypeScript. Plain HTML/CSS/JS only.
- No web fonts (Google Fonts, Adobe Fonts, etc.). Stick to the system serif stack already defined.
- No analytics, trackers, or third-party scripts.
- No changes to the visual style without Ben's explicit approval.

## Adding a tool

Single-file tools live here directly (drop `tool-slug.html` in the root). Multi-file or commit-history-worthy tools live in the sister `tools.benreeve.dev` repo. Either way, add a colophon entry — template at the bottom of `colophon.html`.
