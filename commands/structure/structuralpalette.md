# IVO:STRUCTURALPALETTE

> Toggle visibilitas palette Structural (tab Framing + Bracing) tanpa memulai pick loop; tab terakhir dipertahankan.

## Cara Akses

- **Ribbon:** Tab Ingenevo Tools → Panel Structure → Tombol Structural Palette
- **Command Line:** `IVO:STRUCTURALPALETTE`
- **Alias:** —

## Cara Penggunaan

1. Jalankan perintah `IVO:STRUCTURALPALETTE`
2. Jika palette Structural sedang tersembunyi, palette akan ditampilkan
3. Jika palette Structural sedang ditampilkan, palette akan disembunyikan
4. Tab terakhir yang aktif akan dipertahankan. Palette ini punya **empat** tab:

| Tab | Isinya |
|:----|:-------|
| **Framing** | Tipe column dan beam untuk [IVO:FRAMING](commands/structure/framing.md), [IVO:COLUMN](commands/structure/column.md), [IVO:BEAM](commands/structure/beam.md) |
| **Bracing** | Tipe bracing untuk [IVO:BRACING](commands/structure/bracing.md) dan [IVO:DIM2BRACING](commands/structure/dim2bracing.md) |
| **Member Schedule** | Tombol pembersih tabel schedule — lihat [IVO:SCHEDULE](commands/structure/schedule.md) |
| **Footing** | Kedua offset yang dipakai [IVO:FOOTING](commands/structure/footing.md) |

<!-- screenshot -->

## Tips & Catatan

> [!NOTE]
> Tab **Footing** tidak punya perintah pembukanya sendiri — satu-satunya jalan ke sana adalah membuka palette ini lalu mengklik tabnya.

> [!WARNING]
> Perintah ini membutuhkan **lisensi aktif**. Jalankan [IVO:LICENSE](commands/help/license.md) untuk mengaktifkan lisensi.

> [!TIP]
> Gunakan perintah ini sebagai toggle cepat. Jika Anda hanya ingin menampilkan atau menyembunyikan secara eksplisit, gunakan `IVO:SHOWSTRUCTURALPALETTE` atau `IVO:HIDESTRUCTURALPALETTE`.

## Lihat Juga

- [IVO:SHOWSTRUCTURALPALETTE](commands/structure/showstructuralpalette.md) — menampilkan palette secara eksplisit
- [IVO:HIDESTRUCTURALPALETTE](commands/structure/hidestructuralpalette.md) — menyembunyikan palette secara eksplisit
