# FAQ / Troubleshooting

Frequently asked questions and common troubleshooting procedures.

---

## Plugin tab does not appear on Ribbon

**Symptom:** After loading the plugin, the "Ingenevo Tools" tab is missing from the Ribbon.

**Solution:**
1. Ensure you loaded the correct `BricsCadPlugin.App.dll` matching your BricsCAD version.
2. Check the command line output for loading errors.
3. Restart BricsCAD and reload the assembly.

---

## Error: eLockViolation

**Symptom:** `eLockViolation` error appears when clicking palette controls.

**Solution:**
Ensure you are using the latest plugin build with proper transactional locking helpers enabled for modeless palette interactions.

---

## License expired or invalid

**Symptom:** Premium features restricted due to license error.

**Solution:**
1. Run `IVO:LICENSE` to open the license activation modal and check current status.

---

> [!TIP]
> Contact support if your issue is not listed here (see [About](en/about.md)).
