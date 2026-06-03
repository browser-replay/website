# browserreplay-website

This repo is the source for **browserreplay.com** — the public landing page for the [browser-replay](https://github.com/browser-replay/browser-replay) open source project.

## What browser-replay is

browser-replay is an open source TypeScript library for recording and replaying DOM interactions in the browser. It is a separately maintained project built on top of [rrweb](https://github.com/rrweb-io/rrweb). Key packages:

- `@browser-replay/record` — captures DOM mutations, user interactions, and network events
- `@browser-replay/replay` — replay engine
- `@browser-replay/player` — React player UI component
- `@browser-replay/player-core` — framework-agnostic shared player logic
- `@browser-replay/core` — record + replay core primitives

Use cases: bug reproduction via session replay, automated test generation from real user flows, UX research, incident analysis.

## This repo

Plain HTML + CSS. No build step, no framework, no bundler. Open `index.html` directly in a browser to preview, or use `npx serve .`.

```
.
├── index.html               # Main landing page (all content lives here)
├── styles/
│   └── main.css             # All styles
├── public/
│   ├── favicon.ico          # (add your own)
│   └── og-image.png         # Open Graph image, 1200×630px (add your own)
├── .github/
│   └── workflows/
│       └── deploy.yml       # Auto-deploys to GitHub Pages on push to main
├── CLAUDE.md
└── README.md
```

## Deployment

Deploys automatically to GitHub Pages via the included workflow on every push to `main`. Custom domain: `browserreplay.com` (configure with a `CNAME` file + DNS once the domain is connected).

To enable: go to **Settings → Pages** and set Source to **GitHub Actions**.

## Conventions

- Keep it plain HTML + CSS — do not introduce a build step, framework, or npm dependencies.
- The colour scheme is a dark GitHub-style theme. Keep changes consistent with the existing CSS custom properties in `styles/main.css`.
- All copy should be accurate to the actual browser-replay project. If in doubt, refer to the [main repo README](https://github.com/browser-replay/browser-replay).
- Attribution to rrweb must remain visible (MIT license requirement).
