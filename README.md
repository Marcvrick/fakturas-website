# Fakturas.app — Marketing Website

Marketing landing page and blog for [fakturas.app](https://fakturas.app), an invoice scanning platform for accounting firms in Paraguay.

## Stack

- Static HTML/CSS/JS (no framework, no build step)
- Hosted on **GitHub Pages** with custom domain (`fakturas.app`)
- Blog: static HTML pages in `/blog/`

## Structure

```
├── index.html                  # Main landing page (Spanish)
├── landing-aktivate-style.html # Alternate landing (English)
├── landing-aktivate-style-v2.html # Alternate landing v2 (Spanish)
├── blog/
│   ├── index.html              # Blog listing
│   ├── briefs/                 # Content briefs (markdown, not deployed)
│   ├── KEYWORD-ACTION-PLAN.md  # SEO strategy + funnel mapping
│   └── *.html                  # 22 blog posts (SIFEN, facturacion electronica, IVA flow, etc.)
├── favicon.ico                 # Multi-size (16/32/48px)
├── favicon-32.png
├── favicon-192.png
├── favicon-512.png
├── apple-touch-icon.png        # 180x180
├── robots.txt
├── sitemap.xml
├── feed.xml                    # RSS feed
├── CNAME                       # GitHub Pages custom domain → fakturas.app
└── google*.html                # Search Console verification
```

## Related Repos

- **App (Next.js):** `Marcvrick/facturas-py-web` → deployed on Vercel at `app.fakturas.app`

## Deployment

Push to `main` → GitHub Pages auto-deploys. No build step needed.

## Brand

- Primary green: `#4edea3`
- Favicon: white "F" on `#4edea3` green square

### May 6, 2026 — IVA pillar article + homepage SEO + CTR rewrites

- **New pillar article:** `blog/declaracion-iva-mensual-paraguay-contadores.html` (~4,000 words). Covers Form 120 V4, RG 90, perpetual calendar, prorrateo, rectificativas, sanciones. 3 schemas (Article + HowTo + FAQPage). Mid-funnel hub linking to 8 spoke articles.
- **Nav cleanup:** removed "Contacto" link from 22 files (it was a duplicate anchor to the homepage `#cta`).
- **Homepage SEO quick wins** (`index.html`):
  - Title: added "Paraguay" geo signal → `Fakturas.app — Declaraciones IVA Paraguay sin perder tiempo`
  - Meta description: tightened to 150 chars (was 192)
  - Canonical + `og:url` aligned with trailing slash (`https://fakturas.app/`)
  - Added `Organization` + `WebSite` JSON-LD schemas (now 3 total)
  - Added `priceValidUntil` to all 3 pricing offers
  - Fixed broken `href="#"` "Conoce el flujo de trabajo" anchor → links to new IVA pillar
  - New "Articulos recientes" section above the CTA (3 article cards + "Ver todos" CTA)
  - `dns-prefetch` for `app.fakturas.app`
- **CTR rewrites on 3 lowest-performing pages** (GSC: 0–0.5% CTR, 338 combined impressions):
  - `multas-sanciones-facturacion-electronica`: 79→61 ch title, leads with `Gs. 354.890.000`
  - `certificado-digital-facturacion-electronica`: 81→61 ch title, drops "Guia completa" cliché
  - `proveedores-estado-facturacion-electronica`: 84→60 ch title, "obligatoria 2026" hook upfront
  - All 3 updated `<title>`, meta description, OG, Twitter; H1s left untouched to preserve ranking signals.

### Mar 24, 2026 — Mobile hero rework + ROI in Guaranies

- iPhone mockup: locked to real 9:19.5 aspect ratio (no more elongated phone)
- iPhone centered overlapping the portal contable dashboard on mobile
- Hidden chart card on mobile for cleaner layout
- Phone mockup switched to light theme (#f0f0f0) matching actual app UI
- Shrunk Editar/Validar/Rechazar action buttons on mobile
- ROI comparison section: switched from USD to Guaranies (₲470K vs ₲670K+)

### Mar 23, 2026 — Added favicon to all pages

- White F on brand green (#4edea3), all sizes (ico, 32/192/512px PNG, apple-touch-icon)
- Added to all 19 HTML files (homepage, landings, blog index, 15 blog posts)
- Also deployed to `app.fakturas.app` via Vercel (Next.js `layout.tsx` metadata + `public/` assets)
