# wisnu.rafi — Portfolio

My personal portfolio. Security Engineer at BeyondSoft Singapore.
Built with Next.js 16, React 19, and hand-written CSS — no CSS framework,
no icon library, no animation library. The `dependencies` list is three
lines long and it's staying that way.

## Design

`system24 calm` — a quiet, Discord-inspired dark theme. DM Mono everywhere,
oklch grays, one purple accent, square corners, thin labeled panels.
One calm scroll-reveal animation; nothing else moves.

The full concept, rules, and rejected anti-patterns live in `DESIGN.md`.
Read it before touching anything visual.

## Getting started

```bash
npm install
npm run dev
```

Open [http://localhost:3000](http://localhost:3000).

## How content works

There is no CMS. Every word on the site lives in one file:

```
src/lib/data.ts   # projects, changelog, expertise, stack — edit this
```

To add or update a project, edit its entry in `data.ts` — title, blurb,
description, tags, repo link. The components render whatever is there.
Copy is written in the owner's voice: plain, specific, no buzzwords.

**Project screenshots are hotlinked, not committed.** Each project's
image comes from that repo's GitHub social preview
(`opengraph.githubassets.com/...`). To change a screenshot, update the
repo's social image on GitHub — the site picks it up automatically.

## SEO

Set the production URL — it's the base for metadata, sitemap, and OG:

```bash
cp .env.example .env.local
# NEXT_PUBLIC_SITE_URL=https://your-domain.com
```

What's wired up: full metadata in `layout.tsx`, `sitemap.ts`, `robots.ts`,
JSON-LD (`components/json-ld.tsx`), a dynamic OG card
(`opengraph-image.tsx`, system24 styled), and `llms.txt` for AI crawlers
(`app/llms.txt/route.ts`).

## Scripts

- `npm run dev` — local dev server
- `npm run build` — production build
- `npm run start` — serve the production build
- `npm run lint` — eslint

## Structure

```
src/
  app/
    page.tsx            # composition
    layout.tsx          # DM Mono font + metadata
    globals.css         # the entire design system (custom CSS)
    sitemap.ts / robots.ts / llms.txt/route.ts
    opengraph-image.tsx # dynamic OG card
  components/           # topbar, hero, profile, changelog, expertise,
                        # work, stack, contact, footer, statusbar, ...
  lib/
    data.ts             # all content lives here
```

## Project docs

- `DESIGN.md` — the design concept and rules
- `CONTRIBUTING.md` — how to contribute (small fixes welcome)
- `SECURITY.md` — how to report security issues
- `roadmap.txt` — where it's heading, and what's out of scope

## Privacy

No analytics, no cookies, no tracking. This site collects nothing.

## License

MIT — see `LICENSE`.
