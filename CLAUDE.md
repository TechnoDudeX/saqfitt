# CLAUDE.md — SAQFITT

## Project overview

Static HTML/CSS/JS site for SAQFITT — Saqlain's fitness coaching brand. No build step. Deployed on Netlify (auto-deploys on push to `main`).

## Pages

| File | URL | Notes |
|------|-----|-------|
| `index.html` | `/` | Main coaching landing page |
| `links.html` | `/links` | Links page (formerly `/linktree`) |
| `media.html` | `/media` | Media kit |
| `hevy.html` | `/hevy` | Hevy Coach partnership proposal |
| `humehealth.html` | `/humehealth` | Hume Health UGC partnership proposal |
| `404.html` | — | Custom 404 |

## Design system

### index.html (main site)
- **Light theme**: `#f7f5f1` background, `#ffffff` cards, `#111111` text, `#555555` muted text
- Accent: `#c28800` (brand gold). For small accent-colored text (labels, small headings) use the darker `--accent-text` `#8a6000` for WCAG AA contrast; large display headings keep `#c28800`.
- Fonts: `Bebas Neue` (display) + `DM Sans` (body)
- `404.html` and `favicon.svg` follow this same light/gold system.

> Note: the site was redesigned from an earlier dark + lime (`#0a0a0a` / `#c8ff00`) look to the current light + gold theme. Any lingering lime is legacy.

### Partnership pages (hevy.html, humehealth.html)
- Each has its own aesthetic matched to the partner brand
- `hevy.html` follows the Hevy Coach site aesthetic: clean white/light, blue `#006799`, and uses the **Inter** body font (a deliberate Hevy-brand match — not DM Sans)
- `humehealth.html` follows a dark aesthetic with Hume blue `#3881ff`

### Navbar
- Each page hand-maintains its **own** copy of the SAQFITT navbar — they are **not** shared or included. Editing the nav on one page does **not** update the others; keep them in sync manually.

## Key context

- **Saq is a Hevy Ambassador** — targeting Toronto / North America
- **Social handles:** both TikTok accounts are live — `@saqfitt` (main brand handle) and `@trainwithsaq` (Hevy-ambassador content account for the Toronto market). Instagram/YouTube/Hevy are all `@saqfitt`.
- **Canonical contact email is `saqlainfit@gmail.com`** — used site-wide, including the main site and media kit.
- `hevy.html` is a pitch for a **Hevy Coach partnership** (not the ambassador programme — he's already in it)
- Partnership pages are `noindex, nofollow` — private, shared directly with brand contacts. (They are **not** blocked in `robots.txt`: a `Disallow` would stop crawlers from ever reading the `noindex` tag, so the meta tag does the work alone.)
- The `/links` route replaced `/linktree` — do not recreate `linktree.html`

## Deployment

```bash
git add <files>
git commit -m "message"
git push
```

Netlify picks it up automatically. No build command needed (`netlify.toml` sets publish to root).
