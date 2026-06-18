# Color Cascade

A tiny, dependency-free reflex game that runs in a single HTML file. Colored
tiles fall from the top of the playfield — tap (or press) the button matching
the **lowest** tile to pop it before it reaches the bottom. The longer you
survive, the faster they fall.

## Play

Open [`index.html`](index.html) in any modern browser — that's it. There's no
build step, no server, and no dependencies.

## How to play

- Four colored tiles fall: **red**, **blue**, **green**, and **yellow**.
- Pop the **lowest** tile by hitting its matching color.
- A tile reaching the bottom, or a wrong tap, costs you a life.
- You start with **3 lives**. Each successful pop speeds the game up.
- Your best score is saved locally in the browser.

### Controls

| Input            | Action        |
| ---------------- | ------------- |
| On-screen button | Pop that color |
| `R` / `←`        | Red           |
| `B` / `↑`        | Blue          |
| `G` / `↓`        | Green         |
| `Y` / `→`        | Yellow        |
| `Space` / `Enter`| Start / restart |

## Tech notes

Everything — markup, styles, game loop, and sound — lives in
[`index.html`](index.html). Tiles animate via `requestAnimationFrame`, sound
effects are generated on the fly with the Web Audio API (no audio files), and
your high score persists through `localStorage`.
