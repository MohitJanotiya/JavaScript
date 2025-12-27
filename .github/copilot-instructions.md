## Purpose

This repository is a very small static HTML project (two top-level pages: `index.html` and `list.html`). This file gives concise, actionable guidance to an AI coding agent so it can be immediately productive editing content, fixing HTML issues, and producing small improvements.

## Quick orientation
- Project type: static HTML (no build tooling, frameworks, or tests present).
- Entrypoints: `index.html` (resume/profile content) and `list.html` (HTML lists & table examples).
- External integrations: a few external links (LinkedIn, GitHub, Netlify) and an avatar image loaded from GitHub.

## How to run / verify locally
- The site can be previewed by opening the HTML files directly in a browser. For a local server preview (recommended for link testing), use a quick static server, e.g.:

```sh
python3 -m http.server 8000
# then open http://localhost:8000/index.html
```

## What changes are safe to make without asking
- Content edits: copy/text updates inside `index.html` and `list.html` (names, bullets, paragraphs, links).
- Minor markup fixes: correct obvious HTML typos (unclosed tags, malformed attributes) when they clearly fix rendering (but prefer minimal diffs).
- External URLs: update or replace links (e.g., update portfolio/Netlify links) if the new URL is authoritative.

## What to avoid or ask about first
- Do not introduce a build system, framework, or major refactor without asking the repo owner.
- Avoid large structural rewrites (moving to React, adding CSS frameworks) unless requested.

## Project-specific patterns & examples
- Contact link (edit the email): the mailto anchor is in `index.html` near the top. Example: `<a href="mailto:mjanotiya@gmail.com">mjanotiya@gmail.com</a>`.
- Avatar image: `index.html` uses an external GitHub avatar URL. If changing, prefer a secure external URL or add a local `/assets/` folder and update the src accordingly.
- Details widget: the resume uses a `<details>` element for soft skills — keep this semantic pattern if adding similar collapsible sections.
- Tables & examples: `list.html` contains table markup and sample lists. Some table rows/cells include malformed attributes (e.g., `td.` or stray attributes). When fixing, prefer minimal edits and ensure the visual layout remains the same.

## Debugging and validation tips
- Use the browser DevTools to check rendering and console errors.
- Run the HTML through an online validator (W3C) or a local linter to find structural issues before committing.

## Pull request guidance
- Describe intent in the PR title and description (e.g., "Fix broken table markup in list.html" or "Update email and links in index.html").
- Include a short screenshot or note how you verified the change (local server URL + browser used).

## If you need more context
- Ask the repo owner before adding build tooling, tests, or moving assets.
- When in doubt about content (e.g., personal data or resume changes), request confirmation before committing.

---
If anything above is unclear or you want different conventions (e.g., add CSS or set up a dev server), tell me which direction and I will update this file.
