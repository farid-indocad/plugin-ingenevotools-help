# Pengaturan

Halaman ini menjelaskan **bagaimana pengaturan IngenevoTools disusun**, dan bagian mana yang bisa Anda pilih sendiri.

> [!IMPORTANT]
> **Nilai pengaturan ditentukan oleh profil kantor, bukan diisi drafter.** Profil disusun tim IndoCAD dan dibawa installer. Yang Anda pilih lewat [`IVO:SETTINGS`](commands/settings/settings.md) hanyalah **profil mana** yang dipakai. Kalau sebuah nilai perlu diubah — paper size, prefix nama sheet, tipe column, dan seterusnya — minta perubahannya ke tim IndoCAD.

## Apa yang ditentukan profil

| Bagian | Isinya |
|:-------|:-------|
| **General** | Preferensi umum, termasuk Help URL yang dibuka [`IVO:HELP`](commands/help/help.md) |
| **Sheet Manager** | Paper · Sheet Name · Title Block (berikut Drawing Index dan Extraction Rules) · Drawing Register · Viewport · Viewframe |
| **Structure** | Daftar tipe Column, Beam, dan Bracing beserta gaya gambarnya, serta pengaturan Footing |
| **Member Schedule** | Aturan pembersihan tabel untuk [`IVO:SCHEDULE`](commands/structure/schedule.md) |

Setelan **Detail Library** tidak ikut profil — ia milik komputer Anda sendiri dan diatur lewat [`IVO:DETAILLIBRARYSETTINGS`](commands/detail-library/detaillibrarysettings.md).

## Profil

Pengaturan disimpan sebagai **profil** — satu berkas XML per profil, dan satu penunjuk yang menentukan mana yang sedang aktif.

Installer membawa satu profil kantor: **Intrax**. Profil lama **Default** dan **IndoCAD** sudah pensiun — installer menghapus keduanya, dan komputer yang masih memakainya dipindahkan ke Intrax.

Untuk berganti profil, jalankan [`IVO:SETTINGS`](commands/settings/settings.md), pilih profilnya, lalu tekan **OK**. Berganti profil **mengganti seluruh set nilai sekaligus** dan berlaku langsung, tanpa perlu memuat ulang plugin atau menutup BricsCAD.

## Di mana berkasnya

```
%AppData%\IngenevoTools\
  Profiles\           ← satu berkas per profil
  Schedule\           ← tabel lookup Member Schedule
  Cleanup\            ← preset IVO:CLEANUP
  detail-library.xml  ← setelan Detail Library komputer ini
```

Buka lewat [`IVO:OPENSETTINGSFOLDER`](commands/settings/opensettingsfolder.md).

> [!WARNING]
> **Jangan mengedit profil kantor dengan tangan.** Installer menimpa profil yang dibawanya **setiap kali dipasang**, jadi suntingan Anda hilang di pembaruan berikutnya. Minta perubahannya ke tim IndoCAD agar ikut paket berikutnya.

## Hal yang perlu diketahui

> [!NOTE]
> [`IVO:SETTINGS`](commands/settings/settings.md) **tidak membutuhkan lisensi aktif**, jadi Anda selalu bisa melihat dan mengganti profil yang dipakai.

> [!TIP]
> Banyak perintah tidak menanyakan apa pun karena jawabannya sudah ada di profil — paper size, prefix nama sheet, nama block title block, tipe column. Kalau sebuah perintah menghasilkan sesuatu yang tidak Anda harapkan, periksa dulu **profil mana yang sedang aktif** sebelum mencurigai perintahnya.
