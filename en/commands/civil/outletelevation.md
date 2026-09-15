# IVO:OUTLETELEVATION

> Calculates a pipe's outlet elevation from a picked run length, an inlet elevation, and a 1:X gradient.

## How to Access

- **Ribbon:** Ingenevo Tools Tab → Civil Panel → Outlet Elevation button
- **Command Line:** `IVO:OUTLETELEVATION`
- **Alias:** `IVO:OE`

## How to Use

1. Run `IVO:OUTLETELEVATION` or `IVO:OE`
2. Click points along the pipe run to measure its length
3. Enter the inlet elevation
4. Enter the gradient, in 1:X form
5. The calculated outlet elevation is reported

## Options / Parameters

| Parameter | Description |
|:----------|:------------|
| **Run points** | Picked in sequence to measure the pipe length |
| **Inlet Elevation** | Elevation at the pipe's inlet |
| **Gradient** | Pipe slope, written as 1:X |

<!-- screenshot -->

## Tips & Notes

> [!WARNING]
> This command requires an **active license**. Run [IVO:LICENSE](en/commands/help/license.md) to activate yours.

> [!NOTE]
> The length comes from the points **you pick**, not from any drawing object. Make sure the points follow the real pipe route — the calculation cannot tell that they do not.

## See Also

- [Command List](en/command-list.md) — every IngenevoTools command
