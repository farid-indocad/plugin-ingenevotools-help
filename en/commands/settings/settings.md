# IVO:SETTINGS

> Opens the plugin settings window.

## How to Access

- **Ribbon:** Ingenevo Tools Tab → Settings Panel → Settings button
- **Command Line:** `IVO:SETTINGS`
- **Alias:** —

## How to Use

1. Run `IVO:SETTINGS`
2. The settings window opens with a group tree on the left:

| Group | What it holds |
|:------|:--------------|
| **General** | General preferences, including the Help URL [IVO:HELP](en/commands/help/help.md) opens |
| **Sheet Manager** | Paper, Sheet Name, Title Block (with Drawing Index and Extraction Rules), Drawing Register, Viewport, Viewframe |
| **Structure** | The Column, Beam, and Bracing type lists, plus Footing settings |
| **Detail Library** | Library folders and the thumbnail cache folder |
| **Member Schedule** | Cleanup rules for [IVO:SCHEDULE](en/commands/structure/schedule.md) |

3. Click a group to see its options — **each option's explanation appears right beside its input field**
4. Press **OK** or **Apply** to save

<!-- screenshot -->

## Tips & Notes

> [!NOTE]
> This command **does not require an active license.** Settings hold your own configuration — profiles, column types, title block rules — that you may have spent a long time building. Locking you out of it because a subscription lapsed by a day would be holding your own data hostage.

> [!TIP]
> Every option's explanation lives inside this window, not on the documentation site. That is deliberate: an explanation copied into two places drifts apart quickly, and the one inside the dialog can never go stale.

> [!TIP]
> Settings are stored as **profiles**. The installer ships three of them — `Default`, `Intrax`, and `IndoCAD` — so a new drafter starts with the office standard rather than a blank slate.

> [!NOTE]
> Changes take effect immediately. There is no need to reload the plugin or restart BricsCAD.

> [!WARNING]
> If you edit the settings file by hand, **close this window first.** It holds the whole document in memory and rewrites the file when you press OK or Apply — your hand edits would be overwritten.

## See Also

- [IVO:OPENSETTINGSFOLDER](en/commands/settings/opensettingsfolder.md) — open the folder holding profiles and presets
- [Settings](en/settings.md) — how the settings are organised
