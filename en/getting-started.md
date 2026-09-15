# Getting Started

This page follows one drawing from start to print. The **order** is the point — it is the part that is visible neither on the ribbon nor in the sidebar.

> [!NOTE]
> Haven't installed the plugin yet? Start with [Installation](en/installation.md).

---

## 1. Activate your license

Type [`IVO:LICENSE`](en/commands/help/license.md) and activate. Without it almost every command is refused — see the [Command List](en/command-list.md) for the seven exceptions.

## 2. Pick a settings profile

Open [`IVO:SETTINGS`](en/commands/settings/settings.md). The installer already ships three office-standard profiles — **Default**, **Intrax**, and **IndoCAD** — so you do not have to build one from scratch.

The profile decides paper size, sheet name prefix, title block name, and the column/beam/bracing types. **The commands that follow read from here and will not ask again**, so a mistake at this step propagates through the whole drawing.

## 3. Prepare the ViewFrames in model space

Draw a **ViewFrame** block for every sheet to be produced, then select them all and run [`IVO:RENUMBERVIEWFRAME`](en/commands/sheet-manager/renumberviewframe.md).

Numbering follows **left-to-right position**, not the order you clicked. Do this **before** the next step, because layout names are derived from the ViewFrame numbers.

## 4. Build the sheets

| Situation | Command |
|:----------|:--------|
| New drawing, no layouts yet | [`IVO:CREATELAYOUT`](en/commands/sheet-manager/createlayout.md) — builds every layout from scratch |
| Layouts already exist, you want more | [`IVO:ADDLAYOUT`](en/commands/sheet-manager/addlayout.md) — adds only, deletes nothing |

> [!WARNING]
> `IVO:CREATELAYOUT` **deletes every existing layout** first. On a drawing whose sheets somebody else has already worked on, what you want is almost always `IVO:ADDLAYOUT`.

## 5. Fill title blocks from Excel

Three commands, in order:

1. [`IVO:CREATEREGISTER`](en/commands/sheet-manager/createregister.md) — creates the Excel register next to the drawing
2. [`IVO:EDITREGISTER`](en/commands/sheet-manager/editregister.md) — opens it for you to fill in
3. [`IVO:UPDATETITLEBLOCK`](en/commands/sheet-manager/updatetitleblock.md) — writes its contents into each layout's title block attributes

Excel rows are matched to layouts **by name**. If a title block comes out empty, it is usually because the layout name and the row name are not identical.

## 6. Tidy up before printing

| Command | What it does |
|:--------|:-------------|
| [`IVO:RENUMBERLAYOUT`](en/commands/sheet-manager/renumberlayout.md) | Renumbers layout names sequentially |
| [`IVO:SORTLAYOUT`](en/commands/sheet-manager/sortlayout.md) | Orders the tabs to follow those names |
| [`IVO:MATCHALLLAYOUTSETTINGS`](en/commands/utilities/matchalllayoutsettings.md) | Unifies printer, paper, and scale across every layout |

## 7. Print

[`IVO:PRINTPDF`](en/commands/print/printpdf.md) — tick the sheets, set their order, choose one combined PDF or one PDF per sheet.

---

## Habits that save time

> [!TIP]
> **Select first, then run the command.** Most commands honour objects you selected before typing, so you do not have to select twice.

> [!TIP]
> **Use the aliases.** `IVO:SX` for Safe Explode, `IVO:MSX` for Multi Safe Explode, `IVO:CRL` for Create Layout. They are all listed in the [Command List](en/command-list.md).

> [!TIP]
> **Type `IVO:` and let BricsCAD's autocomplete do the rest.** If you forget a command name, [`IVO:COMMANDS`](en/commands/help/commands.md) prints the whole list without opening a browser.

> [!NOTE]
> The structural commands — [Framing](en/commands/structure/framing.md), [Column](en/commands/structure/column.md), [Beam](en/commands/structure/beam.md), [Bracing](en/commands/structure/bracing.md), [Footing](en/commands/structure/footing.md) — take their types from the Structural palette. Open it with [`IVO:STRUCTURALPALETTE`](en/commands/structure/structuralpalette.md) and check the types before you start drawing.
