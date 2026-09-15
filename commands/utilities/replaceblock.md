# IVO:REPLACEBLOCK

> Mengganti block reference terpilih dengan block lain, mempertahankan properti penempatan dan nilai atribut yang cocok.

## Cara Akses

- **Ribbon:** Tab Ingenevo Tools → Panel Utilities → Tombol Replace Block
- **Command Line:** `IVO:REPLACEBLOCK`
- **Alias:** —

## Cara Penggunaan

1. Jalankan perintah `IVO:REPLACEBLOCK`
2. Pilih block reference yang ingin diganti (**sumber**)
3. Tunjuk block yang akan menggantikannya (**target**)
4. Pilih apakah properti penempatan block sumber ikut dipertahankan
5. Pilih **mode perataan**:

| Mode | Cara menempatkan block pengganti |
|:-----|:---------------------------------|
| **Insertion** | Memakai titik sisip block sumber apa adanya |
| **Center** | Menyamakan titik tengah bounding box sumber dan target |
| **Reference** | Anda menunjuk sendiri titik acuan pada sumber dan pada target |

6. Seluruh block sumber terpilih diganti dengan target

<!-- screenshot -->

## Tips & Catatan

> [!WARNING]
> Perintah ini membutuhkan **lisensi aktif**. Jalankan [IVO:LICENSE](commands/help/license.md) untuk mengaktifkan lisensi.

> [!TIP]
> **Nilai atribut yang namanya sama ikut terbawa** ke block pengganti. Atribut yang tidak punya pasangan di block target tidak dipindahkan.

> [!NOTE]
> Mode **Center** berguna saat block sumber dan target punya titik sisip yang berbeda letaknya — misalnya yang satu di sudut, yang lain di tengah. Tanpa itu, block pengganti akan meloncat.

> [!TIP]
> Kalau kedua block punya titik acuan yang jelas tapi bukan titik sisipnya — misalnya sumbu lubang baut — pakai mode **Reference** dan tunjuk titik itu di kedua block.

## Lihat Juga

- [IVO:CHANGEBASEPOINT](commands/utilities/changebasepoint.md) — mengubah titik dasar definisi block
- [IVO:INITIALBLOCK](commands/utilities/initialblock.md) — menyiapkan objek menjadi block yang bersih
