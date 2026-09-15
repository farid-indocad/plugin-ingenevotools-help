# IVO:EDITREGISTER

> Membuka berkas register Excel milik drawing yang sedang aktif.

## Cara Akses

- **Ribbon:** Tab Ingenevo Tools → Panel Sheet Manager → Tombol Edit Register
- **Command Line:** `IVO:EDITREGISTER`
- **Alias:** —

## Cara Penggunaan

1. Pastikan drawing aktif **sudah tersimpan** ke disk
2. Jalankan perintah `IVO:EDITREGISTER`
3. Berkas register di sebelah drawing dibuka di aplikasi spreadsheet default Anda

<!-- screenshot -->

## Tips & Catatan

> [!WARNING]
> Perintah ini membutuhkan **lisensi aktif**. Jalankan [IVO:LICENSE](commands/help/license.md) untuk mengaktifkan lisensi.

> [!NOTE]
> Berkas register harus **sudah ada**. Kalau belum, buat lebih dulu dengan [IVO:CREATEREGISTER](commands/sheet-manager/createregister.md).

> [!TIP]
> Nama dan ekstensi berkas register diatur di `IVO:SETTINGS` → **Sheet Manager > Drawing Register**. Dengan format `Auto` (bawaan), plugin mencari `.xlsx` lebih dulu lalu `.xls`.

> [!NOTE]
> Perintah ini, [IVO:CREATEREGISTER](commands/sheet-manager/createregister.md), dan [IVO:UPDATETITLEBLOCK](commands/sheet-manager/updatetitleblock.md) memakai satu aturan yang sama untuk menentukan berkas register milik sebuah drawing — ketiganya tidak mungkin menunjuk berkas yang berbeda.

## Lihat Juga

- [IVO:CREATEREGISTER](commands/sheet-manager/createregister.md) — membuat register baru dari template
- [IVO:UPDATETITLEBLOCK](commands/sheet-manager/updatetitleblock.md) — mengisi title block dari register
- [IVO:OPENFOLDER](commands/sheet-manager/openfolder.md) — membuka folder drawing aktif
