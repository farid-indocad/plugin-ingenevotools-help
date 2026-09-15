# IVO:RECTANGLE

> Menyisipkan rectangle berukuran custom yang sudutnya bisa menempel ke geometri sekitar.

## Cara Akses

- **Ribbon:** — (tidak ada tombol ribbon)
- **Command Line:** `IVO:RECTANGLE`
- **Alias:** —

## Cara Penggunaan

1. Jalankan perintah `IVO:RECTANGLE`
2. Tentukan ukuran rectangle (**Width × Height**)
3. Gerakkan cursor — rectangle mengikuti dengan **titik tengahnya di posisi cursor**
4. Saat salah satu sudut rectangle mendekati geometri di sekitarnya, **seluruh rectangle bergeser kaku** supaya sudut itu mendarat tepat di target
5. Klik untuk menempatkan

<!-- screenshot -->

## Tips & Catatan

> [!WARNING]
> Perintah ini membutuhkan **lisensi aktif**. Jalankan [IVO:LICENSE](commands/help/license.md) untuk mengaktifkan lisensi.

> [!NOTE]
> **Inilah yang membedakannya dari `RECTANG` bawaan BricsCAD.** Menggambar kotak bukan nilai tambahnya — cara menempatkannya yang penting: keempat sudut dipantau bersamaan selama Anda menggeser cursor, jadi rectangle kolom bisa menempel ke sudut dinding **lewat sudutnya sendiri**, bukan lewat titik tengahnya.

> [!TIP]
> Hasilnya adalah **closed LWPolyline** biasa, jadi bisa diedit, di-offset, dan di-hatch seperti polyline lain.

> [!NOTE]
> Karena titik tengah rectangle yang mengikuti cursor, penempatan tanpa snap akan memusatkan rectangle di titik yang Anda klik.

## Lihat Juga

- [IVO:COLUMN](commands/structure/column.md) — menempatkan column struktur berikut labelnya
- [IVO:CHANGEBASEPOINT](commands/utilities/changebasepoint.md) — mengubah titik dasar block
