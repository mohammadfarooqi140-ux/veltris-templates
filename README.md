# Veltris — Free Template Library

The public library behind [templates.veltris.uk](https://templates.veltris.uk).
Every template Veltris gives away with its reels lives here, and every one of
them is **free** — complete source code, no paywall, no catch.

## What's inside

- `index.html` — the library page. A grid of template cards; each card shows a
  live, scaled-down preview of the template itself (an iframe of the real page,
  frozen at its settled state), with **View live** and **Download** buttons.
- `templates/` — the templates themselves. Each one is a **single self-contained
  HTML file** (HTML, CSS & JavaScript in one file, no build step, no external
  requests). "Download" on a card simply saves that file.
- Currently 11 templates: the Glassy CRM series (V5–V12), Glassy Admin Panel
  V1 & V2, Glassy OTP V5, Glassy Login Form V2 and Glassy Sidebar V5.

## How it deploys

Fully static — there is nothing to build.

- **Host:** Vercel.
- **Root directory:** this folder (the repository root).
- **Framework preset:** Other / none. No build command, no output directory
  override — Vercel serves the files exactly as they are.
- **Domain:** `templates.veltris.uk` (DNS record lives in Cloudflare).

Everything in the repo is a text file (HTML/Markdown), so the whole site can be
pushed and reviewed as plain text.

## Adding a template

1. Drop the single-file template into `templates/<slug>.html`.
2. Add a card for it in `index.html`: an iframe preview pointing at
   `templates/<slug>.html?t=<settled-time>` with a `data-oy` vertical offset
   that frames the dashboard, a View live link, and a Download link to the same
   file.
3. Push. New templates are added as the reels drop.
