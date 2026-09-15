# IVO:BOUNDARY

> Menyusun ulang satu polyline tertutup berwarna putih dari garis cyan (muka luar) dan kuning (as dinding).

## Cara Akses

- **Ribbon:** — (tidak ada tombol ribbon)
- **Command Line:** `IVO:BOUNDARY`
- **Alias:** `IVO:BND`

## Cara Penggunaan

1. Pilih garis-garis yang menggambarkan keliling ruangan (boleh sebelum perintah dijalankan — preselection dihormati):
   - **Cyan** (ACI 4) — muka luar dinding
   - **Kuning** (ACI 2) — as dinding
2. Jalankan perintah `IVO:BOUNDARY` atau `IVO:BND`
3. Boundary digambar di sisi **dalam** — tidak ada prompt
4. Command line melaporkan apa yang terjadi:

```
[IngenevoTools] Boundary created: 3 room(s) + 1 pocket(s), 28 segment(s) used,
                6 ignored (4 wrong colour, 2 not straight), 0 outside the ring.
```

<!-- screenshot -->

## Tips & Catatan

> [!WARNING]
> Perintah ini membutuhkan **lisensi aktif**. Jalankan [IVO:LICENSE](commands/help/license.md) untuk mengaktifkan lisensi.

> [!NOTE]
> Warna garis sumber **bukan sekadar penanda visual — itulah yang menentukan jaraknya.** Cyan berarti muka luar dinding, kuning berarti as dinding yang letaknya separuh jarak dari boundary. Garis dengan warna lain diabaikan dan dihitung sebagai `wrong colour`.

> [!NOTE]
> Perintah ini **hanya menambah**. Garis sumber tidak diubah, tidak dipindah, dan tidak dihapus. Seluruh hasilnya adalah satu langkah undo.

> [!TIP]
> Hasilnya berupa polyline tertutup di layer **BOUNDARY** — layer itu dibuat otomatis kalau belum ada, dan warna entity-nya dipaksa putih supaya hasilnya tetap putih walau layer-nya sudah ada dengan warna lain.

> [!NOTE]
> Kalau Z garis sumber tidak seragam, boundary digambar di elevasi **0** dan Anda diberi tahu. Kalau seragam, elevasinya mengikuti sumber.

### Kalau tidak ada yang tergambar

Perintah membatalkan diri dan menjelaskan alasannya, bukan diam:

| Pesan | Artinya | Yang harus dilakukan |
|:------|:--------|:---------------------|
| `Ring not closed` | Keliling masih berlubang | **Garis yang ujungnya menggantung otomatis dijadikan seleksi aktif** — zoom ke seleksi itu untuk melihat letak celahnya. Koordinat celah pertama juga disebut di pesan |
| `Cyan and yellow disagree on which side is inward` | Cyan dan kuning menunjuk arah dalam yang berlawanan di suatu tepi | Periksa tepi di koordinat yang disebutkan |
| `Not enough cyan/yellow lines` | Kurang dari tiga tepi terbentuk | Pastikan seleksi Anda benar-benar mencakup keliling ruangannya |
| `Layer BOUNDARY terkunci` | Layer tujuan terkunci | Buka kunci layer `BOUNDARY` |

> [!TIP]
> Garis yang diabaikan dan tepi di luar ring **dihitung dan dilaporkan, bukan dianggap error** — boundary tetap tergambar. Angka-angka itu berguna untuk memastikan tidak ada yang tertinggal tanpa Anda sadari.

### IVO:BOUNDARYDUMP — mencari tahu kenapa gagal

Kalau sebuah gambar terus menolak menutup, `IVO:BOUNDARYDUMP` menulis laporan diagnostik untuk seleksi yang sama **tanpa menggambar apa pun**: segmen apa saja yang terbaca, berapa tepi yang terbentuk, di mana setiap celahnya, dan berapa jarak yang benar-benar terukur antara garis cyan dan kuning yang sejajar.

1. Pilih garis yang sama seperti saat `IVO:BOUNDARY` gagal
2. Jalankan `IVO:BOUNDARYDUMP`
3. Command line menyebutkan lokasi berkas laporannya

> [!TIP]
> Berkas laporan inilah yang paling berguna untuk dikirim ke tim Ingenevo kalau sebuah gambar tidak mau diproses.

## Lihat Juga

- [IVO:FOOTING](commands/structure/footing.md) — turunan perintah ini dengan dua offset yang bisa diatur sendiri
