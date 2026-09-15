# FAQ / Troubleshooting

Masalah yang benar-benar muncul di lapangan, berikut jalan keluarnya.

---

## Tab "Ingenevo Tools" tidak muncul setelah dipasang

**Kemungkinan terbesar: BricsCAD sedang terbuka saat installer dijalankan.** Pemasangannya berhasil, tapi versi barunya baru aktif setelah BricsCAD **ditutup dan dibuka lagi**.

1. Tutup BricsCAD sepenuhnya, lalu buka lagi
2. Kalau masih belum muncul, klik dua kali installer yang sama sekali lagi dan tekan tombol **Reinstall**
3. Kalau tetap tidak ada, kirim `%LocalAppData%\Ingenevo\install-log.txt` ke tim Ingenevo

---

## Semua perintah IVO ditolak, padahal tab-nya ada

Plugin terpasang tapi **lisensi belum diaktifkan**. Ketik [`IVO:LICENSE`](commands/help/license.md) dan aktifkan.

Tujuh perintah tetap bisa dijalankan tanpa lisensi — `IVO:LICENSE`, `IVO:ABOUT`, `IVO:HELP`, `IVO:COMMANDS`, `IVO:SETTINGS`, `IVO:OPENSETTINGSFOLDER`, dan `IVO:HIDESTRUCTURALPALETTE`. Kalau ketujuh itu jalan tapi sisanya tidak, inilah penyebabnya.

---

## Aktivasi ditolak karena batas perangkat

Seluruh slot lisensi Anda sudah terpakai — biasanya oleh komputer lama yang sudah tidak dipakai lagi.

Daftar mesinnya tidak ditampilkan di jendela lisensi. Yang bisa Anda lakukan:

- Di komputer lama yang masih bisa dinyalakan: buka [`IVO:LICENSE`](commands/help/license.md) → **Remove**
- Kalau komputernya sudah tidak ada: hubungi tim Ingenevo

> [!WARNING]
> Menghapus plugin atau memformat komputer **tidak** membebaskan slot lisensi. Selalu tekan **Remove** dulu sebelum meninggalkan sebuah komputer.

---

## Perintah tidak ditemukan ("Unknown command")

1. Semua perintah berawalan `IVO:` — periksa penulisannya, termasuk tanda titik dua
2. Jalankan [`IVO:COMMANDS`](commands/help/commands.md) untuk melihat daftar perintah yang benar-benar terdaftar
3. Kalau `IVO:COMMANDS` sendiri tidak dikenali, plugin-nya belum termuat — lihat [Instalasi](instalasi.md)

---

## Perintah berjalan tapi tidak menanyakan apa-apa

Itu biasanya **memang perilakunya**, bukan kerusakan. Banyak perintah membaca pengaturannya dari [`IVO:SETTINGS`](commands/settings/settings.md) alih-alih bertanya tiap kali — misalnya paper size pada [`IVO:CREATELAYOUT`](commands/sheet-manager/createlayout.md), format penomoran pada [`IVO:RENUMBERLAYOUT`](commands/sheet-manager/renumberlayout.md), dan kedua offset pada [`IVO:FOOTING`](commands/structure/footing.md).

Kalau hasilnya tidak sesuai harapan, periksa [Pengaturan](settings.md) lebih dulu.

---

## Title block tidak terisi setelah IVO:UPDATETITLEBLOCK

Baris Excel dicocokkan ke layout **berdasarkan nama layout**. Sheet yang kosong hampir selalu berarti nama di kolom kunci Excel tidak sama persis dengan nama layout-nya.

Periksa juga:

1. Title block harus **block reference beratribut** — teks biasa dan mtext tidak bisa diisi
2. Nama sheet Excel yang dibaca diatur di `IVO:SETTINGS` → **Sheet Manager › Drawing Register › Worksheet**

---

## IVO:PRINTPDF tidak menghasilkan PDF

1. Pastikan printer/plotter PDF sudah dikonfigurasi di BricsCAD
2. Pastikan folder output bisa ditulis (bukan read-only, bukan share yang terputus)
3. Jalankan [`IVO:MATCHALLLAYOUTSETTINGS`](commands/utilities/matchalllayoutsettings.md) lebih dulu agar semua layout memakai page setup yang sama

---

## IVO:BLTSCALE sudah dijalankan, tapi "U" tidak mengembalikannya

Memang tidak bisa. [`IVO:BLTSCALE`](commands/utilities/bltscale.md) mengubah **system variable**, dan perubahan system variable tidak masuk riwayat undo.

Jalankan ulang perintah itu dengan nilai yang lama untuk mengembalikannya.

---

## IVO:BOUNDARY atau IVO:FOOTING menolak menggambar

Keduanya melapor **alasannya** di command line, bukan diam. Yang paling sering:

- **`Ring not closed`** — keliling masih berlubang. Garis yang ujungnya menggantung **otomatis dijadikan seleksi aktif**; zoom ke seleksi itu untuk melihat letak celahnya
- **`wrong colour`** — pada [`IVO:BOUNDARY`](commands/structure/boundary.md), warna garis menentukan jaraknya. Hanya cyan dan kuning yang dibaca

Kalau sebuah gambar terus menolak, jalankan `IVO:BOUNDARYDUMP` pada seleksi yang sama dan kirimkan berkas laporannya ke tim Ingenevo.

---

> [!TIP]
> Masalah Anda tidak ada di sini? Hubungi tim Ingenevo lewat informasi di halaman [Tentang](about.md). Lampirkan `%LocalAppData%\Ingenevo\install-log.txt` untuk masalah pemasangan, atau `%AppData%\IngenevoTools\license-log.txt` untuk masalah lisensi.
