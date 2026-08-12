# Color Scheme: "Coral Pink"

Alternate accent palette for the TangoHost app, built on the Warm Earthy base.

## Tokens

| Role | Value | Notes |
|---|---|---|
| Accent (primary) | `#ED6558` | Coral pink, slightly more saturated. Replaces `#C1663D` everywhere `accentColor` is used (buttons, active tabs/chips, links, "You" avatars, selected states). |
| Background (screen) | `oklch(97% 0.015 65)` | Warmed slightly to pair with the coral accent. |
| Rider/avatar tag — teal | `oklch(56% 0.07 195)` | Cool counterpoint color used for a subset of rider avatars (e.g. Lucía, Sofía, Priya); kept unchanged from other explored schemes. |

## Avatar bubble palette (full set)
These are the distinct colors assigned to individual rider/roommate avatars across the app's seed data — not theme tokens, but the actual per-person swatches currently in use, since the live implementation has drifted from this set:

| Color | Used for (examples) |
|---|---|
| `oklch(70% 0.14 35)` | Marina S., Julieta P. |
| `oklch(64% 0.12 250)` | Diego R., Carlos & Ana |
| `oklch(56% 0.07 195)` | Lucía F., Sofía M., Priya K. (teal counterpoint) |
| `oklch(60% 0.02 75)` | Tomás B. (neutral gray) |
| `oklch(58% 0.1 200)` | Carlos M. |
| `#ED6558` (= accent) | "You" — always uses the current accent color, not a fixed swatch |

These colors cycle across riders/roommates and are decorative identity colors, not semantic — any consistent palette of 4–5 distinct hues works, but the app should reference this set (or the accent for "You") rather than inventing new ones.

All other tokens (card white `#fff`, text grays `oklch(20%/42%/50%/55% 0.02 75)`, status tint colors for travel status, card shadows/radii) are unchanged from the Warm Earthy base.

## Implementation notes for Claude Code
- The accent is a themeable prop (`accentColor`) on the root component in the prototype — wire your app's theme/token layer the same way (single source of truth for the accent), then set it to `#E8756B`.
- Update the shared background token to `oklch(97% 0.015 65)` (or its RGB/hex equivalent in your system).
- Watch for any hardcoded avatar/"You" colors that should instead reference the accent token rather than a literal value.

## Reference file
`Trip Details - Warm Earthy -Coral Pink-.dc.html` in this project is the live prototype using this exact scheme.
