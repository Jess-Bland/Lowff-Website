# LOWFF Website — Deployment Package

Deployment-ready export of the current approved LOWFF prototype. Designed to run at **https://jess-bland.github.io/Lowff-Website/** using the existing GitHub Pages configuration.

## 1. What to upload

Upload the contents of this ZIP to the **root of your `Lowff-Website`** repository. Files:

- `index.html` — the full website (homepage opens directly). Every screen (Home, Women's, Men's, Collections, Product Detail, About, Follow, Contact, Delivery & Returns, Search, Bag) lives inside this file and is reached via hash-based navigation (`#/home`, `#/shop?g=women`, `#/product/flow-state-tank`, etc).
- `support.js` — runtime required by `index.html`. Same folder.
- `uploads/` — local brand assets: LOWFF logos (black + white), the Flow State collection artwork, the four Flow State colourway graphics, and the electric-blue brand-strip background pattern.
- `README.md` — this file.

## 2. What to remove from the existing repository

Replace whatever is at the repo root with these files. Delete any of these older files if present:

- `LOWFF *.dc.html` earlier boards (Homepage 03, Listing 04, Product Detail 05, Bag Checkout 06, Information 07, Community/Search 08, Components 02A/02B, Audit Index, Visual Foundations, Flow State Exploration, older `LOWFF Storefront.dc.html`)
- Any `client-review/`, `export/`, `deploy/`, `audit-export/`, `LOWFF-typography-review/`, `lowff-deploy/` folders from previous exports
- Any older `index.html` that isn't this one

Do **not** delete GitHub-specific files (`.gitignore`, `CNAME`, your own repo `README.md` if you keep one, GitHub Pages workflow).

## 3. Assets and services that need an internet connection

- **Product & campaign photography** is served from the live LOWFF site (`https://lowff.co.uk/wp-content/uploads/...`) — internet required for those images to render. Local logos, Flow State graphics, artwork and background are bundled in `uploads/` and load offline.
- **Fonts** — Anton and Inter load from Google Fonts (`https://fonts.googleapis.com`). Not bundled locally. If offline support is needed later, self-host both families and update the `<link>` in the `<head>` of `index.html`.

## Prototype limitations (unchanged)

- **Checkout is not implemented.** The Bag "Checkout" action opens a labelled prototype-handoff dialog. No payment functionality has been added.
- **Bag, filter and search state is in-memory** — a full page reload clears the bag.
- **Follow page** is a curated gallery, not a live Instagram feed.
- **Product data** is embedded in `index.html` — no CMS or backend.

## Verified before packaging

- Layout tokens: one `--page-x` gutter scale (20 → 40 → 64 → 96 px) and one shared `--content-max` (1200 px) rail control every page's horizontal alignment. Home, About, Collections and Follow all inherit the global `.page` gutter — no inline horizontal padding overrides remain.
- Homepage hero renders flush under the header (`.page.home-page { padding-top: 0 }`), image full-bleed, "BOLDNESS HAS NO BORDERS." headline on one line, hero body aligned to the same left guide as SHOP FLOW STATE, MEET THE COLLECTION and About body content at every desktop width.
- Section heading system: eyebrow (Inter 500 / 11 px / 0.24em / uppercase / #3A3A3C) → 12 px gap → Anton 400 heading, consistent across SHOP FLOW STATE, MEET THE COLLECTION, About sections, Follow, Collections and shop listings.
- MEET THE COLLECTION vertical rhythm: heading → 16 px → filter pills → 28 px → product image.
- Flow State section: 4 colourway graphics on top + 4 on-model photographs below, in square containers, with the shared eyebrow + Anton headline pattern.
- MOVE BOLDLY brand strip and About community band both use `uploads/Background.png` behind the electric-blue fallback.
- Navigation order: Men's · Women's · Collections · About · Follow · Contact — header and mobile menu.
- Women's shop: photographic intro + 3-across product grid. Men's shop: single-product feature layout for the T-Shirt.
- Typography: Anton for every heading, Inter for every paragraph and interface element.
- Hash-based navigation and all working interactions preserved (menu, filter drawer, product detail, bag, search).

## Cannot verify from this environment

- Exact rendered layout on GitHub Pages under `/Lowff-Website/` — asset paths are relative so no path fix is required, but the final render depends on your Pages configuration.
- Live product photography from `lowff.co.uk` — those URLs load in your browser but cannot be embedded into offline snapshots from here (CORS). If any URL changes on the live site, it will break here too.
- Google Fonts CDN availability — assumed uptime.
