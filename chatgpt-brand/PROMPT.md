# Prompt for ChatGPT: new logo mark + overall design ideas for Campaign GRID

I am building a landing page for **Campaign GRID**, a campaign workspace for one election seat in Malaysia (Johor Bahru, parliamentary seat P.160). Audience: candidates, election agents, and party organisations. Tone: authoritative, calm, trustworthy.

Attached files (read them first; if you cannot open one, tell me and I will paste it):
- `current-mark.png`, a screenshot of the current logo mark (gold outline, two overlapping squares rotated 45 degrees, forming an eight-point star).
- `current-landing-en.html`, the live page.
- `kimi-direction-a.html`, a redesign I like as a base ("Mission Control", dark ops-console look).
- `kimi-review.md`, known defects in that redesign.
- `COPY-RULES.md`, facts and claims you must respect. It overrides any design instinct.

## Job 1: replace the logo mark
The current mark is being dropped. In small gold line-art the eight-point star can be misread as a religious or national symbol, and in Malaysian politics that risk is not worth taking. I need a mark that is **culturally neutral and cannot be read as a symbol of any religion, country, movement or party**.

Do NOT use or resemble: any star (5, 6 or 8 point) or starburst, crescent, cross, wheel or sun rays, shields, flags or national crests, scales, hands, doves, keys, or any party logo. Avoid interlocking triangles or overlapping squares. Avoid colour pairings that read as a Malaysian party or coalition on their own.

The mark should say "one workspace to run a campaign", using the product's own ideas. Directions to explore (invent better ones freely):
- a "G" or "CG" built from grid cells (the product is called GRID)
- a 3x3 or 4x4 grid with one highlighted cell (this is stage 4 of six)
- a six-step rising ladder with step 4 highlighted (the GRID family is a ladder of six stages: Personal, Leader, Readiness, **Campaign**, Representative, Executive)
- a route or path through checkpoints (schedule, field, approval, media, expenses, incidents)
- a ballot-slip or document form with a notch, abstract enough to stay neutral

Deliver **4 distinct concepts**. For each:
1. Clean hand-written **SVG** (viewBox `0 0 64 64`, no raster, no external fonts, no gradients needed). Also a horizontal lockup with the wordmark "CAMPAIGN GRID" using outlined paths or a system-safe font stack.
2. One line on the idea, and one line on why it cannot be misread as a religious, national or party symbol.
3. Proof it survives: shown at 16 px (favicon), 32 px and 128 px; in one colour; and on both the dark navy `#0a1a30` and cream `#f6f3ea`.

Brand colours to work with: navy `#0a1a30`, gold `#dcb63f`, rust `#b3400f` / `#d4571f`, paper `#f6f3ea`. Font today: Instrument Sans (headings/body) and IBM Plex Mono (labels). You may suggest small changes but keep it recognisably this family.
Then **recommend one** and say why. Say plainly if none of the four is strong enough.

## Job 2: overall design ideas
Review the live page and Kimi's direction A as a sharp art director. I want ideas to make it clearly better, not a list of generic tips. Give **8 to 12 ideas**, ranked by impact, each with: what to change, why it helps a candidate or election agent decide, and how hard it is (small / medium / large). Cover at least: the hero and first five seconds; how the GRID ladder and the "wall" (data separation) are told; trust without fake proof; the conversion path (Request activation / See the demo); mobile; Bahasa Melayu as the primary language for a Johor audience; motion; and colour or imagery choices that keep the brand politically neutral.
Also point out anything in my current copy or layout that a Malaysian election agent could find off-putting, suspicious or culturally wrong.

## Hard constraints
- Follow `COPY-RULES.md` exactly: no prices, no claims about unbuilt features (polling-day mode, archive, seat limits, AI), no invented statistics, testimonials or "trusted by", no photos of real or realistic people.
- Everything must work as a single self-contained HTML file: inline SVG/CSS/JS only, no external images. Google Fonts and GSAP from cdnjs are the only allowed externals.
- Accessible: WCAG AA contrast, visible focus, reduced-motion respected, readable at 375 px.
- Do not rewrite the whole page. This pass is the mark and the ideas.

## Deliverables and file names
You cannot write to my disk, so please give me each item as a **downloadable file** (or, if that is not possible, as one clearly labelled code block per file). Use exactly these names:
```
logo/concept-1.svg   logo/concept-1-lockup.svg
logo/concept-2.svg   logo/concept-2-lockup.svg
logo/concept-3.svg   logo/concept-3-lockup.svg
logo/concept-4.svg   logo/concept-4-lockup.svg
logo/preview.html    (one page showing all four at 16/32/128 px, one-colour, dark and cream)
ideas/DESIGN-IDEAS.md  (Job 2, max 3 pages)
SUMMARY.md             (your recommended mark and your top 3 ideas, 10 lines max)
```
Be honest: if you did not test something (for example rendering at 16 px), say so instead of ticking it off.

Start by restating the constraints in 6 lines, then do the work.
