# Shared Interface

## Top Bar

### Load Texture

Loads the trim sheet image the canvas displays and trims are drawn against. This is purely visual reference for laying out trims; it does not assign a material to anything in the scene.

### Assign Material

Captures whichever material is currently active in the Material Editor and stores it as this setup's Trim Material.

Any decal TrimKit creates afterward is automatically assigned this material, so placed geometry shows the correct texture immediately instead of coming in with a default material.

The button's label updates to show the name of the currently assigned material.

### Save Setup

Writes the current trims, mapping mode, loaded texture path, and assigned material name to a `.json` file.

Because the file format is shared between the 3ds Max and Blender versions of TrimKit, a setup saved in one program opens correctly in the other, with trims landing in exactly the same place on the texture.

### Load Setup

Loads a previously saved `.json` setup file, restoring its trims, mapping mode, texture, and material assignment into the current mode.

### Clear Setup

Removes all trims, the loaded texture, and the assigned material for the current mode, giving you a clean slate for starting a new trim sheet.

### Lock

A toggle that protects the current setup from accidental changes.

It's available both as a padlock button next to Add/Delete in the Trims list and as a small draggable padlock icon overlaid directly on the canvas, kept in sync with each other; drag the canvas icon to move it out of the way, or click it (without dragging) to toggle Lock.

While locked, trims can still be selected, but not added, deleted, moved, resized, or renamed.

Loading a Setup that already has trims in it locks it automatically, and Clear Setup unlocks it again once the setup is empty.

## Trims List

### Trim list

Shows every trim currently defined on the sheet. Double-click a name to rename it. Selecting a trim in the list also selects it on the canvas, and vice versa.

### Add

Creates a new trim rectangle on the canvas, a default-sized box you can then drag and resize, and adds it to the trim list.

### Delete

Removes the currently selected trim from both the list and the canvas.

## The Canvas

The canvas is where trims are actually drawn and edited, not just previewed.

- **Draw:** click and drag on empty canvas space to draw a new trim rectangle.
- **Move:** click and drag inside an existing trim to reposition it. The cursor becomes an open hand.
- **Resize:** hover over a trim's edge or corner until the cursor changes to a resize arrow, then drag to resize from that side or corner.

The canvas works even before a texture is loaded, showing a plain placeholder square so trims can still be laid out and saved ahead of time.

## Scale / Move / Tweaks

These controls operate on UVs that are already mapped onto a trim. They reposition or resize the mapped UVs without re-unwrapping anything.

### U Axis / V Axis

Toggle buttons that determine which axes a Scale operation affects.

Toggle one, both, or neither on before scaling to constrain the scale to horizontal only, vertical only, or both directions.

### Scale amount

Numeric field containing the scale factor applied when the Scale button is pressed.

### Scale pivot

Dropdown with the following options:

- Middle
- Bottom-Left
- Bottom-Right
- Top-Left
- Top-Right

This is the point the selected trim's UVs scale from.

### Scale

Applies the scale amount, along the enabled axes, from the chosen pivot, to the UVs currently mapped onto the selected trim.

### Move amount

Numeric field containing the distance moved when a Move button is pressed.

### U Move / V Move

Nudge the mapped UVs horizontally (U) or vertically (V) by the move amount.

### Rotate Mode

Dropdown with two options:

- **Stay in Trim:** rotates the UVs and re-fits them onto the selected trim's rectangle. In Decal Placer, this also stretches the UVs to fill the trim on both axes.
- **Standard:** just rotates the UVs in place, with no trim snapping or rescaling.

### Rotate -90 / Rotate 90

Rotates the selected trim's mapped UVs 90° counter-clockwise or clockwise, following whichever Rotate Mode is active.

### Flip Horizontal / Flip Vertical

Mirrors the mapped UVs left to right or top to bottom, in place.
