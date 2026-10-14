# Black Turtle Salon — project guide

Website project for **Black Turtle Salon**, a men's hairdressing & barbering salon at **1056 Budapest, Szerb utca 8.** (formerly *Barberhood Midtown*). Verified business facts live in `content/salon-facts.md`. Never invent salon facts (prices, names, hours); if something isn't in that file, mark it as a placeholder and ask.

## Status

**Concept / design-system phase.** Do not scaffold, code, or deploy the website until the user explicitly says so. Current work happens in Paper.

- Paper file: **Black Turtle — Design System** — https://app.paper.design/file/01M4WS0X30AFDSN4WHVWCG52S1
  - **Board *Brand Book — Black Turtle Salon*** (the current, owner-facing version). It reads in this order: header → shopfront hero → intro/contents → 01 Logo & turtle → 02 Colours → 03 Materials, Textures → 04 Typography → 05 Shapes & details (shell, arch, slash, pole) → 06 Website building blocks → Appendix for the developer (spacing, grid, depth & motion) → shopfront footer.
  - Boards *Design System — Black Turtle* and *Motifs — Black Turtle*: earlier working versions. Leave them untouched as history; make new edits on the Brand Book.
- The structural system (type scale, spacing, grid, motion) was reverse-engineered from sainturbain.com as a reference only. No Saint Urbain content, names or colours should remain.

## Brand system (source of truth = Paper tokens)

**Colour roles (60 / 30 / 10)**
| Role | Token | Hex | Notes |
|---|---|---|---|
| Primary | `--color-primary` → `--color-oxford` | `#1A1918` | Ground |
| Secondary | `--color-secondary` → `--color-off-white` | `#E8E8E8` | Type on dark, light ground |
| Accent | `--color-accent` → `--color-sandstone` | `#D4C3B3` | Facade stone. Hover, serif emphasis, active |
| Accent on light | `--color-mahogany` | `#7E412A` | Sandstone fails contrast on off-white; use mahogany there |

Material colours (from the interior/facade photos, for textures and surfaces, not UI chrome): leather `#1A140F`, leather-sheen `#424038`, walnut `#351A12`, mahogany `#7E412A`, cognac `#B07656`, chrome `#ACAAAA`, apricot `#CDA487` (door frame), sandstone `#D4C3B3`. Neutrals: graphite `#3E3E3E` (hairlines), black, white.

No yellow/blue. They were removed on purpose.

**Type**: sans `--font-sans` (Inter Tight, stand-in for PP Neue Montreal, weight 400 for nearly everything); serif `--font-serif` (EB Garamond, stand-in for ITC Garamond Light), set ~10% larger than the sans it sits next to.
Font rule (strict): **sans for everything**: menus, buttons, list rows, prices, swatch names, card titles, running text/marquee, reviews. **Serif only for one highlighted word or phrase inside a large headline (≥48px)**, usually in the accent colour (e.g. "Hajvágás és szakáll, *precízen.*", "The *arch*"). Never a whole sentence, never a nav item, never alternating in a list. Scale: 12/14/16/18 (body)/20/24/32/36/48/66/72/120 (hero). Labels: 14px caps, +6% tracking. Display: −2% tracking.

**Spacing**: 5px base; 5/10/15/20, then steps of 10 up to 200. Gutter 20; edge margin 10/15/20 (mobile/≥768/≥1200); section padding 120; block gap 80.

**Grid**: fluid 12 columns, no max width, edge-to-edge. Breakpoints 576/768/1024/1200/1441/1800.

**Depth**: flat. No box-shadows, square corners (radius 0, pills only for tags/CTA). Overlapping solid planes; header uses `mix-blend-mode: difference`. Easing `cubic-bezier(.645,.045,.355,1)`, transforms .4–.7s, colour .25s linear.

**Motifs**: Turtle (the logo line-art, always present; bleed it off the frame, never shrink below 40px, use the roundel badge below that), Shell (irregular facet mesh from the turtle plates), Arch (shopfront door: 3:4, radius = width/2), Slash (~55° hairline from the wordmark, joins paired words), Pole (55° stripes, only as thin tape).

**Textures** (each material has a job):
- Herringbone, the floor: booking, pricing, anything you walk through. Use the vector (`textures/vector-herringbone-*.svg`).
- Tufting, the chair: barber profiles, anything personal. Use the vector (`textures/vector-tufting-*.svg`); it is also the portrait placeholder.
- Stone facade (rusticated ashlar): address, hours, footer, the hero. The real facade has **only horizontal grooves, no vertical joints**. Use `textures/vector-rustication-*.svg`, `textures/hero-rustication-sandstone.svg` (1440 wide), or photo tiles `textures/tile-ashlar*.png`. Don't use the old `vector-ashlar-*` / `tile-stone*` (they have vertical joints). Hero and footer = rustication wall + arched doorway with the voussoir ring (`textures/arch-voussoirs-sandstone.svg`): interior photo inside the arch in the hero, the turtle inside it in the footer.
- Marquee/running text shows the signature services (Skinfade hajvágás, Szakáll igazítás, Hosszú ollós hajvágás, Gyerek hajvágás).
- Reviews component: rating summary (5,0 · 438) + 3 verbatim Google quotes from `content/reviews.md`.
- "Quiet" variants (oxford duotone / oxford vectors) are for full-bleed grounds; the full-colour versions only for contained panels.

## Assets

`assets/`
- `src/`: originals (interior.webp, facade.png, logo PNGs). Don't modify.
- `turtle-*.png`, `wordmark-*.png`: transparent recolourable logo cut-outs
- `texture-*.png|jpg`, `photo-*.jpg`, `facade-*.png`: crops
- `textures/`: vector SVG textures (preferred), seamless 512px photo tiles + duotones, `preview-tiles.jpg`. Known issues: `tile-wood*` has faint banding and `tile-leather*` shows quadrant seams (source photos are low-res); use the vectors instead. The stone tiles are clean.
- Repo root also has `blackturtle-interior-1…4.webp` (unused so far) and the original logo PNGs.

`content/`: `salon-facts.md` (verified facts + sources), `services.json` (full scraped service list with descriptions), `reviews.md` (verbatim Google reviews + display rules).

Copy rules: site content is Hungarian; explanations in the brand book are plain English for the owner. No invented services, offers or quotes. Saturday hours currently follow Salonic (09–15) until the owner confirms.

The facade screenshot has a video play button baked in. Ask for a clean shopfront photo before using it prominently.

## Planned site sections (content to gather; no build yet)

1. **Rólunk** (About)
2. **Barberek** (Barbers)
3. **Időpontfoglalás** (Booking) — currently via Salonic: https://blackturtlesalon.salonic.hu
4. **Szolgáltatások** (Services, with descriptions)
5. **Állás lehetőség** (Careers)
6. **Termékek** (Products) — later

Primary language Hungarian; English secondary (Salonic is bilingual).

## Working conventions

- Delegate mechanical or research work (image processing, scraping, lookups, summaries) to the `utility` agent (Haiku 5.5). Keep Paper/MCP design work in the main session (subagents don't have the Paper tools).
- Plain fetches can't read Google Maps/Instagram. Use the Playwright browser for those.
- In Paper: use tokens (`var(--color-…)`), never raw hex; screenshot-review after each section; call `finish_working_on_nodes` when done.
- Image processing scripts go in `/tmp/bt-scripts/`, not in `assets/`.

## Open questions

- Saturday hours conflict (Salonic 09–15 vs Google Maps closed).
- Licensed fonts: PP Neue Montreal / ITC Garamond, or keep the free stand-ins?
- Clean facade photo; barber portraits; About text; job postings.
