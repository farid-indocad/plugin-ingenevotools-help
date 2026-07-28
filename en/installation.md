# Installation

Guide to installing the IngenevoTools plugin in BricsCAD.

## Prerequisites

- **BricsCAD** V20, V21, V22, V23, V24, V25, or V26
- **Windows** operating system (64-bit)

## Method 1: NETLOAD (Recommended for Development)

The quickest method to load the plugin manually.

1. Open BricsCAD
2. Type the `NETLOAD` command in the command line
3. Select the assembly output file:

```
bin\Debug\<Version>\BricsCadPlugin.App.dll
```

> [!NOTE]
> Replace `<Version>` with your BricsCAD version (e.g., `V23`).

4. The plugin will be active immediately. The **Ingenevo Tools** tab will appear in the Ribbon.

## Method 2: APPLOAD (Persistent per Session)

The plugin will be loaded automatically every time BricsCAD is opened.

1. Type the `APPLOAD` command in the BricsCAD command line
2. Click the **Add** button and select `BricsCadPlugin.App.dll`
3. Add it to the **Startup Suite** so the plugin loads automatically

## Method 3: Registry DemandLoad (Production Deployment)

For production distribution to multiple computers.

1. Open the file `deploy/registry/register-plugin.reg`
2. Adjust the plugin installation folder path
3. Import the `.reg` file to Windows registry (double-click or `regedit`)

> [!WARNING]
> Make sure the paths in the `.reg` file match the plugin installation location on the target computer.

## Verify Installation

After loading the plugin, verify by:

1. Check that the **Ingenevo Tools** tab appears in the Ribbon
2. Type `IVO:COMMANDS` to see the list of commands
3. Type `IVO:ABOUT` to see plugin version information

<!-- screenshot -->
