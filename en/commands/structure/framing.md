# IVO:FRAMING

> Draws a chain of columns and beams together, LINE-style: a column at every vertex, a beam on every segment.

## How to Access

- **Ribbon:** Ingenevo Tools Tab → Structure Panel → Framing button
- **Command Line:** `IVO:FRAMING`
- **Alias:** —

## How to Use

1. Run `IVO:FRAMING`
2. Click the first point — a column is placed there
3. Click the next point — a beam is drawn on the segment, and a column at the vertex
4. Keep clicking to extend the chain
5. Press **Enter** or **right-click** to finish

## Options / Parameters

The column and beam types come from the Structural palette's **Framing** tab, and can also be set under `IVO:SETTINGS` → **Structure**.

<!-- screenshot -->

## Tips & Notes

> [!WARNING]
> This command requires an **active license**. Run [IVO:LICENSE](en/commands/help/license.md) to activate yours.

> [!NOTE]
> It behaves like the LINE command — click points in sequence to form a chain. Columns land on every point, beams on every segment between them.

> [!TIP]
> If you only need columns, use [IVO:COLUMN](en/commands/structure/column.md). If you only need beams, use [IVO:BEAM](en/commands/structure/beam.md).

> [!TIP]
> To place columns on beams that already exist, use [IVO:GENCOLUMN](en/commands/structure/gencolumn.md) instead of redrawing them.

## See Also

- [IVO:COLUMN](en/commands/structure/column.md) — columns only
- [IVO:BEAM](en/commands/structure/beam.md) — beams only
- [IVO:GENCOLUMN](en/commands/structure/gencolumn.md) — columns at the ends of existing beams
