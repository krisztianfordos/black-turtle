# Design reference: Saint Urbain (structure only)

Last verified: 2026-10-14

## Sources
- https://sainturbain.com (structural reference only; values as recorded in the project brief, not re-verified in this pass)
- `CLAUDE.md` ("reverse-engineered from sainturbain.com as a reference only. No Saint Urbain content, names or colours should remain.")

## Scope
This file records only the structural system taken from sainturbain.com. No content, copy, imagery, names or colours from that site are used in Black Turtle. Black Turtle's own palette and fonts are in `CLAUDE.md`.

## Typefaces
- Original: PP Neue Montreal (sans) and ITC Garamond Light (serif)
- Black Turtle stand-ins: Inter Tight (sans) and EB Garamond (serif)

## Type scale (px)
12 / 14 / 15 / 16 / 18 / 20 / 22 / 24 / 28 / 32 / 36 / 40 / 48 / 66 / 72
- Hero: 120 (Min(8.33vw, 120px))

## Spacing
- Utilities 5 to 200 in steps

## Container
- container-fluid margins: 10 / 15 / 20 at <768 / ≥768 / ≥1200

## Grid
- grid repeat(n, minmax(0, 1fr)) for n = 1 to 10 columns
- Gap: 20

## Breakpoints (px)
576 / 768 / 1024 / 1200 / 1441 / 1800

## Z-index ladder
- 0 to 2 (base layers)
- 1000 to 9000 (overlays)

## Depth and effects
- No box-shadows
- `mix-blend-mode: difference` on the header and on link underlines

## Motion
- Easing (main): cubic-bezier(.645, .045, .355, 1), transforms .4 to .7 s
- Colour transitions: .25 s linear
- Second easing: cubic-bezier(.215, .61, .355, 1), 1.25 s
- Headline stagger: 100 ms per line, 30 ms per character

## Original palette (NOT used as-is)
- Oxford #1A1918
- Off-white #E8E8E8
- Yellow #F6EA18
- Blue #0915E7

Yellow and blue were deliberately removed from Black Turtle. Black Turtle's palette is in `CLAUDE.md` (oxford #1A1918, off-white #E8E8E8, sandstone #D4C3B3, mahogany #7E412A); only the first two values coincide with the original.
