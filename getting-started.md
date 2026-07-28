# Getting Started

Panduan memulai penggunaan IngenevoTools setelah instalasi.

## Langkah 1: Muat Plugin

Ikuti salah satu metode di halaman [Instalasi](instalasi.md) untuk memuat plugin ke BricsCAD.

## Langkah 2: Kenali Ribbon Panel

Setelah plugin dimuat, tab **Ingenevo Tools** akan muncul di Ribbon BricsCAD. Tab ini berisi 14 panel yang mengelompokkan perintah berdasarkan fungsinya:

| Panel | Fungsi Utama |
|:------|:-------------|
| Structural Palette | Toggle palette untuk framing & bracing |
| Block | Manajemen block reference |
| Framing | Menggambar column dan beam |
| Bracing | Menggambar ikatan angin |
| Change Base Point | Mengubah titik dasar block |
| Layout | Manajemen layout tabs |
| Library | Perpustakaan gambar detail |
| License | Manajemen lisensi plugin |
| Outlet Elevation | Perhitungan elevasi pipa |
| Plot | Cetak massal ke PDF |
| Rectangle | Gambar rectangle kolom |
| Register | Buka register metadata |
| Renumber Layout | Penomoran layout |
| Safe Explode | Explode aman dengan validasi |
| Selection | Seleksi entitas lanjutan |
| Settings | Pengaturan umum plugin |
| Solid2Hatch | Konversi SOLID ke hatch |
| Title Block | Update kop gambar massal |
| Utility | About, Help, Commands |

<!-- screenshot -->

## Langkah 3: Jalankan Perintah Pertama

Coba jalankan perintah pertama Anda:

1. Ketik `IVO:COMMANDS` di command line
2. Lihat daftar semua perintah yang tersedia
3. Coba ketik `IVO:ABOUT` untuk melihat info plugin

## Langkah 4: Konfigurasikan Pengaturan

Buka pengaturan plugin dengan `IVO:SETTINGS` untuk menyesuaikan:

- **General** — URL Help, preferensi umum
- **Structure > Column** — Tipe kolom default untuk perintah Framing
- **Structure > Bracing** — Tipe bracing default

Lihat halaman [Pengaturan](settings.md) untuk detail lengkap.

## Tips

> [!TIP]
> Semua perintah IngenevoTools menggunakan prefix `IVO:`. Ketik `IVO:` di command line dan gunakan autocomplete BricsCAD untuk menemukan perintah.

> [!TIP]
> Beberapa perintah memiliki alias pendek, misalnya `IVO:SX` untuk `IVO:SAFEEXPLODE`. Lihat dokumentasi masing-masing command untuk mengetahui alias-nya.
