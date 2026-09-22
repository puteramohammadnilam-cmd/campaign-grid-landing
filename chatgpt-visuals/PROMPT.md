# Prompt for ChatGPT: add real visual richness to the Campaign GRID landing page

You are a senior visual/brand designer working on an already-shipped page. Your job is not to redesign it — the layout, copy, sections and behaviour are locked in and approved. Your job is to make it look designed: real illustrations, icons, diagrams and imagery in place of the plain text-and-boxes it has today.

## Files you have (read them first)
- `reference/current-ms.html` — the live page, Malay, the primary language.
- `reference/current-en.html` — the English twin. Same structure, same behaviour.
- `reference/COPY-RULES.md` — what may and may not be claimed or shown. Read this before anything else. It overrides any design instinct.
- `reference/brand/selected-cell.svg`, `selected-cell-lockup.svg`, `favicon-2x2.svg` — the approved brand mark (a 3×3 grid, one cell filled). Use it; do not invent a new one.

If you cannot read a file, ask me to paste it — do not guess its contents.

## What "add visuals" means here
The page today is text, cards and borders — no illustration, no icons beyond a couple of inline SVGs, no imagery, no motion. Add:
1. **A hero visual** — an illustration, graphic or animated element behind or beside the headline that makes the page feel designed in the first three seconds. Tie it to the product (a schedule, a map of zones, an approval queue, the grid motif) or keep it abstract and brand-led. No stock-photo look.
2. **An icon per feature** — the six-jobs section (schedule, field, approval, media, expenses, incidents) currently has plain text only. Give each one a small custom icon or mark, consistent in style with each other and with the brand mark.
3. **A diagram for "the wall"** (the section explaining that campaign data never touches office data) — this is the page's most important trust claim and it is currently a plain four-item list. Turn it into something visual: two separated spaces, a barrier, whatever reads clearly at a glance.
4. **A diagram for the GRID ladder** (the six-stage timeline, Campaign GRID at stage 4) — make the "you are here" moment visually obvious, not just a coloured tag.
5. **A social share image** (Open Graph / `og:image`, 1200×630) using the brand mark and the headline, so a shared link looks intentional.
6. **Optional, only if it clearly helps:** a small amount of tasteful motion — a scroll reveal, a hover state, a subtle loop in the hero graphic. Respect `prefers-reduced-motion`; the page must be fully readable and correct with motion off and with images off (alt text everywhere).

Do not add a photograph of a person, real or generated, anywhere. See the hard constraints below for why.

## Hard constraints (same as previous rounds — read in full)
- **From COPY-RULES.md:** no prices, no claims about unbuilt features (polling-day mode, freeze/archive, seat limits, AI, self-serve sign-up), no voter/supporter numbers, no testimonials or "trusted by" claims, no invented statistics.
- **No photos of real or realistic people**, anywhere, for any reason — this is a political product with a fictional candidate, and a face (real, stock, or AI-generated) reads as a claim about a real person.
- **No stars (5, 6 or 8-point), starbursts, crescents, crosses, wheels, sun rays, shields, flags, national or party emblems, or anything that could be misread as one.** This is why the brand mark is a plain grid, not a star — keep every new graphic to the same standard.
- **Keep the brand mark as-is.** Use `selected-cell.svg` / `selected-cell-lockup.svg` for anything that needs the mark. Do not redraw it, recolour it into something else, or introduce a second mark.
- **Keep the structure, copy and section order.** You are illustrating what is already written, not rewriting it. If a section's wording genuinely needs a small change to fit a new visual, flag it in your notes rather than changing it silently.
- **Keep every working part exactly as it behaves today:** the `EMAIL`, `WHATSAPP`, `DEMO_URL` constants near the top of the script; the `data-demo` elements (hidden until `DEMO_URL` is set); `#wa-direct` / `#send-wa` (hidden until `WHATSAPP` is set); the six-tab workspace example (keyboard-operable, one panel visible, `role="tab"`/`role="tabpanel"`); the approval open/closed toggle; the activation form (composes a draft in the visitor's own email/WhatsApp app, sends nothing itself); the `[hidden]{display:none!important}` rule. Test each of these still works after your changes.
- **Keep Malay as the primary language and English as the exact twin.** Whatever you change, change in both files identically — same structure, same element ids, same behaviour, translated text only.
- **Accessibility:** WCAG AA contrast on any text over a new image or graphic, alt text on every meaningful image, `aria-hidden="true"` on decorative graphics, visible focus states preserved, nothing readable only by colour.

## Technical constraints
- Two files, self-contained HTML with inline CSS/JS, same as today. New images go in a sibling `assets/` folder and are referenced by relative path (e.g. `assets/hero.svg`) — do not inline large images as base64 data URIs, and do not point at any external image host or CDN. Fonts stay Google Fonts; no other external script or style host beyond what the page already uses.
- **Prefer SVG for icons and diagrams** — they stay crisp at any size, are tiny, and are easy for me to recolour later. Use raster (WebP, or PNG if WebP isn't practical) only where a vector genuinely can't do the job, such as a textured hero background.
- **Size budget:** every new file under `assets/` should be as small as you can make it. Guideline: icons a few KB each, the hero graphic under ~150KB, the OG image under ~200KB, total added weight under ~1MB. This is a static site with no image-optimisation build step, so what you export is what ships.
- No new JavaScript libraries or frameworks. Vanilla JS only, as today.
- Brand tokens to match: navy `#0a1a30` (with `#0d1f38`/`#102540` as supporting darks), gold `#dcb63f`, rust `#b3400f` / `#d4571f`, paper `#f6f3ea`. Type: Instrument Sans (body/headings), IBM Plex Mono (labels/metadata).

## Where to save your work
Write ONLY inside `output/`. Do not edit `reference/`.
```
output/campaign-grid.ms.html
output/campaign-grid.html
output/assets/               (every new SVG/WebP/PNG you create, sensibly named)
output/NOTES.md
```
`NOTES.md` (max 40 lines): what you added and why, in plain terms; every place you deviated from the current copy or structure and why; a checklist of the constraints above, each marked pass or not-checked — be honest, don't tick what you didn't verify (e.g. "tested with images off: not-checked" if you didn't actually test it); anything you're unsure about.

## How to work
1. Read every reference file. In 8–10 lines, restate the constraints you must not break, in your own words.
2. Plan the six visual pieces above briefly before building anything: what each one is, in one line.
3. Build the Malay file first, in full, then produce the English twin from it (same visuals, translated text, same ids/behaviour).
4. Review your own output against every constraint above and fix what fails before saying you're done.
5. Finish with the list of files you wrote and a 5-line summary. No long preamble.
