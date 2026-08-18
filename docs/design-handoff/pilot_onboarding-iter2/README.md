derivative
# Handoff: Pilot Onboarding Page (marketing/instructions page, not app UI)

## Overview
A standalone web page emailed/linked to beta testers of Connectango. It's a step-by-step guide (bookmarking the PWA, logging in, resetting password, joining the CincOH event, offering/finding rides, offering/finding room shares, Facebook profile linking) with small illustrative phone-mockups next to each step.

## About the Design File
`Pilot Onboarding Page.dc.html` + `support.js` are a **design reference prototype**. This page itself is a simple static content page (not an interactive app screen) — it can likely be shipped close to as-is, published as a static page (e.g. GitHub Pages, as referenced by its own link `cincoh5pilot.html`). The phone mockups embedded per step are simplified illustrations, not exact production screens — treat them as directional references for a developer/designer to sanity-check against the real app's current screens, not as pixel-exact specs.

## Structure
- Header: "Connectango" wordmark + "Beta pilot guide" subtitle.
- Intro paragraph on focus/scope of the pilot, including a note that hosting and registration-partner features aren't implemented yet.
- Numbered steps (1–9+), each: number badge (circular, accent-colored terracotta `#C1663D`), step title (Fraunces serif, 24px/700), body copy (Work Sans, 17px, `oklch(42% 0.02 75)`), and a small phone mockup illustration to the right.
- Steps cover: bookmark to home screen, log in + reset password, join the CincOH event, find/offer a ride (with mini route/companion mockups), Facebook profile linking, offer/find a room share, and looking someone up on Facebook.

## Content
All copy is final as written — do not rephrase; this is the literal text sent to real beta testers.

## Design Tokens
- Fonts: Fraunces (serif, headings/titles) + Work Sans (sans, body/UI text)
- Accent: `#C1663D` (terracotta — note this is a slightly different shade than the in-app coral accent `#ED6558`; confirm with design whether to unify)
- Body text: `oklch(42% 0.02 75)`; step number badge text: white
- Background: cream, `oklch(98% 0.012 75)`-family
- Phone mockup frame: 230px wide, `390/844` aspect ratio, 5px black border, 16px radius, drop shadow

## Notes for implementation
- This is not app code — it's a one-off informational page. No state, no interactivity beyond static content.
- If publishing as-is, host at the URL already referenced elsewhere in the project (`cincoh5pilot.html`) so the beta email's link resolves correctly.
- The phone mockups are illustrative flat HTML/CSS re-creations of app screens, some already updated to match real screenshots supplied by design — no image assets to extract.

## Files
- `Pilot Onboarding Page.dc.html` — the full page.
- `support.js` — prototype templating runtime (reference only, not to be ported).
