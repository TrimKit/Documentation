![TrimKit](assets/trimkit-logo-wide.png){ width="480" }

Trim sheet texturing, decal placement, and edge decals for 3ds Max and Blender.

TrimKit is a unified texturing tool that speeds up trim sheet workflows. It brings three tools into a single window with a shared canvas and control set.

## Modes

- **[Trim](trim-mode/)** — Unwrap and snap face selections onto a trim sheet.
- **[Decal Placer](decal-placer/)** — Click to place standalone flat or surface-wrapping decals.
- **[Edge Decal](edge-decal/)** — Generate mitered decal strips along selected edge loops.

## Shared Features

All three modes share:

- A trim sheet canvas to load a texture and draw or edit trim rectangles on it
- A trim list for adding, deleting, and renaming trims
- Scale / Move / Tweaks controls for adjusting UVs already mapped onto a trim
- Save / Load / Clear Setup

Setups can be saved to and loaded from a JSON file. Because the tool exists as both a 3ds Max script and a Blender add-on, the same setup file opens correctly in either program.
