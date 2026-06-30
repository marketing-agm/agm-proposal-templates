# AGM Real Estate Group — Multi-Family Proposal Micro-Site

**CONFIDENTIAL — proposal material. Private repository. Do not make public.**

A digital micro-site version of AGM's *Proposal for Management Services · Multi-Family*. Each
proposal slide is its own page in a single-file static site (`index.html`, no build step, no
dependencies). Fonts load from Google Fonts; everything else is inline.

## What this is
The deck's fourteen sections, rebuilt as an institutional, navigable micro-site:

1. About AGM · 2. Management Team · 3. Investment Strategy · 4. Facilities, Maintenance & Capital
Projects · 5. Financial Management · 6. AGM Master Insurance Program · 7. Leasing Execution &
Revenue Maximization · 8. MFTE & MHA Programs · 9. Mixed-Use & Commercial Leasing · 10. Market
Comparatives · 11. Digital Strategy & Property Exposure · 12. Tools & Technology · 13. Fee Overview ·
14. Management Fees.

Slide copy is reproduced verbatim. The layout, palette (navy `#00202F`, brand blue `#3A8DDE`,
serif/sans pairing), and rail-and-content structure follow the AGM proposal design system. Each page
adds whitespace and interaction — a per-page navy/blue summary rail, an interactive history timeline,
a leasing funnel that links stages to detail, expandable technology platforms, hover-reactive cards
and pills, reveal-on-scroll, prev/next paging, a reading-progress bar, and a light/dark toggle.

## Local preview
Open `index.html` in a browser. That's it. Deep-link a section with the URL hash, e.g.
`index.html#leasing`.

## Deploy — Cloudflare Pages (AGM standard pattern)
1. Cloudflare dashboard → **Workers & Pages → Create → Pages → Connect to Git** → select this repo.
2. Settings: Framework preset **None** · Build command **(empty)** · Build output directory **/**
3. Every push to `main` auto-deploys production; every branch/PR gets its own preview URL.

## REQUIRED before sharing any URL: Cloudflare Access
Zero Trust → Access → Applications → **Add self-hosted application**:
- Application domain: `<project>.pages.dev` **and** `*.<project>.pages.dev` (preview deployments are
  otherwise public).
- Policy: Allow → Emails → leadership list. One-time PIN works without SSO setup.

## Operational notes
- `_headers` enforces `noindex` and security headers at the edge.
- Bracketed placeholders (e.g. `[ Property Name ]`, `X%`, `$X`) are intentional — they are filled in
  per engagement, matching the source proposal template.
- Featured-asset tiles are placeholders; drop in property photography by swapping the `.asset-tile`
  elements for `<img>` tags when imagery is available.
