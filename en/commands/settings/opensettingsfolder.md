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
> If the folder does not exist yet, the command **creates it first** — so it works even on a machine that has never saved any settings.

> [!WARNING]
> **Do not hand-edit the office profiles in `Profiles\`.** The installer overwrites them every time it runs, so your edits are lost at the next update. Ask the IndoCAD team for the change.

> [!TIP]
> You will mostly need this folder to drop in your own [IVO:CLEANUP](en/commands/utilities/cleanup.md) preset variants, or to fetch a file the IndoCAD team asks for when you report a problem.

## See Also

- [IVO:SETTINGS](en/commands/settings/settings.md) — choose the settings profile
- [IVO:OPENFOLDER](en/commands/sheet-manager/openfolder.md) — opens the active drawing's folder
