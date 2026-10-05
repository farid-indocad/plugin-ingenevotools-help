# IVO:SETTINGS

> Chooses the settings profile the plugin uses.

## How to Access

- **Ribbon:** IngenevoTools Tab → Settings Panel → Settings button
- **Command Line:** `IVO:SETTINGS`
- **Alias:** `IVO:US`

## How to Use

1. Run `IVO:SETTINGS` or `IVO:US`
2. The **Settings profile** window opens and lists the profiles installed on this machine. The one in use is marked **(in use)**
3. Pick the profile that fits the drawings you are working on, then press **OK**. **Cancel** closes the window without changing anything
4. The new profile takes effect immediately, including the type lists in the Structural palette

<!-- screenshot -->

## Tips & Notes

> [!NOTE]
> **Values inside a profile cannot be changed here.** Profiles are office standards that the installer overwrites on every install, so edits on a drafter's machine would be lost at the next update. If a value needs to change, ask the IndoCAD team.

> [!NOTE]
> This command **does not need an active license**, so you can always see and change which profile is in use.

> [!TIP]
> The installer ships the **Intrax** office profile. The old **Default** and **IndoCAD** profiles are retired, so this list usually holds only Intrax — unless the IndoCAD team has installed another profile on your machine.

> [!NOTE]
> If switching fails, the window stays open and shows why (`Could not switch to …`). The previous profile stays in use.

## See Also

- [IVO:OPENSETTINGSFOLDER](en/commands/settings/opensettingsfolder.md) — open the folder where profiles and presets are stored
- [Settings](en/settings.md) — how the settings are organised
