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
- Dark theme: `#0a0a0a` background
- Accent: `#c8ff00` (lime)
- Fonts: `Bebas Neue` (display) + `DM Sans` (body)
- The SAQFITT nav from this file is reused on partnership pages

### Partnership pages (hevy.html, humehealth.html)
- Each has its own aesthetic matched to the partner brand
- All reuse the SAQFITT navbar from `index.html` (dark frosted glass, lime logo)
- `hevy.html` follows the Hevy Coach site aesthetic: clean white/light, blue `#006799`
- `humehealth.html` follows a dark aesthetic with Hume blue `#3881ff`

## Key context

- **Saq is a Hevy Ambassador** — TikTok at `@trainwithsaq`, targeting Toronto / North America
- `hevy.html` is a pitch for a **Hevy Coach partnership** (not the ambassador programme — he's already in it)
- Partnership pages are `noindex, nofollow` — private, shared directly with brand contacts
- The `/links` route replaced `/linktree` — do not recreate `linktree.html`

## Deployment

```bash
git add <files>
git commit -m "message"
git push
```

Netlify picks it up automatically. No build command needed (`netlify.toml` sets publish to root).
