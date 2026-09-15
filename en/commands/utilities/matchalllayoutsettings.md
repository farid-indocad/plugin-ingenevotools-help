# IVO:MATCHALLLAYOUTSETTINGS

> Copies the active layout's page setup to every other layout.

## How to Access

- **Ribbon:** Ingenevo Tools Tab → Utilities Panel → Match Layout Settings button
- **Command Line:** `IVO:MATCHALLLAYOUTSETTINGS`
- **Alias:** `IVO:MALS`

## How to Use

1. **Switch to the layout tab** whose page setup you want to use as the source — this command cannot run from the Model tab
2. Run `IVO:MATCHALLLAYOUTSETTINGS` or `IVO:MALS`
3. A Yes/No confirmation appears, naming the source layout
4. Press **Enter** to apply (default **Yes**), or answer **No** to cancel

<!-- screenshot -->

## Tips & Notes

> [!WARNING]
> This command requires an **active license**. Run [IVO:LICENSE](en/commands/help/license.md) to activate yours.

> [!IMPORTANT]
> This **overwrites the page setup on every other layout**. Make sure the active layout has the right printer, paper size, and scale before answering Yes.

> [!NOTE]
> Must be run from a **layout tab**, not from **Model**. Model space has no page setup to copy.

> [!TIP]
> All the changes are a **single undo step** — one `U` restores every layout's page setup at once.

> [!TIP]
> Run this before [IVO:PRINTPDF](en/commands/print/printpdf.md) so all sheets print with the same printer and paper size.

## See Also

- [IVO:PRINTPDF](en/commands/print/printpdf.md) — batch print layouts to PDF
- [IVO:BLTSCALE](en/commands/utilities/bltscale.md) — unify linetype scaling across layouts
