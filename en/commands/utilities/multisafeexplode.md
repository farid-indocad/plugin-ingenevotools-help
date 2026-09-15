# IVO:MULTISAFEEXPLODE

> Recursively explodes nested blocks down to primitive objects.

## How to Access

- **Ribbon:** Ingenevo Tools Tab → Utilities Panel → Multi Safe Explode button
- **Command Line:** `IVO:MULTISAFEEXPLODE`
- **Alias:** `IVO:MSX`

## How to Use

1. Run `IVO:MULTISAFEEXPLODE` or `IVO:MSX`
2. Select one or more block references
3. Press **Enter** to confirm
4. The blocks are exploded repeatedly until only primitive objects remain

<!-- screenshot -->

## Tips & Notes

> [!WARNING]
> This command requires an **active license**. Run [IVO:LICENSE](en/commands/help/license.md) to activate yours.

> [!NOTE]
> Blocks on locked layers are skipped, the same as [IVO:SAFEEXPLODE](en/commands/utilities/safeexplode.md).

> [!IMPORTANT]
> Recursive explosion is hard to reverse by hand. If you only need to go one level down, use [IVO:SAFEEXPLODE](en/commands/utilities/safeexplode.md) instead.

## See Also

- [IVO:SAFEEXPLODE](en/commands/utilities/safeexplode.md) — explode one level only
