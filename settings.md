# Pengaturan

Halaman ini menjelaskan **bagaimana pengaturan IngenevoTools disusun** — bukan mendaftar satu per satu opsinya.

> [!IMPORTANT]
> Penjelasan setiap opsi hidup **di dalam jendela Settings**, tampil tepat di sebelah kolom isiannya. Itu disengaja: penjelasan yang disalin ke dua tempat akan cepat berselisih, dan yang ada di dalam dialog tidak pernah bisa basi. Halaman ini tidak menyalinnya.

Buka dengan [`IVO:SETTINGS`](commands/settings/settings.md).

## Struktur pohon pengaturan

| Grup | Isinya |
|:-----|:-------|
| **General** | Preferensi umum, termasuk Help URL yang dibuka [`IVO:HELP`](commands/help/help.md) |
| **Sheet Manager** | Paper · Sheet Name · Title Block (berikut Drawing Index dan Extraction Rules) · Drawing Register · Viewport · Viewframe |
| **Structure** | Daftar tipe Column, Beam, dan Bracing, serta pengaturan Footing |
| **Detail Library** | Folder library dan folder cache thumbnail |
| **Member Schedule** | Aturan pembersihan tabel untuk [`IVO:SCHEDULE`](commands/structure/schedule.md) |

<!-- screenshot -->

## Profil

Pengaturan disimpan sebagai **profil** — satu berkas XML per profil, dan satu penunjuk yang menentukan mana yang sedang aktif.

Installer menanam tiga profil bawaan: **Default**, **Intrax**, dan **IndoCAD**. Drafter baru karena itu langsung punya pengaturan standar kantor tanpa menyusunnya sendiri.

Berganti profil dilakukan dari dalam jendela Settings, dan **mengganti seluruh set nilai sekaligus** — bukan menggabungkannya.

## Di mana berkasnya

```
%AppData%\IngenevoTools\
  Profiles\      ← satu berkas per profil
  Schedule\      ← tabel lookup Member Schedule
  Cleanup\       ← preset IVO:CLEANUP
```

Buka lewat [`IVO:OPENSETTINGSFOLDER`](commands/settings/opensettingsfolder.md).

> [!WARNING]
> **Tutup dulu jendela Settings sebelum mengedit berkas ini dengan tangan.** Jendela itu memegang seluruh isinya di memori dan menulis ulang berkasnya saat Anda menekan OK atau Apply — suntingan tangan Anda akan tertimpa tanpa peringatan.

> [!NOTE]
> Komentar yang **Anda** tulis sendiri di dalam berkas tidak bertahan. Setiap penyimpanan membangun ulang seluruh dokumen dari konfigurasi yang sedang berjalan. Komentar yang ditulis plugin sendiri diperbarui tiap kali menyimpan, jadi tidak pernah basi.

## Hal yang perlu diketahui

> [!NOTE]
> [`IVO:SETTINGS`](commands/settings/settings.md) **tidak membutuhkan lisensi aktif.** Isinya konfigurasi milik Anda sendiri, yang mungkin sudah lama Anda susun — mengunci aksesnya saat langganan lewat sehari sama saja menyandera data Anda.

> [!NOTE]
> Perubahan berlaku **langsung**, tanpa perlu memuat ulang plugin atau menutup BricsCAD.

> [!TIP]
> Banyak perintah tidak menanyakan apa pun karena jawabannya sudah ada di sini — paper size, prefix nama sheet, nama block title block, tipe column. Kalau sebuah perintah menghasilkan sesuatu yang tidak Anda harapkan, periksa pengaturannya lebih dulu sebelum mencurigai perintahnya.
