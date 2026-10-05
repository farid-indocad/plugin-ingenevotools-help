# Catatan Rilis

Perubahan yang terlihat oleh drafter. Rincian teknis pemasangan dan build ada di repository plugin.

> [!TIP]
> Versi yang benar-benar terpasang di komputer Anda selalu bisa dilihat lewat [`IVO:ABOUT`](commands/help/about.md).

---

## 2.1.0 — rilis 28 September 2026

Versi minor pertama sesudah 2.0.0, terutama penyelarasan lisensi. Lisensi yang beredar tetap berlaku — tidak perlu lisensi baru.

### Ditambahkan

- **Kuota perangkat penuh kini mengarahkan ke portal pelanggan.** Saat aktivasi ditolak karena batas perangkat, jendela lisensi menawarkan membuka [portal pelanggan](https://app-licsvc.azurewebsites.net/portal), tempat Anda melepas mesin yang tidak dipakai lagi. Lihat [`IVO:LICENSE`](commands/help/license.md).

### Diubah

- **Plugin mengirim nama komputer, IP lokal, dan nama Windows ke server lisensi**, supaya tiap mesin tampil dengan namanya sendiri di portal. Tidak bisa dimatikan.

### Dihapus

- **`IVO:BOUNDARY`, `IVO:BND`, dan `IVO:BOUNDARYDUMP`.** Ketiganya alat untuk tahap pengembangan dan kini menjawab "Unknown command". Perintah terdekat yang tetap ada adalah [`IVO:FOOTING`](commands/structure/footing.md).

### Diperbaiki

- **Lisensi yang ditahan kini benar-benar menahan plugin**, dengan pesan "Your licence is on hold". Setelah tahanan dilepas, lisensi pulih sendiri saat BricsCAD dibuka ulang.
- **Tombol ribbon di BricsCAD V20 menampilkan ikon**, bukan tanda tanya.
- **Pick pertama [`IVO:COLUMN`](commands/structure/column.md) dan [`IVO:FRAMING`](commands/structure/framing.md) tidak lagi terkunci ORTHO.** Titik pertama bebas seperti pada `LINE`; ORTHO berlaku mulai titik kedua.

---

## 2.0.0 — penyegaran 22 September 2026

### Diperbaiki

- **[`IVO:PRINTPDF`](commands/print/printpdf.md) benar-benar menghasilkan PDF.** Sebelumnya perintah ini melaporkan sukses tanpa satu pun berkas tertulis. Kini PDF dibuat lewat publish bawaan BricsCAD:
  - hasilnya dilaporkan di command line, tanpa jendela apa pun sesudahnya
  - pertanyaan "timpa berkas?" kini datang dari BricsCAD sendiri
  - gambar yang belum pernah disimpan ditolak sebelum jendela terbuka

---

## 2.0.0 — penyegaran 17 September 2026

Pasang ulang dengan installer untuk mendapatkan preset CLEANUP kantor — preset hanya disemai saat pemasangan.

### Ditambahkan

- **Preset [`IVO:CLEANUP`](commands/utilities/cleanup.md) kantor ikut terpasang**: sebelas berkas, satu per builder (AVIA HOMES, DIXON, JGK, MAKAAN, METRICON, ORBIT HOMES QLD, REMMUS, SIMOND, TEMPO, TICK HOMES, VERONA).
- **Gaya per type untuk Column, Beam, dan Bracing** di [Pengaturan](settings.md): warna (ByLayer, ByBlock, atau indeks), layer, linetype, skala linetype, dan lineweight untuk yang digambar, serta warna dan text style untuk labelnya.

### Diubah

- **[`IVO:FRAMING`](commands/structure/framing.md), [`IVO:COLUMN`](commands/structure/column.md), [`IVO:BEAM`](commands/structure/beam.md), dan [`IVO:BRACING`](commands/structure/bracing.md) tidak lagi memunculkan palette Structural.** Buka palette-nya dengan [`IVO:STRUCTURALPALETTE`](commands/structure/structuralpalette.md).

### Dihapus

- **Preset contoh `cleanup-general.xml` tidak lagi dibuat.** Berkas yang sudah ada tidak dihapus — buang sendiri dari `%AppData%\IngenevoTools\Cleanup\` kalau tidak diperlukan.

### Diperbaiki

- **Kriteria warna `ByLayer` dan `ByBlock` di preset CLEANUP kini berfungsi.** Sebelumnya keduanya tidak pernah cocok dengan objek apa pun.

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
