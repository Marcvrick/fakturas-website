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
│   └── *.html                  # 15 blog posts (SIFEN, facturacion electronica, etc.)
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

### Mar 23, 2026 — Added favicon to all pages

- White F on brand green (#4edea3), all sizes (ico, 32/192/512px PNG, apple-touch-icon)
- Added to all 19 HTML files (homepage, landings, blog index, 15 blog posts)
- Also deployed to `app.fakturas.app` via Vercel (Next.js `layout.tsx` metadata + `public/` assets)
