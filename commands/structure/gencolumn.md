# IVO:GENCOLUMN

> Menempatkan column di kedua ujung setiap beam yang dipilih, tanpa menghapus beam-nya.

## Cara Akses

- **Ribbon:** — (tidak ada tombol ribbon, disengaja)
- **Command Line:** `IVO:GENCOLUMN`
- **Alias:** `IVO:GC`

## Cara Penggunaan

1. Pilih beam yang sudah tergambar (boleh sebelum perintah dijalankan — preselection dihormati)
2. Jalankan perintah `IVO:GENCOLUMN` atau `IVO:GC`
3. Column ditempatkan di **kedua ujung** setiap beam terpilih; beam-nya sendiri dibiarkan utuh
4. Command line melaporkan hasilnya:

```
[GenColumn] Created 14 "H 200x100" column(s) from 9 beam(s), 3 point(s) already had one, 0 failed.
```

<!-- screenshot -->

## Tips & Catatan

> [!WARNING]
> Perintah ini membutuhkan **lisensi aktif**. Jalankan [IVO:LICENSE](commands/help/license.md) untuk mengaktifkan lisensi.

> [!NOTE]
> Ujung beam yang berjarak **kurang dari satu satuan gambar** dianggap titik yang sama dan hanya mendapat **satu** column — bukan dua yang bertumpuk.

> [!NOTE]
> Setiap column menghadap mengikuti arah beam-nya sendiri. Kalau di satu titik ada lebih dari satu beam dengan arah berbeda, sudut column diambil dari **beam yang paling panjang**, dan perintah memberi tahu Anda berapa titik yang mengalami hal itu.

> [!TIP]
> Tipe column yang dipakai adalah tipe yang aktif di palette Structural tab **Framing** — sama dengan yang dipakai [IVO:COLUMN](commands/structure/column.md). Perintah ini tidak menanyakannya.

> [!NOTE]
> **Perintah ini sengaja tidak diberi tombol ribbon.** Tombol ribbon menjalankan perintah lewat jalur yang membuang preselection, padahal seluruh perintah ini dibangun di atas seleksi yang Anda buat lebih dulu. Tombol itu justru akan membuatnya tidak bisa dipakai.

> [!TIP]
> Titik yang sudah punya column tidak akan mendapat column kedua — jumlahnya dilaporkan terpisah sebagai `already had one`. Jadi menjalankan perintah ini dua kali pada beam yang sama aman.

## Lihat Juga

- [IVO:COLUMN](commands/structure/column.md) — menggambar column dengan menunjuk titik satu per satu
- [IVO:FRAMING](commands/structure/framing.md) — menggambar rantai column dan beam sekaligus
- [IVO:BEAM](commands/structure/beam.md) — menggambar beam saja
