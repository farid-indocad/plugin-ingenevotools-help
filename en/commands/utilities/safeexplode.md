# IVO:SAFEEXPLODE

> Explodes the selected block references one level, with validation (locked layers are skipped).

## How to Access

- **Ribbon:** Ingenevo Tools Tab → Utilities Panel → Safe Explode button
- **Command Line:** `IVO:SAFEEXPLODE`
- **Alias:** `IVO:SX`

## How to Use

1. Run `IVO:SAFEEXPLODE` or `IVO:SX`
2. Select one or more block references to explode
3. Press **Enter** to confirm
4. The blocks are exploded one level — nested blocks inside them stay intact

<!-- screenshot -->

## Tips & Notes

> [!WARNING]
> This command requires an **active license**. Run [IVO:LICENSE](en/commands/help/license.md) to activate yours.

> [!NOTE]
> This is safer than the native EXPLODE because it:
> - skips blocks on locked layers automatically
> - explodes one level only, never recursively

> [!TIP]
> For recursive explosion down to primitive objects, use [IVO:MULTISAFEEXPLODE](en/commands/utilities/multisafeexplode.md).

## See Also

- [IVO:MULTISAFEEXPLODE](en/commands/utilities/multisafeexplode.md) — explode nested blocks recursively
- [IVO:INITIALBLOCK](en/commands/utilities/initialblock.md) — prepare objects to become a clean block
