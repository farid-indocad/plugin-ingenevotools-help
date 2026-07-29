# FAQ / Troubleshooting

Kumpulan pertanyaan dan masalah umum beserta solusinya.

---

## Plugin tidak muncul di Ribbon

**Gejala:** Setelah memuat plugin, tab "Ingenevo Tools" tidak muncul di Ribbon.

**Solusi:**
1. Pastikan Anda memuat file `BricsCadPlugin.App.dll` yang benar (sesuai versi BricsCAD)
2. Periksa command line BricsCAD untuk pesan error saat loading
3. Coba restart BricsCAD dan muat ulang plugin
4. Pastikan versi .NET Framework/SDK yang dibutuhkan sudah terinstal

---

## Error: eLockViolation

**Gejala:** Muncul error `eLockViolation` saat menjalankan perintah dari palette.

**Solusi:**
Ini biasanya terjadi ketika database gambar diakses dari konteks modeless (seperti klik tombol di palette) tanpa document lock. Pastikan plugin yang Anda gunakan adalah versi terbaru yang sudah menangani locking secara otomatis.

---

## Lisensi expired atau tidak valid

**Gejala:** Beberapa fitur tidak bisa diakses, muncul pesan lisensi kadaluarsa.

**Solusi:**
1. Jalankan `IVO:LICENSE` untuk mengecek status dan membuka dialog lisensi
3. Masukkan kode lisensi baru atau perpanjang lisensi yang ada

---

## Perintah tidak ditemukan

**Gejala:** Ketik perintah `IVO:xxx` tapi BricsCAD menampilkan "Unknown command".

**Solusi:**
1. Pastikan plugin sudah dimuat (lihat [Instalasi](instalasi.md))
2. Periksa penulisan perintah — semua perintah menggunakan prefix `IVO:`
3. Jalankan `IVO:COMMANDS` untuk melihat daftar perintah yang tersedia

---

## Batch Print PDF gagal

**Gejala:** Perintah `IVO:PRINTPDF` tidak menghasilkan file PDF.

**Solusi:**
1. Pastikan printer/plotter PDF sudah dikonfigurasi di BricsCAD
2. Periksa pengaturan page setup di layout yang ingin dicetak
3. Pastikan folder output PDF bisa ditulis (tidak read-only)

---

> [!TIP]
> Jika masalah Anda tidak tercantum di sini, hubungi support melalui informasi di halaman [Tentang](about.md).
