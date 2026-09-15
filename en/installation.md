# Installation

Installing IngenevoTools takes **four steps** and does not need Administrator rights.

## Requirements

- **BricsCAD** V20 through V26
- **Windows** 64-bit

## Four steps

1. **Open the link** sent by the Ingenevo team, then **double-click** `IngenevoToolsSetup.exe`
2. A single window opens and works on its own. Wait a few seconds until it says **"Ingenevo Tools has been installed"**, then press **Close**
3. **Open BricsCAD.** The **Ingenevo Tools** tab appears on the ribbon by itself
4. Type **`IVO:LICENSE`** and activate your license

<!-- screenshot -->

> [!NOTE]
> There is nothing to choose and nothing to answer. The installer **detects on its own** which BricsCAD versions are on your machine — if there is more than one, all of them are served at once.

> [!IMPORTANT]
> Step 4 is not optional. Without an active license almost every `IVO:` command is refused, even though the plugin is installed and its tab is visible. Only seven commands still run — see the [Command List](en/command-list.md).

## If BricsCAD is open

The install still succeeds, but the new version only takes effect after BricsCAD is **closed and reopened**. The installer window says so.

## Plugin missing or behaving oddly

Double-click **the same installer** again. If that version is already installed, the window offers a **Reinstall** button — press it.

## Verifying

Once BricsCAD is open:

1. The **Ingenevo Tools** tab is visible on the ribbon
2. Type [`IVO:COMMANDS`](en/commands/help/commands.md) to list the commands
3. Type [`IVO:ABOUT`](en/commands/help/about.md) to see the installed version

## Uninstalling

Two ways, both equivalent:

- **Settings › Apps › Ingenevo Tools › Uninstall**
- or double-click **`Uninstall Ingenevo Tools.exe`** in `%LocalAppData%\Ingenevo\IngenevoTools\`

Your settings and license are **not** removed.

> [!WARNING]
> **If you will not use the plugin on this machine again, release the device first** via [`IVO:LICENSE`](en/commands/help/license.md) → **Remove**, **before** uninstalling. Deleting the files does **not** free the license slot on the server — it stays claimed by a machine you no longer use.

## If something fails

Send this file to the Ingenevo team:

```
%LocalAppData%\Ingenevo\install-log.txt
```

> [!TIP]
> Installing is **idempotent** — repeating it is safe and breaks nothing. When in doubt, run the installer again.
