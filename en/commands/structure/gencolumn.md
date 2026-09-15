# IVO:GENCOLUMN

> Places a column at both ends of every selected beam, keeping the beams.

## How to Access

- **Ribbon:** — (no ribbon button, deliberately)
- **Command Line:** `IVO:GENCOLUMN`
- **Alias:** `IVO:GC`

## How to Use

1. Select beams that are already drawn (a selection made beforehand is honoured)
2. Run `IVO:GENCOLUMN` or `IVO:GC`
3. Columns are placed at **both ends** of every selected beam; the beams themselves are left intact
4. The command line reports the result:

```
[GenColumn] Created 14 "H 200x100" column(s) from 9 beam(s), 3 point(s) already had one, 0 failed.
```

<!-- screenshot -->

## Tips & Notes

> [!WARNING]
> This command requires an **active license**. Run [IVO:LICENSE](en/commands/help/license.md) to activate yours.

> [!NOTE]
> Beam ends **less than one drawing unit apart** count as the same point and get **one** column, not two stacked on top of each other.

> [!NOTE]
> Each column faces the way its own beam runs. Where several beams meet at one point at different angles, the column's angle is taken from the **longest** beam, and the command tells you how many points that happened at.

> [!TIP]
> The column type used is the one active on the Structural palette's **Framing** tab — the same one [IVO:COLUMN](en/commands/structure/column.md) uses. This command never asks.

> [!NOTE]
> **This command deliberately has no ribbon button.** A ribbon button dispatches through a path that drops the pre-selection, and this whole command is built around a selection you made first. The button would make it unusable.

> [!TIP]
> Points that already have a column do not get a second one — they are reported separately as `already had one`. Running this twice over the same beams is therefore safe.

## See Also

- [IVO:COLUMN](en/commands/structure/column.md) — place columns by picking points one at a time
- [IVO:FRAMING](en/commands/structure/framing.md) — draw a chain of columns and beams together
- [IVO:BEAM](en/commands/structure/beam.md) — draw beams only
