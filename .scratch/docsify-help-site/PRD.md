# PRD: IngenevoTools Help — Docsify Documentation Site

## Problem Statement

IngenevoTools is a BricsCAD plugin with 36 commands across 14+ ribbon panels,
but it has **no end-user documentation site**. When users press the `IVO:HELP`
command (which opens a URL in their default browser), there is nothing to land
on. Drafters and engineers using the plugin in BricsCAD have no searchable,
browsable reference to learn how each command works, what options it accepts, or
how to troubleshoot issues. The existing `README.md` in the plugin repo is
developer-oriented and not suitable as a user-facing help resource.

## Solution

Build a **bilingual (Bahasa Indonesia / English) documentation website** using
**Docsify**, hosted on **GitHub Pages** at
`https://farid-indocad.github.io/plugin-ingenevotools-help/`. The site will
provide one dedicated page per command (36 pages), grouped by Ribbon Panel in a
collapsible sidebar, plus general-purpose pages (Beranda, Instalasi, Getting
Started, Settings, FAQ, Changelog, About). The site will support auto dark/light
theme toggle and include Search, Copy Code, and Pagination plugins. Bahasa
Indonesia is the default language with a switcher to English.

## User Stories

1. As a drafter using IngenevoTools, I want to type `IVO:HELP` and land on a
   documentation homepage, so that I can quickly find help without leaving my
   workflow.
2. As a new user, I want a Getting Started page, so that I can learn the basic
   workflow of IngenevoTools within minutes of installing it.
3. As a user, I want an Installation page with all 3 methods (NETLOAD, APPLOAD,
   Registry), so that I can choose the method that suits my environment.
4. As a user, I want to search for a command by name (e.g., "FRAMING"), so that
   I can jump directly to its documentation without browsing the sidebar.
5. As a user, I want each command page to show Cara Akses (Ribbon path + command
   line + alias), so that I know all the ways to invoke a command.
6. As a user, I want step-by-step usage instructions for each command, so that I
   can follow along while working in BricsCAD.
7. As a user, I want to see available options/parameters for a command, so that
   I understand what inputs are expected.
8. As a user, I want screenshots or GIFs showing the command in action, so that
   I can visually confirm I'm doing it right.
9. As a user, I want Tips & Catatan on each command page, so that I'm aware of
   edge cases, limitations, or best practices.
10. As a user, I want the sidebar to group commands by Ribbon Panel with
    collapsible sections, so that I can navigate intuitively based on how I see
    the plugin in BricsCAD.
11. As a user who prefers dark mode, I want the documentation to automatically
    match my OS theme preference, so that reading is comfortable.
12. As a user who prefers light mode, I want to manually toggle to light theme,
    so that I can override the default if needed.
13. As a user, I want pagination (prev/next) at the bottom of each page, so that
    I can read through related commands sequentially.
14. As a user, I want to copy command names from code blocks with one click, so
    that I can paste them directly into BricsCAD's command line.
15. As an Indonesian-speaking user, I want the documentation in Bahasa Indonesia
    by default, so that I can read in my native language.
16. As an English-speaking user, I want to switch the documentation to English,
    so that I can understand the content without a language barrier.
17. As a user experiencing issues, I want a FAQ/Troubleshooting page, so that I
    can resolve common problems without contacting support.
18. As a user, I want a Settings page explaining all options in `IVO:SETTINGS`,
    so that I can configure the plugin optimally.
19. As a user, I want a Changelog page, so that I can see what's new or fixed in
    each plugin version.
20. As a user, I want an About/Contact page, so that I know who made the plugin
    and how to reach support.
21. As a user on mobile or tablet, I want the documentation to be responsive, so
    that I can look up commands on any device.
22. As a user, I want the Beranda (homepage) to show a feature overview and
    quick links to the most important sections, so that I can orient myself
    immediately.
23. As a user exploring the Structural Palette commands, I want
    `IVO:STRUCTURALPALETTE`, `IVO:SHOWSTRUCTURALPALETTE`, and
    `IVO:HIDESTRUCTURALPALETTE` grouped together in the sidebar, so that I can
    find all related commands in one place.
24. As a user working with Framing, I want `IVO:FRAMING`, `IVO:COLUMN`, and
    `IVO:BEAM` grouped together, so that I understand the relationship between
    these commands.
25. As a user, I want command aliases (e.g., `IVO:SX` for `IVO:SAFEEXPLODE`)
    clearly documented, so that I can use shortcuts confidently.
26. As a user, I want the documentation to load instantly without a build step
    or server-side rendering, so that there's no waiting.

## Implementation Decisions

### Technology & Hosting

- **Docsify** as the documentation framework — client-side rendering, zero build
  step, Markdown-native.
- **GitHub Pages** serving from the root (`/`) of the `main` branch in the
  `plugin-ingenevotools-help` repository.
- Site URL: `https://farid-indocad.github.io/plugin-ingenevotools-help/`

### Bilingual Strategy

- **Bahasa Indonesia** content lives at the root level (default language).
- **English** content lives under an `/en/` directory with a mirrored folder
  structure.
- A language switcher in the navbar allows toggling between ID and EN.
- Each language has its own `_sidebar.md` and `_navbar.md`.

### Docsify Configuration & Plugins

- **docsify-darklight-theme** for auto dark/light toggle following OS
  preference.
- **docsify search plugin** for full-text search across all pages.
- **docsify-copy-code** for one-click code block copying.
- **docsify-pagination** for prev/next navigation at page bottom.

### Site Structure (Indonesian — root level)

```
/
├── index.html              (Docsify entry point)
├── README.md               (Beranda / Homepage)
├── _sidebar.md             (Sidebar navigation — ID)
├── _navbar.md              (Top navbar — ID)
├── .nojekyll               (Disable Jekyll processing)
├── instalasi.md
├── getting-started.md
├── settings.md
├── faq.md
├── changelog.md
├── about.md
├── _media/                 (Screenshots, GIFs, assets)
│
├── commands/
│   ├── structural-palette/
│   │   ├── structuralpalette.md
│   │   ├── showstructuralpalette.md
│   │   └── hidestructuralpalette.md
│   ├── block/
│   │   └── replaceblock.md
│   ├── framing/
│   │   ├── framing.md
│   │   ├── column.md
│   │   └── beam.md
│   ├── bracing/
│   │   └── bracing.md
│   ├── change-base-point/
│   │   └── changebasepoint.md
│   ├── layout/
│   │   ├── sortlayout.md
│   │   ├── bltscale.md
│   │   └── matchalllayoutsettings.md
│   ├── library/
│   │   ├── detaillibrary.md
│   │   └── detaillibrarysettings.md
│   ├── license/
│   │   ├── license.md
│   │   └── licenseinfo.md
│   ├── outlet-elevation/
│   │   └── outletelevation.md
│   ├── plot/
│   │   └── printpdf.md
│   ├── rectangle/
│   │   └── rectangle.md
│   ├── register/
│   │   └── editregister.md
│   ├── renumber-layout/
│   │   └── renumberlayout.md
│   ├── safe-explode/
│   │   ├── safeexplode.md
│   │   └── multisafeexplode.md
│   ├── selection/
│   │   ├── selectsimilarspecified.md
│   │   └── deselectsimilar.md
│   ├── settings-cmd/
│   │   └── settings.md
│   ├── solid2hatch/
│   │   └── solid2hatch.md
│   ├── title-block/
│   │   └── updatetitleblock.md
│   └── utility/
│       ├── about.md
│       ├── help.md
│       └── commands.md
│
└── en/                     (English mirror)
    ├── README.md
    ├── _sidebar.md
    ├── _navbar.md
    ├── installation.md
    ├── getting-started.md
    ├── settings.md
    ├── faq.md
    ├── changelog.md
    ├── about.md
    └── commands/           (Same structure as ID)
        └── ...
```

### Command Page Template

Every command page follows a consistent template:

1. **Title** — `IVO:COMMANDNAME`
2. **Description** — One-line summary
3. **Cara Akses / How to Access** — Ribbon path, command line, alias (if any)
4. **Cara Penggunaan / How to Use** — Step-by-step instructions
5. **Opsi / Parameter** — Table of options (if applicable)
6. **Screenshot / GIF** — Placeholder comment initially
7. **Tips & Catatan / Tips & Notes** — Edge cases, best practices

### Branding

- Navbar title: **"IngenevoTools"** (text only, no logo image)
- No custom domain — using default GitHub Pages URL

### Media Assets

- All media stored in `/_media/` directory
- Command pages use `<!-- screenshot -->` placeholder comments initially
- Screenshots and GIFs to be added incrementally by the user

## Testing Decisions

Since this is a static documentation site (no application logic), traditional
unit/integration testing does not apply. Verification is instead:

- **Local preview**: Run `docsify serve` locally to verify all pages render
  correctly, sidebar navigation works, search indexes properly, and language
  switching functions.
- **Link validation**: Manually verify that all internal links in sidebars and
  cross-references resolve to existing pages.
- **GitHub Pages deployment**: After pushing to `main`, verify the live site
  loads at `https://farid-indocad.github.io/plugin-ingenevotools-help/`.
- **Cross-browser**: Spot-check in Chrome, Firefox, and Edge to ensure theme
  toggle and search work.
- **Responsive check**: Verify the site renders well on mobile viewport sizes.

The primary "seam" for testing is the **local Docsify dev server**
(`docsify serve`), which mirrors the exact behavior of the GitHub Pages
deployment.

## Out of Scope

- **Content writing for step-by-step instructions**: The scaffold will include
  template placeholders. Detailed usage instructions for each of the 36 commands
  require domain expertise and BricsCAD screenshots that must be authored by the
  plugin developer.
- **Custom domain setup** (`help.ingenevo.com` or similar): URL will use default
  GitHub Pages. Custom domain can be added later.
- **Logo/icon design**: Branding is text-only ("IngenevoTools") for now.
- **CI/CD pipeline**: Docsify requires no build step; deployment is direct push
  to `main`.
- **Analytics integration** (Google Analytics, etc.): Can be added later via
  Docsify plugin.
- **Comments/feedback system**: No user feedback mechanism on the help pages.
- **PDF export**: No offline PDF generation of documentation.
- **Versioned documentation** (docs per plugin version): Single latest version
  for now.

## Further Notes

- The `IVO:HELP` command in the plugin already supports opening a configurable
  URL via `IVO:SETTINGS > General > Help URL`. Once the site is live, the
  default Help URL in the plugin should be updated to point to
  `https://farid-indocad.github.io/plugin-ingenevotools-help/`.
- The English translation (`/en/` folder) will initially contain the same
  template structure as the Indonesian root, but with English headings and
  placeholder text. Full English translation is a follow-up effort.
- The repository `plugin-ingenevotools-help` already exists in the workspace at
  `d:\FARID\source\repos\ingenevo\ingenevo-plugin\plugin-ingenevotools-help\`
  and is currently empty (aside from `.agents` config). All Docsify files will
  be created here.
