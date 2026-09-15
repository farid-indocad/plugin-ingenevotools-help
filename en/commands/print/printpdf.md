# IVO:PRINTPDF

> Batch prints the selected sheet layouts to PDF.

## How to Access

- **Ribbon:** Ingenevo Tools Tab → Print Panel → Print PDF button
- **Command Line:** `IVO:PRINTPDF`
- **Alias:** —

## How to Use

1. Run `IVO:PRINTPDF`
2. Tick the layouts to print, and set their **order** with the up/down buttons
3. Choose the **printer** and **paper size**, then the **plot style**
4. Set the output folder, and pick an output mode:
   - **Single** — all layouts combined into one PDF file
   - **Multi** — one PDF file per layout
5. Press **Print**. If a file of that name already exists, you are asked before it is overwritten
6. When finished, you are offered the option to open the file or its folder

<!-- screenshot -->

## Tips & Notes

> [!WARNING]
> This command requires an **active license**. Run [IVO:LICENSE](en/commands/help/license.md) to activate yours.

> [!IMPORTANT]
> Make sure a PDF printer/plotter is configured in BricsCAD before running this command.

> [!TIP]
> Run [IVO:MATCHALLLAYOUTSETTINGS](en/commands/utilities/matchalllayoutsettings.md) first to make sure every layout uses the same page setup — otherwise sheets can come out at different sizes or scales.

## See Also

- [IVO:MATCHALLLAYOUTSETTINGS](en/commands/utilities/matchalllayoutsettings.md) — unify page setup before printing
- [IVO:SORTLAYOUT](en/commands/sheet-manager/sortlayout.md) — order the layout tabs
