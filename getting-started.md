# Getting Started

Halaman ini mengikuti satu gambar dari awal sampai tercetak. Urutannya yang penting — itulah yang tidak terlihat di ribbon maupun di sidebar.

> [!NOTE]
> Belum memasang plugin? Mulai dari [Instalasi](instalasi.md) dulu.

---

## 1. Aktifkan lisensi

Ketik [`IVO:LICENSE`](commands/help/license.md) dan aktifkan. Tanpa ini hampir semua perintah ditolak — lihat [Daftar Command](daftar-command.md) untuk tujuh pengecualiannya.

## 2. Pilih profil pengaturan

Buka [`IVO:SETTINGS`](commands/settings/settings.md). Installer sudah menanam tiga profil standar kantor — **Default**, **Intrax**, dan **IndoCAD** — jadi Anda tidak perlu menyusunnya dari nol.

Profil menentukan paper size, prefix nama sheet, nama block title block, dan tipe column/beam/bracing. **Perintah-perintah berikutnya membaca dari sini dan tidak akan menanyakannya lagi**, jadi kesalahan di langkah ini akan menyebar ke seluruh gambar.

## 3. Siapkan ViewFrame di model space

Gambar block **ViewFrame** untuk setiap sheet yang akan dibuat, lalu pilih semuanya dan jalankan [`IVO:RENUMBERVIEWFRAME`](commands/sheet-manager/renumberviewframe.md).

Penomorannya mengikuti **posisi kiri ke kanan**, bukan urutan Anda mengklik. Lakukan ini **sebelum** langkah berikutnya, karena nama layout diturunkan dari nomor ViewFrame.

## 4. Bangun sheet-nya

| Situasi | Perintah |
|:--------|:---------|
| Gambar baru, belum ada layout | [`IVO:CREATELAYOUT`](commands/sheet-manager/createlayout.md) — membangun semua layout dari nol |
| Sudah ada layout, mau menambah | [`IVO:ADDLAYOUT`](commands/sheet-manager/addlayout.md) — hanya menambah, tidak menghapus |

> [!WARNING]
> `IVO:CREATELAYOUT` **menghapus seluruh layout yang ada** lebih dulu. Pada gambar yang sheet-nya sudah dikerjakan orang lain, yang Anda inginkan hampir selalu `IVO:ADDLAYOUT`.

## 5. Isi title block dari Excel

Tiga perintah, berurutan:

1. [`IVO:CREATEREGISTER`](commands/sheet-manager/createregister.md) — membuat berkas register Excel di sebelah gambar
2. [`IVO:EDITREGISTER`](commands/sheet-manager/editregister.md) — membukanya untuk Anda isi
3. [`IVO:UPDATETITLEBLOCK`](commands/sheet-manager/updatetitleblock.md) — menuliskan isinya ke atribut title block di tiap layout

Baris Excel dicocokkan ke layout **berdasarkan namanya**. Kalau ada title block yang kosong, itu biasanya karena nama layout dan nama baris tidak sama persis.

## 6. Rapikan sebelum cetak

| Perintah | Gunanya |
|:---------|:--------|
| [`IVO:RENUMBERLAYOUT`](commands/sheet-manager/renumberlayout.md) | Menomori ulang nama layout secara berurutan |
| [`IVO:SORTLAYOUT`](commands/sheet-manager/sortlayout.md) | Menata urutan tab agar mengikuti namanya |
| [`IVO:MATCHALLLAYOUTSETTINGS`](commands/utilities/matchalllayoutsettings.md) | Menyamakan printer, kertas, dan skala di semua layout |

## 7. Cetak

[`IVO:PRINTPDF`](commands/print/printpdf.md) — centang sheet-nya, atur urutannya, pilih satu PDF gabungan atau satu PDF per sheet.

---

## Kebiasaan yang menghemat waktu

> [!TIP]
> **Seleksi dulu, perintah kemudian.** Sebagian besar perintah menghormati objek yang sudah Anda pilih sebelum mengetiknya, jadi Anda tidak perlu memilih dua kali.

> [!TIP]
> **Pakai alias.** `IVO:SX` untuk Safe Explode, `IVO:MSX` untuk Multi Safe Explode, `IVO:CRL` untuk Create Layout. Semuanya tercantum di [Daftar Command](daftar-command.md).

> [!TIP]
> **Ketik `IVO:` lalu biarkan autocomplete BricsCAD bekerja.** Kalau lupa nama perintah, [`IVO:COMMANDS`](commands/help/commands.md) menampilkan seluruh daftarnya tanpa perlu membuka browser.

> [!NOTE]
> Perintah struktur — [Framing](commands/structure/framing.md), [Column](commands/structure/column.md), [Beam](commands/structure/beam.md), [Bracing](commands/structure/bracing.md), [Footing](commands/structure/footing.md) — mengambil tipenya dari palette Structural. Buka dengan [`IVO:STRUCTURALPALETTE`](commands/structure/structuralpalette.md) dan pastikan tipenya benar sebelum mulai menggambar.
