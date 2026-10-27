# Painting Rooms

Walkable, path-traced clay models of the rooms inside paintings, rebuilt in metres by treating each canvas as a photograph.

**First room: Caravaggio, *The Calling of Saint Matthew* (1599-1600, 322 x 340 cm).**

Live page: https://mbayen-dev.github.io/painting-rooms/

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

The painting image is public domain. Next planned room: Velazquez, *Las Meninas*.
