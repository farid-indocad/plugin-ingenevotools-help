# IVO:CREATELAYOUT

> Menghapus **semua** layout yang ada, lalu membangunnya ulang dari block ViewFrame di model space.

## Cara Akses

- **Ribbon:** Tab Ingenevo Tools → Panel Sheet Manager → Tombol Create Layout
- **Command Line:** `IVO:CREATELAYOUT`
- **Alias:** `IVO:CRL`

## Cara Penggunaan

1. Pastikan block **ViewFrame** sudah tergambar di model space
2. Jalankan perintah `IVO:CREATELAYOUT` atau `IVO:CRL`
3. Muncul prompt konfirmasi yang **menampilkan pengaturan yang akan dipakai**:

```
Create layouts — Paper: A3, Prefix: SH-, Additional: 2.
Delete all existing layouts and continue? [Yes/No] <Yes>:
```

4. Tekan **Enter** untuk lanjut (default **Yes**), atau jawab **No** untuk membatalkan
5. Jendela progress muncul selama layout dibangun — ada tombol **Cancel** di sana
6. Setelah selesai, command line melaporkan paper size, prefix, jumlah layout tambahan, dan total layout yang dibuat

<!-- screenshot -->

## Tips & Catatan

> [!WARNING]
> Perintah ini membutuhkan **lisensi aktif**. Jalankan [IVO:LICENSE](commands/help/license.md) untuk mengaktifkan lisensi.

> [!WARNING]
> Perintah ini **menghapus seluruh layout yang ada** sebelum membuat yang baru. Kalau Anda hanya ingin menambah layout tanpa menghapus apa pun, gunakan [IVO:ADDLAYOUT](commands/sheet-manager/addlayout.md).

> [!NOTE]
> **Kalau Anda menekan Cancel di tengah jalan, layout lama sudah terlanjur terhapus.** Seluruh perintah ini adalah **satu langkah undo**, jadi ketik `U` sekali untuk memulihkan semuanya. Command line akan mengingatkan Anda soal ini saat pembatalan terjadi — tidak ada tanda lain di layar yang menyiratkannya.

> [!TIP]
> Perintah ini **tidak menanyakan** template maupun paper size. Semua nilai itu dibaca dari `IVO:SETTINGS` → **Sheet Manager** sebelum prompt muncul, dan itulah sebabnya prompt konfirmasi menyebutkan nilainya — yang Anda lihat di prompt persis yang akan dipakai.

> [!NOTE]
> Layout "additional" adalah layout **kosong tanpa viewport**, dan jumlahnya diatur di settings. Yang menentukan layout mana yang kosong adalah **posisinya dalam urutan pembuatan**, bukan namanya — penamaannya tetap berurutan seperti layout lain.

## Lihat Juga

- [IVO:ADDLAYOUT](commands/sheet-manager/addlayout.md) — menambah layout tanpa menghapus yang sudah ada
- [IVO:RENUMBERVIEWFRAME](commands/sheet-manager/renumberviewframe.md) — menomori ulang block ViewFrame sebelum layout dibangun
- [IVO:SORTLAYOUT](commands/sheet-manager/sortlayout.md) — mengurutkan tab layout berdasarkan nama
