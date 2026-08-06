# Handoff: Pilot Tester Onboarding Page

## Overview
A single marketing/instructional web page walking pilot testers of the TangoHost app through first-time setup and core actions: logging in, bookmarking the app to their home screen, creating a trip, posting arrival/return rides, and creating or joining a room share. Sent to pilot testers ahead of the "Chicago CincOH 5th" event.

## About the Design Files
The file in this bundle (`Pilot Onboarding Page.dc.html` + `support.js`) is a **design reference built as an HTML prototype** — it shows intended look, layout, and copy, not production code to copy directly. Recreate this page in the target site's existing environment (its framework, component library, and routing), matching the visuals and copy below. The `support.js` runtime is specific to this prototyping tool and has no equivalent in a real codebase — ignore it beyond reading developer intent from the markup structure.

## Fidelity
**High-fidelity.** Colors, type sizes/weights, spacing, and all copy are final as shown. Treat the values below as authoritative. The phone "mockups" illustrating each step are illustrative recreations of app screens (not real screenshots) — they exist only to help the reader visualize each step, and do not need to be pixel-matched if the real app screens differ; use the real app screens there instead if available.

## Screens / Views
This is a single scrolling page, no navigation between views. Sections top to bottom:

### 1. Hero
Centered text block, max-width 600px, centered horizontally on the page (page max-width 1000px, centered, side padding 40px, top padding 100px).
- Eyebrow: "Chicago CincOH 5th · Pilot Testers" — 15px, weight 700, uppercase, letter-spacing 0.14em, color `#C1663D` (brand terracotta).
- Title: "Getting started with the app" — Fraunces serif, 52px, weight 700, letter-spacing -0.01em, color `oklch(20% 0.02 75)` (near-black warm gray), margin-top 16px.
- Subhead: "Thanks for helping us test! Follow these steps to get set up before the event." — Work Sans, 19px, color `oklch(42% 0.02 75)`, margin-top 18px, line-height 1.5.

### 2. "Getting set up" section header
- Heading: "Getting set up" — Fraunces, 28px, weight 700, margin-top 80px (from hero).
- Sub-note directly below: "Requires an iOS device (iPhone)." — Work Sans, 15px, weight 600, color `oklch(50% 0.02 75)`, margin-top 6px.

### 3. Step rows (steps 1–4, then "Ride home & room sharing" header, then steps 5–7)
Each step is a horizontal row: numbered badge + title + description on the left (flex:1), one or more phone mockups on the right (flex-shrink:0). Rows are separated by a 1px top border (`oklch(90% 0.015 75)`), 32px vertical padding, `align-items:flex-start`, 40px gap (24px gap for step 2's row, which has 3 mockups). The row above step 5 and the row before step 7 additionally carry a bottom border, bookending each of the two step groups.

Number badge: 34×34 circle, background `#C1663D`, white text, Fraunces 16px weight 700, centered.

Step title: Fraunces, 24px, weight 700, color `oklch(20% 0.02 75)`, margin-top 14px (from badge).

Step description: Work Sans, 17px, color `oklch(42% 0.02 75)`, margin-top 8px, line-height 1.5.

Phone mockup frame (steps 1, 3–7): 230px wide, aspect-ratio 390:844 (iPhone proportions), `box-sizing:border-box` (so border/padding don't change the rendered size), white or tinted background per step, border-radius 16px, box-shadow `0 8px 20px rgba(0,0,0,0.1)`, border `5px solid #1a1a1a` (device bezel look).

Step 2's three mockups are smaller: 165px wide, same aspect ratio, `box-sizing:border-box`, 14px border-radius, `4px solid #1a1a1a` border, laid out in a row with 10px gap.

**Step 1 — "Go to the app & log in"**
Copy: "Open my link and log in with the account I set up for you."
Mockup: top bar "Log in" (Fraunces 11px bold) on a light bar; body centered — "TangoHost" wordmark (Fraunces 18px bold, dark plum `oklch(20% 0.05 300)`), tagline "Ride shares & room shares for tango trips" (7px), Email field, Password field (both pill/rounded rect placeholders, tan-tinted background `oklch(92% 0.015 60)`), and an orange pill "Sign in" button (`#C1663D` bg, white text, fully rounded).

**Step 2 — "Bookmark it on your phone"**
Copy: "Tap Share, then "Add to Home Screen", then confirm."
Three mockups showing the iOS flow:
1. Share sheet: "Share" row highlighted teal, then "Add to Bookmarks", "Add Bookmark to…", divider, "New Tab", "New Private Tab", divider, bottom icon row (Bookmarks / All Tabs).
2. Expanded options list: icon row (Copy / Add to Bookmarks / Add to Reading List / View Less), then "Add Bookmark to…", "Add to Favorites", "Add to Quick Note", "Find on Page", **"Add to Home Screen" highlighted**, divider, "Markup", "Print" (last two dimmed).
3. "Add to Home Screen" confirmation dialog: header with title + blue "Add" action, app icon placeholder ("A" on gray square) + name "abrazos-pilot" + truncated URL, "Open as Web App" row with a green toggle (on), helper text "An icon will be added to your Home Screen so you can quickly access this website."

**Step 3 — "Create a trip for CincOH"**
Copy: "Tap the + button, search "CincOH", and join the event."
Mockup: "My Trips" header, one existing trip card ("Buenos Aires Trip"), bottom sheet with two options ("Create a new trip", and a highlighted "Search events ("CincOH")" row), and a circular orange "+" button top-right.

**Step 4 — "Create your arrival ride"**
Copy: "Airport → venue, with your arrival time."
Mockup: "Offer a carpool" form — Start location field ("O'Hare (ORD)"), End location field ("Venue — CincOH"), orange "Post carpool" button.

**"Ride home & room sharing" section header** — Fraunces 28px weight 700, margin-top 64px.

**Step 5 — "Create your return ride"**
Copy: "Venue → airport, with your departing time."
Mockup: same carpool form, reversed: Start = "Venue — CincOH", End = "O'Hare (ORD)".

**Step 6 — "Create a room share"**
Copy: "Have a room or a spot open? Post it under Rooms."
Mockup: "Offer a room" form — Type field ("Private room · Airbnb"), Beds available field ("2 beds"), orange "Post room" button.

**Step 7 — "Or join a room share"**
Copy: "Browse Rooms and request a spot in someone else's."
Mockup: "Rooms" list header, two room cards ("Marina S. · 2 beds left", "Diego R. · 1 bed left"), orange "Request to join" button pinned to the bottom.

### 4. Closing
Centered text block, margin-top 80px:
- "You're all set!" — Fraunces, 40px, weight 700.
- "Update your travel status as you go on the day you are travelling. And message Isabelle if you have any questions." — Work Sans, 18px, color `oklch(42% 0.02 75)`, max-width 600px centered, line-height 1.6.

## Interactions & Behavior
This page is static informational content — no interactive elements, forms, or state. All "mockups" are non-functional illustrations. If the real app supports deep-linking (e.g. jumping straight to "create a trip" or "offer a carpool"), consider making the relevant step text or mockup a link to that flow, but this isn't part of the current design.

## State Management
None — static content page.

## Design Tokens

**Colors**
- Background: `oklch(98% 0.012 75)` (warm cream)
- Primary text: `oklch(20% 0.02 75)`
- Secondary text: `oklch(42% 0.02 75)` / `oklch(50% 0.02 75)` / `oklch(55% 0.02 75)` (graduated warm grays)
- Accent (brand terracotta): `#C1663D`
- Row divider: `oklch(90% 0.015 75)`
- Mockup device bezel: `#1a1a1a`
- Mockup backgrounds vary per step: `#fff`, `oklch(93% 0.015 75)`, `oklch(96% 0.012 75)`, `oklch(90% 0.01 75)`, `oklch(94% 0.01 75)`

**Typography**
- Display/headings: Fraunces (serif), weights 600–700
- Body/UI text: Work Sans (sans-serif), weights 400–700
- Hero title: 52px; section headings: 28px; step titles: 24px; step body: 17px; hero subhead: 19px

**Spacing / radii**
- Page max-width: 1000px, centered, 40px side padding
- Step row vertical padding: 32px; row gap: 40px (24px for step 2)
- Phone frame radius: 16px (14px for step 2's smaller ones)
- Number badge: 34px circle

## Assets
No photographic assets. All icons in the mockups are inline SVG line icons (see markup for exact paths). No external images.

## Files
- `Pilot Onboarding Page.dc.html` — the full page. Single scrolling document, no separate screens/routes.
- `support.js` — this prototyping tool's runtime (reference only, not to be ported).
