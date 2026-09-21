# Campaign GRID Landing

Standalone landing page for Campaign GRID. Two self-contained language files in `landing-pages/`; BM (`campaign-grid.ms.html`) is the primary presentation, with `campaign-grid.html` as the English twin.
Only external dependencies: Google Fonts and GSAP (cdnjs). No build step.

## Vault
Notes and decisions: `~/Documents/Obsidian Vault/Projects/Campaign GRID Landing/`.
Check `Decisions/` before changing scope. Positioning source: `~/Projects/grid-ecosystem-report`.

## Rules for the copy
- Claim only what is built (see `~/Projects/smart-dun`, `/kempen` panel) or what the report labels Existing.
- No prices until the commercial lead confirms them.
- No voter or supporter numbers. State that spending is recorded, never that compliance is advised.
- WhatsApp number lives in the `WHATSAPP` constant; empty hides the WhatsApp buttons.
- The demo has not been deployed (user confirmed 2026-09-21). `DEMO_URL` is empty; demo links request access by email. When deployed, update the URL, labels and public-page/team-login explanation together.
- Keep copy, contact settings and behaviour equivalent in both language files. The form prepares a draft in the visitor’s email/WhatsApp app; it never sends from the page.
- Trap: a `hidden` attribute loses to any author `display:` rule (e.g. `.btn`). The file has `[hidden]{display:none!important}` for this; keep it.

## Approved visual identity (2026-09-21)
- The user chose **Concept 02 — Selected cell**: a 3×3 grid with the fourth cell filled. Source assets are in `brand/`.
- No Grid G, hybrids, overlapping-square star, religious/national emblems or party imagery. This user decision overrides the old star allowance in historical reference COPY-RULES files.
- Keep navy, gold, dark rust and paper; use Instrument Sans and IBM Plex Mono. Dark rust actions retain AA text contrast, including hover.
- Direction A is the base, with legible mobile layouts, keyboard controls and reduced-motion support. Illustrative workspace data must remain labelled fictional.
- See `DESIGN-NOTES.md` for the delivered scope, checks and pre-deployment settings. No deployment has been performed.
- Favicon: `brand/favicon-2x2.svg` (2×2 grid, fourth cell filled, bolder cells) is embedded as the tab icon in both pages. The full 3×3 mark is unreadable at 16 px.
- Entry page is the Malay one (`campaign-grid.ms.html`); the English page is the twin behind the EN link. When a site root exists, serve the Malay page as `index.html`.
