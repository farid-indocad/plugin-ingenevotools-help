# IVO:SCHEDULE

> Membuka palette Structural pada tab Member Schedule, untuk merapikan isi teks tabel schedule.

## Cara Akses

- **Ribbon:** Tab Ingenevo Tools → Panel Structure → Tombol Schedule
- **Command Line:** `IVO:SCHEDULE`
- **Alias:** —

## Cara Penggunaan

1. Jalankan perintah `IVO:SCHEDULE` — palette **Structural** terbuka pada tab **Schedule**
2. Di drawing, pilih target yang ingin dikerjakan:
   - **Klik beberapa sel** di dalam tabel schedule → hanya sel itu yang diproses
   - **Pilih tabelnya** tanpa masuk ke sel mana pun → seluruh tabel diproses (baris header dilewati)
3. Tekan salah satu dari empat tombol di palette:

| Tombol | Fungsi |
|:-------|:-------|
| **Clean** | Merapikan isi teks sel yang dipilih ke format baku |
| **Copy** | Menyalin isi sel ke clipboard **apa adanya**, tanpa dibersihkan |
| **Paste** | Menempelkan isi clipboard ke sel apa adanya |
| **Paste cleaned** | Menempelkan isi clipboard sambil merapikannya |

4. Hasilnya ditulis di baris status palette **dan** di command line, berikut rentang sel yang benar-benar dikerjakan

<!-- screenshot -->

## Tips & Catatan

> [!WARNING]
> Perintah ini membutuhkan **lisensi aktif**. Jalankan [IVO:LICENSE](commands/help/license.md) untuk mengaktifkan lisensi.

> [!NOTE]
> Fitur ini **hanya menyentuh isi teks sel**. Tinggi baris, tinggi huruf, font, alignment, warna dan lineweight grid tabel **tidak diubah sama sekali**.

> [!TIP]
> **Copy selalu menyalin apa adanya, dan itu disengaja.** Kalau penyalinan ikut membersihkan, isi clipboard akan berbeda dari yang terlihat di layar. Yang benar-benar perlu dibersihkan adalah teks mentah yang **masuk** lewat paste — karena itu ada **Paste cleaned**, bukan "Copy cleaned".

> [!NOTE]
> Semua aksi dijalankan lewat tombol palette, bukan lewat command line. Saat sel tabel sedang aktif, BricsCAD menyerahkan keyboard ke editor sel — perintah yang diketik di command line tidak akan diproses, dan malah bisa mendarat di dalam sel. Itulah sebabnya hanya ada **satu** perintah di sini, yaitu untuk membuka palette-nya.

> [!TIP]
> Palette tetap terbuka sampai Anda menutupnya sendiri, jadi Anda bisa berpindah dari satu tabel ke tabel lain tanpa menjalankan perintah ini lagi.

## Lihat Juga

- [IVO:STRUCTURALPALETTE](commands/structure/structuralpalette.md) — membuka palette Structural (tab terakhir yang aktif)
- [IVO:SHOWSTRUCTURALPALETTE](commands/structure/showstructuralpalette.md) — menampilkan palette Structural
