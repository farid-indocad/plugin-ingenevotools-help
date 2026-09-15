# IVO:RENUMBERLAYOUT

> Mengatur penomoran halaman layout secara sekuensial; format prefiks/sufiks/digit diatur lewat opsi "Settings" pada command line.

## Cara Akses

- **Ribbon:** Tab Ingenevo Tools → Panel Renumber Layout → Tombol Renumber Layout
- **Command Line:** `IVO:RENUMBERLAYOUT`
- **Alias:** —

## Cara Penggunaan

1. Jalankan perintah `IVO:RENUMBERLAYOUT`
2. Ikuti prompt di command line untuk mengatur format penomoran:
   - **Prefix** — teks sebelum nomor (opsional)
   - **Suffix** — teks setelah nomor (opsional)
   - **Start Number** — nomor awal
   - **Digits** — jumlah digit (misalnya 2 → 01, 02, 03...)
3. Semua layout akan dinomori ulang secara sekuensial

## Opsi / Parameter

| Parameter | Deskripsi | Contoh |
|:----------|:----------|:-------|
| **Prefix** | Teks sebelum nomor | `Sheet-` |
| **Suffix** | Teks setelah nomor | ` of 10` |
| **Start Number** | Nomor awal penomoran | `1` |
| **Digits** | Jumlah digit minimum | `2` → 01, 02, ... |

<!-- screenshot -->

## Tips & Catatan

> [!TIP]
> Contoh hasil: dengan prefix `Sheet-`, digits `2`, dan start `1`, layout akan dinamai `Sheet-01`, `Sheet-02`, `Sheet-03`, dst.
