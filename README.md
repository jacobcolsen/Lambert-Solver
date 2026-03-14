# Lambert Solver — Interactive Orbital Mechanics

An interactive, educational Lambert transfer solver visualized in a single self-contained HTML file. No dependencies, no build step — just open in a browser.

## What is Lambert's Problem?

Given two position vectors and a time of flight, Lambert's problem finds the unique orbit connecting them. It is the core computation behind interplanetary trajectory design, orbital rendezvous, and satellite transfer maneuvers.

## Features

- **Earth-centered 2D visualization** with real globe texture and to-scale Moon
- **Universal-variable Lambert solver** (Bate/Mueller/White formulation)
- **Interactive satellites** — drag to reposition, time-of-flight slider for live recomputation
- **Transfer orbit visualization** with ΔV burn vectors
- **Step-by-step math walkthrough** showing each Newton-Raphson iteration
- **ΔV vs ToF curve** — visualize the full tradeoff space and find the minimum-energy transfer
- **Spacecraft animation** along the transfer arc
- **Hohmann transfer detection** with callout when the solution converges to minimum energy

## Usage

1. Clone the repo
2. Open `lambert_solver.html` in any modern browser
3. No server required — runs entirely client-side

```bash
git clone https://github.com/jacobcolsen/Lambert-Solver.git
cd Lambert-Solver
open index.html
```

## Controls

| Input | Action |
|-------|--------|
| Scroll wheel | Zoom toward cursor |
| Click + drag | Pan |
| Drag satellite | Reposition on orbit, recomputes transfer |
| ToF slider | Adjust time of flight, reshapes transfer ellipse |
| HOHMANN button | Snap to minimum-energy Hohmann transfer |
| RESET VIEW | Return to default zoom/pan |

## Physics Reference

| Quantity | Value Used |
|----------|-----------|
| Earth GM (μ) | 3.986004418 × 10⁵ km³/s² |
| Earth radius | 6,371 km |
| Moon semi-major axis | 384,400 km |
| Moon eccentricity | 0.0549 |
| Moon radius | 1,737 km |

## Development Phases

The project is built in six incremental phases, each tested independently:

| Phase | Description |
|-------|-------------|
| 1 | Canvas foundation — Earth, orbits, satellites, UI shell |
| 2 | Lambert solver core — universal variable algorithm, Hohmann validation |
| 3 | Transfer visualization — ellipse, ΔV vectors, orbit parameter table |
| 4 | Interactivity — draggable satellites, live ToF slider |
| 5 | Math & education panels — step-by-step solver, tooltips, ΔV vs ToF chart |
| 6 | Animation & polish — spacecraft animation, Hohmann detection, final UX |

See `phase_prompts.txt` for the implementation prompts for each phase.

## Files

```
index.html            — main application (single file, self-contained)
earth top view.jpg    — Earth top-down texture (NASA Blue Marble)
moon.jpg              — Moon top-down texture
phase_prompts.txt     — development phase prompts
```

## License

MIT
