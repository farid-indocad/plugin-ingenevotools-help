# IVO:SELECTSIMILARSPECIFIED

> Selects entities similar to the picked one, filtered by the properties you specify.

## How to Access

- **Ribbon:** Ingenevo Tools Tab → Utilities Panel → Select Similar button
- **Command Line:** `IVO:SELECTSIMILARSPECIFIED`
- **Alias:** —

## How to Use

1. Run `IVO:SELECTSIMILARSPECIFIED`
2. Pick a reference entity
3. Specify which properties must match (entity type, layer, colour, linetype, and so on)
4. Every entity matching that filter becomes selected

<!-- screenshot -->

## Tips & Notes

> [!WARNING]
> This command requires an **active license**. Run [IVO:LICENSE](en/commands/help/license.md) to activate yours.

> [!TIP]
> More precise than the native SELECTSIMILAR, because you decide which properties count as "similar" rather than accepting a fixed set.

> [!TIP]
> To narrow an existing selection instead of building one, use [IVO:DESELECTSIMILAR](en/commands/utilities/deselectsimilar.md).

## See Also

- [IVO:DESELECTSIMILAR](en/commands/utilities/deselectsimilar.md) — remove similar entities from the selection
- [IVO:CLEANUP](en/commands/utilities/cleanup.md) — filter and highlight by a saved preset
