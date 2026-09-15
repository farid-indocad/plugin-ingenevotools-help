# Tentang IngenevoTools

## Deskripsi

**Ingenevo Tools** adalah plugin BricsCAD untuk produktivitas drafting dan engineering: penggambaran struktur, pembangunan sheet dari block ViewFrame, pengisian title block massal dari Excel, cetak massal ke PDF, dan sejumlah utilitas gambar.

Daftar lengkap perintahnya ada di [Daftar Command](daftar-command.md).

## Versi

Versi plugin saat dokumentasi ini ditulis: **2.0.0**

> [!TIP]
> Jangan berpegang pada angka di atas — **versi yang benar-benar terpasang di komputer Anda** selalu bisa dilihat lewat [`IVO:ABOUT`](commands/help/about.md) di dalam BricsCAD.

## Kompatibilitas

| BricsCAD | Target .NET | Status |
|:---------|:------------|:-------|
| V20 | .NET Framework 4.6.1 | ✅ Diuji berjalan |
| V21 | .NET Framework 4.6.1 | ⚙️ Dibangun & dikemas, belum diuji berjalan |
| V22 | .NET Framework 4.8 | ⚙️ Dibangun & dikemas, belum diuji berjalan |
| V23 | .NET Framework 4.8 | ✅ Diuji berjalan |
| V24 | .NET Framework 4.8 | ⚙️ Dibangun & dikemas, belum diuji berjalan |
| V25 | .NET Framework 4.8 | ⚙️ Dibangun & dikemas, belum diuji berjalan |
| V26 | .NET 8.0 | ✅ Diuji berjalan |

> [!NOTE]
> Ketiga versi yang sudah diuji menutupi **ketiga target .NET** yang dipakai plugin ini. Empat versi sisanya berbagi target dengan salah satu yang sudah terbukti, jadi yang belum terverifikasi tinggal hal-hal khas per versi SDK-nya — bukan lagi cara plugin dibangun dan dimuat.

## Pembuat

- **Perusahaan:** Ingenevo

> [!IMPORTANT]
> **Website dan email support belum diisi.** Isilah dua baris di bawah ini sebelum situs dibagikan ke drafter — halaman [FAQ](faq.md) mengarahkan pembaca ke sini untuk menghubungi tim.
>
> - **Website:** _(belum diisi)_
> - **Email support:** _(belum diisi)_

## Hak Cipta

Copyright © 2026 Ingenevo. Seluruh hak dilindungi.

Ingenevo Tools adalah perangkat lunak proprietary. Tidak ada izin yang diberikan untuk menyalin, memodifikasi, atau mendistribusikan ulang tanpa persetujuan tertulis dari Ingenevo.

## Kontak Support

1. Periksa halaman [FAQ](faq.md) lebih dulu — sebagian besar masalah lapangan ada di sana
2. Hubungi tim Ingenevo lewat informasi di atas, dengan melampirkan berkas log yang relevan:

| Masalah | Berkas yang dilampirkan |
|:--------|:------------------------|
| Pemasangan | `%LocalAppData%\Ingenevo\install-log.txt` |
| Lisensi | `%AppData%\IngenevoTools\license-log.txt` |

## Versi Dokumentasi

Situs ini dibangun dengan [Docsify](https://docsify.js.org/) dan di-hosting di [GitHub Pages](https://pages.github.com/).
