# IVO:INITIALBLOCK

> Normalizes the selected objects to Layer 0 / ByBlock, then opens the native BLOCK dialog with them preloaded.

## How to Access

- **Ribbon:** Ingenevo Tools Tab → Utilities Panel → Initial Block button
- **Command Line:** `IVO:INITIALBLOCK`
- **Alias:** `IVO:IBLOCK`

## How to Use

1. Select the objects that will become a block (a selection made beforehand is honoured)
2. Run `IVO:INITIALBLOCK` or `IVO:IBLOCK`
3. The plugin changes four properties on every selected object:

| Property | New value |
|:---------|:----------|
| Layer | `0` |
| Color | ByBlock |
| Linetype | ByBlock |
| Lineweight | ByBlock |

4. BricsCAD's native **Block Definition** dialog opens with those objects already loaded under *Select objects*
5. Continue as usual — name the block, set the base point, then **OK**

<!-- screenshot -->

## Tips & Notes

> [!WARNING]
> This command requires an **active license**. Run [IVO:LICENSE](en/commands/help/license.md) to activate yours.

> [!NOTE]
> Objects on **locked layers are skipped** — everything else in the same selection is still processed.

> [!WARNING]
> **If you press Cancel in the Block Definition dialog, the property normalization still stands.** That dialog belongs to BricsCAD, not to the plugin, so cancelling it does not put Layer and ByBlock back. Type `U` once to undo the normalization — all four property changes are a single undo step.

> [!TIP]
> The Layer 0 + ByBlock convention is what lets a block inherit layer and colour from wherever it is inserted, instead of imposing its own appearance. This command sets that convention up in one move.

> [!NOTE]
> There is no entity-type filter. Lines, circles, text, and block references are all accepted.

## See Also

- [IVO:REPLACEBLOCK](en/commands/utilities/replaceblock.md) — swap block instances for another block
- [IVO:CHANGEBASEPOINT](en/commands/utilities/changebasepoint.md) — change a block's base point
- [IVO:SAFEEXPLODE](en/commands/utilities/safeexplode.md) — explode a block one level, safely
