# Interior push-in (brand-board prototype)

A barbershop interior drawn entirely in Canvas 2D (no libraries, no bitmaps) with a slow 16 s gimbal dolly-in
between the two barber chairs. Based on interior photo 4. Prototype visual only, not the website.

## Open
Open `index.html` in a browser (no build, no server). It plays once and holds on the last frame.

## URL parameters
- `?t=SECONDS` freezes at that time (0 to 16), no animation.
- `&w=..&h=..` canvas size in CSS px (default 1440x820). The same camera is re-framed by aspect: landscape is
  cover-style, portrait pulls back slightly so both chairs stay centred (460x600 works for the arch crop).
- Console: `seek(t)` renders any time.

## Scene (world units are metres)
Room 7.8 m wide with back wall at z = 4.4. Everything is a world-space polygon projected each frame through a
pinhole camera (eye, look-at, focal length, near-plane clipping). Nothing is a scaled bitmap.
- Back/side walls, ceiling, skirting, light wash from the front-left.
- Herringbone floor: ~1.6k planks at 45 degrees to the walls, walnut/mahogany/cognac tones, grain, gloss.
- Two black-framed mirrors with real reflections (scene mirrored across the wall plane, plus virtual floor).
- Two tufted leather chairs (box/prism solids, back-face culled, shaded, diamond tufting and buttons, chrome
  arms, column, round base, footrest), floor reflections and contact shadows.
- Wall shelves with bottles and a trailing plant, monstera in a white pot, framed map, trolley with bottles.
- Vignette and a deterministic grain overlay (mulberry32 + hash, no Math.random).

## Camera
`render(t)` is a pure function of time. Eye travels (1.0, 1.35, -3.0) to (0.45, 1.3, -0.5) with distance eased by the
integral of a smoothstep speed profile (soft start and stop). Gimbal drift: lateral sway, tiny yaw, pitch and roll.

## Exports
See `/assets/renders/`. Command: headless Chrome with `--force-device-scale-factor=2 --window-size=W,H`
and `index.html?t=T&w=W&h=H`.
