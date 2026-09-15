# IVO:CLEANUP

> Filters the selected objects against a preset and highlights the matches. It deletes nothing.

## How to Access

- **Ribbon:** Ingenevo Tools Tab → Utilities Panel → Cleanup button
- **Command Line:** `IVO:CLEANUP`
- **Alias:** —

## How to Use

1. Select the objects you want to filter (a selection made before running the command is honoured)
2. Run `IVO:CLEANUP`
3. Pick a **preset file** from the numbered command-line menu:

```
Select a preset configuration file [1-<structural>/2-<mep>]:
```

4. Pick the **preset** you want from that file:

```
Select a cleanup preset [1-<Remove Dimension Lines>/2-<Remove Red Lines>]:
```

5. Objects matching the preset's criteria become **highlighted** (the active selection)
6. The command line reports the count, e.g. `Successfully cleanup 15 objects based on the preset: Remove Dimension Lines`

<!-- screenshot -->

## Tips & Notes

> [!WARNING]
> This command requires an **active license**. Run [IVO:LICENSE](en/commands/help/license.md) to activate yours.

> [!NOTE]
> This command **deletes nothing, changes nothing, and moves nothing.** It filters, then selects. Once the objects are highlighted, the next move is yours — press `Delete`, change their layer, whatever you need.

> [!TIP]
> Presets live as XML files in `%AppData%\IngenevoTools\Cleanup\`. Open the folder with [IVO:OPENSETTINGSFOLDER](en/commands/settings/opensettingsfolder.md). If that folder is still empty, the plugin copies example presets into it automatically the first time you run the command.

> [!NOTE]
> One preset can hold **several filters at once**, combined with **OR** between filters and **AND** within a filter. A preset with two filters:
>
> ```
> Filter 1: entityType=LINE, layer=0, linetype=Continuous
> Filter 2: entityType=LINE, layer=Defpoints
> ```
>
> An object matches if it is a LINE on layer `0` with linetype `Continuous`, **or** a LINE on layer `Defpoints`.

> [!NOTE]
> Text comparisons are **case-insensitive** and use **no wildcards** — `defpoints` equals `Defpoints`, but `Dim*` matches nothing.

## See Also

- [IVO:SELECTSIMILARSPECIFIED](en/commands/utilities/selectsimilarspecified.md) — select similar entities by property filter
- [IVO:DESELECTSIMILAR](en/commands/utilities/deselectsimilar.md) — deselect similar entities
