# IVO:LICENSE

> Membuka jendela manajemen lisensi: aktivasi, perpanjangan, trial, dan pelepasan perangkat.

## Cara Akses

- **Ribbon:** Tab Ingenevo Tools → Panel Help → Tombol License
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
> Kalau aktivasi ditolak dengan pesan tentang **batas perangkat**, artinya seluruh slot lisensi Anda sudah terpakai. Daftar mesin yang memakainya tidak ditampilkan di jendela ini — hubungi tim Ingenevo, atau tekan **Remove** di komputer yang sudah tidak dipakai.

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
