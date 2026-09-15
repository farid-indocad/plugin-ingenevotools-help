# IVO:INITIALBLOCK

> Menormalkan objek terpilih ke Layer 0 / ByBlock, lalu membuka dialog BLOCK bawaan dengan objek itu sudah terpilih.

## Cara Akses

- **Ribbon:** Tab Ingenevo Tools → Panel Utilities → Tombol Initial Block
- **Command Line:** `IVO:INITIALBLOCK`
- **Alias:** `IVO:IBLOCK`

## Cara Penggunaan

1. Pilih objek yang akan dijadikan block (boleh sebelum perintah dijalankan — preselection dihormati)
2. Jalankan perintah `IVO:INITIALBLOCK` atau `IVO:IBLOCK`
3. Plugin mengubah keempat properti berikut pada setiap objek terpilih:

| Properti | Nilai baru |
|:---------|:-----------|
| Layer | `0` |
| Color | ByBlock |
| Linetype | ByBlock |
| Lineweight | ByBlock |

4. Dialog **Block Definition** bawaan BricsCAD terbuka dengan objek tadi sudah termuat di bagian *Select objects*
5. Lanjutkan seperti biasa — beri nama block, tentukan base point, lalu **OK**

<!-- screenshot -->

## Tips & Catatan

> [!WARNING]
> Perintah ini membutuhkan **lisensi aktif**. Jalankan [IVO:LICENSE](commands/help/license.md) untuk mengaktifkan lisensi.

> [!NOTE]
> Objek yang berada di **layer terkunci dilewati** — objek lain dalam seleksi yang sama tetap diproses.

> [!WARNING]
> **Kalau Anda menekan Cancel di dialog Block Definition, normalisasi propertinya tetap berlaku.** Dialog BLOCK itu milik BricsCAD, bukan plugin, jadi membatalkannya tidak mengembalikan Layer dan ByBlock ke keadaan semula. Ketik `U` sekali untuk mengurungkan normalisasinya — seluruh perubahan properti adalah satu langkah undo.

> [!TIP]
> Konvensi Layer 0 + ByBlock inilah yang membuat block mewarisi layer dan warna dari tempat ia disisipkan, bukan memaksakan tampilannya sendiri. Perintah ini menyiapkan konvensi itu dalam satu langkah.

> [!NOTE]
> Tidak ada penyaringan jenis objek. Line, circle, text, maupun block reference sama-sama diterima.

## Lihat Juga

- [IVO:REPLACEBLOCK](commands/utilities/replaceblock.md) — mengganti instance block dengan block lain
- [IVO:CHANGEBASEPOINT](commands/utilities/changebasepoint.md) — mengubah titik dasar block
- [IVO:SAFEEXPLODE](commands/utilities/safeexplode.md) — meng-explode block satu level dengan aman
