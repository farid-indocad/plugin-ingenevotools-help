# IVO:DIM2BRACING

> Mengubah dimension linear/aligned terpilih menjadi bracing berikut label-nya, lalu menghapus dimension-nya.

## Cara Akses

- **Ribbon:** Tab Ingenevo Tools → Panel Structure → Tombol Dim to Bracing
- **Command Line:** `IVO:DIM2BRACING`
- **Alias:** `IVO:D2B`

## Cara Penggunaan

1. Pilih dimension **aligned** atau **linear** yang ingin diubah (boleh sebelum perintah dijalankan — preselection dihormati)
2. Jalankan perintah `IVO:DIM2BRACING` atau `IVO:D2B`
3. Setiap dimension terpilih diganti menjadi bracing dengan tipe yang sedang aktif, dan dimension aslinya **dihapus**
4. Command line melaporkan hasilnya:

```
[Dim2Bracing] Converted 8 dimension(s) to "ANGLE 50x50x5" bracing, 2 skipped, 0 failed.
```

<!-- screenshot -->

## Tips & Catatan

> [!WARNING]
> Perintah ini membutuhkan **lisensi aktif**. Jalankan [IVO:LICENSE](commands/help/license.md) untuk mengaktifkan lisensi.

> [!NOTE]
> Tipe bracing yang dipakai adalah tipe yang sedang aktif di palette Structural tab **Bracing** — perintah ini tidak menanyakannya. Atur tipenya lebih dulu lewat [IVO:BRACING](commands/structure/bracing.md) atau `IVO:SETTINGS` → **Structure > Bracing**.

> [!NOTE]
> Dimension yang **dihitung sebagai skipped** adalah yang bukan tipe aligned/linear — misalnya angular, radial, atau diameter. Dimension itu dibiarkan utuh, tidak dihapus.

> [!TIP]
> Seluruh seleksi diproses sebagai **satu langkah undo**. Kalau hasilnya tidak sesuai harapan, satu `U` mengembalikan semua dimension yang terhapus sekaligus.

## Lihat Juga

- [IVO:BRACING](commands/structure/bracing.md) — menggambar bracing langsung dengan menunjuk titik
- [IVO:STRUCTURALPALETTE](commands/structure/structuralpalette.md) — membuka palette tempat tipe bracing diatur
