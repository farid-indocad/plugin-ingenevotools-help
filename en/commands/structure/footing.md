# IVO:FOOTING

> Draws footing outlines from the selected outer-face and centreline lines.

## How to Access

- **Ribbon:** — (no ribbon button)
- **Command Line:** `IVO:FOOTING`
- **Alias:** `IVO:FTG`

## How to Use

1. Open the **Structural** palette → **Footing** tab, and fill in the two offsets to use
2. In the drawing, select the outer-face and centreline lines that describe the footing
3. Run `IVO:FOOTING` or `IVO:FTG`
4. The footing is drawn immediately — **there is no prompt at all**
5. The success message **names the offsets actually used**:

```
[IngenevoTools] Footing created: 2 room(s) + 0 pocket(s), 24 segment(s) used,
                3 ignored (2 wrong colour, 1 not straight), 0 outside the ring.
                Offsets used: outer 300, inner 150.
```

<!-- screenshot -->

## Tips & Notes

> [!WARNING]
> This command requires an **active license**. Run [IVO:LICENSE](en/commands/help/license.md) to activate yours.

> [!NOTE]
> **This command asks nothing, and does not open the palette.** Both offsets come from the Structural palette's Footing tab, whose initial values come from settings — so it works even if you have never opened the palette.
>
> The palette is deliberately not shown: you run this on a selection you just made, and a palette appearing over the drawing at that moment is a good way to lose it.

> [!TIP]
> Because there is no prompt, **the success message is the only evidence on screen of which offsets were used.** Get into the habit of reading it — a footing drawn from a stale palette value looks exactly like one drawn from the right one.

> [!NOTE]
> The source lines are **not changed, moved, or deleted** — this command only adds. The whole result is a single undo step.

> [!NOTE]
> If either offset in the palette is invalid, the command refuses to run and shows the same error the palette's **Create** button would.

### When nothing is drawn

The command cancels itself and explains why, rather than going quiet:

| Message | What it means | What to do |
|:--------|:--------------|:-----------|
| `Ring not closed` | The perimeter still has gaps | **The dangling lines are made the active selection** — zoom to that selection to see where the gaps are |
| `Outer and inner lines disagree on which side is inward` | The outer-face and centreline lines point inward in opposite directions | Check the edge at the reported coordinate |
| `Not enough outer/inner lines to form a footing` | Fewer than three edges were formed | Make sure the selection covers the whole footing perimeter |
| `Layer "..." is locked` | The target layer is locked | Unlock it and run again |

> [!NOTE]
> If the source lines' Z values are not uniform, the footing is drawn at elevation **0** and you are told so.

> [!TIP]
> The **Footing** tab has no command of its own — open the Structural palette with [IVO:STRUCTURALPALETTE](en/commands/structure/structuralpalette.md) and click the tab.

## See Also

- [IVO:BOUNDARY](en/commands/structure/boundary.md) — the command this one was forked from, with fixed offsets
- [IVO:STRUCTURALPALETTE](en/commands/structure/structuralpalette.md) — open the palette where the footing offsets live
