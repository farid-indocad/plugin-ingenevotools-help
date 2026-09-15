# IVO:CREATEREGISTER

> Membuat berkas register Excel untuk drawing aktif dengan menyalin template bawaan.

## Cara Akses

- **Ribbon:** Tab Ingenevo Tools → Panel Sheet Manager → Tombol Create Register
- **Command Line:** `IVO:CREATEREGISTER`
- **Alias:** —

## Cara Penggunaan

1. Buka drawing yang **sudah pernah disimpan** — register dibuat di sebelah berkas DWG-nya
2. Jalankan perintah `IVO:CREATEREGISTER`
3. Plugin menentukan nama berkas register dari nama drawing, lalu menyalin template ke folder yang sama
4. Jika berkas register dengan nama itu **sudah ada**, muncul prompt konfirmasi:

```
Register file "A-101.xlsx" already exists. Overwrite? [Yes/No] <No>:
```

5. Jawab **Yes** untuk menimpa, atau tekan **Enter** untuk membatalkan (default-nya **No**)

<!-- screenshot -->

## Tips & Catatan

> [!WARNING]
> Perintah ini membutuhkan **lisensi aktif**. Jalankan [IVO:LICENSE](commands/help/license.md) untuk mengaktifkan lisensi.

> [!NOTE]
> Drawing harus sudah disimpan ke disk. Drawing baru yang belum pernah di-save tidak punya lokasi folder, jadi perintah tidak tahu harus menaruh register di mana.

> [!TIP]
> Nama, ekstensi, dan lokasi template register semuanya bisa diatur lewat `IVO:SETTINGS` → **Sheet Manager > Drawing Register**:
>
> | Opsi | Fungsi |
> |:-----|:-------|
> | **Format** | `Auto` (default) mencoba `.xlsx` dulu lalu `.xls`. Bisa dipaksa ke `Xlsx`, `Xls`, atau `XlsThenXlsx` |
> | **Template Path** | Kosongkan untuk memakai template bawaan `dr_default.*` di folder plugin, atau tunjuk berkas template sendiri lewat tombol **Browse** |
> | **Worksheet** | Nama sheet yang dibaca [IVO:UPDATETITLEBLOCK](commands/sheet-manager/updatetitleblock.md) untuk mengambil data title block |

> [!NOTE]
> Kalau **Template Path** diisi tapi berkasnya tidak ditemukan, perintah **tidak** diam-diam jatuh kembali ke template bawaan — ia melapor gagal. Ini disengaja, supaya salah ketik pada path tidak tersembunyi di balik hasil yang kelihatan benar.

> [!TIP]
> `IVO:CREATEREGISTER`, [IVO:EDITREGISTER](commands/sheet-manager/editregister.md), dan [IVO:UPDATETITLEBLOCK](commands/sheet-manager/updatetitleblock.md) memakai satu aturan yang sama untuk menentukan "berkas register milik drawing ini", jadi ketiganya selalu menunjuk berkas yang sama.

## Lihat Juga

- [IVO:EDITREGISTER](commands/sheet-manager/editregister.md) — membuka register yang sudah ada
- [IVO:UPDATETITLEBLOCK](commands/sheet-manager/updatetitleblock.md) — mengisi title block massal dari register
