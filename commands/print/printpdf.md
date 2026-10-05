# IVO:PRINTPDF

> Melakukan cetak massal (batch print) layout sheet gambar terpilih ke format PDF.

## Cara Akses

- **Ribbon:** Tab IngenevoTools → Panel Print → Tombol Print PDF
- **Command Line:** `IVO:PRINTPDF`
- **Alias:** —

## Cara Penggunaan

1. **Simpan drawing lebih dulu.** Gambar yang belum pernah disimpan ditolak sebelum jendela terbuka, karena publish menunjuk sheet lewat berkas DWG di disk
2. Jalankan perintah `IVO:PRINTPDF`
3. Centang layout yang ingin dicetak, dan atur **urutannya** dengan tombol naik/turun. Kolom **Paper** dan **Plot Style** menunjukkan pengaturan tiap layout
4. Pilih mode keluaran:
   - **Multi-sheet** — semua layout digabung menjadi satu berkas PDF
   - **Single-sheet** — satu berkas PDF per layout
5. Tentukan **lokasi keluaran** (folder dan nama berkas). Folder yang belum ada akan dibuat
6. Pilih **plot style** yang dipakai untuk cetakan ini
7. Tekan **Print**. Jendela ditutup dan BricsCAD mulai mencetak
8. Hasilnya dilaporkan **di command line** — jumlah PDF yang dibuat, lalu satu baris per berkas

<!-- screenshot -->

## Tips & Catatan

> [!WARNING]
> Perintah ini membutuhkan **lisensi aktif**. Jalankan [IVO:LICENSE](commands/help/license.md) untuk mengaktifkan lisensi.

> [!NOTE]
> **Setelah mencetak tidak ada jendela apa pun**, berhasil maupun gagal. Kalau tidak ada PDF yang terbentuk, command line menulis `No PDF was produced.` beserta alasannya dan lokasi berkas jejak `%AppData%\IngenevoTools\printpdf-log.txt`. Lampirkan berkas itu saat melapor masalah cetak.

> [!NOTE]
> Kalau berkas dengan nama yang sama sudah ada, **BricsCAD sendiri** yang bertanya apakah berkas itu akan ditimpa. Kalau Anda menjawab **No**, berkas itu memang tidak ditulis, dan command line melaporkannya sebagai tidak dibuat — itu wajar, bukan kerusakan.

> [!NOTE]
> Pada mode **Single-sheet**, nama tiap berkas diturunkan dari nama layout. Kalau ada karakter yang tidak boleh dipakai di nama berkas, Anda ditanya **Adjust file names?** sebelum mencetak.

> [!NOTE]
> Plot style yang dipilih hanya dipakai untuk cetakan ini — plot style tiap layout dikembalikan seperti semula sesudahnya. Ukuran kertas selalu mengikuti page setup layout masing-masing.

> [!TIP]
> Gunakan [IVO:MATCHALLLAYOUTSETTINGS](commands/utilities/matchalllayoutsettings.md) terlebih dahulu untuk memastikan semua layout menggunakan page setup yang sama.

## Lihat Juga

- [IVO:MATCHALLLAYOUTSETTINGS](commands/utilities/matchalllayoutsettings.md) — menyeragamkan page setup sebelum mencetak
- [IVO:SORTLAYOUT](commands/sheet-manager/sortlayout.md) — menata urutan tab layout
