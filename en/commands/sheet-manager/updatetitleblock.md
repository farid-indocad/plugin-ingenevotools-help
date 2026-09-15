# IVO:UPDATETITLEBLOCK

> Fills title block attributes across many layouts at once, from an Excel file.

## How to Access

- **Ribbon:** Ingenevo Tools Tab → Sheet Manager Panel → Update Title Block button
- **Command Line:** `IVO:UPDATETITLEBLOCK`
- **Alias:** —

## How to Use

1. Make sure this drawing's **Excel register** exists and is filled in — create it with [IVO:CREATEREGISTER](en/commands/sheet-manager/createregister.md), fill it via [IVO:EDITREGISTER](en/commands/sheet-manager/editregister.md)
2. Run `IVO:UPDATETITLEBLOCK`
3. The plugin reads that register and, for each row:
   - **matches the row to a layout by its name**
   - writes the mapped columns into that layout's title block attributes

<!-- screenshot -->

## Tips & Notes

> [!WARNING]
> This command requires an **active license**. Run [IVO:LICENSE](en/commands/help/license.md) to activate yours.

> [!IMPORTANT]
> **Values are not typed on the command line — they come from the Excel file.** To change what a title block says, change the register and run this command again.

> [!NOTE]
> Matching is done by **layout name**. A row whose name matches no layout is not written anywhere.

> [!TIP]
> The register read here is the same file used by [IVO:CREATEREGISTER](en/commands/sheet-manager/createregister.md) and [IVO:EDITREGISTER](en/commands/sheet-manager/editregister.md). Which worksheet is read is set under `IVO:SETTINGS` → **Sheet Manager > Drawing Register > Worksheet**.

> [!NOTE]
> The title block must be a **block reference with attributes**. Plain text and mtext cannot be filled by this command.

> [!TIP]
> The title block's block name and the column-to-attribute mapping are set under `IVO:SETTINGS` → **Sheet Manager > Title Block**.

## See Also

- [IVO:CREATEREGISTER](en/commands/sheet-manager/createregister.md) — create the Excel register
- [IVO:EDITREGISTER](en/commands/sheet-manager/editregister.md) — open the register to fill it in
