# Review of Kimi K3 output (2026-09-21)

Method: scripted checks against `reference/COPY-RULES.md`, then both pages opened in a browser at pane width (872 px) and 375 px, console checked, fonts and contrast measured.

## Rules check (both directions)
| Rule | A "Mission Control" | B "The Long Route" |
|---|---|---|
| No prices | Pass, but shows "RM 148,220.50 of RM 200,000.00" in a fictional expenses mock (labelled) | Pass |
| No unbuilt-feature claims (polling day, archive, seats, AI) | Pass | Pass |
| No social proof, no real names, no images | Pass | Pass |
| Wiring hooks (EMAIL, WHATSAPP, DEMO_URL, data-demo, #activate, #wa-direct, #send-wa, [hidden] rule) | All present; WhatsApp hidden, demo buttons live | Same |
| External requests | Google Fonts + GSAP only | Same |
| Content visible if GSAP fails | Yes (hidden only via JS) | Yes |
| Console errors | None | None |
| Horizontal scroll at 375 px | None | None |
| BM switch | Links to `campaign-grid.ms.html`, which does not exist in `output/` (expected until BM is built) | Same |

## Defects
**A**
1. Zone-completion bars (`span.bar`) stack on top of the "FIELD - ZONE COMPLETION" header in the hero board: a grey pill covers the title.
2. Triage cards: status pills touch the text ("draft 14[GATE ON]").
3. 51 text elements under 11 px on mobile (mono labels). Too small to read.
4. `#d4571f` on navy is 4.31:1, just under AA if used for small text.
5. Mobile header wraps the logo onto three lines.
6. The RM figures could be read as pricing. Use a percentage or drop the currency.

**B**
1. Headline font "Fraktur" does not exist on Google Fonts. It silently falls back to Georgia (Kimi's note calls it a "humanist display serif"). The intended typography never loads.
2. Between 641 and 980 px the six-jobs rows squeeze descriptions into a 100 px column (`.job{grid-template-columns:44px 1fr 100px}`).
3. Wall section: dark gold `#7b5f0e` on navy is 2.9:1 (fails AA); rust on navy is 3.04:1.
4. Cream page departs from the navy brand family; only the wall is navy.
5. 40 text elements under 11 px on mobile.
6. Copy drift: "for the length of the campaign" is a new claim.

## Verdict
Both are honest and wired correctly. **A is the better base**: stronger visuals (ops board, zone map, expenses bar, wall schematic, sticky rail) and closer to the brand. B's route diagram is a good idea worth borrowing. B needs more repair.
Neither is ready to ship. Do not copy into `landing-pages/` until A's defects are fixed and the BM twin exists.
