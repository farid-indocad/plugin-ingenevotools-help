# Command List

Every IngenevoTools command, grouped the way the panels are grouped on the **Ingenevo Tools** ribbon tab.

The **Ribbon** column marks whether a command has a button of its own. Commands marked **—** can only be run from the command line — some of them deliberately so, because a ribbon button would discard the selection you already made.

> [!TIP]
> The same list is available inside BricsCAD via [IVO:COMMANDS](en/commands/help/commands.md), without opening a browser.

---

## Print

| Command | Alias | Ribbon | What it does |
|:---------|:------|:------:|:-------|
| [IVO:PRINTPDF](en/commands/print/printpdf.md) | — | ✓ | Batch print layouts to PDF |

## Sheet Manager

| Command | Alias | Ribbon | What it does |
|:---------|:------|:------:|:-------|
| [IVO:OPENFOLDER](en/commands/sheet-manager/openfolder.md) | — | ✓ | Open the active drawing's folder |
| [IVO:UPDATETITLEBLOCK](en/commands/sheet-manager/updatetitleblock.md) | — | ✓ | Batch update title blocks from Excel |
| [IVO:CREATEREGISTER](en/commands/sheet-manager/createregister.md) | — | ✓ | Create an Excel register for the active drawing from the template |
| [IVO:EDITREGISTER](en/commands/sheet-manager/editregister.md) | — | ✓ | Open the active drawing's Excel register |
| [IVO:CREATELAYOUT](en/commands/sheet-manager/createlayout.md) | `IVO:CRL` | ✓ | Replace **all** layouts with new ones from the ViewFrame blocks |
| [IVO:ADDLAYOUT](en/commands/sheet-manager/addlayout.md) | `IVO:ADL` | ✓ | Add layouts for the selected ViewFrames, keeping existing ones |
| [IVO:SORTLAYOUT](en/commands/sheet-manager/sortlayout.md) | — | ✓ | Sort layout tabs by name |
| [IVO:RENUMBERLAYOUT](en/commands/sheet-manager/renumberlayout.md) | — | ✓ | Sequential layout renumbering |
| [IVO:RENUMBERVIEWFRAME](en/commands/sheet-manager/renumberviewframe.md) | `IVO:RVF` | ✓ | Renumber selected ViewFrame blocks left to right |

## Utilities

| Command | Alias | Ribbon | What it does |
|:---------|:------|:------:|:-------|
| [IVO:SAFEEXPLODE](en/commands/utilities/safeexplode.md) | `IVO:SX` | ✓ | Explode blocks one level, safely |
| [IVO:MULTISAFEEXPLODE](en/commands/utilities/multisafeexplode.md) | `IVO:MSX` | ✓ | Recursively explode nested blocks |
| [IVO:CLEANUP](en/commands/utilities/cleanup.md) | — | ✓ | Filter and highlight objects matching a cleanup preset |
| [IVO:SOLID2HATCH](en/commands/utilities/solid2hatch.md) | `IVO:S2H` | ✓ | Convert SOLID objects to hatches |
| [IVO:INITIALBLOCK](en/commands/utilities/initialblock.md) | `IVO:IBLOCK` | ✓ | Normalize a selection to layer 0 / ByBlock and open the BLOCK dialog |
| [IVO:REPLACEBLOCK](en/commands/utilities/replaceblock.md) | — | ✓ | Replace block instances |
| [IVO:BLTSCALE](en/commands/utilities/bltscale.md) | `IVO:BLTS` | ✓ | Set MSLTSCALE/PSLTSCALE on all layouts |
| [IVO:MATCHALLLAYOUTSETTINGS](en/commands/utilities/matchalllayoutsettings.md) | `IVO:MALS` | ✓ | Copy page setup to all layouts |
| [IVO:CHANGEBASEPOINT](en/commands/utilities/changebasepoint.md) | — | ✓ | Change a block's base point |
| [IVO:RECTANGLE](en/commands/utilities/rectangle.md) | — | — | Draw a rectangle column with corner snap |
| [IVO:SELECTSIMILARSPECIFIED](en/commands/utilities/selectsimilarspecified.md) | — | ✓ | Select similar entities by filter |
| [IVO:DESELECTSIMILAR](en/commands/utilities/deselectsimilar.md) | — | ✓ | Deselect similar entities |

## Structure

| Command | Alias | Ribbon | What it does |
|:---------|:------|:------:|:-------|
| [IVO:FRAMING](en/commands/structure/framing.md) | — | ✓ | Draw a chain of columns and beams together, LINE-style |
| [IVO:COLUMN](en/commands/structure/column.md) | — | ✓ | Draw a column at every picked vertex, without beams |
| [IVO:BEAM](en/commands/structure/beam.md) | — | ✓ | Draw a beam line and label on every segment of a picked chain |
| [IVO:BRACING](en/commands/structure/bracing.md) | — | ✓ | Draw bracing details |
| [IVO:DIM2BRACING](en/commands/structure/dim2bracing.md) | `IVO:D2B` | ✓ | Convert linear dimensions into bracing |
| [IVO:SCHEDULE](en/commands/structure/schedule.md) | — | ✓ | Clean up member schedule table text |
| [IVO:STRUCTURALPALETTE](en/commands/structure/structuralpalette.md) | — | ✓ | Toggle the Structural palette |
| [IVO:SHOWSTRUCTURALPALETTE](en/commands/structure/showstructuralpalette.md) | — | — | Show the Structural palette |
| [IVO:HIDESTRUCTURALPALETTE](en/commands/structure/hidestructuralpalette.md) | — | — | Hide the Structural palette |
| [IVO:GENCOLUMN](en/commands/structure/gencolumn.md) | `IVO:GC` | — | Place a column at the ends of every selected beam, keeping the beams |
| [IVO:FOOTING](en/commands/structure/footing.md) | `IVO:FTG` | — | Draw footing outlines from the outer-face and centreline lines |
| [IVO:BOUNDARY](en/commands/structure/boundary.md) | `IVO:BND` | — | Rebuild a boundary from selected cyan and yellow lines |
| [IVO:BOUNDARYDUMP](en/commands/structure/boundary.md) | — | — | Report why a boundary came out wrong, without drawing anything |

## Civil

| Command | Alias | Ribbon | What it does |
|:---------|:------|:------:|:-------|
| [IVO:OUTLETELEVATION](en/commands/civil/outletelevation.md) | `IVO:OE` | ✓ | Calculate pipe outlet elevation from picked points |

## Detail Library

| Command | Alias | Ribbon | What it does |
|:---------|:------|:------:|:-------|
| [IVO:DETAILLIBRARY](en/commands/detail-library/detaillibrary.md) | — | ✓ | Open the detail library |
| [IVO:DETAILLIBRARYSETTINGS](en/commands/detail-library/detaillibrarysettings.md) | — | — | Configure Detail Library folders and cache from the command line |

## Settings

| Command | Alias | Ribbon | What it does |
|:---------|:------|:------:|:-------|
| [IVO:SETTINGS](en/commands/settings/settings.md) | — | ✓ | Open the plugin settings window |
| [IVO:OPENSETTINGSFOLDER](en/commands/settings/opensettingsfolder.md) | — | — | Open the folder holding settings, profiles, and presets |

## Help

| Command | Alias | Ribbon | What it does |
|:---------|:------|:------:|:-------|
| [IVO:LICENSE](en/commands/help/license.md) | — | ✓ | License management |
| [IVO:HELP](en/commands/help/help.md) | — | ✓ | Open this online documentation |
| [IVO:ABOUT](en/commands/help/about.md) | — | ✓ | Show plugin information |
| [IVO:COMMANDS](en/commands/help/commands.md) | — | — | Show the command list on the command line |

---

> [!NOTE]
> Almost every command above requires an **active license**. Exactly **seven** do not:
>
> [IVO:LICENSE](en/commands/help/license.md) · [IVO:ABOUT](en/commands/help/about.md) · [IVO:HELP](en/commands/help/help.md) · [IVO:COMMANDS](en/commands/help/commands.md) · [IVO:SETTINGS](en/commands/settings/settings.md) · [IVO:OPENSETTINGSFOLDER](en/commands/settings/opensettingsfolder.md) · [IVO:HIDESTRUCTURALPALETTE](en/commands/structure/hidestructuralpalette.md)
>
> The first six draw nothing. The seventh is on the list because refusing a command that means *stop using this* would only trap the user with a palette they cannot close.
