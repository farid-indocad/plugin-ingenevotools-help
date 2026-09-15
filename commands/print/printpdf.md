# IVO:PRINTPDF

> Melakukan cetak massal (batch print) layout sheet gambar terpilih ke format PDF.

## Cara Akses

- **Ribbon:** Tab Ingenevo Tools → Panel Print → Tombol Print PDF
- **Command Line:** `IVO:PRINTPDF`
- **Alias:** —

## Cara Penggunaan

1. Jalankan perintah `IVO:PRINTPDF`
2. Centang layout yang ingin dicetak, dan atur **urutannya** dengan tombol naik/turun
3. Pilih **printer** dan **ukuran kertas**, lalu **plot style** yang diinginkan
4. Tentukan folder output, dan pilih mode keluaran:
   - **Single** — semua layout digabung menjadi satu berkas PDF
   - **Multi** — satu berkas PDF per layout
5. Tekan **Print**. Kalau berkas dengan nama itu sudah ada, Anda ditanya lebih dulu sebelum ditimpa
6. Setelah selesai, Anda ditawari membuka berkas atau foldernya langsung

<!-- screenshot -->

## Tips & Catatan

> [!WARNING]
> Perintah ini membutuhkan **lisensi aktif**. Jalankan [IVO:LICENSE](commands/help/license.md) untuk mengaktifkan lisensi.

> [!IMPORTANT]
> Pastikan printer/plotter PDF sudah dikonfigurasi di BricsCAD sebelum menjalankan perintah ini.

> [!TIP]
> Gunakan [IVO:MATCHALLLAYOUTSETTINGS](commands/utilities/matchalllayoutsettings.md) terlebih dahulu untuk memastikan semua layout menggunakan page setup yang sama.

## Lihat Juga

- [IVO:MATCHALLLAYOUTSETTINGS](commands/utilities/matchalllayoutsettings.md) — menyeragamkan page setup sebelum mencetak
- [IVO:SORTLAYOUT](commands/sheet-manager/sortlayout.md) — menata urutan tab layout
