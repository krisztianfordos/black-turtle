# Black Turtle barbershop: interior analysis for procedural canvas redraw

Sources: `/Users/fordoskrisztian/claude/black-turtle/blackturtle-interior-{1,2,3,4}.webp` (all 1360x907, RGB).
Note on the photos: photo 3 is the Mezzalama cape chair with a ring light and staircase. Photo 4 is the two tufted barber chairs.

Conventions: object positions are % of the photo frame as `left / top / width / height`, with top-left origin. Depth numbers run back (1) to front (higher). Horizon and vanishing points are eyeballed, so treat them as medium-to-low confidence. Hex values are medians of small sample boxes and may vary by about 10%.

---

## Photo 1: fern wall, grey velvet armchair, Black Turtle poster

**Camera**
- Position: close, about 1.2 m high, eye level. Sited to the right of the sideboard, angled slightly left.
- Lens: normal to short tele (about 50-70 mm equiv.), shallow depth of field, foreground chair blurred.
- Vanishing points: none usable. Verticals (fern edge, pipe, poster) are nearly parallel.
- Horizon: about 60% from top (y about 540 px), roughly level with the sideboard top.

**Composition**

| Object | left | top | w | h | depth |
|---|---|---|---|---|---|
| Fern wall, full height, dense green | 0 | 0 | 49 | 100 | 1 |
| Poster "BLACK TURTLE" on white wall | 59 | 9 | 18 | 57 | 2 |
| White vertical pipe | 50 | 15 | 3 | 62 | 2 |
| Wood sideboard with lattice panel | 47 | 62 | 28 | 20 | 3 |
| Pachira plant, white pot | 42 | 41 | 17 | 22 | 3 |
| Succulent, grey pot | 58 | 56 | 4 | 8 | 4 |
| Black and white bottle | 69 | 51 | 5 | 15 | 4 |
| Grey velvet armchair, gold legs | 17 | 59 | 30 | 33 | 5 |
| Two-tier wood side table | 0 | 85 | 20 | 15 | 6 |
| Chrome and glass tray (foreground) | 40 | 76 | 34 | 24 | 7 |
| Blurred black barber chair (foreground right) | 74 | 0 | 26 | 100 | 7 |

**Objects in detail**
- Fern wall: artificial boxwood/fern panel, near-vertical, bright leaf highlights.
- Armchair: grey velvet, vertical channel tufting on the back, horizontal channel tufts on the seat, flared arms, tapered brass/gold legs.
- Side table: two stacked dark-walnut tiers with rounded trapezoid tops.
- Poster: matte charcoal, white line-art turtle logo, white "BLACK TURTLE" title, smaller "MALE HAIRDRESSING / BARBERING" with a strike-through. Leans on the sideboard.
- Sideboard: rustic walnut-brown, black metal lattice panel, open shelf.
- Pachira: braided trunk, glossy green leaves, cream pot.
- Blurred chair: black leather with a chrome base edge.
- Wall: white, slightly cool. Floor and skirting not visible.

**Lighting**
- Soft daylight-style light from the left, lighting the fern strongly and the poster evenly.
- Chrome tray edge has a highlight. Shadows are soft and short. No floor reflections visible.

---

## Photo 2: wide overview from high vantage (three cape chairs, sink)

**Camera**
- Position: high, about 2.5-3 m (mezzanine or landing, rear-left), looking down about 30-35 degrees.
- Lens: wide, about 24-28 mm equiv.
- Vanishing points: floor herringbone and wall lines converge toward upper centre. Estimated VP about (48%, 12%), horizon about 20% from top. Low confidence.

**Composition**

| Object | left | top | w | h | depth |
|---|---|---|---|---|---|
| Ceiling LED panels (4, hung on wires) | 12 | 0 | 55 | 15 | 1 |
| Fern wall strip (left edge) | 0 | 25 | 4 | 40 | 1 |
| Black Turtle board on wood cabinet | 13 | 35 | 14 | 25 | 2 |
| Grey armchair (back-left) | 9 | 52 | 12 | 10 | 2 |
| Mirror A (left) | 30 | 28 | 9 | 23 | 2 |
| Mirror B (centre) | 44 | 27 | 6 | 24 | 2 |
| Wall TV | 67 | 19 | 11 | 10 | 2 |
| Map frame on wall | 59 | 32 | 4 | 11 | 2 |
| Rolled towel shelf | 66 | 29 | 11 | 10 | 2 |
| Chair 1 (back-centre) | 49 | 39 | 8 | 18 | 3 |
| Chair 2 (mid-left) | 35 | 41 | 10 | 22 | 4 |
| Sink and shampoo recliner | 61 | 46 | 16 | 13 | 3 |
| Trolley (left) | 28 | 40 | 6 | 19 | 4 |
| Wood side tables | 11 | 61 | 12 | 7 | 5 |
| Grey chair (front-left) | 9 | 65 | 16 | 18 | 5 |
| Chair 3 (front-right, large) | 55 | 55 | 22 | 33 | 6 |
| Trolley (right) | 76 | 61 | 8 | 18 | 5 |
| Ring light on stand | 86 | 45 | 13 | 40 | 6 |
| Fiddle-leaf plant (front-right corner) | 72 | 82 | 22 | 18 | 7 |

**Objects in detail**
- Chairs: black cape with logo, chrome column, round black-and-chrome base, chrome footrest.
- Sink: black ceramic basin with a black recline chair.
- Mirrors: tall, thin black frames.
- TV: black, wall-mounted.
- Floor: glossy herringbone, orange-red-brown. Each block is about 1/6 of a chair-base diameter, with chevrons at roughly 45 degrees.
- Ring light: white and bright, on a black tripod.
- Walls: white and slightly warm. Ceiling: white with exposed beams.

**Lighting**
- Overhead LED panels, cool-neutral and strong.
- Chairs have soft contact shadows. Floor has glossy highlight patches from the panels and orange-gold glints under the chairs.

---

## Photo 3: Mezzalama cape chair, ring light, mirror, staircase

**Camera**
- Position: eye level or slightly above, about 1.3-1.4 m, standing beside the chair and looking across.
- Lens: normal to slightly wide, about 35-40 mm equiv.
- Vanishing points: mirror and wall verticals are upright. Stair underside and railing converge toward the right. Horizon about 55% from top. Low confidence.

**Composition**

| Object | left | top | w | h | depth |
|---|---|---|---|---|---|
| Left wood panel wall | 0 | 0 | 8 | 100 | 1 |
| Wall shelf with bottles and hanging pothos | 31 | 8 | 12 | 25 | 1 |
| Stair railing (wood slats, top-right) | 68 | 0 | 32 | 43 | 1 |
| Framed print on wall | 45 | 38 | 3 | 17 | 2 |
| Large mirror | 43 | 0 | 24 | 100 | 2 |
| Reflected chair in mirror | 52 | 41 | 13 | 57 | 2 |
| Ring light (behind headrest) | 23 | 21 | 11 | 22 | 3 |
| Hero chair cape (Mezzalama logo) | 12 | 42 | 42 | 58 | 4 |
| Hero chair headrest | 20 | 34 | 9 | 9 | 4 |
| Left metal rack | 8 | 63 | 6 | 21 | 4 |
| Ficus in grey pot | 71 | 32 | 15 | 38 | 3 |
| Fridge with drinks | 88 | 63 | 12 | 37 | 3 |
| Dracaena, striped leaves | 59 | 57 | 26 | 32 | 5 |
| Snake plant, black pot | 75 | 78 | 8 | 22 | 6 |

**Objects in detail**
- Chair: charcoal cape with red and white logo. Black leather headrest.
- Ring light: white circular LED on an arm.
- Mirror: floor-to-ceiling, thin black frame.
- Staircase: warm walnut, vertical slats.
- Fridge: glass door with cans and bottles inside.
- Floor: warm reddish wood, partly visible in the mirror reflection. Herringbone not confirmed.
- Walls: white.

**Lighting**
- Bright, soft, top-front light.
- Ring light glow sits on the headrest.
- Mirror shows a ceiling light reflection. Warm wood reflects in the floor.

---

## Photo 4: two tufted barber chairs, mirrors, herringbone floor (recommended hero)

**Camera**
- Position: eye level, about 1.2-1.3 m, 2-3 m from the chairs, slightly right of centre and looking across to the left mirror.
- Lens: normal, about 35-40 mm equiv.
- Vanishing points: floor edges converge toward about (50%, 45%). Verticals are near-upright. Horizon about 42-48% from top. Medium confidence.

**Composition**

| Object | left | top | w | h | depth |
|---|---|---|---|---|---|
| Map poster, black frame, right wall | 86 | 21 | 12 | 26 | 1 |
| Left mirror (tall, thin black frame) | 12 | 1 | 20 | 82 | 2 |
| Centre mirror | 46 | 10 | 14 | 67 | 2 |
| Hanging green plant above mirror, with shelf | 33 | 7 | 5 | 23 | 2 |
| Potted plant, large leaves, white pot | 65 | 26 | 11 | 23 | 3 |
| Chair R (right, tufted) | 63 | 32 | 21 | 55 | 4 |
| Black rack, against right wall | 74 | 49 | 9 | 27 | 4 |
| Chair L (left, tufted, nearest) | 20 | 28 | 29 | 72 | 5 |
| Hair-dryer rack, left wall | 3 | 28 | 8 | 23 | 2 |
| Left three-tier trolley (front-left) | 0 | 50 | 12 | 41 | 6 |

**Objects in detail**
- Chairs: black button-tufted leather back and seat, chrome armrest caps, chrome column, round black-and-chrome base, chrome footrest with black leather pad. Black capes with a small red and white logo.
- Mirrors: tall, black hairline frames, reflecting the room.
- Plants: hanging green plant on a wood shelf above the mirror. Large-leaved potted plant (variegated green, white pot) on the right.
- Trolley: black metal, three tiers, bottles on top.
- Map poster: black-and-white city map in a black frame, with "BARBERHOOD" text.
- Floor: reddish-brown herringbone wood, glossy. Blocks are about 1/7 of a chair-base diameter, with chevrons at about 45 degrees to the walls.
- Walls: warm white plaster.

**Lighting**
- Soft, even light from overhead and front-left.
- Highlights on chrome armrest caps and on tufts.
- Floor shows soft specular glints. Shadows under chairs and footrests are soft and short.

---

## Palette (sampled, 10 colours)

| Hex | Where / what |
|---|---|
| #c8bfb4 | Warm white wall (photo 4) |
| #c7c3c0 | Cooler white wall and ceiling (photo 2) |
| #cfad97 | Light herringbone floor, sunlit (photo 2) |
| #b87550 | Mid floor, warm reddish (photo 4) |
| #431e13 | Dark floor, walnut gap and shadow (photo 4) |
| #0a0d0a | Tufted leather, near-black in shadow (photo 4) |
| #c3c9d0 | Chrome highlight on armrest cap (photo 4) |
| #143107 | Fern wall, deep green (photo 1) |
| #4b800e | Pachira leaf, bright green (photo 1) |
| #414142 | Poster, charcoal (photo 1) |

Also measured but not in the 10: grey velvet armchair #63645d (photo 1), cape charcoal #787878 (photo 3), leather tuft highlight #2d2e29 (photo 4, sampled inside a shadow region).

---

## Recommended hero shot: photo 4

**Why photo 4.** Both chairs are fully visible in a clean, low-clutter frame. The mirrors, plants and trolleys give about 6 depth planes. The herringbone floor provides perspective cues. Photo 2 is a high-angle overview that would be hard to reproduce procedurally. Photo 3 is tight and cluttered, and photo 1 is not chair-focused.

**Cover-crop mapping (photo 4 to 1440x820).** Scale = 1440/1360 = 1.0588. Y offset = 110 px. So X = px * 1.0588 and Y = py * 1.0588 - 110. Chair L's footrest is clipped at the bottom edge.

**Layers, back to front (1440x820 frame)**

| # | Layer | x | y | w | h | Parallax factor |
|---|---|---|---|---|---|---|
| 1 | Back wall, warm white, with map frame | 0 | 0 | 1440 | 470 | 0.20 |
| 1b | Map frame (on wall) | 1233 | 96 | 175 | 244 | 0.22 |
| 2 | Mirrors (left 175,0 / centre 664,0) | 175 | 0 | 288 | 689 | 0.40 |
| 2b | Hanging plant and shelf above mirror | 476 | 0 | 75 | 176 | 0.42 |
| 3 | Potted plant, back right | 932 | 144 | 153 | 212 | 0.50 |
| 4 | Floor plane (herringbone, warm mid to dark) | 0 | 470 | 1440 | 350 | 0.80 |
| 5 | Chair R, tufted, right | 910 | 197 | 297 | 529 | 0.90 |
| 6 | Right trolley, against right wall | 1122 | 361 | 80 | 259 | 0.95 |
| 7 | Chair L, tufted, nearest (bottom clipped) | 291 | 160 | 413 | 660 | 1.12 |
| 8 | Left trolley, front-left | 0 | 366 | 180 | 403 | 1.20 |
| 9 | Foreground vignette (dark corners, soft blur) | 0 | 0 | 1440 | 820 | 0.00 (fixed) |

**Camera move (16 s dolly-in)**
- Start: scale 1.00, focal point (720, 410). Full frame as laid out above.
- End: scale 1.18, focal point (700, 470). Chairs fill more of the frame.
- Easing: ease-in-out over 16 s.
- Per layer: scale_layer = 1 + factor * (scale_camera - 1), and offset from the focal point scaled by the same factor.
- Drift: horizontal sine of plus or minus 6 px at 0.06 Hz, plus a vertical bob of plus or minus 2 px at 0.2 Hz (gimbal feel).
