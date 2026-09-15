# IVO:RENUMBERVIEWFRAME

> Renumbers the selected ViewFrame blocks in left-to-right order.

## How to Access

- **Ribbon:** Ingenevo Tools Tab → Sheet Manager Panel → Renumber Viewframe button
- **Command Line:** `IVO:RENUMBERVIEWFRAME`
- **Alias:** `IVO:RVF`

## How to Use

1. Select the **ViewFrame** blocks to renumber (a selection made beforehand is honoured)
2. Run `IVO:RENUMBERVIEWFRAME` or `IVO:RVF`
3. New numbers are written to the ViewFrame attribute **by their left-to-right position**

<!-- screenshot -->

## Tips & Notes

> [!WARNING]
> This command requires an **active license**. Run [IVO:LICENSE](en/commands/help/license.md) to activate yours.

> [!NOTE]
> **The order comes from position in model space, not from the order you selected them.** The leftmost ViewFrame gets the first number no matter which one you clicked first.

> [!TIP]
> The target attribute name and the digit count are read from `IVO:SETTINGS` → **Sheet Manager > Viewframe** and **Sheet Name** — this command does not ask.

> [!TIP]
> Run this **before** [IVO:CREATELAYOUT](en/commands/sheet-manager/createlayout.md) or [IVO:ADDLAYOUT](en/commands/sheet-manager/addlayout.md), because layout names are derived from the ViewFrame numbers.

## See Also

- [IVO:CREATELAYOUT](en/commands/sheet-manager/createlayout.md) — build layouts from ViewFrames
- [IVO:ADDLAYOUT](en/commands/sheet-manager/addlayout.md) — add layouts from selected ViewFrames
- [IVO:RENUMBERLAYOUT](en/commands/sheet-manager/renumberlayout.md) — renumber layout names
