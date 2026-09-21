# Campaign GRID landing redesign — 21 September 2026

## Approved direction

The user selected **Concept 02 — Selected cell**, the original 3×3 mark with the fourth cell filled. Neither the Grid G nor either hybrid was selected. The selected mark is used in both headers, footers and embedded favicons.

Direction A provides the navy workspace foundation. The redesign uses readable Instrument Sans, IBM Plex Mono for metadata, a restrained gold accent, dark rust actions, and a paper section for the campaign/office boundary. BM is the primary presentation; the English twin carries equivalent content and behaviour.

## Files and behaviour

- `landing-pages/campaign-grid.ms.html`: BM page, primary preview.
- `landing-pages/campaign-grid.html`: English page.
- `brand/selected-cell.svg` and `brand/selected-cell-lockup.svg`: chosen source assets.
- Each page works independently as a self-contained HTML file. The other language file must remain beside it for the language switch. CSS, JavaScript, icons and favicon are inline; only Google Fonts are requested externally.
- Six illustrative workspace tabs support pointer and keyboard input. The approval example distinguishes closing a fact-check from approving a draft. All activities and the candidate are explicitly fictional; P.160 Johor Bahru remains a real constituency reference.
- Both email requests and activation-form drafts use the existing Katalys email address. The page sends nothing. Required-name validation runs before drafting; localized subjects and body labels match the chosen language.
- With JavaScript disabled, the direct email links and all six examples remain readable. The interactive form is hidden with an explanatory fallback.

## Pre-deployment settings

The user confirmed that the demo has **not been deployed**. `DEMO_URL` is empty; “Request demo access” / “Mohon akses demo” prepares an email request. No live demo URL is claimed. When the demo is deployed, update the URL, link labels and explanation together: the public fictional-candidate page is open, while the team workspace requires an issued login.

`WHATSAPP` remains empty and WhatsApp links/buttons are hidden. Populate only with a confirmed number, identically in both files. Do not replace the existing email address without instruction.

No deployment, external message or code commit was performed in this pass. Both pages were saved into the existing landing-page project. When a site root is configured later, use the BM page as the entry page unless instructed otherwise.

## Copy boundaries

No prices, real people imagery, party symbols, voter/supporter numbers, testimonials or unbuilt-feature claims. No star motif. Only stages four and five are available; the others are marked planned without dates. Removed the implied personal-record migration and the broad “stores no voter data” claim. The campaign remains separate from office/citizen records; there is no voting-intent field or supporter estimate. Spending records do not advise on compliance or block spending; responsibility stays with the election agent.

## Verification

- Chromium: both languages at 320, 375, 768, 1024, 1280 and 1440 CSS pixels. No page or content overflow at any checked width.
- All six tabs expose exactly one panel; keyboard navigation and a visible 3 px focus outline work.
- Approval example correctly switches to “ready for approval” and resets to “open”.
- Invalid form submission focuses the required name field; valid inputs produce a localized draft with preserved newlines and special characters. No message was sent and the external email-app handoff was not exercised.
- Both language links reach the correct sibling page; WhatsApp controls remain hidden.
- Reduced motion disables smooth scrolling; no active animations.
- No JavaScript fallback: six examples and direct email remain visible, form is hidden.
- Computed contrast check found no failures among 128 visible text elements per language in the default state. This is not a full WCAG audit.
- Unique IDs, valid internal anchors, fonts-only external dependencies, no old mark or placeholder demo domain; no browser script errors.
- Visually inspected BM desktop/mobile hero, workspace example and activation form, plus the full English page. Screen-reader testing, Safari/Firefox, live email delivery and deployed-demo access were not tested.
