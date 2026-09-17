# Decal Placer

Decal Placer creates new decal geometry, small overlay meshes for details like bolts, stickers, grime, or trim strips, rather than mapping UVs on existing faces.

## Place Decal

An interactive, click-to-place tool.

Click anywhere in the viewport and a decal is placed at that point, oriented to the surface under the cursor, using the current **Size, Rotation, Push, and Wrap** settings, each read live so you can adjust the fields while placing.

If the click misses all geometry, the decal falls back to a world-aligned plane facing the current view.

## Assign Decal to Selection

Instead of placing a new decal by clicking, this unwraps and maps the currently selected faces directly onto the active trim, always in Fit mode.

Useful when you want a decal-style trim mapping applied to specific existing geometry rather than a separate floating decal object.

## Size

Sets how big the placed decal is, proportional to the selected trim's own footprint.

It's normalized against the largest trim on the sheet, so the same Size value produces visually consistent results across differently shaped trims.

## Rotation

Rotates the decal around its placement normal before it's placed.

## Push

Lifts the finished decal slightly off the surface it sits on, to prevent it from z-fighting or flickering against the base mesh.

It's applied as a Push/Displace modifier on the decal object rather than baked into its vertices, so it can be tweaked non-destructively after placement.

## Wrap

Toggle with two states:

- **On:** the decal is built to follow the curvature of the surface it's placed on, rather than staying perfectly flat.
- **Off:** the decal is a flat quad, oriented to the surface but not bent to match it.
