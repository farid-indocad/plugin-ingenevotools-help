# IVO:PRINTPDF

> Batch prints the selected sheet layouts to PDF.

## How to Access

- **Ribbon:** IngenevoTools Tab → Print Panel → Print PDF button
- **Command Line:** `IVO:PRINTPDF`
- **Alias:** `IVO:PPP`

## How to Use

1. **Save the drawing first.** A drawing that has never been saved is refused before the window opens, because publishing identifies sheets by the DWG file on disk
2. Run `IVO:PRINTPDF`
3. Tick the layouts to print, and set their **order** with the up/down buttons. The **Paper** and **Plot Style** columns show each layout's settings
4. Pick an output mode:
   - **Multi-sheet** — all layouts combined into one PDF file
   - **Single-sheet** — one PDF file per layout
5. Set the **output location** (folder and file name). A folder that does not exist yet will be created
6. Choose the **plot style** to use for this print
7. Press **Print**. The window closes and BricsCAD starts printing
8. The result is reported **on the command line** — how many PDFs were created, then one line per file

<!-- screenshot -->

## Tips & Notes

> [!WARNING]
> This command requires an **active license**. Run [IVO:LICENSE](en/commands/help/license.md) to activate yours.

> [!NOTE]
> **No window appears after printing**, whether it worked or not. If no PDF was produced, the command line says `No PDF was produced.` with the reason and the location of the trace file `%AppData%\IngenevoTools\printpdf-log.txt`. Attach that file when reporting a printing problem.

> [!NOTE]
> If a file of the same name already exists, **BricsCAD itself** asks whether to replace it. If you answer **No**, that file is genuinely not written, and the command line reports it as not created — that is expected, not a fault.

> [!NOTE]
> In **Single-sheet** mode each file is named after its layout. If a name contains characters that are not allowed in file names, you are asked **Adjust file names?** before printing.

> [!NOTE]
> The plot style you pick is used for this print only — each layout's own plot style is put back afterwards. Paper size always follows each layout's page setup.

> [!TIP]
> Run [IVO:MATCHALLLAYOUTSETTINGS](en/commands/utilities/matchalllayoutsettings.md) first to make sure every layout uses the same page setup — otherwise sheets can come out at different sizes or scales.

## See Also

- [IVO:MATCHALLLAYOUTSETTINGS](en/commands/utilities/matchalllayoutsettings.md) — unify page setup before printing
- [IVO:SORTLAYOUT](en/commands/sheet-manager/sortlayout.md) — order the layout tabs
