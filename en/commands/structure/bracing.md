# IVO:BRACING

> Draws bracing details.

## How to Access

- **Ribbon:** Ingenevo Tools Tab → Structure Panel → Bracing button
- **Command Line:** `IVO:BRACING`
- **Alias:** —

## How to Use

1. Run `IVO:BRACING`
2. Follow the command-line prompts to set the bracing points
3. The bracing detail is drawn using the active bracing type

## Options / Parameters

The bracing type comes from the Structural palette's **Bracing** tab, and can also be set under `IVO:SETTINGS` → **Structure > Bracing**.

<!-- screenshot -->

## Tips & Notes

> [!WARNING]
> This command requires an **active license**. Run [IVO:LICENSE](en/commands/help/license.md) to activate yours.

> [!NOTE]
> The chosen bracing type is remembered and used as the default for the next run.

> [!TIP]
> If the bracing positions already exist as linear dimensions, [IVO:DIM2BRACING](en/commands/structure/dim2bracing.md) converts them in bulk instead of redrawing each one.

## See Also

- [IVO:DIM2BRACING](en/commands/structure/dim2bracing.md) — convert linear dimensions into bracing
- [IVO:STRUCTURALPALETTE](en/commands/structure/structuralpalette.md) — open the palette where the bracing type is set
