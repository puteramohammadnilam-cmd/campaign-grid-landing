# Campaign GRID visual pass

## Added
- A layered campaign-operations hero graphic: zones, route, schedule and approval queue.
- Six matching line icons for schedule, field, approval, media, expenses and incidents.
- A stronger two-space data-boundary diagram with a physical barrier treatment.
- A connected six-stage GRID rail with the approved selected-cell mark at stage four.
- Malay and English 1200×630 Open Graph PNGs, plus editable SVG sources.
- Subtle hero route motion and card hover motion, both non-essential.

## Deviations from the reference
- Copy and section order: no changes; normalized page text matches each reference exactly.
- Structure: added one decorative hero image and one decorative stage-four mark; feature SVGs moved to assets.
- Metadata: added `og:image` details and changed the embedded favicon to the approved local asset.
- Behavior: `data-demo` links now stay hidden while `DEMO_URL` is empty, as the brief explicitly requires; the reference showed email fallbacks.

## Constraint checklist
- PASS — Malay primary; English has the same 321-element structure, IDs and behavior.
- PASS — no prices, testimonials, statistics, voter/supporter numbers or unbuilt-feature claims added.
- PASS — no people, photos, party/national/religious symbols, stars, crescents, flags or emblems added.
- PASS — approved grid files copied unchanged and used for favicon/ladder/share artwork.
- PASS — `EMAIL`, `WHATSAPP`, `DEMO_URL`, form code, tab code and `[hidden]` rule preserved.
- PASS — six tabs keyboard-tested; one panel visible; approval open/closed toggle tested.
- PASS — WhatsApp controls and demo links verified hidden with empty constants.
- PASS — all visible copy matches the references; no meaningful content depends on images.
- PASS — decorative images use empty alt text plus `aria-hidden`; headings retain the meaning.
- PASS — sampled text/color pairs meet WCAG AA (lowest checked ratio: 5.74:1).
- PASS — desktop and 390×844 mobile renders visually checked; no browser console errors.
- PASS — reduced-motion fallbacks present in page CSS and the animated hero SVG.
- PASS — all referenced local assets resolve; total `assets/` weight is about 244 KB.
- NOT CHECKED — browser rendering with image loading explicitly disabled.
- NOT CHECKED — launching the visitor's external email or WhatsApp app from the form.
