# Privacy

This site is a static portfolio. It doesn't have a backend, a database,
accounts, or a contact form — so there is almost nothing to say here,
which is the point.

**What this site collects: nothing.** No analytics, no tracking pixels,
no cookies, no fingerprinting, no "insights". I don't know who visited,
how long you stayed, or what you clicked. I like it that way.

**Contact is just links.** The contact section is a `mailto:` link and a
GitHub link. Clicking email opens your own mail client — nothing is sent
through this site, and nothing is logged by it. If you email me, then
obviously I see your email, because you emailed me.

**Third-party requests your browser makes:**

- Project screenshots are hotlinked from GitHub's CDN
  (`opengraph.githubassets.com`). When you load the work section, your
  browser fetches those images directly from GitHub — GitHub sees those
  requests the way it sees any image load. I don't get any data from it.
- The font (DM Mono) is self-hosted. No Google Fonts, no font CDN.

**Hosting.** The site is hosted as a static Next.js export. The hosting
provider sees standard server logs (IP, requested path, timestamp) the
way any web host does. I don't look at them, and there's no analytics
layer on top.

**Your control.** There's nothing to opt out of because there's nothing
opted in. If you want zero third-party requests, block
`opengraph.githubassets.com` in your content blocker — the site still
works, the screenshots just won't load.
