# Review of the ChatGPT visuals pass (2026-09-22)

Method: automated checks against `reference/COPY-RULES.md`, structural diff between the two languages, then both pages opened in a browser at desktop, phone width and images-off, with the six-tab example, the approval toggle and the contact-form hooks all exercised by hand.

## Rules check
No prices, no unbuilt-feature claims, no testimonials or fake numbers, no real party names, no photos of people, no star or other symbol that could be misread as religious/national/party. Only Google Fonts requested externally. Brand mark copied byte-for-byte from `reference/brand/`.

## What's new and good
- Hero graphic: an abstract zone map with a route and two small panel mockups, in brand colours only, with its own `prefers-reduced-motion` handling baked into the SVG.
- A distinct line icon for each of the six jobs.
- "The wall" is now two separated boxes with a barrier between them, instead of a plain four-item list.
- The GRID ladder is a connected rail; stage 4 is unmistakably highlighted.
- A 1200×630 social share image per language, built from the same mark and palette.
- Total added weight: 244 KB (guideline was under ~1 MB).
- Malay and English are structurally identical (same tags, same ids) — only the language-specific OG image path differs, correctly.
- 0 contrast failures across 125 text elements, no sideways scroll at 375px, page stays fully readable with images turned off, all six tabs work by keyboard, the approval toggle behaves correctly (closing the check enables approval without auto-approving it).

## One defect found, and fixed
The two "Request demo access" links (hero and contact section) were marked `hidden` in the delivered markup, so with today's empty `DEMO_URL` they were **entirely invisible** — no way to ask for demo access at all. This is not something ChatGPT invented: my own prompt wrongly said `data-demo` elements should be "hidden until `DEMO_URL` is set", copying the pattern that's correct for the WhatsApp button but wrong for this one. The real rule (confirmed against the current live page) is: these links are always visible, with a working `mailto:` fallback, and the script only swaps their `href` once a real demo address exists. ChatGPT followed the wrong instruction and flagged the change honestly in its own notes rather than hiding it.

**Fix applied:** removed the `hidden` attribute from both elements in both language files. Verified: the button now shows with the email link today, and still correctly switches to a live demo URL once `DEMO_URL` is set (tested by simulating the swap).

## Verdict
Ready to ship once the fix above is confirmed — which it now is. Not yet copied into `landing-pages/` or `docs/`; that step is still pending.
