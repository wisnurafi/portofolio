# Contributing to portofolio

This is a personal site — my name, my career, my taste. I don't expect
drive-by PRs, and most design decisions here are deliberate, not open
for debate. That said, if you spot a typo, a broken link, or a real bug,
a small PR is welcome.

## Setup

```bash
npm install
npm run dev
```

Open http://localhost:3000.

## Before you change anything visual

Read `DESIGN.md`. The short version:

1. Dark only. One background, two panel tones, oklch grays.
2. One accent: purple for interactive highlights, green only for live dots.
3. DM Mono for everything. No second font, ever.
4. Square corners. No border radius anywhere.
5. One animation: a calm reveal (fade + 20px rise). Nothing else moves.
6. Show, don't list: real screenshots, real copy, no lorem anything.

And the anti-patterns that get a PR closed on sight: grid backgrounds,
pill badges, fake code comments, em-dashes in copy, generic status pills,
marquee tickers, custom cursors, magnetic buttons, horizontal scroll
gimmicks. If it looks like a template, it does not ship.

## Content

All copy lives in `src/lib/data.ts` — projects, changelog, expertise,
stack. Edit the data, not the components, unless the layout itself needs
to change. Copy is written in the owner's voice: plain, specific, no
buzzwords. Match it or don't touch it.

Project screenshots are hotlinked from each repo's GitHub social preview
(`opengraph.githubassets.com`). To change a project's image, change that
repo's social image — the site picks it up automatically. Don't commit
image files here.

## Checks

```bash
npm run lint     # eslint
npm run build    # must compile clean
```

## Pull requests

- One small change per PR.
- Commit messages read like a human wrote them: `fix: ...`, `feat: ...`.
- Don't add dependencies. The `dependencies` list is three lines long
  (next, react, react-dom) and it's staying that way.
- Don't add analytics, tracking, cookies, or a contact form. See
  `roadmap.txt` for why these are explicitly out of scope.
