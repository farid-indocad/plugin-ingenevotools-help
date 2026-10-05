# IVO:CLEANUP

> Filters the selected objects against a preset and highlights the matches. It deletes nothing.

## How to Access

- **Ribbon:** IngenevoTools Tab → Utilities Panel → Cleanup button
- **Command Line:** `IVO:CLEANUP`
- **Alias:** —

## How to Use

1. Run `IVO:CLEANUP`
2. **Select the objects you want to filter.** A selection made before running the command is used straight away, and this step is skipped
3. Pick a **preset file** from the numbered command-line menu:

```
Select a preset configuration file [1-<AVIA HOMES>/2-<DIXON>/3-<JGK>/.../11-<VERONA>]:
```

4. Pick the **preset** you want from that file:

```
Select a cleanup preset [1-<SITE PLAN>/2-<FLOOR PLAN>/3-<ELEVATIONS>]:
```

5. Objects matching the preset's criteria become **highlighted** (the active selection)
6. The command line reports the count, e.g. `Successfully cleanup 15 object(s) based on the preset: FLOOR PLAN`

<!-- screenshot -->

## Tips & Notes

> [!WARNING]
> This command requires an **active license**. Run [IVO:LICENSE](en/commands/help/license.md) to activate yours.

> [!NOTE]
> This command **deletes nothing, changes nothing, and moves nothing.** It filters, then selects. Once the objects are highlighted, the next move is yours — press `Delete`, change their layer, whatever you need.

> [!TIP]
> **The installer brings eleven office preset files**, one per builder: AVIA HOMES, DIXON, JGK, MAKAAN, METRICON, ORBIT HOMES QLD, REMMUS, SIMOND, TEMPO, TICK HOMES, and VERONA. The name in the menu is the file name without the `cleanup-` prefix.

> [!NOTE]
> Presets live as XML files in `%AppData%\IngenevoTools\Cleanup\`. Open the folder with [IVO:OPENSETTINGSFOLDER](en/commands/settings/opensettingsfolder.md).
>
> The eleven office files are **overwritten every time the installer runs**, so do not edit them in place. If you need your own variant, save it under another name (for example `cleanup-METRICON-yourname.xml`) — the installer never touches a file name it did not bring.
>
> If the folder is empty, the command stops and **names the folder the presets belong in**.

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
