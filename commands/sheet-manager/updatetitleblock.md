# IVO:UPDATETITLEBLOCK

> Mengisi atribut title block di banyak layout sekaligus, dari berkas Excel.

## Cara Akses

- **Ribbon:** Tab Ingenevo Tools → Panel Sheet Manager → Tombol Update Title Block
- **Command Line:** `IVO:UPDATETITLEBLOCK`
- **Alias:** —

## Cara Penggunaan

1. Pastikan berkas **register Excel** drawing ini sudah ada dan terisi — buat dengan [IVO:CREATEREGISTER](commands/sheet-manager/createregister.md), isi dengan [IVO:EDITREGISTER](commands/sheet-manager/editregister.md)
2. Jalankan perintah `IVO:UPDATETITLEBLOCK`
3. Plugin membaca register tersebut, lalu untuk setiap baris:
   - **mencocokkan baris dengan layout berdasarkan namanya**
   - menulis kolom-kolom yang dipetakan ke atribut title block di layout itu

<!-- screenshot -->

## Tips & Catatan

> [!WARNING]
> Perintah ini membutuhkan **lisensi aktif**. Jalankan [IVO:LICENSE](commands/help/license.md) untuk mengaktifkan lisensi.

> [!IMPORTANT]
> **Nilainya tidak diketik di command line — sumbernya berkas Excel.** Untuk mengubah isi title block, ubah isi register-nya lalu jalankan ulang perintah ini.

> [!NOTE]
> Pencocokan dilakukan lewat **nama layout**. Baris yang namanya tidak cocok dengan layout mana pun tidak akan tertulis ke mana-mana.

> [!TIP]
> Berkas register yang dibaca adalah berkas yang sama dengan yang dipakai [IVO:CREATEREGISTER](commands/sheet-manager/createregister.md) dan [IVO:EDITREGISTER](commands/sheet-manager/editregister.md). Nama sheet yang dibaca diatur di `IVO:SETTINGS` → **Sheet Manager > Drawing Register > Worksheet**.

> [!NOTE]
> Title block harus berupa **block reference beratribut**. Teks biasa dan mtext tidak bisa diisi oleh perintah ini.

> [!TIP]
> Nama block title block dan pemetaan kolom ke atribut diatur di `IVO:SETTINGS` → **Sheet Manager > Title Block**.

## Lihat Juga

- [IVO:CREATEREGISTER](commands/sheet-manager/createregister.md) — membuat berkas register Excel
- [IVO:EDITREGISTER](commands/sheet-manager/editregister.md) — membuka register untuk diisi
