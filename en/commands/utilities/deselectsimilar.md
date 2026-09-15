# IVO:DESELECTSIMILAR

> Removes entities similar to the picked one from the current selection.

## How to Access

- **Ribbon:** Ingenevo Tools Tab → Utilities Panel → Deselect Similar button
- **Command Line:** `IVO:DESELECTSIMILAR`
- **Alias:** —

## How to Use

1. Make a selection in the drawing
2. Run `IVO:DESELECTSIMILAR`
3. Pick a reference entity
4. Entities similar to it are removed from the selection; the rest stay selected

<!-- screenshot -->

## Tips & Notes

> [!WARNING]
> This command requires an **active license**. Run [IVO:LICENSE](en/commands/help/license.md) to activate yours.

> [!TIP]
> Useful for "everything except this" selections: select broadly first, then subtract the categories you do not want.

## See Also

- [IVO:SELECTSIMILARSPECIFIED](en/commands/utilities/selectsimilarspecified.md) — select similar entities by filter
- [IVO:CLEANUP](en/commands/utilities/cleanup.md) — filter and highlight by a saved preset
