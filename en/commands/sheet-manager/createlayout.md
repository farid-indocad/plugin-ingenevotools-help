# IVO:CREATELAYOUT

> Deletes **all** existing layouts, then rebuilds them from the ViewFrame blocks in model space.

## How to Access

- **Ribbon:** Ingenevo Tools Tab → Sheet Manager Panel → Create Layout button
- **Command Line:** `IVO:CREATELAYOUT`
- **Alias:** `IVO:CRL`

## How to Use

1. Make sure the **ViewFrame** blocks are drawn in model space
2. Run `IVO:CREATELAYOUT` or `IVO:CRL`
3. A confirmation prompt appears that **shows the settings about to be used**:

```
Create layouts — Paper: A3, Prefix: SH-, Additional: 2.
Delete all existing layouts and continue? [Yes/No] <Yes>:
```

4. Press **Enter** to continue (default **Yes**), or answer **No** to cancel
5. A progress window runs while the layouts are built — it has a **Cancel** button
6. When finished, the command line reports the paper size, prefix, additional count, and total layouts created

<!-- screenshot -->

## Tips & Notes

> [!WARNING]
> This command requires an **active license**. Run [IVO:LICENSE](en/commands/help/license.md) to activate yours.

> [!WARNING]
> This command **deletes every existing layout** before creating the new ones. If you only want to add layouts without removing anything, use [IVO:ADDLAYOUT](en/commands/sheet-manager/addlayout.md).

> [!NOTE]
> **If you press Cancel partway through, the old layouts are already gone.** The whole command is a **single undo step**, so typing `U` once restores them all. The command line says so when you cancel — nothing else on screen would suggest it.

> [!TIP]
> This command **does not ask** for a template or paper size. Those values are read from `IVO:SETTINGS` → **Sheet Manager** before the prompt appears, which is why the prompt states them — what you see in the prompt is exactly what will be used.

> [!NOTE]
> "Additional" layouts are **blank layouts with no viewport**, and their count is set in settings. What makes a layout blank is its **position in the creation order**, not its name — naming stays sequential like every other layout.

## See Also

- [IVO:ADDLAYOUT](en/commands/sheet-manager/addlayout.md) — adds layouts without deleting existing ones
- [IVO:RENUMBERVIEWFRAME](en/commands/sheet-manager/renumberviewframe.md) — renumber ViewFrame blocks before building layouts
- [IVO:SORTLAYOUT](en/commands/sheet-manager/sortlayout.md) — sort layout tabs by name
