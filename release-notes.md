# Catatan Rilis

Perubahan yang terlihat oleh drafter. Rincian teknis pemasangan dan build ada di repository plugin.

> [!TIP]
> Versi yang benar-benar terpasang di komputer Anda selalu bisa dilihat lewat [`IVO:ABOUT`](commands/help/about.md).

---

## 2.0.0 — penyegaran 15 September 2026

Nomor versinya tetap 2.0.0; yang diperbarui adalah berkas installer-nya.

**Bagi drafter tidak ada yang berubah.** Yang Anda terima tetap `IngenevoToolsSetup.exe` dengan jendela, tombol Reinstall, dan pesan "tutup dan buka lagi BricsCAD" yang sama. Penyegaran ini menambah berkas terpisah untuk keperluan tim IT.

---

## 2.0.0 — penyegaran 14 September 2026

### Ditambahkan

- **Profil pengaturan standar kantor ikut terpasang.** Installer menanam profil **Default**, **Intrax**, dan **IndoCAD**, sehingga drafter baru langsung punya pengaturan kantor tanpa menyusunnya sendiri. Lihat [Pengaturan](settings.md).
- **Editor aturan ekstraksi title block** di `IVO:SETTINGS`, sehingga aturan pembacaan title block tidak perlu lagi diubah dengan mengedit berkas XML secara manual.
- **Uninstaller yang bisa ditemukan sendiri** di folder plugin, selain lewat Settings › Apps.

### Diubah

- **Pemasangan kini lewat installer**, menggantikan jalur logon script. Empat langkah, tanpa hak Administrator — lihat [Instalasi](instalasi.md).

---

## 2.0.0 — rilis 18 Agustus 2026

Rilis pertama IngenevoTools sebagai plugin .NET, menggantikan plugin AutoLISP sebelumnya.

### Lisensi

- **Trial 14 hari** yang bisa dimulai sendiri dari dalam plugin lewat [`IVO:LICENSE`](commands/help/license.md)

### Perintah

- **Struktur** — [`IVO:FRAMING`](commands/structure/framing.md) (rantai ala LINE: column di tiap vertex, beam di tiap segmen), [`IVO:COLUMN`](commands/structure/column.md), [`IVO:BEAM`](commands/structure/beam.md), [`IVO:BRACING`](commands/structure/bracing.md)
- **Sheet Manager** — [`IVO:CREATELAYOUT`](commands/sheet-manager/createlayout.md), [`IVO:ADDLAYOUT`](commands/sheet-manager/addlayout.md), [`IVO:SORTLAYOUT`](commands/sheet-manager/sortlayout.md), [`IVO:RENUMBERLAYOUT`](commands/sheet-manager/renumberlayout.md), [`IVO:RENUMBERVIEWFRAME`](commands/sheet-manager/renumberviewframe.md)
- **Detail Library** — [`IVO:DETAILLIBRARY`](commands/detail-library/detaillibrary.md) dengan thumbnail yang dirender sendiri
- **Cetak & register** — [`IVO:PRINTPDF`](commands/print/printpdf.md), [`IVO:CREATEREGISTER`](commands/sheet-manager/createregister.md), [`IVO:EDITREGISTER`](commands/sheet-manager/editregister.md), [`IVO:UPDATETITLEBLOCK`](commands/sheet-manager/updatetitleblock.md)
- **Gambar & seleksi** — [`IVO:RECTANGLE`](commands/utilities/rectangle.md) dengan CornerSnap, [`IVO:SELECTSIMILARSPECIFIED`](commands/utilities/selectsimilarspecified.md), [`IVO:DESELECTSIMILAR`](commands/utilities/deselectsimilar.md)
- **Lain-lain** — [`IVO:SCHEDULE`](commands/structure/schedule.md), [`IVO:OUTLETELEVATION`](commands/civil/outletelevation.md), dan perintah utilitas lainnya

Daftar lengkapnya ada di [Daftar Command](daftar-command.md).

### Pengaturan

- **Profil bernama**, bisa ditukar dari dalam jendela Settings

### Kompatibilitas

- BricsCAD V20 sampai V26 — lihat [Tentang](about.md) untuk status pengujian tiap versi
