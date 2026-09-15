# About IngenevoTools

## Description

**Ingenevo Tools** is a BricsCAD plugin for drafting and engineering productivity: structural drawing, building sheets from ViewFrame blocks, filling title blocks in bulk from Excel, batch printing to PDF, and a set of drawing utilities.

The full command list is in the [Command List](en/command-list.md).

## Version

Plugin version at the time this documentation was written: **2.0.0**

> [!TIP]
> Do not rely on the number above — **the version actually installed on your machine** is always available via [`IVO:ABOUT`](en/commands/help/about.md) inside BricsCAD.

## Compatibility

| BricsCAD | .NET target | Status |
|:---------|:------------|:-------|
| V20 | .NET Framework 4.6.1 | ✅ Verified running |
| V21 | .NET Framework 4.6.1 | ⚙️ Built & packaged, not yet verified running |
| V22 | .NET Framework 4.8 | ⚙️ Built & packaged, not yet verified running |
| V23 | .NET Framework 4.8 | ✅ Verified running |
| V24 | .NET Framework 4.8 | ⚙️ Built & packaged, not yet verified running |
| V25 | .NET Framework 4.8 | ⚙️ Built & packaged, not yet verified running |
| V26 | .NET 8.0 | ✅ Verified running |

> [!NOTE]
> The three verified versions cover **all three .NET targets** the plugin uses. The remaining four each share a target with one that is already proven, so what is unverified is version-specific SDK behaviour — no longer how the plugin is built and loaded.

## Author

- **Company:** Ingenevo

> [!IMPORTANT]
> **The website and support email have not been filled in.** Please complete the two lines below before sharing this site with drafters — the [FAQ](en/faq.md) page directs readers here to contact the team.
>
> - **Website:** _(not filled in)_
> - **Support email:** _(not filled in)_

## Copyright

Copyright © 2026 Ingenevo. All rights reserved.

Ingenevo Tools is proprietary software. No permission is granted to copy, modify, or redistribute it without written consent from Ingenevo.

## Support

1. Check the [FAQ](en/faq.md) first — most field problems are covered there
2. Contact the Ingenevo team using the details above, attaching the relevant log file:

| Problem | File to attach |
|:--------|:---------------|
| Installation | `%LocalAppData%\Ingenevo\install-log.txt` |
| Licensing | `%AppData%\IngenevoTools\license-log.txt` |

## Documentation

This site is built with [Docsify](https://docsify.js.org/) and hosted on [GitHub Pages](https://pages.github.com/).
