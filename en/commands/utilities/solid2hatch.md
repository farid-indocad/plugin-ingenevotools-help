# IVO:SOLID2HATCH

> Converts selected 2D SOLID objects into SOLID-pattern hatches, keeping colour and layer.

## How to Access

- **Ribbon:** Ingenevo Tools Tab → Utilities Panel → Solid2Hatch button
- **Command Line:** `IVO:SOLID2HATCH`
- **Alias:** `IVO:S2H`

## How to Use

1. Run `IVO:SOLID2HATCH` or `IVO:S2H`
2. Select one or more SOLID objects (2D filled quads)
3. Press **Enter** to confirm
4. Each SOLID is replaced by a SOLID-pattern hatch — **the original SOLID is deleted**
5. The original's colour and layer are preserved

<!-- screenshot -->

## Tips & Notes

> [!WARNING]
> This command requires an **active license**. Run [IVO:LICENSE](en/commands/help/license.md) to activate yours.

> [!TIP]
> The whole conversion is a **single undo step**. One `U` brings back every deleted SOLID at once.

> [!NOTE]
> This works on 2D SOLID objects only, not 3D solids. 2D SOLIDs usually come from the native SOLID command or from importing older formats.

> [!TIP]
> Converting to hatch makes editing easier — a hatch boundary is far simpler to modify than a 2D SOLID.

## See Also

- [IVO:SAFEEXPLODE](en/commands/utilities/safeexplode.md) — explode a block one level, safely
