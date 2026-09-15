# IVO:SORTLAYOUT

> Sorts the layout tabs by name, ascending, using natural order.

## How to Access

- **Ribbon:** Ingenevo Tools Tab → Sheet Manager Panel → Sort Layout button
- **Command Line:** `IVO:SORTLAYOUT`
- **Alias:** —

## How to Use

1. Run `IVO:SORTLAYOUT`
2. Every layout tab is immediately sorted by name — **nothing is asked**

<!-- screenshot -->

## Tips & Notes

> [!WARNING]
> This command requires an **active license**. Run [IVO:LICENSE](en/commands/help/license.md) to activate yours.

> [!NOTE]
> The sort is **natural**, not plain alphabetical. That means `SH-2` comes before `SH-10`, not after it as it would in a text sort.

> [!NOTE]
> The **Model** tab is not sorted — only paper space layouts are reordered.

> [!TIP]
> This command only reorders the tabs; it **does not rename layouts**. To renumber their names, use [IVO:RENUMBERLAYOUT](en/commands/sheet-manager/renumberlayout.md).

## See Also

- [IVO:RENUMBERLAYOUT](en/commands/sheet-manager/renumberlayout.md) — renumber layout names sequentially
- [IVO:ADDLAYOUT](en/commands/sheet-manager/addlayout.md) — add layouts from ViewFrame blocks
