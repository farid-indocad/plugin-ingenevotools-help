# IVO:OPENSETTINGSFOLDER

> Membuka folder tempat settings, profil, dan preset plugin disimpan di Windows Explorer.

## Cara Akses

- **Ribbon:** — (tidak ada tombol ribbon)
- **Command Line:** `IVO:OPENSETTINGSFOLDER`
- **Alias:** —

## Cara Penggunaan

1. Jalankan perintah `IVO:OPENSETTINGSFOLDER`
2. Windows Explorer terbuka di folder berikut:

```
%AppData%\IngenevoTools\
```

3. Di dalamnya Anda akan menemukan:

| Isi | Fungsi |
|:----|:-------|
| `Profiles\` | Satu berkas XML per profil settings. Profil yang aktif ditunjuk oleh sebuah pointer |
| `Schedule\` | `schedule-tables.xml` — tabel lookup untuk [IVO:SCHEDULE](commands/structure/schedule.md) |
| `Cleanup\` | Berkas preset untuk [IVO:CLEANUP](commands/utilities/cleanup.md) |
| `detail-library.xml` | Setelan [Detail Library](commands/detail-library/detaillibrarysettings.md) komputer ini — folder library dan cache thumbnail |

<!-- screenshot -->

## Tips & Catatan

> [!NOTE]
> Ini salah satu dari sedikit perintah yang **tidak membutuhkan lisensi aktif maupun drawing yang terbuka**. Ia murni membuka folder, bukan mengerjakan sesuatu pada gambar.

> [!TIP]
> Kalau foldernya belum ada, perintah ini **membuatnya lebih dulu** — jadi tetap bekerja di komputer yang belum pernah menyimpan pengaturan apa pun.

> [!WARNING]
> **Jangan mengedit profil kantor di `Profiles\` dengan tangan.** Installer menimpanya setiap kali dipasang, jadi suntingan Anda hilang di pembaruan berikutnya. Minta perubahannya ke tim IndoCAD.

> [!TIP]
> Folder ini paling sering dibutuhkan untuk menaruh varian preset [IVO:CLEANUP](commands/utilities/cleanup.md) Anda sendiri, atau untuk mengambil berkas yang diminta tim IndoCAD saat Anda melapor masalah.

## Lihat Juga

- [IVO:SETTINGS](commands/settings/settings.md) — memilih profil pengaturan
- [IVO:OPENFOLDER](commands/sheet-manager/openfolder.md) — membuka folder drawing yang sedang aktif
