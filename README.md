# Painting Rooms

Walkable, path-traced clay models of the rooms inside paintings, rebuilt in metres by treating each canvas as a photograph.

**First room: Caravaggio, *The Calling of Saint Matthew* (1599-1600, 322 x 340 cm).**

Live site: https://mbayen-dev.github.io/painting-rooms/ (home page with all rooms)

Rooms: `calling.html`, `las-meninas.html`, `folies-bergere.html`, `daughters-of-boit.html`.

## How it works
- The camera is solved from the painting: horizon at row 513 of 1197, focal length 1110 px (from the 45 degree shutter's distance point), eye height 1.52 m.
- Each figure joint and piece of furniture is back-projected from its pixels onto the floor plane or back wall.
- Sanity checks that were not fitted: stool seat 0.51 m, table top about 0.72 m, standing figure 1.70 m.
- Rendering uses three.js, with an optional progressive path tracer (three-gpu-pathtracer) for bounce light and soft shadows.

## Confidence
- Measured: figure floor positions, table, stool, window, shutter.
- Inferred: back wall depth, left wall, light direction.
- Invented: hidden bodies, ceiling, floor extent, the open right side.
- Open: the painted dark wedge on the wall is not reproduced.

**Second room: Velazquez, *Las Meninas* (1656, 318 x 276 cm)** at `las-meninas.html`, with four theories of how it was painted: as painted, royals at the viewer's position, the mirror reflecting the canvas (Snyder and Cohen), and painted from a large mirror. The viewing distance is an adjustable assumption because one vanishing point cannot fix it.

**Third room: Manet, *A Bar at the Folies-Bergere* (1882, 96 x 130 cm)** at `folies-bergere.html`. Four readings of the mirror: as painted, a real flat mirror with the viewer in the middle, the barmaid moved between two moments, and a single off-axis viewpoint. A slider sets how far the glass stands behind her, the main unknown.

**Fourth room: Sargent, *The Daughters of Edward Darley Boit* (1882, 222 x 223 cm)** at `daughters-of-boit.html`. One fixed room and three movable light sources. A tonal-match score and a "test all seven combinations" button rank which on/off combination best reproduces the painting's pattern of light.

All painting images are public domain.
