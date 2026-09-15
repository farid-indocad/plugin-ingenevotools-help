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

<!-- screenshot -->

## Tips & Catatan

> [!NOTE]
> Ini salah satu dari sedikit perintah yang **tidak membutuhkan lisensi aktif maupun drawing yang terbuka**. Ia murni membuka folder, bukan mengerjakan sesuatu pada gambar.

> [!TIP]
> Kalau foldernya belum ada, perintah ini **membuatnya lebih dulu** — jadi tetap bekerja walaupun Anda belum pernah menekan Save di jendela Settings.

> [!WARNING]
> **Tutup dulu jendela Settings sebelum mengedit berkas XML dengan tangan.** Jendela itu memegang seluruh isinya di memori dan menulis ulang berkasnya saat Anda menekan OK atau Apply — suntingan tangan Anda akan tertimpa tanpa peringatan.

> [!NOTE]
> Komentar yang **Anda** tulis sendiri di dalam berkas settings tidak bertahan. Setiap penyimpanan membangun ulang seluruh dokumen, jadi apa pun yang bukan berasal dari konfigurasi yang sedang berjalan akan hilang. Komentar yang ditulis plugin sendiri diperbarui tiap kali menyimpan.

> [!TIP]
> Sebagian besar pengaturan lebih aman diubah lewat [IVO:SETTINGS](commands/settings/settings.md), yang menampilkan penjelasan tiap opsi tepat di sebelah kolom isiannya.

## Lihat Juga

- [IVO:SETTINGS](commands/settings/settings.md) — jendela pengaturan plugin
- [IVO:OPENFOLDER](commands/sheet-manager/openfolder.md) — membuka folder drawing yang sedang aktif
