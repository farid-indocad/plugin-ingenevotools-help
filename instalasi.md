# Instalasi

Memasang IngenevoTools butuh **empat langkah** dan tidak butuh hak Administrator.

## Prasyarat

- **BricsCAD** V20 sampai V26
- **Windows** 64-bit

## Empat langkah

1. **Buka tautan** yang dikirim tim IndoCAD, lalu **klik dua kali** `IngenevoToolsSetup.exe`
2. Satu jendela terbuka dan bekerja sendiri. Tunggu beberapa detik sampai ia berkata **"IngenevoTools has been installed."**, lalu tekan **Close**
3. **Buka BricsCAD.** Tab **IngenevoTools** muncul sendiri di ribbon
4. Ketik **`IVO:LICENSE`** dan aktifkan lisensi Anda

<!-- screenshot -->

> [!NOTE]
> Tidak ada yang perlu dipilih dan tidak ada pertanyaan. Installer **mendeteksi sendiri** versi BricsCAD yang ada di komputer Anda — kalau ada lebih dari satu, semuanya dilayani sekaligus.

> [!IMPORTANT]
> Langkah 4 bukan opsional. Tanpa lisensi aktif, hampir semua perintah `IVO:` akan ditolak walaupun plugin-nya sudah terpasang dan tab-nya sudah terlihat. Hanya tujuh perintah yang tetap jalan — lihat [Daftar Command](daftar-command.md).

## Kalau BricsCAD sedang terbuka

Pemasangan tetap berhasil, tapi versi barunya **baru aktif setelah BricsCAD ditutup dan dibuka lagi**. Jendela installer akan mengatakan itu.

## Plugin hilang atau berperilaku aneh

Klik dua kali **installer yang sama** sekali lagi. Kalau versi itu memang sudah terpasang, jendelanya menawarkan tombol **Reinstall** — tekan itu.

Kalau Reinstall gagal, jendelanya menyebut versi BricsCAD yang gagal dipasang. Penyebab paling umum adalah BricsCAD yang masih terbuka — tutup BricsCAD sepenuhnya, lalu jalankan installer sekali lagi.

> [!NOTE]
> Jendela installer **tidak bisa ditutup selama sedang bekerja**. Itu disengaja: pemasangan yang terputus di tengah jalan dulu bisa membuat plugin hilang. Kalaupun pemasangan gagal, versi yang sudah terpasang sebelumnya tetap utuh.

## Verifikasi

Setelah BricsCAD dibuka:

1. Tab **IngenevoTools** terlihat di ribbon
2. Ketik [`IVO:COMMANDS`](commands/help/commands.md) untuk melihat daftar perintah
3. Ketik [`IVO:ABOUT`](commands/help/about.md) untuk melihat versi yang terpasang

## Melepas plugin

Dua jalan, keduanya sama saja:

- **Settings › Apps › IngenevoTools › Uninstall**
- atau klik dua kali **`Uninstall Ingenevo Tools.exe`** di `%LocalAppData%\Ingenevo\IngenevoTools\`

Pengaturan dan lisensi Anda **tidak ikut terhapus**.

> [!WARNING]
> **Kalau Anda tidak akan memakai plugin ini lagi di komputer ini, lepaskan perangkatnya dulu** lewat [`IVO:LICENSE`](commands/help/license.md) → **Remove**, **sebelum** melepas plugin. Menghapus berkasnya **tidak** membebaskan slot lisensi di server — slot itu akan tetap terpakai oleh komputer yang sudah tidak Anda pakai.
