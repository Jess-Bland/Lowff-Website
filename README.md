# LOWFF Website, review package

Current LOWFF storefront prototype for review. **Not client-approved.** No approval has been recorded and not all feedback is complete. Intended to run at https://jess-bland.github.io/Lowff-Website/ (not published from here).

## Package contents
- `LOWFF Storefront.dc.html`: the design-project source.
- `index.html`: the deployable copy, byte-for-byte identical to `LOWFF Storefront.dc.html` (204,318 bytes, checked at export).
- `support.js`: the runtime both HTML files need (same folder).
- `uploads/`: every local image the HTML references (8 files): `Background.png`, `FULL_BLACK@300x.png`, `FULL_WHITE@300x.png`, `FLOW STATE-05-f57730b5.png`, `FLOW STATE-09-0b058515.png`, `about-ig-boldness-crop.png`, `IMG_8031.jpg`, `lowff-cursor.png`.

Hash routes: `#/home`, `#/shop`, `#/shop?g=men`, `#/shop?g=women`, `#/shop?c=flow-state-2`, `#/shop?c=flow-state`, `#/collections`, `#/accessories`, `#/product/<slug>`, `#/about`, `#/follow`, `#/contact`, `#/returns`, `#/search`, `#/bag`.

## Internet access required
- **Product, campaign and community photography** loads from lowff.co.uk. Without a connection, these tiles show empty frames with their descriptions.
- **Fonts** load from Google Fonts. Offline, a fallback font is used.
- **Instagram links** go to instagram.com.
- Logos, the brand background, Flow State artwork, the two About posts and the cursor are local files and work offline.

## Completed work
- 7-product catalogue whose collection split matches the live lowff.co.uk product metadata. Woman: Flow State Dress £65, Tank Top £32.50, Skort £37.50 (Flow State); Sports Bra £27.50, Shorts £35 (Flow State 2.0). Men: Flow State Men's T-Shirt £29.50 (Flow State); Men's Shorts £32.50 (Flow State 2.0).
- Navigation. Desktop primary: Men · Woman · Collections · Follow · Contact. Mobile menu: Shop all, Men, Woman, Collections, Accessories, About, Follow, Contact. Footer: Shop, Support, Follow. Both repaired navigation behaviours are preserved unchanged in this package.
- Collections uses one hero photograph, as requested in Pastel #31.
- Homepage "Meet the LOWFFERS" is accurately captioned as LOWFF campaign photography.
- About gallery. The two text-bearing @_lowff_ posts ("Boldness has no borders", "Beyond the Mirror") are shown uncropped: contained in the 4:5 frame on a black ground with no distortion. Ordinary photography still fills its tiles. IMG_1247 and IMG_1180 are described as clothing on hangers. Slot 3 is a labelled placeholder.
- Shared newsletter appears once above the footer on every page.
- The bag persists in this browser (localStorage) across pages and reloads. Checkout is a labelled prototype hand-off with no payment.
- Contact and newsletter forms validate and give honest prototype feedback. Nothing is sent or subscribed, and no personal email address is published.
- Accessories is a sampling preview only, with no products, prices, stock or dates.

## Missing content
- **Fabric composition.** Material names and percentages are needed for all seven products; none are published on lowff.co.uk. The Tank Top text mentions spandex (LOWFF's own copy) but gives no breakdown.
- **Swatch values and colour identification.** Approved Purple and Green swatch values are needed. Confirm that deep indigo = Purple and bright cobalt = Blue in the 2.0 range.
- **Product-colour photo mappings, 7 missing.** For each, an approved image of that product in that colour is needed. A labelled illustrative fallback is shown meanwhile.
  1. Men's Shorts: Blue
  2. Men's T-Shirt: Blue
  3. Men's T-Shirt: Beige
  4. Men's T-Shirt: Purple
  5. Men's T-Shirt: Green
  6. Tank Top: Purple
  7. Tank Top: Green

  An approved group photograph can be used if the correct product and colour are unmistakable in it. New individual photographs are not automatically required.
- **Homepage tagged customer imagery.** The original request was tagged customer posts. The current campaign photos are accurately captioned, but keeping them needs the client to agree to change that request. Until then this item stays outstanding.
- **About Instagram.** Original exports of "Boldness has no borders" and "Beyond the Mirror" (the current files are post screenshots) and their approval. A third approved @_lowff_ post for the pending slot.
- **Community "Tagged by you".** 4 approved customer/ambassador posts, each with permission, handle and post URL.
- **Behind the scenes.** 4 individual Instagram post URLs. Tiles currently open the @_lowff_ profile as a fallback.
- **Accessories and events.** Accessories products, imagery and timing (currently a sampling preview only). Events content stays hidden until real events exist.

## Client decisions
- **Dress and Skort colours.** These stay Blue, Black and Beige, matching the verified live catalogue. Purple/Green is only a possible future-range question unless LOWFF confirms availability.
- **Hero treatments.** Collections keeps one hero photograph (Pastel #31). The three-photo desktop treatments on Men and Community still need client approval.
- **Homepage imagery.** Agree whether to keep campaign photography instead of the originally requested tagged customer imagery.
- **Wording.** "Women" (written brief) vs "Woman" (dictated); the prototype uses Woman. Community heading grammar: "Join a Bold LOWFFERS." Revised About copy: "Every sport, every athlete."
- **Image approvals.** Hero imagery and crops, the homepage campaign break photo, and the About post treatment.

## Development requirements
- Client-editable (CMS) copy, images, fabric composition and colour photos.
- An automatic Instagram feed section, separate from the hand-curated "Tagged by you" and "Behind the scenes" content.
- Private contact-form delivery, with no address exposed.
- A newsletter provider connection.
- Real commerce: products, stock (the live Men's T-Shirt currently shows Sold Out), bag, checkout and payment.

## Verification status
- The two HTML copies were confirmed byte-for-byte identical at export. The local images in `uploads/` match the design-project originals byte-for-byte.
- **About gallery:** the geometry was measured at 390px and 1440px. Both text-bearing posts show 100% of their width and height, and the photography tiles fill their frames. Automated screenshots showed the local post artwork but **omitted the lowff.co.uk photography**, so visual verification of the photo tiles remains **unconfirmed**.
- **Background check: incomplete.** No completed result has been recorded.
- Final rendering on GitHub Pages has not been verified.
