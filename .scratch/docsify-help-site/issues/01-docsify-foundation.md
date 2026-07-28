# 01 — Docsify foundation & GitHub Pages scaffold

**What to build:** A working Docsify site that a user can open locally via `docsify serve` and see the "IngenevoTools" branded homepage. The entry point (`index.html`) is configured with all four plugins (dark/light toggle, search, copy-code, pagination), the navbar shows "IngenevoTools" branding and a language switcher placeholder, the sidebar has a placeholder structure, and `.nojekyll` disables Jekyll processing. The site is immediately deploy-ready to GitHub Pages at `https://farid-indocad.github.io/plugin-ingenevotools-help/`.

**Blocked by:** None — can start immediately.

**Status:** ready-for-agent

- [ ] Create `index.html` with Docsify CDN setup, configured `basePath`, `name: 'IngenevoTools'`, `loadSidebar: true`, `loadNavbar: true`, `subMaxLevel: 2`, and `search`, `auto2top`, `pagination` settings
- [ ] Include plugin scripts: `docsify-darklight-theme`, `docsify/plugins/search`, `docsify-copy-code`, `docsify-pagination`
- [ ] Create initial `README.md` (Beranda) with a welcome heading and plugin overview placeholder
- [ ] Create `_sidebar.md` with placeholder navigation structure
- [ ] Create `_navbar.md` with "IngenevoTools" title and language switcher (🇮🇩 / 🇬🇧)
- [ ] Create `.nojekyll` empty file
- [ ] Create `_media/` directory with a `.gitkeep` placeholder
- [ ] Verify `docsify serve` loads the site locally without errors
