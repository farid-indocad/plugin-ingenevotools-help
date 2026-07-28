# IVO:SELECTSIMILARSPECIFIED

> Memilih entitas sejenis berdasarkan filter properti yang dipilih (layer, warna, jenis garis, dll.).

## Cara Akses

- **Ribbon:** Tab Ingenevo Tools → Panel Selection → Tombol Select Similar Specified
- **Command Line:** `IVO:SELECTSIMILARSPECIFIED`
- **Alias:** —

## Cara Penggunaan

1. Pilih satu entitas sebagai referensi
2. Jalankan perintah `IVO:SELECTSIMILARSPECIFIED`
3. Pilih filter properti yang ingin dicocokkan:
   - Layer
   - Warna (Color)
   - Jenis garis (Linetype)
   - Tipe entitas
   - Dan lainnya
4. Semua entitas dalam gambar yang cocok dengan filter akan dipilih

<!-- screenshot -->

## Tips & Catatan

> [!TIP]
> Berbeda dari SELECTSIMILAR bawaan BricsCAD, perintah ini memungkinkan Anda memilih filter properti mana yang digunakan untuk pencocokan.

> [!TIP]
> Gunakan [IVO:DESELECTSIMILAR](commands/selection/deselectsimilar.md) untuk mengurangi entitas sejenis dari seleksi yang sudah ada.
