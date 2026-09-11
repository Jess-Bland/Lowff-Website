# LOWFF Storefront — Live Review Site

Static site for the LOWFF storefront prototype. Deployed via GitHub Pages.

## First-time deploy

1. Push all files in this folder to the root of the `main` branch of https://github.com/Jess-Bland/Lowff-Website
2. In the repo on GitHub: **Settings → Pages**
3. Under **Build and deployment**, set:
   - Source: **Deploy from a branch**
   - Branch: **main** / **/ (root)**
4. Save. GitHub Pages will build and publish within ~1 minute.

Live URL will be: **https://jess-bland.github.io/Lowff-Website/**

## Updating

Replace files and push again to `main` — Pages redeploys automatically.

## Files

- `index.html` — the storefront (renamed from `storefront.dc.html`)
- `support.js` — Design Component runtime (required)
- `uploads/` — local logo assets
- `.nojekyll` — tells GitHub Pages to serve files as-is
