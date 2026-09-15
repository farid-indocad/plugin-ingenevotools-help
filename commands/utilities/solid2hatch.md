# IVO:SOLID2HATCH

> Mengonversi objek SOLID (2D filled quad) menjadi hatch pattern SOLID dengan warna dan layer sama.

## Cara Akses

- **Ribbon:** Tab Ingenevo Tools → Panel Utilities → Tombol Solid2Hatch
- **Command Line:** `IVO:SOLID2HATCH`
- **Alias:** `IVO:S2H`

## Cara Penggunaan

1. Jalankan perintah `IVO:SOLID2HATCH` atau `IVO:S2H`
2. Pilih satu atau lebih objek SOLID (2D filled quad)
3. Tekan **Enter** untuk konfirmasi
4. Setiap objek SOLID diganti dengan hatch pattern SOLID — **objek SOLID aslinya dihapus**
5. Warna dan layer dari SOLID asli dipertahankan

<!-- screenshot -->

## Tips & Catatan

> [!TIP]
> Seluruh konversi adalah **satu langkah undo**. Satu `U` mengembalikan semua SOLID yang terhapus sekaligus.

> [!WARNING]
> Perintah ini membutuhkan **lisensi aktif**. Jalankan [IVO:LICENSE](commands/help/license.md) untuk mengaktifkan lisensi.

> [!NOTE]
> Perintah ini hanya bekerja pada objek SOLID 2D (bukan 3D SOLID). Objek SOLID 2D biasanya dihasilkan dari perintah SOLID bawaan atau hasil impor dari format lama.

> [!TIP]
> Konversi ke hatch memudahkan editing — hatch lebih mudah dimodifikasi boundary-nya dibandingkan SOLID 2D.

## Lihat Juga

- [IVO:SAFEEXPLODE](commands/utilities/safeexplode.md) — meng-explode block satu level dengan aman
