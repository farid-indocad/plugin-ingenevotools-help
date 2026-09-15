# IVO:ADDLAYOUT

> Adds layouts for the ViewFrame blocks you select, without deleting any existing layout.

## How to Access

- **Ribbon:** Ingenevo Tools Tab → Sheet Manager Panel → Add Layout button
- **Command Line:** `IVO:ADDLAYOUT`
- **Alias:** `IVO:ADL`

## How to Use

1. Select the **ViewFrame** blocks you want layouts for (a selection made beforehand is honoured)
2. Run `IVO:ADDLAYOUT` or `IVO:ADL`
3. A progress window runs while the layouts are built — it has a **Cancel** button
4. The command line reports how many layouts were created, and how many frames each ViewFrame type claimed:

```
[IngenevoTools] Total Layouts Created: 6.
[IngenevoTools] Viewframe types — A1 Plan: 4, A3 Detail: 2.
```

<!-- screenshot -->

## Tips & Notes

> [!WARNING]
> This command requires an **active license**. Run [IVO:LICENSE](en/commands/help/license.md) to activate yours.

> [!NOTE]
> **There is no confirmation, and none is needed** — this command only adds, never deletes. If you press Cancel partway through, the layouts already created are **kept**.

> [!TIP]
> It does not ask for paper size, prefix, or title block. All of those are read from `IVO:SETTINGS` → **Sheet Manager**.

> [!IMPORTANT]
> The **Viewframe types** line is worth reading every time. A ViewFrame type pattern that is too loose does not fail — it swallows another type's frames and produces sheets at the wrong scale. The run looks correct until somebody opens a sheet and reads its viewport. These per-type counts are the only sign on screen.

> [!TIP]
> To rebuild **every** layout from scratch, use [IVO:CREATELAYOUT](en/commands/sheet-manager/createlayout.md) — but note that it deletes all existing layouts first.

## See Also

- [IVO:CREATELAYOUT](en/commands/sheet-manager/createlayout.md) — rebuild every layout from scratch
- [IVO:RENUMBERVIEWFRAME](en/commands/sheet-manager/renumberviewframe.md) — renumber ViewFrames before building layouts
- [IVO:SORTLAYOUT](en/commands/sheet-manager/sortlayout.md) — sort the layout tabs
