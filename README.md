# Solar System Animation

An interactive, fully CSS/JS solar system — no images, no external libraries, no build step. Open `index.html` in any browser.

## Features

- All 8 planets + Moon + Sun — drawn with pure CSS radial gradients
- Saturn's rings using CSS `::before` pseudo-element
- Animated starfield on `<canvas>` with twinkling effect
- 200-dot asteroid belt between Mars and Jupiter
- Orbit rings drawn in CSS, each with real relative orbital periods
- Speed control slider (0.1× to 5×)
- Hover any planet or the sun for fact tooltip (diameter, day length, year, moons)

## Usage

Just open `index.html` in Chrome, Firefox, Edge, or Safari. No server needed.

## How it works

| Feature | Technique |
|---------|-----------|
| Planet orbits | CSS `@keyframes spin` + `animation-duration` per orbit |
| Planet appearance | CSS `radial-gradient` — no images |
| Saturn ring | `::before` pseudo-element with `border-radius: 50%` + `rotateX(70deg)` |
| Starfield | HTML5 `<canvas>` — 700 stars with sine-wave twinkling |
| Asteroid belt | 200 positioned `<div>` dots scattered around a circular `<div>` |
| Speed control | JS reads slider, recalculates `animation-duration` per element |
| Tooltips | `data-name` + `data-info` attributes, positioned via `mousemove` |

## Original source

Rebuilt from `solarsy.html` and `solarssystem.html` in `archive/Web_Pages/` — both versions used `C:\Users\dhruv\Desktop\HTML_PICS\` absolute image paths that broke on any other machine. This version works everywhere with zero file dependencies.
