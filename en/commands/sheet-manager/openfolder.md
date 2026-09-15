# IVO:OPENFOLDER

> Opens the active drawing's folder in Windows Explorer.

## How to Access

- **Ribbon:** Ingenevo Tools Tab → Sheet Manager Panel → Open Folder button
- **Command Line:** `IVO:OPENFOLDER`
- **Alias:** —

## How to Use

1. Make sure the active drawing has been saved
2. Run `IVO:OPENFOLDER`
3. Windows Explorer opens at the folder containing the active drawing

<!-- screenshot -->

## Tips & Notes

> [!WARNING]
> This command requires an **active license**. Run [IVO:LICENSE](en/commands/help/license.md) to activate yours.

> [!NOTE]
> A drawing that has never been saved has no folder, so the command cannot open one.

> [!TIP]
> Handy for reaching the project folder — including the drawing's Excel register — without hunting for it in Explorer.

## See Also

- [IVO:EDITREGISTER](en/commands/sheet-manager/editregister.md) — open this drawing's Excel register
- [IVO:OPENSETTINGSFOLDER](en/commands/settings/opensettingsfolder.md) — open the plugin's settings folder
