# Prompt for Kimi K3: revamp the Campaign GRID landing page

You are a senior product designer and front-end engineer. Redesign one landing page so it looks and feels premium, distinctive and trustworthy, with real visual content, while keeping every fact exactly as specified.

## Files you have
- `reference/current-en.html`  - the current page (English). Study its structure, copy and script.
- `reference/current-ms.html`  - the Malay twin. Do NOT redo it now; only keep its needs in mind.
- `reference/COPY-RULES.md`    - what may and may not be claimed. Read it first. It overrides any design instinct.
If you cannot read files, ask me to paste them. Do not guess their contents.

## Goal
Make the page better and nicer in UI and UX, with visuals and a memorable flare of design, for candidates, election agents and party organisations deciding whether to request an activation. One clear job for the page: get a qualified visitor to press "Request activation" or "See the demo".

## Deliver TWO distinct art directions, as I want to choose
Both directions must be genuinely different in concept, not two colour swaps. Examples to stretch from, not to copy: (a) "the war-room": a live command-centre feel, dense, dark, data-forward, product UI as the hero; (b) "the campaign trail": editorial, warm, map and route storytelling, bolder type. Invent your own if better. Give each a one-line name.

For each direction include:
1. A memorable hero visual built in inline SVG/CSS/canvas (no external images), tied to the product (schedule, zones/map, approvals, expenses cap) or the eight-point star.
2. At least two product-UI mockups drawn in HTML/CSS/SVG with fictional demo data, labelled "Demo data, fictional".
3. The GRID ladder redesigned as a real storytelling moment (stage 4 clearly "you are here"; stages 5 live, others planned).
4. The "wall" section turned into something visual, not a plain list.
5. A stronger conversion path: sticky or repeated CTA, clear demo button, the contact/form block.
6. Considered motion: purposeful, restrained, respects `prefers-reduced-motion`.

## Keep these working hooks (the page is wired to them)
- Script constants at the top: `EMAIL`, `WHATSAPP` (empty by default), `DEMO_URL` and the localhost switch. Keep them editable and keep their behaviour.
- Elements: `id="activate"` section; buttons with `data-demo` (shown only when `DEMO_URL` is set, opens in a new tab); `#wa-direct`, `#send-wa` hidden unless `WHATSAPP` is set; the form only composes a mailto/WhatsApp message (no server); the `[hidden]{display:none!important}` rule.
- The form and privacy note: nothing is sent from the page; warn not to include voter or supporter details.
- English only in this pass.

## Hard constraints
- One self-contained HTML file per direction. Inline CSS and JS. External allowed: Google Fonts and GSAP from cdnjs only. No other CDNs, no analytics, no trackers, no external images. Total size under 600 KB per file, no big base64 blobs.
- Works at 375 px width with a 16 px side gutter and no horizontal scroll. Desktop 1440 px looks intentional, not stretched.
- Accessibility: WCAG AA contrast, visible focus, semantic headings in order, alt text or `aria-hidden` on decorative SVG, keyboard operable, reduced-motion respected. Content must stay visible if GSAP fails to load.
- Copy: follow `COPY-RULES.md` exactly. Tighten and sharpen the wording, but add no new claims. If a visual needs a number, use obviously fictional demo data and label it.

## Where to save (important)
Write ONLY inside `output/`. Do not edit anything in `reference/` or elsewhere.
```
output/direction-a/index.html
output/direction-a/NOTES.md
output/direction-b/index.html
output/direction-b/NOTES.md
output/SUMMARY.md
```
Each `NOTES.md` (max 40 lines): the concept in 2 sentences; palette and type choices; what changed vs the current page and why; every place you used fictional demo data; anything you were unsure about or could not verify; a checklist of the constraints above, each marked pass or not-checked (be honest, do not tick what you did not test).
`SUMMARY.md` (max 20 lines): compare the two directions, which you would ship and why, and what you would test with real visitors.

## How to work
1. Read the reference files. In 10 lines, restate the constraints you must not break.
2. Plan both directions briefly (name, hero idea, palette, type, motion idea).
3. Build direction A fully, then B fully. Reuse nothing lazily between them.
4. Review your own output against the constraints and fix what fails before saying you are done.
5. Finish with the list of files written and a 5-line summary. No long preamble.
