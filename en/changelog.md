# Changelog

Changes as a drafter sees them. Installation and build details live in the plugin repository.

> [!TIP]
> The version actually installed on your machine is always available via [`IVO:ABOUT`](en/commands/help/about.md).

---

## 2.0.0 — refreshed 15 September 2026

The version number stays 2.0.0; what changed is the installer file.

**Nothing changes for drafters.** What you receive is still `IngenevoToolsSetup.exe`, with the same window, Reinstall button, and "close and reopen BricsCAD" message. This refresh adds a separate file for the IT team's use.

---

## 2.0.0 — refreshed 14 September 2026

### Added

- **Office-standard settings profiles ship with the installer.** It plants the **Default**, **Intrax**, and **IndoCAD** profiles, so a new drafter starts with the office setup instead of building one. See [Settings](en/settings.md).
- **Title block extraction rule editor** in `IVO:SETTINGS`, so those rules no longer have to be changed by editing XML by hand.
- **A self-locating uninstaller** in the plugin folder, alongside the Settings › Apps route.

### Changed

- **Installation now goes through an installer**, replacing the logon-script route. Four steps, no Administrator rights — see [Installation](en/installation.md).

---

## 2.0.0 — released 18 August 2026

The first release of IngenevoTools as a .NET plugin, replacing the previous AutoLISP plugin.

### Licensing

- **14-day trial**, startable from inside the plugin via [`IVO:LICENSE`](en/commands/help/license.md)

### Commands

- **Structure** — [`IVO:FRAMING`](en/commands/structure/framing.md) (a LINE-style chain: a column at each vertex, a beam on each segment), [`IVO:COLUMN`](en/commands/structure/column.md), [`IVO:BEAM`](en/commands/structure/beam.md), [`IVO:BRACING`](en/commands/structure/bracing.md)
- **Sheet Manager** — [`IVO:CREATELAYOUT`](en/commands/sheet-manager/createlayout.md), [`IVO:ADDLAYOUT`](en/commands/sheet-manager/addlayout.md), [`IVO:SORTLAYOUT`](en/commands/sheet-manager/sortlayout.md), [`IVO:RENUMBERLAYOUT`](en/commands/sheet-manager/renumberlayout.md), [`IVO:RENUMBERVIEWFRAME`](en/commands/sheet-manager/renumberviewframe.md)
- **Detail Library** — [`IVO:DETAILLIBRARY`](en/commands/detail-library/detaillibrary.md) with self-rendered thumbnails
- **Print & register** — [`IVO:PRINTPDF`](en/commands/print/printpdf.md), [`IVO:CREATEREGISTER`](en/commands/sheet-manager/createregister.md), [`IVO:EDITREGISTER`](en/commands/sheet-manager/editregister.md), [`IVO:UPDATETITLEBLOCK`](en/commands/sheet-manager/updatetitleblock.md)
- **Drawing & selection** — [`IVO:RECTANGLE`](en/commands/utilities/rectangle.md) with CornerSnap, [`IVO:SELECTSIMILARSPECIFIED`](en/commands/utilities/selectsimilarspecified.md), [`IVO:DESELECTSIMILAR`](en/commands/utilities/deselectsimilar.md)
- **Others** — [`IVO:SCHEDULE`](en/commands/structure/schedule.md), [`IVO:OUTLETELEVATION`](en/commands/civil/outletelevation.md), and the remaining utilities

The full list is in the [Command List](en/command-list.md).

### Settings

- **Named profiles**, switchable from inside the Settings window

### Compatibility

- BricsCAD V20 through V26 — see [About](en/about.md) for the test status of each version
