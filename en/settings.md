# Settings

This page explains **how IngenevoTools settings are organised** — it does not list the options one by one.

> [!IMPORTANT]
> Every option's explanation lives **inside the Settings window**, shown right beside its input field. That is deliberate: an explanation copied into two places drifts apart quickly, and the one inside the dialog can never go stale. This page does not duplicate it.

Open it with [`IVO:SETTINGS`](en/commands/settings/settings.md).

## The settings tree

| Group | What it holds |
|:------|:--------------|
| **General** | General preferences, including the Help URL [`IVO:HELP`](en/commands/help/help.md) opens |
| **Sheet Manager** | Paper · Sheet Name · Title Block (with Drawing Index and Extraction Rules) · Drawing Register · Viewport · Viewframe |
| **Structure** | The Column, Beam, and Bracing type lists, plus Footing settings |
| **Detail Library** | Library folders and the thumbnail cache folder |
| **Member Schedule** | Table cleanup rules for [`IVO:SCHEDULE`](en/commands/structure/schedule.md) |

<!-- screenshot -->

## Profiles

Settings are stored as **profiles** — one XML file per profile, plus a pointer recording which one is active.

The installer ships three: **Default**, **Intrax**, and **IndoCAD**. A new drafter therefore starts with the office standard rather than building one from nothing.

Switching profiles is done inside the Settings window, and **replaces the whole set of values at once** — it does not merge them.

## Where the files live

```
%AppData%\IngenevoTools\
  Profiles\      ← one file per profile
  Schedule\      ← Member Schedule lookup tables
  Cleanup\       ← IVO:CLEANUP presets
```

Open it with [`IVO:OPENSETTINGSFOLDER`](en/commands/settings/opensettingsfolder.md).

> [!WARNING]
> **Close the Settings window before editing these files by hand.** It holds the whole document in memory and rewrites the file when you press OK or Apply — your hand edits would be overwritten without warning.

> [!NOTE]
> Comments **you** write in the file do not survive. Every save rebuilds the whole document from the running configuration. Comments written by the plugin itself are refreshed on each save, so they are never stale.

## Worth knowing

> [!NOTE]
> [`IVO:SETTINGS`](en/commands/settings/settings.md) **does not require an active license.** Its contents are your own configuration, which you may have spent a long time building — locking you out because a subscription lapsed by a day would be holding your own data hostage.

> [!NOTE]
> Changes take effect **immediately**, with no need to reload the plugin or restart BricsCAD.

> [!TIP]
> Many commands ask nothing because the answer is already here — paper size, sheet name prefix, title block name, column type. If a command produces something you did not expect, check the settings before suspecting the command.
