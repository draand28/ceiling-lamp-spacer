# Ceiling lamp cable spacer

Spacer disc that pushes a 12 cm ceiling lamp canopy 30 mm away from the ceiling,
so the wires and connectors inside the canopy have room.

Modeled with SolidCraft (solidcraft-cli, script `build.json`).

## Dimensions

| Parameter | Value | Note |
|---|---|---|
| D_OUT | 180 mm | outer diameter |
| H | 30 mm | overall height |
| T | 1 mm | wall thickness (side, top, bottom) |
| D_HOLE | 110 mm | opening in the ceiling-side face |
| W_RIB | 10 mm | solid rib across the full diameter |

- Cavity: 178 mm dia x 28 mm, open towards the ceiling through the 110 mm hole.
- Lamp-side face: closed (1 mm).
- Rib: 10 mm wide, full diameter, 29 mm tall, solid, arc ends flush with the
  outer wall, top flush with the ceiling-side face. Built as a box intersected
  with the outer cylinder, so it fuses to the wall without slivers.
- Volume 108 cm3, mass about 139 g at default material density.

## Files

- `build.json` - SolidCraft command script, edit parameters here and re-run
- `spacer.solidcraft` - SolidCraft design file
- `spacer.step` - STEP export
- `spacer.stl` - STL export for slicing
- `v-iso.png`, `v-bottom.png`, `v-section.png` - views

## Rebuild

```
solidcraft-cli run build.json --out spacer.step --save spacer.solidcraft
solidcraft-cli run --in spacer.solidcraft --out spacer.stl
```

## Printing

Print with the closed lamp-side face on the bed: no support needed, the rib
stands on the floor and the opening faces up.
