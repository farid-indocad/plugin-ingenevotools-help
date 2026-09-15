# IVO:RENUMBERLAYOUT

> Renumbers every paper space layout sequentially, with a preview and a confirmation.

## How to Access

- **Ribbon:** Ingenevo Tools Tab → Sheet Manager Panel → Renumber Layout button
- **Command Line:** `IVO:RENUMBERLAYOUT`
- **Alias:** —

## How to Use

1. Set the numbering format first, under `IVO:SETTINGS` → **Sheet Manager > Sheet Name**
2. Run `IVO:RENUMBERLAYOUT`
3. The command line shows a **preview** of the old and new names
4. A confirmation appears:

```
Apply renumbering? [Yes/No] <Yes>:
```

5. Press **Enter** to apply, or answer **No** to cancel

<!-- screenshot -->

## Tips & Notes

> [!WARNING]
> This command requires an **active license**. Run [IVO:LICENSE](en/commands/help/license.md) to activate yours.

> [!NOTE]
> **This command does not ask for a numbering format on the command line.** The prefix, digit count, and the rest come from saved settings, so every drawing in a project uses the same format without anyone having to remember it.

> [!TIP]
> Read the preview before answering Yes. It is the last chance to see each layout's new name before it is applied.

> [!TIP]
> After renumbering, run [IVO:SORTLAYOUT](en/commands/sheet-manager/sortlayout.md) so the tab order follows the new names.

## See Also

- [IVO:SORTLAYOUT](en/commands/sheet-manager/sortlayout.md) — sort layout tabs by name
- [IVO:RENUMBERVIEWFRAME](en/commands/sheet-manager/renumberviewframe.md) — renumber ViewFrame blocks in model space
- [IVO:SETTINGS](en/commands/settings/settings.md) — where the numbering format lives
