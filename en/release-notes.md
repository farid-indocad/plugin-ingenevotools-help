# Release Notes

Changes as a drafter sees them. Installation and build details live in the plugin repository.

> [!TIP]
> The version actually installed on your machine is always available via [`IVO:ABOUT`](en/commands/help/about.md).

---

## 2.1.0 — released 28 September 2026

The first minor version after 2.0.0, mostly bringing licensing into line. Existing licenses stay valid — no new license is needed.

### Added

- **A full device quota now points you to the customer portal.** When activation is refused because of the device limit, the license window offers to open the [customer portal](https://app-licsvc.azurewebsites.net/portal), where you release machines you no longer use. See [`IVO:LICENSE`](en/commands/help/license.md).

### Changed

- **The plugin sends the computer name, local IP address, and Windows version name to the license server**, so each machine shows up under its own name in the portal. This cannot be turned off.

### Removed

- **`IVO:BOUNDARY`, `IVO:BND`, and `IVO:BOUNDARYDUMP`.** All three were development tools and now answer "Unknown command". The closest command that remains is [`IVO:FOOTING`](en/commands/structure/footing.md).

### Fixed

- **A license on hold now actually holds the plugin**, with the message "Your licence is on hold". Once the hold is lifted, the license comes back by itself when BricsCAD is reopened.
- **Ribbon buttons in BricsCAD V20 show their icons**, not a question mark.
- **The first pick of [`IVO:COLUMN`](en/commands/structure/column.md) and [`IVO:FRAMING`](en/commands/structure/framing.md) is no longer ORTHO-locked.** The first point is free, as in `LINE`; ORTHO applies from the second point.

---

## 2.0.0 — refreshed 22 September 2026

### Fixed

- **[`IVO:PRINTPDF`](en/commands/print/printpdf.md) actually produces PDFs.** Before, it reported success without writing a single file. PDFs are now made through BricsCAD's own publish:
  - the result is reported on the command line, with no window afterwards
  - the "replace file?" question now comes from BricsCAD itself
  - a drawing that has never been saved is refused before the window opens

---

## 2.0.0 — refreshed 17 September 2026

Reinstall with the installer to get the office CLEANUP presets — presets are only planted at install time.

### Added

- **Office [`IVO:CLEANUP`](en/commands/utilities/cleanup.md) presets are installed**: eleven files, one per builder (AVIA HOMES, DIXON, JGK, MAKAAN, METRICON, ORBIT HOMES QLD, REMMUS, SIMOND, TEMPO, TICK HOMES, VERONA).
- **Per-type styles for Column, Beam, and Bracing** in [Settings](en/settings.md): colour (ByLayer, ByBlock, or an index), layer, linetype, linetype scale, and lineweight for what gets drawn, plus colour and text style for its label.

### Changed

- **[`IVO:FRAMING`](en/commands/structure/framing.md), [`IVO:COLUMN`](en/commands/structure/column.md), [`IVO:BEAM`](en/commands/structure/beam.md), and [`IVO:BRACING`](en/commands/structure/bracing.md) no longer pop up the Structural palette.** Open it with [`IVO:STRUCTURALPALETTE`](en/commands/structure/structuralpalette.md).

### Removed

- **The example preset `cleanup-general.xml` is no longer created.** An existing copy is not deleted — remove it yourself from `%AppData%\IngenevoTools\Cleanup\` if you do not need it.

### Fixed

- **`ByLayer` and `ByBlock` colour criteria in CLEANUP presets now work.** Before, neither ever matched anything.

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
