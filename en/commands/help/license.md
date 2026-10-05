# IVO:LICENSE

> Opens the license manager: activation, renewal, trial, and releasing a device.

## How to Access

- **Ribbon:** IngenevoTools Tab → Help Panel → License button
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
> If activation is refused because of the **device limit**, every slot on your license is in use. The window then asks **Open the customer portal in your browser now?** — press **Yes** to open the **customer portal**, sign in with the code sent to your email, and release the machines you no longer use. This applies to **Activate**, **Update**, and **Renew** alike.
>
> You can also open the portal directly at any time: [https://app-licsvc.azurewebsites.net/portal](https://app-licsvc.azurewebsites.net/portal)

> [!NOTE]
> If IVO commands refuse to run with the message **Your licence is on hold**, your license has been **temporarily put on hold** by the Ingenevo team — not revoked. Contact the Ingenevo team; once the hold is lifted, close and reopen BricsCAD. No re-activation is needed, and no extra slot is used.

> [!NOTE]
> On every activation and license re-check, the plugin sends the **computer name, local IP address, and Windows version name** to the license server, so each machine shows up under its own name in the customer portal. The local IP is not shown in the portal. This cannot be turned off.

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
