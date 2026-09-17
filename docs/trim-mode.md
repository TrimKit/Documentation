# Trim Mode

Trim mode maps an existing face selection onto a trim you already have on the sheet. It's the general-purpose tool for applying a trim to a set of faces.

## Mapping Mode

Dropdown with two options: **Fit** and **Preserve**.

### Fit

Stretches the unwrapped island to fill the selected trim exactly, using all of the trim's space regardless of the island's own proportions.

### Preserve

Keeps the island's real-world proportions intact and fits it into the trim without distorting its aspect ratio.

## Selected Trim

Unwraps the selected faces and maps them onto whichever trim is currently selected in the trim list, using the active Mapping Mode.

### How It Works

TrimKit first tries a quad-grid layout: if every face in the selection is a quad, it lays them out on a shared grid based on real-world edge lengths, so straight strips stay straight and closed loops (like a ring around a cylinder) unwrap as one clean, correctly-cut strip.

If the selection isn't a clean all-quad island, it falls back to a rigid unfold, walking the selected faces and flattening each one by rotating it about the edge it shares with its already-placed neighbor, similar to unfolding a papercraft model.

The result is then oriented and fit or preserved onto the trim.

## Auto Trim

Automatically picks the best-fitting trim for each selected face, rather than requiring you to pick one from the list first.

### How It Works

The selection is first split into islands at UV seams and material boundaries, the same way an artist would naturally think about where a trim sheet's texture should break.

Each island is unwrapped, then tested against every trim on the sheet; whichever trim produces the least stretching, comparing the island's proportions straight-on and rotated 90 degrees, is the one it's mapped onto, using the current Mapping Mode.

This means one Auto Trim click can correctly texture a shape made of multiple materially different parts, such as a barred window sitting on a wall, in a single pass.
