# 07 — English mirror: general-purpose pages

**What to build:** The `/en/` directory with English versions of all 7 general-purpose pages, its own `_sidebar.md` and `_navbar.md`. The language switcher in the root navbar toggles between Indonesian root (`/`) and English (`/en/`). A user clicking "🇬🇧 English" lands on the English homepage and can navigate all English general pages. The English navbar's "🇮🇩 Bahasa Indonesia" link returns to the Indonesian root.

**Blocked by:** 02 — Indonesian general-purpose pages

**Status:** ready-for-agent

- [ ] Create `en/README.md` — English homepage mirroring Indonesian Beranda content
- [ ] Create `en/installation.md` — English translation of `instalasi.md`
- [ ] Create `en/getting-started.md` — English translation of `getting-started.md`
- [ ] Create `en/settings.md` — English translation of `settings.md`
- [ ] Create `en/faq.md` — English translation of `faq.md`
- [ ] Create `en/changelog.md` — English translation of `changelog.md`
- [ ] Create `en/about.md` — English translation of `about.md`
- [ ] Create `en/_sidebar.md` — English sidebar navigation (same structure, English labels)
- [ ] Create `en/_navbar.md` — English navbar with language switcher pointing back to Indonesian root
- [ ] Update root `_navbar.md` language switcher to link to `/en/`
- [ ] Verify language switching works bidirectionally in `docsify serve`
