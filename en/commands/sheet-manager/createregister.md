# IVO:CREATEREGISTER

> Creates the Excel register for the active drawing by copying the template.

## How to Access

- **Ribbon:** IngenevoTools Tab → Sheet Manager Panel → Create Register button
- **Command Line:** `IVO:CREATEREGISTER`
- **Alias:** `IVO:CREG`

## How to Use

1. Open a drawing that **has already been saved** — the register is created next to the DWG file
2. Run `IVO:CREATEREGISTER`
3. The plugin works out the register file name from the drawing name, then copies the template into the same folder
4. If a register file with that name **already exists**, you are asked first:

```
File 'A-101.xlsx' already exists. Overwrite? [Yes/No] <No>:
```

5. Answer **Yes** to overwrite, or press **Enter** to cancel (the default is **No**)

<!-- screenshot -->

## Tips & Notes

> [!WARNING]
> This command requires an **active license**. Run [IVO:LICENSE](en/commands/help/license.md) to activate yours.

> [!NOTE]
> The drawing must already be saved to disk. A new drawing that has never been saved has no folder, so the command has nowhere to put the register.

> [!TIP]
> The register's name, extension, and template come from the [settings profile](en/settings.md), under **Sheet Manager > Drawing Register**. In the **Intrax** office profile:
>
> | Option | Value in Intrax | What it means |
> |:-------|:----------------|:--------------|
> | **Format** | `XlsThenXlsx` | The register is created as `.xls`; when looking for an existing register, `.xls` is tried first, then `.xlsx` |
> | **Template Path** | `Templates\register-intrax.xls` | The template installed with the plugin, in the `Templates\` folder next to the plugin DLL |
> | **Worksheet** | `Intrax` | The sheet name [IVO:UPDATETITLEBLOCK](en/commands/sheet-manager/updatetitleblock.md) reads title block data from |

> [!NOTE]
> The template's extension must match the register format. If it does not — say, an `.xls` template with a format that creates `.xlsx` — the command **refuses** before copying anything, because Excel would reject such a file.

> [!NOTE]
> If **Template Path** is set but the file cannot be found, the command does **not** quietly fall back to the built-in template — it reports failure. That is deliberate, so a typo in the path is not hidden behind a result that looks correct.

> [!TIP]
> `IVO:CREATEREGISTER`, [IVO:EDITREGISTER](en/commands/sheet-manager/editregister.md), and [IVO:UPDATETITLEBLOCK](en/commands/sheet-manager/updatetitleblock.md) share one rule for deciding "which file is this drawing's register", so all three always point at the same file.

## See Also

- [IVO:EDITREGISTER](en/commands/sheet-manager/editregister.md) — opens an existing register
- [IVO:UPDATETITLEBLOCK](en/commands/sheet-manager/updatetitleblock.md) — fills title blocks in bulk from the register
