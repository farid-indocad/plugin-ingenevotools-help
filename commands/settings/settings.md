# IVO:SETTINGS

> Membuka jendela pengaturan plugin.

## Cara Akses

- **Ribbon:** Tab Ingenevo Tools → Panel Settings → Tombol Settings
- **Command Line:** `IVO:SETTINGS`
- **Alias:** —

## Cara Penggunaan

1. Jalankan perintah `IVO:SETTINGS`
2. Jendela pengaturan terbuka dengan pohon grup di sebelah kiri:

| Grup | Isinya |
|:-----|:-------|
| **General** | Preferensi umum, termasuk Help URL yang dibuka [IVO:HELP](commands/help/help.md) |
| **Sheet Manager** | Paper, Sheet Name, Title Block (berikut Drawing Index dan Extraction Rules), Drawing Register, Viewport, Viewframe |
| **Structure** | Daftar tipe Column, Beam, dan Bracing, serta pengaturan Footing |
| **Detail Library** | Folder library dan cache thumbnail |
| **Member Schedule** | Pengaturan pembersihan tabel [IVO:SCHEDULE](commands/structure/schedule.md) |

3. Klik grup untuk melihat opsinya — **penjelasan tiap opsi tampil tepat di sebelah kolom isiannya**
4. Tekan **OK** atau **Apply** untuk menyimpan

<!-- screenshot -->

## Tips & Catatan

> [!NOTE]
> Perintah ini **tidak membutuhkan lisensi aktif.** Isi Settings adalah konfigurasi milik Anda sendiri — profil, tipe column, aturan title block — yang mungkin sudah lama Anda susun. Mengunci aksesnya saat langganan lewat sehari sama saja menyandera data Anda sendiri.

> [!TIP]
> Penjelasan setiap opsi hidup di dalam jendela ini, bukan di situs dokumentasi. Itu disengaja: penjelasan yang disalin ke dua tempat cepat berselisih, dan yang di dalam dialog tidak pernah bisa basi.

> [!TIP]
> Pengaturan disimpan sebagai **profil**. Installer menanam tiga profil bawaan — `Default`, `Intrax`, dan `IndoCAD` — jadi drafter baru langsung punya pengaturan standar kantor tanpa menyusunnya sendiri.

> [!NOTE]
> Perubahan berlaku langsung, tanpa perlu memuat ulang plugin atau menutup BricsCAD.

> [!WARNING]
> Kalau Anda mengedit berkas settings dengan tangan, **tutup dulu jendela ini.** Jendela Settings memegang seluruh isinya di memori dan menulis ulang berkasnya saat Anda menekan OK atau Apply — suntingan tangan Anda akan tertimpa.

## Lihat Juga

- [IVO:OPENSETTINGSFOLDER](commands/settings/opensettingsfolder.md) — membuka folder tempat profil dan preset disimpan
- [Pengaturan](settings.md) — penjelasan struktur pengaturan secara umum
