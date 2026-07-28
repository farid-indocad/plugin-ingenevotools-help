# 02 — Indonesian general-purpose pages

**What to build:** The 7 non-command pages in Bahasa Indonesia, each with substantive template content that a user can read and navigate via the sidebar. The sidebar (`_sidebar.md`) is updated with links to all general pages. A user visiting the site can browse Beranda → Instalasi → Getting Started → Settings → FAQ → Changelog → About without hitting a broken link.

**Blocked by:** 01 — Docsify foundation & GitHub Pages scaffold

**Status:** ready-for-agent

- [ ] Create/update `README.md` (Beranda) — plugin overview, fitur utama, quick links to Instalasi and Getting Started
- [ ] Create `instalasi.md` — 3 metode instalasi (NETLOAD, APPLOAD, Registry) dengan prasyarat, disalin dari README plugin
- [ ] Create `getting-started.md` — panduan workflow dasar pertama kali (load plugin → buka ribbon → jalankan command pertama)
- [ ] Create `settings.md` — penjelasan opsi-opsi di `IVO:SETTINGS` (placeholder sections per kategori: General, Structure > Column, Structure > Bracing)
- [ ] Create `faq.md` — masalah umum & solusi (placeholder: "eLockViolation", "plugin tidak muncul di ribbon", "lisensi expired")
- [ ] Create `changelog.md` — template riwayat versi dengan format tanggal dan kategori (Added/Changed/Fixed)
- [ ] Create `about.md` — info pembuat, versi plugin, hak cipta, cara kontak support
- [ ] Update `_sidebar.md` with links to all general pages above the command sections
