# 09 — Local preview verification & deploy readiness

**What to build:** A verified, deploy-ready Docsify site. Run `docsify serve` and systematically confirm that every aspect of the site works end-to-end. Fix any broken links, rendering issues, or plugin malfunctions discovered during verification. After this ticket, the site can be `git push`-ed to `main` and will work on GitHub Pages without further changes.

**Blocked by:** 02, 03, 04, 05, 06, 07, 08 — All content tickets

**Status:** ready-for-agent

- [ ] Run `docsify serve` and verify the site loads without console errors
- [ ] Verify all 7 Indonesian general-purpose pages render and are reachable from the sidebar
- [ ] Verify all 36 Indonesian command pages render and are reachable from their collapsible sidebar groups
- [ ] Verify all 7 English general-purpose pages render and are reachable from the English sidebar
- [ ] Verify all 36 English command pages render and are reachable from the English sidebar
- [ ] Verify dark/light theme toggle works and follows OS preference on initial load
- [ ] Verify search plugin indexes all pages and returns results for command names (e.g., "FRAMING", "SAFEEXPLODE")
- [ ] Verify copy-code button appears on code blocks and copies content to clipboard
- [ ] Verify pagination (prev/next) links appear at the bottom of each page and navigate correctly
- [ ] Verify language switcher toggles between Indonesian and English correctly in both directions
- [ ] Verify responsive layout on mobile viewport (≤768px width)
- [ ] Fix any issues discovered during verification
- [ ] Confirm site is ready for `git push origin main` → GitHub Pages deployment
