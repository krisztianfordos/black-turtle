# Reference: riso-windowseat "Window Seat" (train journey in code)

## Access status
- Reddit blocked every route: WebFetch refused reddit.com and old.reddit.com; curl on the `.json` endpoint returned 403.
- The post body was not read. The title comes from https://trendshift.io/repositories/255296, which lists the post under the repo's social mentions. The link is probable, not confirmed. "Opus 5.5" in the title is unverified; the repo says only "Claude Code".

## 1. The post
- Title (per Trendshift): "Opus 5.5 creates a train journey drawn entirely in JavaScript".
- Medium: Canvas 2D plus Web Audio, one HTML file, no libraries.
- Result (per repo): "Window Seat", 78 s. A night train seen through one fixed window with a glass of water on the sill. Passages: platform, fields, bridge, tunnel, city, overtaking train, fireworks, fog, dawn viaduct, rain, rainbow halt. Risograph halftone look, 1080 x 1080, 30 fps.

## 2. The repo
- sevenevesai/riso-windowseat, https://github.com/sevenevesai/riso-windowseat (created 2026-09-22, 292 stars).
- Licence: MIT. Embedded piano samples are CC BY 3.0 (Salamander Grand Piano V3), so attribution is required.
- Structure: `films/` (each film is an `index.html` plus `FILM.md`), `prints/`, `docs/`, `studies/`, `tools/` (Node render and verify scripts), `.claude/` (skills).
- Runtime dependencies: none. `tools/` has dev-only npm dependencies for offline MP4 rendering.
- `films/window-seat/index.html` is 3071 lines and 5.5 MB, mostly base64 piano samples.

## 3. Technique
- **Plates, not RGB.** Each object paints alpha into four plate canvases (yellow, pink, blue, indigo). `compose()` screens each plate per pixel against a rotated dot threshold tile with mottling, then multiplies ink onto a baked paper bitmap.
- **No 3D.** Perspective is 2D parallax: screen x = 540 + (X - s) * p, with s the distance travelled. Ground boundaries fan out below the horizon.
- **Clock.** s(t) is the analytic integral of a piecewise smoothstep speed profile. The same s(t) drives every layer, and its acceleration drives a damped pendulum for the water.
- **Loop.** `tick(now)` calls `render(t)`. `render` is a pure function of t, so scrubbing and playback share one path. Scene switches happen while the window is fully covered.
- **Performance.** Canvas is fixed at 1080 and shown at 720 CSS px. Paper, screens and scene bitmaps are built once at load. The per-frame cost is the full 1080 x 1080 x 4-plate pixel loop in `compose()`. MP4s are rendered offline.

Key snippets (`films/window-seat/index.html`):

```js
function S(t) {                       // distance: integral of smoothstep speed (~line 1129)
  if (t <= 0) return 0;
  for (const g of VSEG.segs) {
    if (t <= g.t1) { const L = g.t1 - g.t0, u = (t - g.t0) / L;
      return g.s0 + L * (g.v0 * u + (g.v1 - g.v0) * smI(u)); }
  }
  return VSEG.end + VK[VK.length - 1][1] * (t - VK[VK.length - 1][0]);
}
const sxp = (X, p, s) => 540 + (X - s) * p;   // parallax projection
```

```js
if (a[j * 4 + 3] > th[j]) { o[i] *= mr; o[i + 1] *= mg; o[i + 2] *= mb; }   // compose(): ink vs threshold
```

## 4. Reuse for a slow gimbal push-in into a barbershop interior
**Copy:**
- The plate pipeline (`PL`/`PG`, `put`/`add`/`knock`, `buildScreen`/`buildThr`, `compose`) for the print look. Keep dot screens anchored to the canvas, or texture crawls.
- Deterministic rng (`mulberry32` plus `hash`), never `Math.random` and never state carried between frames.
- The pure `render(t)` / `seek(t)` / rAF `tick` structure.
- `camera()`, `plane()` and `polygon()` from `tools/lib/visual-kit.mjs` (embedded as `Space`). Project world-space geometry each frame; never bilerp in screen space.
- The distance-integral easing, so position, speed and acceleration agree.

**Adapt:**
- Window Seat has no real camera. A push-in needs `Space.camera` with `eye` moving forward along z, projecting every layer through it.
- Per `docs/scene-space.md`: transform geometry, never scale a screened bitmap to fake a dolly. Cache static plates per camera. Interpolate zoom in `1/z` or `log z`. Keep dot pitch fixed.
- Build chairs, mirror, pole and window in world space with `plane()`, and resolve depth order explicitly.
- Frame the hero moment by projected bounds, not by eye.
- The repo has no interior example, so the camera work is new.

**Caveat:** Without the post, the model used and the reception are unverified.
