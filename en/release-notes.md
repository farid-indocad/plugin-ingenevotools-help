# Release Notes

Changes as a drafter sees them. Installation and build details live in the plugin repository.

> [!TIP]
> The version actually installed on your machine is always available via [`IVO:ABOUT`](en/commands/help/about.md).

---

## 2.1.0 — refreshed [DATE]

The version number stays 2.1.0; what changed is the installer file. Run the new installer to get the changes below.

### Added

- **14 short aliases from the LISP plugin**: `IVO:CBP`, `IVO:CREG`, `IVO:DSS`, `IVO:EREG`, `IVO:OUG`, `IVO:OPF`, `IVO:PPP`, `IVO:RNL`, `IVO:RV`, `IVO:RBLOCK`, `IVO:SSS`, `IVO:US`, `IVO:SRL`, and `IVO:UTB`. See the [Command List](en/command-list.md).
- **A Generate Column ribbon button** for [`IVO:GENCOLUMN`](en/commands/structure/gencolumn.md), on the Structure panel. Beams already selected are used straight away.

### Changed

- **[`IVO:SETTINGS`](en/commands/settings/settings.md) now only chooses the profile.** The values inside a profile are put together by the IndoCAD team and shipped with the installer — see [Settings](en/settings.md).
- **Only the Intrax profile ships.** The **Default** and **IndoCAD** profiles are retired; machines using them are moved to Intrax.
- **With the Intrax profile, [`IVO:UPDATETITLEBLOCK`](en/commands/sheet-manager/updatetitleblock.md) writes every value in capitals.**
- **The default register template is now `Templates\register-intrax.xls`**, installed with the plugin. [`IVO:CREATEREGISTER`](en/commands/sheet-manager/createregister.md) now works on any machine.
- **Detail Library settings now belong to the machine**, not the profile — set them with [`IVO:DETAILLIBRARYSETTINGS`](en/commands/detail-library/detaillibrarysettings.md).
- **[`IVO:CLEANUP`](en/commands/utilities/cleanup.md) asks for the objects first**, then the preset file and preset.
- **The plugin is now named `IngenevoTools`**, copyright IndoCAD Pty Ltd — in the installer window and Settings › Apps too.
- **The installer is now about 15 MB** instead of 42 MB, and the uninstaller in the plugin folder about 80 KB.

### Fixed

- **License trial and activation on BricsCAD V26** no longer fail because the machine cannot be identified.
- **[`IVO:PRINTPDF`](en/commands/print/printpdf.md)** no longer re-runs the previous command after printing, reports a 0-byte PDF as empty, and names layouts whose plot style could not be put back.
- **[`IVO:FOOTING`](en/commands/structure/footing.md)** uses the active profile's offsets, even if the Structural palette has never been opened.
- **[`IVO:GENCOLUMN`](en/commands/structure/gencolumn.md)** places columns at the right ends of mirrored or 3D-rotated beams.
- **Beam, column, and bracing labels**: a rotated label's frame and wipeout rotate with it, and the wipeout really covers what lies under the text.
- **An interrupted or failed installation no longer makes the plugin disappear**, and a Reinstall that fails because BricsCAD is open now says so. See [Installation](en/installation.md).

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
