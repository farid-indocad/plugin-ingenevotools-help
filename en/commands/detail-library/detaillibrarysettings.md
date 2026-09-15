# IVO:DETAILLIBRARYSETTINGS

> Manages the Detail Library folders, thumbnail cache, and refresh flag from the command line.

## How to Access

- **Ribbon:** — (no ribbon button)
- **Command Line:** `IVO:DETAILLIBRARYSETTINGS`
- **Alias:** —

## How to Use

1. Run `IVO:DETAILLIBRARYSETTINGS`
2. The current library folders are listed, followed by a keyword menu:

```
Manage library folders [Add/Remove/Done] <Done>:
```

3. Choose **Add** to enter a new folder path, or **Remove** to drop one. **Each change is saved immediately**
4. Choose **Done** to move on to the thumbnail cache folder and the always-refresh flag

## Options / Parameters

| Parameter | Description |
|:----------|:------------|
| **Library folders** | One or more folders holding the standard detail drawings |
| **Cache folder** | Where thumbnail previews are stored |
| **Refresh** | Whether thumbnails are always re-rendered |

<!-- screenshot -->

## Tips & Notes

> [!WARNING]
> This command requires an **active license**. Run [IVO:LICENSE](en/commands/help/license.md) to activate yours.

> [!NOTE]
> Adding a folder that does not exist is refused and re-prompted. An empty entry or Esc returns to the menu without adding anything.

> [!IMPORTANT]
> If the settings file cannot be written — because it is locked or read-only — the command **says so** rather than reporting success. A folder that only ever existed in memory would otherwise vanish at the next restart.

> [!TIP]
> The same settings are available in the settings window under `IVO:SETTINGS` → **Detail Library**, if you would rather not use the command line.

## See Also

- [IVO:DETAILLIBRARY](en/commands/detail-library/detaillibrary.md) — open the Detail Library palette
- [IVO:SETTINGS](en/commands/settings/settings.md) — the plugin settings window
