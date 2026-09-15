# IVO:LICENSE

> Opens the license manager: activation, renewal, trial, and releasing a device.

## How to Access

- **Ribbon:** Ingenevo Tools Tab → Help Panel → License button
- **Command Line:** `IVO:LICENSE`
- **Alias:** —

## How to Use

1. Run `IVO:LICENSE`
2. The **License Manager** window opens in one of three states: **Active**, **Not Active**, or **Expired**
3. Choose an action:

| Button | What it does |
|:-------|:-------------|
| **Activate** | Enter a license key to activate the plugin on this device |
| **Start 14-Day Trial** | Begin a 14-day trial — available in the *Not Active* state |
| **Renew** | Renew a license that has expired |
| **Update** | Refresh the license data from the server |
| **Remove** | **Releases this device** from the license, freeing its slot |
| **Close** | Close the window |

<!-- screenshot -->

## Tips & Notes

> [!NOTE]
> This command **always runs without an active license** — otherwise you could never activate one in the first place.

> [!WARNING]
> **Before you stop using the plugin on a machine, press Remove first.** Uninstalling the plugin or reimaging the machine does **not** free the license slot on the server — that slot stays claimed by a machine that no longer exists.

> [!NOTE]
> If activation is refused with a **device limit** message, every slot on your license is in use. The list of machines using them is not shown in this window — contact the Ingenevo team, or press **Remove** on a machine you no longer use.

> [!TIP]
> When activation goes wrong, the plugin writes a diagnostic trace to the file below. There is no button to open it — open it yourself in Explorer and attach it when you contact the Ingenevo team:
>
> ```
> %AppData%\IngenevoTools\license-log.txt
> ```

> [!NOTE]
> License status is re-checked in the background, so there is no *Refresh* button — you do not have to do anything for a renewal to be picked up.

## See Also

- [IVO:ABOUT](en/commands/help/about.md) — plugin version information
- [Command List](en/command-list.md) — which commands need an active license
