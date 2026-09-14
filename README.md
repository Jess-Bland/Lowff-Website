# LOWFF Website — Deployment Package

Deployment-ready export of the current approved LOWFF prototype. Designed to run at **https://jess-bland.github.io/Lowff-Website/** using the existing GitHub Pages configuration.

## 1. What to upload

Upload the entire contents of this ZIP to the **root of your `Lowff-Website`** repository (not inside a subfolder). The files:

- `index.html` — the full website (homepage opens directly). Every screen — Home, Women's, Men's, Collections, Product Detail, About, Follow, Contact, Delivery & Returns, Search, Bag — lives inside this one file and is reached by the site's own hash-based navigation (`#/home`, `#/shop?g=women`, `#/product/flow-state-tank`, etc).
- `support.js` — runtime required by `index.html`. Keep in the same folder.
- `uploads/` — local brand assets: logos, Flow State collection artwork, Flow State colourway graphics, brand-strip background.
- `README.md` — this file.

## 2. What to remove from the existing repository

Replace whatever is currently at the repository root with the files in this ZIP. If your current site has any of the below, delete them before uploading (they were part of earlier exports and are no longer used):

- Older `LOWFF *.dc.html` files (`LOWFF Storefront.dc.html`, `LOWFF Homepage 03.dc.html`, `LOWFF Listing 04.dc.html`, `LOWFF Product Detail 05.dc.html`, `LOWFF Bag Checkout 06.dc.html`, `LOWFF Information 07.dc.html`, `LOWFF Community Search 08.dc.html`, `LOWFF Components 02A.dc.html`, `LOWFF Components 02B.dc.html`, `LOWFF Audit Index.dc.html`, `LOWFF Visual Foundations.dc.html`, `Flow State Exploration.dc.html`)
- Any `client-review/`, `export/`, `deploy/`, `audit-export/`, `LOWFF-typography-review/` folders from previous exports
- Any older `index.html` that isn't this one

Do **not** delete any GitHub-specific files at the repo root (e.g. `.gitignore`, `README.md` you'd like to keep, `CNAME` for a custom domain).

## 3. Assets and services that need an internet connection

Product photography is served from the live LOWFF site (`https://lowff.co.uk/wp-content/uploads/...`) — an internet connection is required for those images to load. Local assets in `uploads/` (logos, Flow State graphics, artwork, background) are bundled and load offline.

**Fonts** — Anton and Inter are loaded from Google Fonts (`https://fonts.googleapis.com`) at page load. Not bundled locally; internet required. If the site needs to work offline, self-host these two families and update the `<link>` in `index.html`'s `<head>`.

## Prototype limitations (unchanged)

- **Checkout is not implemented.** The Bag "Checkout" action opens a labelled prototype-handoff dialog; no payment functionality has been added.
- **Bag / filters / search state is in-memory** — a full page reload clears the bag.
- **Follow page** is a curated gallery, not a live Instagram feed.
- **Product data** is embedded in `index.html` — no CMS, no backend.

## Verified before packaging

- Homepage hero renders full-width photograph with the "BOLDNESS HAS NO BORDERS." headline on one line at the bottom, dark bottom fade, aligned to the site's content grid.
- Flow State section: eyebrow + one-line "BOLD IN COLOUR. FREE TO MOVE." headline, two rows of four square tiles (four colourway graphics on top, four on-model photographs below), followed by "Shop Flow State" CTA.
- Move Boldly brand strip and About community band both use the `uploads/Background.png` graphic behind the electric-blue fallback.
- Navigation order: Men's · Women's · Collections · About · Follow · Contact (header and mobile menu).
- Women's shop page: photographic intro + 3-across product grid (Dress · Tank · Skort). Men's shop page: single-product feature layout for the T-Shirt.
- Typography: Anton for every heading, Inter for every paragraph and interface element.
- Hash-based navigation and all working interactions (menu, filters drawer, product detail, bag, search) preserved.

## Cannot verify from this environment

- The exact rendered layout on GitHub Pages under `/Lowff-Website/` — asset paths are relative, so no path fix is needed, but the final render depends on your GitHub Pages configuration.
- Live product photography from `lowff.co.uk` — those URLs load in your browser but cannot be embedded into offline snapshots from here (CORS). If any of those URLs change on the live site, they'll break here too.
- Google Fonts CDN availability — assumed uptime.
