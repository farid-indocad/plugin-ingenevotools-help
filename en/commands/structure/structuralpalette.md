# IVO:STRUCTURALPALETTE

> Shows or hides the Structural palette, whichever it currently is not.

## How to Access

- **Ribbon:** Ingenevo Tools Tab → Structure Panel → Structural Palette button
- **Command Line:** `IVO:STRUCTURALPALETTE`
- **Alias:** —

## How to Use

1. Run `IVO:STRUCTURALPALETTE`
2. If the palette is hidden, it is shown
3. If the palette is showing, it is hidden
4. The last active tab is preserved. The palette has **four** tabs:

| Tab | What it holds |
|:----|:--------------|
| **Framing** | Column and beam types for [IVO:FRAMING](en/commands/structure/framing.md), [IVO:COLUMN](en/commands/structure/column.md), [IVO:BEAM](en/commands/structure/beam.md) |
| **Bracing** | Bracing types for [IVO:BRACING](en/commands/structure/bracing.md) and [IVO:DIM2BRACING](en/commands/structure/dim2bracing.md) |
| **Member Schedule** | Schedule table cleanup buttons — see [IVO:SCHEDULE](en/commands/structure/schedule.md) |
| **Footing** | The two offsets used by [IVO:FOOTING](en/commands/structure/footing.md) |

<!-- screenshot -->

## Tips & Notes

> [!WARNING]
> This command requires an **active license**. Run [IVO:LICENSE](en/commands/help/license.md) to activate yours.

> [!NOTE]
> The **Footing** tab has no command of its own — the only way to reach it is to open this palette and click the tab.

> [!TIP]
> Use this as a quick toggle. To show or hide explicitly, use [IVO:SHOWSTRUCTURALPALETTE](en/commands/structure/showstructuralpalette.md) or [IVO:HIDESTRUCTURALPALETTE](en/commands/structure/hidestructuralpalette.md).

## See Also

- [IVO:SHOWSTRUCTURALPALETTE](en/commands/structure/showstructuralpalette.md) — show the palette explicitly
- [IVO:HIDESTRUCTURALPALETTE](en/commands/structure/hidestructuralpalette.md) — hide the palette explicitly
