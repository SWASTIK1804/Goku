# Ultra Instinct Reveal

A single-page interactive hero section that reveals a hidden image as the cursor moves across the screen, built with vanilla JS and the Canvas API — no dependencies, no build step.

## Demo

Move your cursor across the hero area to "power up" the base image into its transformed state, guided by a soft radial trail that follows the pointer.

## Features

- **Cursor-driven reveal** — a smoothed trail of circles masks a second image over the base layer using canvas composite operations
- **Responsive layout** — fluid typography and repositioned content on smaller screens (breakpoint at `680px`)
- **Touch support** — reveal effect also responds to `touchmove`
- **Zero dependencies** — pure HTML, CSS, and JavaScript; Google Fonts loaded via CDN
- **High-DPI aware** — canvas scales correctly on Retina/HiDPI displays

## Tech Stack

| Layer | Details |
|---|---|
| Markup/Styling | HTML5, CSS3 (custom properties, `clip-path`, gradients) |
| Interactivity | Vanilla JavaScript, `requestAnimationFrame` render loop |
| Rendering | HTML5 Canvas (`globalCompositeOperation` masking) |
| Fonts | Bangers, Bebas Neue, Luckiest Guy, Cormorant Garamond (Google Fonts) |

## Getting Started

1. Clone or download this repository
2. Place two same-scene images in the project root:
   - `2.jpg` — base image (always visible underneath)
   - `1.jpg` — revealed image (shown inside the cursor trail)
3. Open `goku-ultra-instinct-reveal.html` in any modern browser — no server or build tools required

```bash
git clone <repo-url>
cd ultra-instinct-reveal
open goku-ultra-instinct-reveal.html
```

## Customization

| What | Where |
|---|---|
| Trail length / smoothing | `TRAIL_LENGTH` and the `0.13` lerp factor in `draw()` |
| Reveal radius | `HEAD_RADIUS` |
| Overlay darkness | `OVERLAY` constant |
| Copy & headings | `.left` / `.right` blocks in the HTML |
| Color palette | CSS custom values in `<style>` (orange `#FF8C1A`, blue `#2E62D9`) |

## Project Structure

```
.
├── goku-ultra-instinct-reveal.html   # markup, styles, and canvas logic
├── 1.jpg                             # revealed-state image
└── 2.jpg                             # base-state image
```

## Notes

This is a fan-made visual effect demo. The character artwork is used for illustrative/portfolio purposes only — swap in your own images to reuse the effect for other projects.

## License

MIT — feel free to adapt the reveal effect for your own use.
