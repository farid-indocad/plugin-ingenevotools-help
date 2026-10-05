# FAQ / Troubleshooting

Problems that actually come up in practice, and how to get past them.

---

## The "IngenevoTools" tab did not appear after installing

**Most likely cause: BricsCAD was open while the installer ran.** The install succeeded, but the new version only takes effect after BricsCAD is **closed and reopened**.

1. Close BricsCAD completely, then open it again
2. If it is still missing, double-click the same installer again and press **Reinstall**
3. If it still does not appear, send `%LocalAppData%\Ingenevo\install-log.txt` to the Ingenevo team

---

## Every IVO command is refused, although the tab is there

The plugin is installed but the **license has not been activated**. Type [`IVO:LICENSE`](en/commands/help/license.md) and activate it.

Seven commands still run without a license — `IVO:LICENSE`, `IVO:ABOUT`, `IVO:HELP`, `IVO:COMMANDS`, `IVO:SETTINGS`, `IVO:OPENSETTINGSFOLDER`, and `IVO:HIDESTRUCTURALPALETTE`. If those seven work and nothing else does, this is why.

---

## Activation refused: device limit reached

Every slot on your license is in use — usually by an old machine that is no longer in service.

What you can do:

- When the license window asks **Open the customer portal in your browser now?**, press **Yes**. In the **customer portal**, sign in with the code from your email and release the machines you no longer use. You can also open the portal directly at [https://app-licsvc.azurewebsites.net/portal](https://app-licsvc.azurewebsites.net/portal)
- On the old machine, if it still boots: open [`IVO:LICENSE`](en/commands/help/license.md) → **Remove**

> [!WARNING]
> Uninstalling the plugin or reimaging a machine does **not** free its license slot. Always press **Remove** before leaving a machine behind.

---

## Commands refused with "Your licence is on hold"

Your license has been **temporarily put on hold** by the Ingenevo team — for example while a payment is pending — not revoked. Contact the Ingenevo team. Once the hold is lifted, close and reopen BricsCAD; the license comes back with the same key and machine, with no re-activation.

---

## "Unknown command"

1. Every command starts with `IVO:` — check the spelling, including the colon
2. Run [`IVO:COMMANDS`](en/commands/help/commands.md) to see which commands are actually registered
3. If `IVO:COMMANDS` itself is not recognised, the plugin is not loaded — see [Installation](en/installation.md)

---

## A command runs but asks nothing

That is usually **the intended behaviour**, not a fault. Many commands read their configuration from the [settings profile](en/settings.md) instead of asking each time — paper size for [`IVO:CREATELAYOUT`](en/commands/sheet-manager/createlayout.md), the numbering format for [`IVO:RENUMBERLAYOUT`](en/commands/sheet-manager/renumberlayout.md), and both offsets for [`IVO:FOOTING`](en/commands/structure/footing.md).

If the result is not what you expected, check the [Settings](en/settings.md) first.

---

## Title blocks stayed empty after IVO:UPDATETITLEBLOCK

Excel rows are matched to layouts **by layout name**. An empty sheet almost always means the key column in Excel does not match the layout name exactly.

Also check:

1. The title block must be a **block reference with attributes** — plain text and mtext cannot be filled
2. Which worksheet is read comes from the [settings profile](en/settings.md), under **Sheet Manager › Drawing Register › Worksheet** (in the Intrax profile: `Intrax`)

---

## IVO:PRINTPDF produced no PDF

1. Make sure a PDF printer/plotter is configured in BricsCAD
2. Make sure the output folder is writable — not read-only, not a disconnected share
3. Run [`IVO:MATCHALLLAYOUTSETTINGS`](en/commands/utilities/matchalllayoutsettings.md) first so every layout uses the same page setup

---

## I ran IVO:BLTSCALE and "U" will not undo it

It cannot. [`IVO:BLTSCALE`](en/commands/utilities/bltscale.md) changes **system variables**, and system variable changes do not enter the undo history.

Run the command again with the previous value to restore it.

---

## IVO:FOOTING refuses to draw

[`IVO:FOOTING`](en/commands/structure/footing.md) **says why** on the command line rather than going quiet. The most common causes:

- **`Ring not closed`** — the perimeter still has gaps. The dangling lines are **automatically made the active selection**; zoom to that selection to see where the gaps are
- **Lines of any other colour are ignored** — only **cyan** (outer face) and **yellow** (centreline) lines are read. The number skipped is reported in the message as `wrong colour`

The full list of messages is on the [`IVO:FOOTING`](en/commands/structure/footing.md) page. If a drawing keeps refusing, send the drawing file to the Ingenevo team.

---

> [!TIP]
> Not listed here? Contact the Ingenevo team using the details on the [About](en/about.md) page. Attach `%LocalAppData%\Ingenevo\install-log.txt` for installation problems, or `%AppData%\IngenevoTools\license-log.txt` for licensing ones.
