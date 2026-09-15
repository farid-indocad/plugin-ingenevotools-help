# IVO:RECTANGLE

> Inserts a custom-sized rectangle whose corners can snap onto surrounding geometry.

## How to Access

- **Ribbon:** — (no ribbon button)
- **Command Line:** `IVO:RECTANGLE`
- **Alias:** —

## How to Use

1. Run `IVO:RECTANGLE`
2. Set the rectangle's size (**Width × Height**)
3. Move the cursor — the rectangle follows it with **its centre at the cursor**
4. When one of the rectangle's corners comes near surrounding geometry, **the whole rectangle shifts rigidly** so that corner lands exactly on the target
5. Click to place it

<!-- screenshot -->

## Tips & Notes

> [!WARNING]
> This command requires an **active license**. Run [IVO:LICENSE](en/commands/help/license.md) to activate yours.

> [!NOTE]
> **This is what separates it from BricsCAD's native `RECTANG`.** Drawing a box is not the point — placing it is: all four corners are watched at once as you move the cursor, so a column rectangle can attach to a wall corner **by its own corner** rather than by its centre.

> [!TIP]
> The result is an ordinary **closed LWPolyline**, so it can be edited, offset, and hatched like any other polyline.

> [!NOTE]
> Because the rectangle's centre follows the cursor, placing it without a snap centres it on the point you click.

## See Also

- [IVO:COLUMN](en/commands/structure/column.md) — place structural columns with labels
- [IVO:CHANGEBASEPOINT](en/commands/utilities/changebasepoint.md) — change a block's base point
