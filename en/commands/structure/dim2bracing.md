# IVO:DIM2BRACING

> Converts selected linear and aligned dimensions into bracing with labels, erasing the dimensions.

## How to Access

- **Ribbon:** Ingenevo Tools Tab → Structure Panel → Dim to Bracing button
- **Command Line:** `IVO:DIM2BRACING`
- **Alias:** `IVO:D2B`

## How to Use

1. Select the **aligned** or **linear** dimensions to convert (a selection made beforehand is honoured)
2. Run `IVO:DIM2BRACING` or `IVO:D2B`
3. Each selected dimension is replaced by bracing of the active type, and the original dimension is **erased**
4. The command line reports the result:

```
[Dim2Bracing] Converted 8 dimension(s) to "ANGLE 50x50x5" bracing, 2 skipped, 0 failed.
```

<!-- screenshot -->

## Tips & Notes

> [!WARNING]
> This command requires an **active license**. Run [IVO:LICENSE](en/commands/help/license.md) to activate yours.

> [!NOTE]
> The bracing type used is whichever is active on the Structural palette's **Bracing** tab — this command never asks. Set it first via [IVO:BRACING](en/commands/structure/bracing.md) or `IVO:SETTINGS` → **Structure > Bracing**.

> [!NOTE]
> Dimensions counted as **skipped** are those that are not aligned or linear — angular, radial, or diameter, for instance. Those are left intact, not erased.

> [!TIP]
> The whole selection is processed as a **single undo step**. If the result is not what you wanted, one `U` brings every erased dimension back at once.

## See Also

- [IVO:BRACING](en/commands/structure/bracing.md) — draw bracing by picking points
- [IVO:STRUCTURALPALETTE](en/commands/structure/structuralpalette.md) — open the palette where the bracing type is set
