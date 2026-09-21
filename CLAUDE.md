# Campaign GRID Landing

Standalone landing page for Campaign GRID. One self-contained HTML file: `landing-pages/campaign-grid.html`.
Only external dependencies: Google Fonts and GSAP (cdnjs). No build step.

## Vault
Notes and decisions: `~/Documents/Obsidian Vault/Projects/Campaign GRID Landing/`.
Check `Decisions/` before changing scope. Positioning source: `~/Projects/grid-ecosystem-report`.

## Rules for the copy
- Claim only what is built (see `~/Projects/smart-dun`, `/kempen` panel) or what the report labels Existing.
- No prices until the commercial lead confirms them.
- No voter or supporter numbers. State that spending is recorded, never that compliance is advised.
- WhatsApp number lives in the `WHATSAPP` constant; empty hides the WhatsApp buttons.
- Demo site address lives in the `DEMO_URL` constant (currently the example `demo.campaign.grid.com`); empty hides the demo buttons.
- Two files: `campaign-grid.html` (EN) and `campaign-grid.ms.html` (BM). The BM file was generated from the EN one by string replacement, so a copy change must be made in both.
- Trap: a `hidden` attribute loses to any author `display:` rule (e.g. `.btn`). The file has `[hidden]{display:none!important}` for this; keep it.
