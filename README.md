# SILKSHIFT

**Own the skyline.** An original, responsive, 3D web-swinging endless runner through a procedurally generated neon city.

**Play:** https://SweeMingXx.github.io/silkshift/

## Controls

| Action | Keyboard | Mobile |
| --- | --- | --- |
| Change lane | Left / Right or A / D | Swipe left / right, or touch buttons |
| Swing | Up, W or Space | Swipe up or Swing button |
| Slide | Down or S | Swipe down or Slide button |
| Pause / resume | P or Escape | Pause / Resume buttons |
| Sound | M | Sound button |

Swing over pink barricades, slide below cyan gates, and change lanes around solid vehicles. Start with 3 lives. Gold shards are worth 25 points; cyan shields restore 1 life up to 3; pink magnets attract shards for 8 seconds. Speed increases from 19 to 36 world units/second. Districts change every 500 m. Best score and sound preference persist locally when browser storage is available.

## Implementation

- Native WebGL with ANGLE instancing; no JavaScript runtime libraries, CDN scripts or build step.
- Procedural city, hero, obstacles, lighting, silk lines, particles and geometry. No external art assets.
- Responsive UI, optional synthesised sound, reduced-motion-aware decorative animation, help dialog, keyboard focus, pause on focus loss, recoverable graphics error messages.
- Optional Google Fonts with local system fallbacks; gameplay does not depend on font loading.
- Five-minute simulation and desktop/mobile browser checks in GitHub Actions. Screenshots are retained as workflow artifacts.
- GitHub Pages deployment runs only after verification succeeds.

## Local development

Serve the repository, for example `python3 -m http.server 8080`, then open `http://localhost:8080`.

For browser checks, run `npm install`, `npx playwright install chromium`, start the local server, then `npm test`. To test another deployment, set `SITE_URL` to its URL without a trailing slash.

## Notes

WebGL with instancing and JavaScript are required. This is a single-player game, with no backend, telemetry, account system or online leaderboard. Scores are browser-local. On devices with limited graphics memory, close other graphics-heavy tabs.

SILKSHIFT is an original game, not affiliated with Marvel, Sony or Subway Surfers. It does not use their characters, names as game branding, logos, music, or artwork.
