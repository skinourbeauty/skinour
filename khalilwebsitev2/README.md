# Clinique du Cèdre — website

A plain HTML/CSS/JS brochure site. No build tools, no framework, no subscriptions —
just three files you can open and edit directly.

## Files

- `index.html` — all page content (text, services, prices, contact info)
- `styles.css` — all colors, fonts, spacing, layout
- `script.js` — mobile menu + auto-updating footer year (that's all the JS does)

## What to replace before going live

Everything below is placeholder content — search `index.html` for these and swap them in:

- Real address, phone number, email, and Instagram handle (mostly done — check `index.html` for anything still bracketed)
- The two images the page now expects (add both to an `images/` folder next to `index.html`):
  - `images/logo.png` — your real logo file, shown on the homepage hero. Until this file exists, the page shows a small fallback note instead of a broken image icon.
  - `images/founder.jpg` — a real photo of the founder, shown in the About section. Same graceful fallback if it's missing.
- The Google Maps embed points at "Galaxy Mall, Gallery Semaan, Beirut" generically — for a pinpoint match, use Google Maps' own "Share > Embed a map" option for the exact building and swap the `src` in the `<iframe>`
- The WhatsApp link and phone number are already set to the real number (+961 81 800 390) — update again if it ever changes

## Running it locally

No install needed. Just open `index.html` in a browser. Or, for a closer-to-production
local preview (recommended so relative links behave correctly):

```
cd clinic-site
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.

## Free hosting options (all $0, no subscription)

Any of these work well for a static site like this one. All three include free
custom-domain support if you later buy a domain name.

### Option A — Cloudflare Pages (recommended, simplest)
1. Create a free Cloudflare account.
2. In the dashboard: Workers & Pages → Create → Pages → Upload assets.
3. Drag in this folder. Done — you get a `*.pages.dev` URL immediately.
4. To update later, just re-upload, or connect a GitHub repo for auto-deploys on every push.

### Option B — GitHub Pages
1. Create a free GitHub account and a new repository.
2. Upload `index.html`, `styles.css`, and `script.js` to the repo root.
3. Repo → Settings → Pages → set source to the `main` branch, root folder.
4. Your site publishes at `https://<username>.github.io/<repo-name>/`.

### Option C — Netlify
1. Create a free Netlify account.
2. Drag this folder onto the Netlify dashboard ("Deploy manually").
3. You get a `*.netlify.app` URL instantly.

All three let you point a real domain (e.g. `cliniqueducedre.com`) at the free site later —
domain registration itself typically costs $10–15/year, but the hosting stays free.
