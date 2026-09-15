# IVO:CHANGEBASEPOINT

> Changes a block definition's base point while every existing instance stays visually in place.

## How to Access

- **Ribbon:** Ingenevo Tools Tab → Utilities Panel → Change Base Point button
- **Command Line:** `IVO:CHANGEBASEPOINT`
- **Alias:** —

## How to Use

1. Run `IVO:CHANGEBASEPOINT`
2. Select the block reference whose base point you want to change
3. Pick the new base point
4. The base point moves, but the block's geometry stays exactly where it appears on screen

<!-- screenshot -->

## Tips & Notes

> [!WARNING]
> This command requires an **active license**. Run [IVO:LICENSE](en/commands/help/license.md) to activate yours.

> [!IMPORTANT]
> This changes the **block definition**, not one instance. Every instance of that block in the drawing is affected.

> [!TIP]
> Useful when a block was defined with an awkward base point — it makes future insertions snap where you expect, without redrawing anything.

## See Also

- [IVO:REPLACEBLOCK](en/commands/utilities/replaceblock.md) — swap block instances for another block
- [IVO:INITIALBLOCK](en/commands/utilities/initialblock.md) — normalize objects before defining a block
