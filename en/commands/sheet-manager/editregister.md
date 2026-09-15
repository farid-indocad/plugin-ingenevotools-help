# IVO:EDITREGISTER

> Opens the Excel register belonging to the active drawing.

## How to Access

- **Ribbon:** Ingenevo Tools Tab → Sheet Manager Panel → Edit Register button
- **Command Line:** `IVO:EDITREGISTER`
- **Alias:** —

## How to Use

1. Make sure the active drawing **has been saved** to disk
2. Run `IVO:EDITREGISTER`
3. The register file next to the drawing opens in your default spreadsheet application

<!-- screenshot -->

## Tips & Notes

> [!WARNING]
> This command requires an **active license**. Run [IVO:LICENSE](en/commands/help/license.md) to activate yours.

> [!NOTE]
> The register file must **already exist**. If it does not, create it first with [IVO:CREATEREGISTER](en/commands/sheet-manager/createregister.md).

> [!TIP]
> The register's name and extension are configurable under `IVO:SETTINGS` → **Sheet Manager > Drawing Register**. With the default `Auto` format, the plugin looks for `.xlsx` first, then `.xls`.

> [!NOTE]
> This command, [IVO:CREATEREGISTER](en/commands/sheet-manager/createregister.md), and [IVO:UPDATETITLEBLOCK](en/commands/sheet-manager/updatetitleblock.md) share one rule for deciding which file is a drawing's register, so the three can never disagree.

## See Also

- [IVO:CREATEREGISTER](en/commands/sheet-manager/createregister.md) — create a register from the template
- [IVO:UPDATETITLEBLOCK](en/commands/sheet-manager/updatetitleblock.md) — fill title blocks from the register
- [IVO:OPENFOLDER](en/commands/sheet-manager/openfolder.md) — open the active drawing's folder
