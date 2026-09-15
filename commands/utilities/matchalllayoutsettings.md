# IVO:MATCHALLLAYOUTSETTINGS

> Menyalin page setup layout yang sedang aktif ke seluruh layout lain.

## Cara Akses

- **Ribbon:** Tab Ingenevo Tools → Panel Utilities → Tombol Match Layout Settings
- **Command Line:** `IVO:MATCHALLLAYOUTSETTINGS`
- **Alias:** `IVO:MALS`

## Cara Penggunaan

1. **Pindah ke tab layout** yang page setup-nya ingin dijadikan acuan — perintah ini tidak bisa dijalankan dari tab Model
2. Jalankan perintah `IVO:MATCHALLLAYOUTSETTINGS` atau `IVO:MALS`
3. Muncul konfirmasi Yes/No yang menyebut layout acuannya
4. Tekan **Enter** untuk menerapkan (default **Yes**), atau jawab **No** untuk membatalkan

<!-- screenshot -->

## Tips & Catatan

> [!WARNING]
> Perintah ini membutuhkan **lisensi aktif**. Jalankan [IVO:LICENSE](commands/help/license.md) untuk mengaktifkan lisensi.

> [!IMPORTANT]
> Perintah ini **menimpa page setup di semua layout lain**. Pastikan layout yang aktif sudah benar printer, ukuran kertas, dan skalanya sebelum menjawab Yes.

> [!NOTE]
> Harus dijalankan dari **tab layout**, bukan dari tab **Model**. Model space tidak punya page setup untuk disalin.

> [!TIP]
> Seluruh perubahan adalah **satu langkah undo** — satu `U` mengembalikan page setup semua layout sekaligus kalau hasilnya tidak sesuai.

> [!TIP]
> Jalankan perintah ini sebelum [IVO:PRINTPDF](commands/print/printpdf.md) supaya seluruh sheet tercetak dengan printer dan ukuran kertas yang seragam.

## Lihat Juga

- [IVO:PRINTPDF](commands/print/printpdf.md) — cetak massal layout ke PDF
- [IVO:BLTSCALE](commands/utilities/bltscale.md) — menyeragamkan linetype scaling di semua layout
