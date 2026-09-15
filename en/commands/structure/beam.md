# IVO:BEAM

> Draws a beam line and its label on every segment of a picked chain.

## How to Access

- **Ribbon:** Ingenevo Tools Tab → Structure Panel → Beam button
- **Command Line:** `IVO:BEAM`
- **Alias:** —

## How to Use

1. Run `IVO:BEAM`
2. Click the start point of the beam segment
3. Click the end point — a labelled beam line is drawn
4. Keep clicking to add further segments
5. Press **Enter** or **right-click** to finish

<!-- screenshot -->

## Tips & Notes

> [!WARNING]
> This command requires an **active license**. Run [IVO:LICENSE](en/commands/help/license.md) to activate yours.

> [!TIP]
> The beam type comes from the Structural palette's **Framing** tab, and can also be set under `IVO:SETTINGS` → **Structure > Beam**.

> [!TIP]
> To draw beams and columns in one pass, use [IVO:FRAMING](en/commands/structure/framing.md).

## See Also

- [IVO:FRAMING](en/commands/structure/framing.md) — columns and beams in one chain
- [IVO:GENCOLUMN](en/commands/structure/gencolumn.md) — add columns to beams already drawn
