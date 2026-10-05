# IVO:LICENSE

> Membuka jendela manajemen lisensi: aktivasi, perpanjangan, trial, dan pelepasan perangkat.

## Cara Akses

- **Ribbon:** Tab IngenevoTools → Panel Help → Tombol License
- **Command Line:** `IVO:LICENSE`
- **Alias:** —

## Cara Penggunaan

1. Jalankan perintah `IVO:LICENSE`
2. Jendela **License Manager** terbuka dan menampilkan salah satu dari tiga keadaan: **Active**, **Not Active**, atau **Expired**
3. Pilih tindakan lewat tombol yang tersedia:

| Tombol | Fungsi |
|:-------|:-------|
| **Activate** | Memasukkan kode lisensi untuk mengaktifkan plugin di perangkat ini |
| **Start 14-Day Trial** | Memulai masa coba 14 hari — tersedia di keadaan *Not Active* |
| **Renew** | Memperpanjang lisensi yang sudah habis masa berlakunya |
| **Update** | Memperbarui data lisensi dari server |
| **Remove** | **Melepaskan perangkat ini** dari lisensi, membebaskan slot-nya |
| **Close** | Menutup jendela |

<!-- screenshot -->

## Tips & Catatan

> [!NOTE]
> Perintah ini **selalu bisa dijalankan tanpa lisensi aktif** — kalau tidak, Anda tidak akan pernah bisa mengaktifkan lisensi sejak awal.

> [!WARNING]
> **Sebelum berhenti memakai plugin di sebuah komputer, tekan Remove lebih dulu.** Menghapus plugin atau memformat komputer **tidak** membebaskan slot lisensi di server — slot itu akan tetap terpakai oleh mesin yang sudah tidak ada.

> [!NOTE]
> Kalau aktivasi ditolak karena **batas perangkat**, artinya seluruh slot lisensi Anda sudah terpakai. Jendelanya lalu bertanya **Open the customer portal in your browser now?** — tekan **Yes** untuk membuka **portal pelanggan**, masuk dengan kode yang dikirim ke email Anda, lalu lepaskan mesin yang sudah tidak dipakai. Ini berlaku di **Activate**, **Update**, maupun **Renew**.
>
> Portal juga bisa dibuka langsung kapan saja: [https://app-licsvc.azurewebsites.net/portal](https://app-licsvc.azurewebsites.net/portal)

> [!NOTE]
> Kalau perintah IVO menolak berjalan dengan pesan **Your licence is on hold**, lisensi Anda sedang **ditahan sementara** oleh tim Ingenevo — bukan dicabut. Hubungi tim Ingenevo; setelah tahanannya dilepas, tutup dan buka lagi BricsCAD. Tidak perlu aktivasi ulang, dan tidak ada slot tambahan yang terpakai.

> [!NOTE]
> Setiap aktivasi dan pemeriksaan ulang lisensi, plugin mengirim **nama komputer, IP lokal, dan nama Windows** ke server lisensi, supaya tiap mesin tampil dengan namanya sendiri di portal pelanggan. IP lokal tidak ditampilkan di portal. Pengiriman ini tidak bisa dimatikan.

> [!TIP]
> Kalau ada masalah aktivasi, plugin menulis jejak diagnostik di berkas berikut. Tidak ada tombol untuk membukanya — buka sendiri lewat Explorer, dan lampirkan saat menghubungi tim Ingenevo:
>
> ```
> %AppData%\IngenevoTools\license-log.txt
> ```

> [!NOTE]
> Status lisensi diperiksa ulang sendiri di latar belakang, jadi tidak ada tombol *Refresh* — Anda tidak perlu melakukan apa pun agar perpanjangan terbaca.

## Lihat Juga

- [IVO:ABOUT](commands/help/about.md) — informasi versi plugin
- [Daftar Command](daftar-command.md) — perintah mana saja yang butuh lisensi aktif
