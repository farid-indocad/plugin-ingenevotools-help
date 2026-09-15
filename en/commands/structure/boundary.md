# IVO:BOUNDARY

> Rebuilds one closed white polyline from the cyan (outer face) and yellow (wall centreline) lines.

## How to Access

- **Ribbon:** — (no ribbon button)
- **Command Line:** `IVO:BOUNDARY`
- **Alias:** `IVO:BND`

## How to Use

1. Select the lines describing the room perimeter (a selection made beforehand is honoured):
   - **Cyan** (ACI 4) — the outer face of the wall
   - **Yellow** (ACI 2) — the wall centreline
2. Run `IVO:BOUNDARY` or `IVO:BND`
3. The boundary is drawn on the **inward** side — there is no prompt
4. The command line reports what happened:

```
[IngenevoTools] Boundary created: 3 room(s) + 1 pocket(s), 28 segment(s) used,
                6 ignored (4 wrong colour, 2 not straight), 0 outside the ring.
```

<!-- screenshot -->

## Tips & Notes

> [!WARNING]
> This command requires an **active license**. Run [IVO:LICENSE](en/commands/help/license.md) to activate yours.

> [!NOTE]
> The source lines' colour is **not just a visual marker — it is what sets the distance.** Cyan means the outer wall face; yellow means the centreline, which sits half that distance from the boundary. Lines of any other colour are ignored and counted as `wrong colour`.

> [!NOTE]
> This command **only adds**. The source lines are not changed, moved, or deleted. The whole result is a single undo step.

> [!TIP]
> The result is a closed polyline on the **BOUNDARY** layer — created automatically if it does not exist, with the entity colour forced to white so the result stays white even if the layer already exists in another colour.

> [!NOTE]
> If the source lines' Z values are not uniform, the boundary is drawn at elevation **0** and you are told so. If they are uniform, the elevation follows the source.

### When nothing is drawn

The command cancels itself and explains why, rather than going quiet:

| Message | What it means | What to do |
|:--------|:--------------|:-----------|
| `Ring not closed` | The perimeter still has gaps | **The dangling lines are made the active selection** — zoom to it to see where the gaps are. The first gap's coordinate is also named |
| `Cyan and yellow disagree on which side is inward` | Cyan and yellow point inward in opposite directions at some edge | Check the edge at the reported coordinate |
| `Not enough cyan/yellow lines` | Fewer than three edges were formed | Make sure the selection really covers the room perimeter |
| `Layer BOUNDARY is locked` | The target layer is locked | Unlock the `BOUNDARY` layer |

> [!TIP]
> Ignored lines and edges outside the ring are **counted and reported, not treated as errors** — the boundary is still drawn. Those numbers are how you confirm nothing was left out without noticing.

### IVO:BOUNDARYDUMP — finding out why it failed

When a drawing keeps refusing to close, `IVO:BOUNDARYDUMP` writes a diagnostic report for the same selection **without drawing anything**: which segments were read, how many edges were formed, where every gap is, and the spacing actually measured between parallel cyan and yellow lines.

1. Select the same lines that `IVO:BOUNDARY` failed on
2. Run `IVO:BOUNDARYDUMP`
3. The command line names the report file's location

> [!TIP]
> That report file is the most useful thing to send the Ingenevo team when a drawing will not process.

## See Also

- [IVO:FOOTING](en/commands/structure/footing.md) — a fork of this command with two freely configurable offsets
