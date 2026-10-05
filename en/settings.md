# Settings

This page explains **how IngenevoTools settings are organised**, and which part of them you choose yourself.

> [!IMPORTANT]
> **Setting values come from the office profile; drafters do not fill them in.** Profiles are put together by the IndoCAD team and shipped with the installer. What you choose in [`IVO:SETTINGS`](en/commands/settings/settings.md) is only **which profile** is used. If a value needs to change — paper size, sheet name prefix, column types, and so on — ask the IndoCAD team to change it.

## What a profile decides

| Part | What it holds |
|:-----|:--------------|
| **General** | General preferences, including the Help URL [`IVO:HELP`](en/commands/help/help.md) opens |
| **Sheet Manager** | Paper · Sheet Name · Title Block (with Drawing Index and Extraction Rules) · Drawing Register · Viewport · Viewframe |
| **Structure** | The Column, Beam, and Bracing type lists with their drawing styles, plus Footing settings |
| **Member Schedule** | Table cleanup rules for [`IVO:SCHEDULE`](en/commands/structure/schedule.md) |

**Detail Library** settings are not part of the profile — they belong to your own machine and are set with [`IVO:DETAILLIBRARYSETTINGS`](en/commands/detail-library/detaillibrarysettings.md).

## Profiles

Settings are stored as **profiles** — one XML file per profile, plus a pointer that says which one is active.

The installer ships one office profile: **Intrax**. The old **Default** and **IndoCAD** profiles are retired — the installer removes both, and machines still using them are moved to Intrax.

To switch profile, run [`IVO:SETTINGS`](en/commands/settings/settings.md), pick the profile, and press **OK**. Switching **replaces the whole set of values at once** and takes effect immediately, with no plugin reload or BricsCAD restart.

## Where the files are

```
%AppData%\IngenevoTools\
  Profiles\           ← one file per profile
  Schedule\           ← Member Schedule lookup tables
  Cleanup\            ← IVO:CLEANUP presets
  detail-library.xml  ← this machine's Detail Library settings
```

Open it with [`IVO:OPENSETTINGSFOLDER`](en/commands/settings/opensettingsfolder.md).

> [!WARNING]
> **Do not edit the office profile by hand.** The installer overwrites the profiles it ships **every time it runs**, so your edits are lost at the next update. Ask the IndoCAD team for the change so it goes into the next package.

## Worth knowing

> [!NOTE]
> [`IVO:SETTINGS`](en/commands/settings/settings.md) **does not need an active license**, so you can always see and change which profile is in use.

> [!TIP]
> Many commands ask nothing because the answer is already in the profile — paper size, sheet name prefix, title block name, column type. If a command produces something you did not expect, check **which profile is active** before suspecting the command.
