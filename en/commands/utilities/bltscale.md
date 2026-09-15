# IVO:BLTSCALE

> Sets MSLTSCALE and PSLTSCALE across every layout at once, to 0 or 1.

## How to Access

- **Ribbon:** Ingenevo Tools Tab → Utilities Panel → BltScale button
- **Command Line:** `IVO:BLTSCALE`
- **Alias:** `IVO:BLTS`

## How to Use

1. Run `IVO:BLTSCALE` or `IVO:BLTS`
2. Enter the value you want — **0** or **1** — and press **Enter**
3. MSLTSCALE (model space) and PSLTSCALE (all layouts) are set to that value together
4. The tab you were on is restored afterwards

## Options / Parameters

| Value | Meaning |
|:------|:--------|
| **0** | Linetype scaling does **not** follow the annotation scale |
| **1** | Linetype scaling follows the annotation scale |

<!-- screenshot -->

## Tips & Notes

> [!WARNING]
> This command requires an **active license**. Run [IVO:LICENSE](en/commands/help/license.md) to activate yours.

> [!IMPORTANT]
> **System variable changes cannot be undone.** Typing `U` will not restore the previous MSLTSCALE and PSLTSCALE values — run this command again with the old value instead.

> [!TIP]
> The command visits each layout to set PSLTSCALE, then returns you to the tab you were on. On a drawing with many layouts you may see a brief flicker — that is normal.

## See Also

- [IVO:MATCHALLLAYOUTSETTINGS](en/commands/utilities/matchalllayoutsettings.md) — copy page setup to all layouts
