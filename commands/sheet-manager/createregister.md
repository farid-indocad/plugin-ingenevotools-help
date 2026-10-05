# IVO:CREATEREGISTER

> Membuat berkas register Excel untuk drawing aktif dengan menyalin template bawaan.

## Cara Akses

- **Ribbon:** Tab IngenevoTools → Panel Sheet Manager → Tombol Create Register
- **Command Line:** `IVO:CREATEREGISTER`
- **Alias:** `IVO:CREG`

## Cara Penggunaan

1. Buka drawing yang **sudah pernah disimpan** — register dibuat di sebelah berkas DWG-nya
2. Jalankan perintah `IVO:CREATEREGISTER`
3. Plugin menentukan nama berkas register dari nama drawing, lalu menyalin template ke folder yang sama
4. Jika berkas register dengan nama itu **sudah ada**, muncul prompt konfirmasi:

```
File 'A-101.xlsx' already exists. Overwrite? [Yes/No] <No>:
```

5. Jawab **Yes** untuk menimpa, atau tekan **Enter** untuk membatalkan (default-nya **No**)

<!-- screenshot -->

## Tips & Catatan

> [!WARNING]
> Perintah ini membutuhkan **lisensi aktif**. Jalankan [IVO:LICENSE](commands/help/license.md) untuk mengaktifkan lisensi.

> [!NOTE]
> Drawing harus sudah disimpan ke disk. Drawing baru yang belum pernah di-save tidak punya lokasi folder, jadi perintah tidak tahu harus menaruh register di mana.

> [!TIP]
> Nama, ekstensi, dan template register ditentukan oleh [profil pengaturan](settings.md), bagian **Sheet Manager > Drawing Register**. Pada profil kantor **Intrax**:
>
> | Opsi | Nilai di Intrax | Artinya |
> |:-----|:----------------|:--------|
> | **Format** | `XlsThenXlsx` | Register dibuat sebagai `.xls`; saat mencari register yang sudah ada, `.xls` dicoba dulu lalu `.xlsx` |
> | **Template Path** | `Templates\register-intrax.xls` | Template yang ikut terpasang bersama plugin, di folder `Templates\` di sebelah DLL plugin |
> | **Worksheet** | `Intrax` | Nama sheet yang dibaca [IVO:UPDATETITLEBLOCK](commands/sheet-manager/updatetitleblock.md) untuk mengambil data title block |

> [!NOTE]
> Ekstensi template harus cocok dengan format register. Kalau tidak — misalnya template `.xls` dengan format yang membuat `.xlsx` — perintah **menolak** sebelum menyalin apa pun, karena berkas seperti itu akan ditolak Excel.

> [!NOTE]
> Kalau **Template Path** diisi tapi berkasnya tidak ditemukan, perintah **tidak** diam-diam jatuh kembali ke template bawaan — ia melapor gagal. Ini disengaja, supaya salah ketik pada path tidak tersembunyi di balik hasil yang kelihatan benar.

> [!TIP]
> `IVO:CREATEREGISTER`, [IVO:EDITREGISTER](commands/sheet-manager/editregister.md), dan [IVO:UPDATETITLEBLOCK](commands/sheet-manager/updatetitleblock.md) memakai satu aturan yang sama untuk menentukan "berkas register milik drawing ini", jadi ketiganya selalu menunjuk berkas yang sama.

## Lihat Juga

- [IVO:EDITREGISTER](commands/sheet-manager/editregister.md) — membuka register yang sudah ada
- [IVO:UPDATETITLEBLOCK](commands/sheet-manager/updatetitleblock.md) — mengisi title block massal dari register
