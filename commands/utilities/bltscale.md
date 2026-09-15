# IVO:BLTSCALE

> Mengatur MSLTSCALE dan PSLTSCALE di seluruh layout sekaligus ke 0 atau 1.

## Cara Akses

- **Ribbon:** Tab Ingenevo Tools → Panel Utilities → Tombol BltScale
- **Command Line:** `IVO:BLTSCALE`
- **Alias:** `IVO:BLTS`

## Cara Penggunaan

1. Jalankan perintah `IVO:BLTSCALE` atau `IVO:BLTS`
2. Masukkan nilai yang diinginkan — **0** atau **1** — lalu tekan **Enter**
3. MSLTSCALE (model space) dan PSLTSCALE (semua layout) diatur serentak ke nilai itu
4. Tab yang sedang aktif dikembalikan seperti semula setelah selesai

## Opsi / Parameter

| Nilai | Artinya |
|:------|:--------|
| **0** | Linetype scaling **tidak** mengikuti annotation scale |
| **1** | Linetype scaling mengikuti annotation scale |

<!-- screenshot -->

## Tips & Catatan

> [!WARNING]
> Perintah ini membutuhkan **lisensi aktif**. Jalankan [IVO:LICENSE](commands/help/license.md) untuk mengaktifkan lisensi.

> [!IMPORTANT]
> **Perubahan system variable tidak bisa di-undo.** Ketik `U` tidak akan mengembalikan MSLTSCALE dan PSLTSCALE ke nilai sebelumnya — jalankan ulang perintah ini dengan nilai yang lama kalau Anda ingin membatalkannya.

> [!TIP]
> Perintah ini berkeliling ke setiap layout untuk mengatur PSLTSCALE, lalu mengembalikan Anda ke tab tempat Anda berada. Pada drawing dengan banyak layout, prosesnya bisa terlihat berkedip sesaat — itu normal.

## Lihat Juga

- [IVO:MATCHALLLAYOUTSETTINGS](commands/utilities/matchalllayoutsettings.md) — menyalin page setup ke seluruh layout
