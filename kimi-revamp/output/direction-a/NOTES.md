# Direction A — "MISSION CONTROL"

## Concept
A dark, dense campaign ops console: the hero itself is the product, framed as a morning ops board. The page
earns trust by *showing* the tool working rather than talking about it. The GRID ladder is a systems readout,
the wall is a schematic of two deployments that cannot touch.

## Palette & type
- Navy `#0a1a30` family, gold `#dcb63f`, rust `#d4571f` accent — copied straight from the brand tokens.
- Display/body: **Instrument Sans** (same as current page); mono accents in **IBM Plex Mono** for labels,
  telemetry and badges so the console language reads as instrumentation, not marketing.

## What changed vs the current page (and why)
- Hero rebuilt from floating shapes + headline into a framed two-pane console (status pill, metadata rows on
  the left; a fictional ops board with six job slots, zone completion bars and a triage mini-pane on the right).
- "Six jobs" cards trimmed to numbered jobs with a mono index row — less generic SaaS, still skimmable.
- Two new drawn mockups: a five-zone fictional map with a late flag, and the expenses cap bar.
- Wall section: new SVG schematic (campaign box × hatching × office box with a 404 inside) plus the four
  clauses as numbered contract clauses, not a flat list.
- Ladder redone as six readout rows; stage 4 is a rust-bordered callout card ("You are here"), stage 5 gold.
- Sticky CTA rail appears after the hero and disappears over the activation section; direct CTAs kept left of
  the form.

## Fictional demo data used (all labelled "demo data, fictional")
- Hero ops board: zone names (CENTRAL/NORTH/TOWN/SOUTH/COAST), completion %, "Draft 14", vehicle incident.
- Zone map mockup + task rows (walkabout, bilik gerakan visit, poster run, survey sweep).
- Expenses mockup: RM 148,220.50 of RM 200,000.00 cap (invented).

## Not verified / unsure
- Route/scroll events in the test harness had to be dispatched manually; the rail logic itself was verified.
- Zone-map label kerning on small phones is cramped by design; check on a real device before shipping.
- Exact-sen figures are placeholders; no real cap value exists on the page.
