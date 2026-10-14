# Plans & decisions — Black Turtle Salon

Last updated: 2026-10-14. Owner of decisions: the project lead (user). Status markers: ✅ done · 🟡 in progress · ⏳ planned · ❓ needs owner input.

## Phase
Concept / brand-book phase. **No website code yet**, except throwaway visual prototypes made only to produce stills for the brand board (see the interior push-in below).

## Website (later)
Sections, Hungarian first, English second:
1. Rólunk (About). ❓ no public text; ask the owner.
2. Barberek (Barbers): 4 barbers, levels from Salonic. ❓ bios and portraits needed.
3. Időpontfoglalás (Booking): link out to Salonic (`/booking/start`) for now.
4. Szolgáltatások (Services, with descriptions): full data in `context/services-pricing.md`.
5. Állás lehetőség (Careers). ❓ nothing public.
6. Termékek (Products). ⏳ later.

## Hero concepts (brand book shows both, stacked)
- **A, Shopfront** ✅: the rusticated sandstone wall (horizontal grooves only), arched doorway with a voussoir ring and **vertical jambs to the ground**, barber pole left of the door, enamel street sign ("V. kerület, Belváros / Szerb utca / → 8") on the wall, text on black plaques aligned to the stone courses. Inside the arch: the interior.
  - A1 ✅: real interior photo inside the arch.
  - A2 ✅: the **code-drawn interior** (first frame of the push-in) inside the arch instead of the photo.
- **B, Interior push-in** ✅ first frame on the board (animation prototype exists, needs polish): a full-bleed background with no stone or arch. A slow "gimbal" dolly-in into the salon, drawn entirely in JavaScript (Canvas 2D, no libraries), in the spirit of "Window Seat" (see `context/reference-train-journey.md`). The brand book shows only the **start frame**. The full animation/video is a later step.
  - Basis: `context/interior-analysis.md` (photo breakdown, palette, recommended shot and depth layers).
  - Technique notes to keep: `render(t)` as a pure function of time; deterministic RNG; world-space geometry projected through a moving camera (no bitmap scaling to fake the dolly); eased distance curve; 12–20 s slow move with slight drift/parallax.
  - Prototype: `prototypes/interior-pushin/index.html` (open in a browser; `?t=SECONDS&w=&h=` freezes a frame). Stills in `assets/renders/`.
  - ⏳ Polish before using it on the site: rounder chair cushions, polished chrome (not flat blocks), a smaller calf-rest so the base shows, chairs angled slightly toward each other, better mirror reflections (no ghosting), cleaner floor reflections (green blob under the plant), the missing dryer rack and right-hand rack, and a better portrait crop for the arch (chairs sit slightly low).

## Footer
✅ The same shopfront wall + arch with the turtle inside; the address as the enamel street sign; hours and contact on a black plaque. Saturday hours ❓ (Salonic 09–15 vs Google closed).

## Brand rules decided
- Colours: Primary Oxford / Secondary Off-white / Accent Sandstone (60/30/10); Mahogany for accents on light pages. Yellow/blue removed.
- Fonts: sans everywhere; serif only for one highlighted word in a ≥48px headline. Street sign: EB Garamond (district line, number) + Inter Tight 600 tight (street name).
- Textures: herringbone (booking/prices), tufted leather (barbers), rusticated stone (address/hours/footer/hero).
- Motifs: turtle, shell facets, arch, slash, barber pole (as an object on the wall + as thin 55° stripe tape).

## Open questions for the owner
- Saturday opening hours
- About text; barber bios and high-res portraits
- Job openings; products/brands used
- Licensed fonts (PP Neue Montreal / ITC Garamond) or keep the free stand-ins
- A clean shopfront photo (current reference has a video play button)
- OK to quote Google reviews on the site (names shortened to first name + initial)
