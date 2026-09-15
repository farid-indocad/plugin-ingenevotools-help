# IVO:REPLACEBLOCK

> Replaces selected block references with another block, preserving placement properties and matching attribute values.

## How to Access

- **Ribbon:** Ingenevo Tools Tab → Utilities Panel → Replace Block button
- **Command Line:** `IVO:REPLACEBLOCK`
- **Alias:** —

## How to Use

1. Run `IVO:REPLACEBLOCK`
2. Select the block references to replace (the **source**)
3. Pick the block that will replace them (the **target**)
4. Choose whether the source blocks' placement properties are preserved
5. Choose an **alignment mode**:

| Mode | How the replacement is positioned |
|:-----|:----------------------------------|
| **Insertion** | Uses the source block's insertion point directly |
| **Center** | Aligns the bounding-box centres of source and target |
| **Reference** | You pick reference points on the source and on the target yourself |

6. Every selected source block is replaced by the target

<!-- screenshot -->

## Tips & Notes

> [!WARNING]
> This command requires an **active license**. Run [IVO:LICENSE](en/commands/help/license.md) to activate yours.

> [!TIP]
> **Attribute values with matching names are carried over** to the replacement block. Attributes with no counterpart in the target are not transferred.

> [!NOTE]
> **Center** mode matters when the source and target have insertion points in different places — one at a corner, the other at the centre, say. Without it the replacement jumps.

> [!TIP]
> When both blocks share an obvious reference point that is not their insertion point — a bolt-hole axis, for instance — use **Reference** mode and pick that point on each.

## See Also

- [IVO:CHANGEBASEPOINT](en/commands/utilities/changebasepoint.md) — change a block definition's base point
- [IVO:INITIALBLOCK](en/commands/utilities/initialblock.md) — prepare objects to become a clean block
