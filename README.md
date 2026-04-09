# KENDLE Labs — labs.kendle.xyz

Landing page for KENDLE Labs, a fractional GTM partner for crypto projects.

## Stack

Static HTML / CSS / JS. No build step. Deploy to Vercel as a static site.

## Structure

```
.
├── index.html              ← main landing page
├── og-image.html           ← source for OG image (1200x630), screenshot to PNG
├── favicon.svg             ← SVG favicon (add favicon.ico + apple-touch-icon.png)
├── site.webmanifest        ← PWA manifest
├── robots.txt
├── sitemap.xml
├── vercel.json             ← Vercel headers, security, caching
├── _redirects              ← Netlify/Cloudflare fallback
└── logos/                  ← brand logos (drop PNG files here)
```

## Deploy to Vercel

1. Push this repo to GitHub
2. Import the repo on [vercel.com/new](https://vercel.com/new)
3. Framework Preset: **Other** (static site, no build command needed)
4. Add custom domain `labs.kendle.xyz` in Vercel project settings
5. Update DNS: add CNAME `labs` → `cname.vercel-dns.com`

## Generating og-image.png

1. Open `og-image.html` in a browser at exactly 1200×630
2. Screenshot it (Cmd+Shift+4 on Mac, drag to select the div)
3. Save as `og-image.png` in project root
4. Commit + push

Or use Puppeteer / Playwright headless:

```bash
npx playwright-chromium screenshot --viewport-size 1200,630 og-image.html og-image.png
```

## TODO

- [ ] Generate `favicon.ico` from `favicon.svg` (use [realfavicongenerator.net](https://realfavicongenerator.net))
- [ ] Generate `apple-touch-icon.png` (180×180)
- [ ] Screenshot `og-image.html` → `og-image.png`
- [ ] Add brand logos to `/logos/` folder
- [ ] Update Calendly links (search `calendly.com` in `index.html`)
- [ ] Update Twitter / LinkedIn URLs in footer and JSON-LD
