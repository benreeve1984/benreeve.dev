# benreeve.dev

Source for [benreeve.dev](https://benreeve.dev) — a small personal site for notes, writing, and one-off tools.

## Stack

- Plain HTML, no framework, no build step
- Hosted on [GitHub Pages](https://pages.github.com/) from the `main` branch root
- DNS via Cloudflare, served from custom domain `benreeve.dev`
- Sister repo [`tools.benreeve.dev`](https://github.com/benreeve1984/tools.benreeve.dev) hosts standalone tools at `tools.benreeve.dev`

## Layout

```
.
├── CNAME           # tells GitHub Pages which custom domain to serve
├── README.md
├── index.html      # landing page
└── colophon.html   # list of pages and tools, each with a link to commit history
```

## Adding a tool

There are two patterns for hosting tools:

1. **Single-file tool, lives in this repo.** Drop `tool-slug.html` in the repo root, then add an entry to the "Tools" section of `colophon.html` using the template at the bottom of that file.
2. **Tool with multiple files, or worth its own commit history.** Build it in the [`tools.benreeve.dev`](https://github.com/benreeve1984/tools.benreeve.dev) repo and add a colophon entry pointing at `https://tools.benreeve.dev/tool-slug.html`.

Either way, the colophon entry should link to the commit history for that file so visitors can see how it was built.

## Local preview

```sh
python3 -m http.server 8000
# then open http://localhost:8000
```

## Deployment

Pushing to `main` deploys automatically via GitHub Pages. Cloudflare sits in front of GitHub Pages with SSL/TLS mode "Full" and the records proxied (orange cloud). The `CNAME` file in this repo tells Pages to serve at `benreeve.dev`.
