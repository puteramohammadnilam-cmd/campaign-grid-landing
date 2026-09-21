# Direction B — "The Long Route"

## Concept
An editorial campaign-trail piece: a wide-format broadsheet with a serif display face and a hand-drawn style
route map that runs from DAY ONE to POLLING DAY, through the six jobs as checkpoints. Reads more like a
long-read about how a campaign actually runs.

## Palette & type
- Cream paper background `#f6f3ea`, dark navy ink `#141d2b`, rust `#b3400f` for the route + emphasis,
  muted gold `#7b5f0e` for numbers and the route line. Inverts to navy `#0a1a30` only on the wall.
- Display: **Fraktur** (a humanist display serif) for headlines and step numerals, **IBM Plex Mono** everywhere
  else — the mono keeps the copy factual and slightly reportorial.
- Hard black borders, no card shadows except on the two printed mockups. Paper-textured via spacing only.

## What changed vs the current page (and why)
- Replaced the standard centred hero with a wide two-column layout: left column carries headline + CTAs,
  right carries a stamp motif and a drawn media-enquiries card.
- New full-width "route" SVG band below the hero: a dashed route with six numbered checkpoint markers and a
  polling-day star at the end. This is the memorable visual — the scroll-drawn version is the only
  non-trivial animation (GSAP, reduced-motion aware, and the path is fully visible without JS).
- Six jobs section rewritten as a ruled table (numbered rows, mono labels).
- Wall section inverted to navy with roman-numeral clauses — reads like a manifesto page.
- Ladder becomes a compact ruled index; stage 4 highlighted with a rust border + drop shadow card.
- Sticky bottom strip (ink bar with gold kicker) acts as persistent CTA, hides over the activation section.
- Form styled like a printed document (border, drop shadow, mono labels).

## Fictional demo data used (all labelled "demo data, fictional")
- Media card: three invented outlets (The Daily, Radio 9, Weeklies) with deadline/answered statuses.
- Approval mockup: "Draft 14 · ceramah poster", fact-check open, approve locked.

## Not verified / unsure
- The route-draw scroll scrub uses GSAP+ScrollTrigger; without JS the path stays fully drawn — verified by
  hiding GSAP in dev tools and confirming the line remains.
- Fraktur numerals render slightly lighter than body; check on a small Android screen.
- The stamp's spin animation is purely decorative.
