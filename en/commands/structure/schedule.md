# IVO:SCHEDULE

> Opens the Structural palette on its Member Schedule tab, for tidying up schedule table cell text.

## How to Access

- **Ribbon:** Ingenevo Tools Tab → Structure Panel → Schedule button
- **Command Line:** `IVO:SCHEDULE`
- **Alias:** —

## How to Use

1. Run `IVO:SCHEDULE` — the **Structural** palette opens on its **Schedule** tab
2. In the drawing, choose what to work on:
   - **Click individual cells** inside the schedule table → only those cells are processed
   - **Select the table** without entering any cell → the whole table is processed (the header row is skipped)
3. Press one of the palette's four buttons:

| Button | What it does |
|:-------|:-------------|
| **Clean** | Tidies the selected cells' text into the standard format |
| **Copy** | Copies cell text to the clipboard **verbatim**, without cleaning |
| **Paste** | Pastes clipboard content into cells as-is |
| **Paste cleaned** | Pastes clipboard content while cleaning it |

4. The result appears in the palette's status line **and** on the command line, including the cell range actually processed

<!-- screenshot -->

## Tips & Notes

> [!WARNING]
> This command requires an **active license**. Run [IVO:LICENSE](en/commands/help/license.md) to activate yours.

> [!NOTE]
> This feature touches **cell text only**. Row height, text height, font, alignment, and the table's grid colours and lineweights are left completely alone.

> [!TIP]
> **Copy is always verbatim, on purpose.** If copying also cleaned, the clipboard would hold something different from what is on screen. What actually needs cleaning is the raw text coming **in** via paste — hence **Paste cleaned**, not "Copy cleaned".

> [!NOTE]
> Every action runs from a palette button, never from the command line. While a table cell is active, BricsCAD hands the keyboard to the cell editor — a typed command is not processed and can end up inside the cell. That is why there is only **one** command here: the one that opens the palette.

> [!TIP]
> The palette stays open until you close it, so you can move from one table to the next without running this command again.

## See Also

- [IVO:STRUCTURALPALETTE](en/commands/structure/structuralpalette.md) — open the Structural palette on its last active tab
- [IVO:SHOWSTRUCTURALPALETTE](en/commands/structure/showstructuralpalette.md) — show the Structural palette
