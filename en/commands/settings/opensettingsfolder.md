# IVO:OPENSETTINGSFOLDER

> Opens the folder holding the plugin's settings, profiles, and presets in Windows Explorer.

## How to Access

- **Ribbon:** — (no ribbon button)
- **Command Line:** `IVO:OPENSETTINGSFOLDER`
- **Alias:** —

## How to Use

1. Run `IVO:OPENSETTINGSFOLDER`
2. Windows Explorer opens at:

```
%AppData%\IngenevoTools\
```

3. Inside you will find:

| Item | What it holds |
|:-----|:--------------|
| `Profiles\` | One XML file per settings profile. A pointer file records which one is active |
| `Schedule\` | `schedule-tables.xml` — the lookup tables for [IVO:SCHEDULE](en/commands/structure/schedule.md) |
| `Cleanup\` | Preset files for [IVO:CLEANUP](en/commands/utilities/cleanup.md) |

<!-- screenshot -->

## Tips & Notes

> [!NOTE]
> This is one of the few commands that needs **neither an active license nor an open drawing**. It only opens a folder; it does nothing to the drawing.

> [!TIP]
> If the folder does not exist yet, the command **creates it first** — so it works even if you have never pressed Save in the Settings window.

> [!WARNING]
> **Close the Settings window before hand-editing any XML file here.** That window holds the whole document in memory and rewrites the file when you press OK or Apply — your hand edits will be overwritten without warning.

> [!NOTE]
> Comments **you** write in the settings file do not survive. Every save rebuilds the whole document, so anything that did not come from the running configuration is lost. Comments written by the plugin itself are refreshed on each save.

> [!TIP]
> Most settings are safer to change through [IVO:SETTINGS](en/commands/settings/settings.md), which shows each option's explanation right beside its input field.

## See Also

- [IVO:SETTINGS](en/commands/settings/settings.md) — the plugin settings window
- [IVO:OPENFOLDER](en/commands/sheet-manager/openfolder.md) — opens the active drawing's folder
