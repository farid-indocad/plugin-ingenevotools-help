# Daftar Command

Seluruh perintah IngenevoTools, dikelompokkan mengikuti panel di tab **Ingenevo Tools** pada Ribbon.

Kolom **Ribbon** menandai apakah perintah punya tombol sendiri. Perintah bertanda **—** hanya bisa dijalankan dari command line — sebagiannya memang sengaja begitu, karena tombol ribbon akan membuang seleksi yang sudah Anda buat.

> [!TIP]
> Daftar yang sama bisa Anda panggil langsung di dalam BricsCAD dengan [IVO:COMMANDS](commands/help/commands.md), tanpa membuka browser.

---

## Print

| Perintah | Alias | Ribbon | Fungsi |
|:---------|:------|:------:|:-------|
| [IVO:PRINTPDF](commands/print/printpdf.md) | — | ✓ | Cetak massal layout ke PDF |

## Sheet Manager

| Perintah | Alias | Ribbon | Fungsi |
|:---------|:------|:------:|:-------|
| [IVO:OPENFOLDER](commands/sheet-manager/openfolder.md) | — | ✓ | Buka folder drawing yang sedang aktif |
| [IVO:UPDATETITLEBLOCK](commands/sheet-manager/updatetitleblock.md) | — | ✓ | Update title block massal dari Excel |
| [IVO:CREATEREGISTER](commands/sheet-manager/createregister.md) | — | ✓ | Buat register Excel untuk drawing aktif dari template |
| [IVO:EDITREGISTER](commands/sheet-manager/editregister.md) | — | ✓ | Buka register Excel milik drawing aktif |
| [IVO:CREATELAYOUT](commands/sheet-manager/createlayout.md) | `IVO:CRL` | ✓ | Ganti **semua** layout dengan yang baru dari block ViewFrame |
| [IVO:ADDLAYOUT](commands/sheet-manager/addlayout.md) | `IVO:ADL` | ✓ | Tambah layout untuk ViewFrame terpilih, layout lama dipertahankan |
| [IVO:SORTLAYOUT](commands/sheet-manager/sortlayout.md) | — | ✓ | Urutkan tab layout berdasarkan nama |
| [IVO:RENUMBERLAYOUT](commands/sheet-manager/renumberlayout.md) | — | ✓ | Penomoran ulang layout secara berurutan |
| [IVO:RENUMBERVIEWFRAME](commands/sheet-manager/renumberviewframe.md) | `IVO:RVF` | ✓ | Nomori ulang block ViewFrame terpilih dari kiri ke kanan |

## Utilities

| Perintah | Alias | Ribbon | Fungsi |
|:---------|:------|:------:|:-------|
| [IVO:SAFEEXPLODE](commands/utilities/safeexplode.md) | `IVO:SX` | ✓ | Explode block satu level, dengan validasi |
| [IVO:MULTISAFEEXPLODE](commands/utilities/multisafeexplode.md) | `IVO:MSX` | ✓ | Explode block bersarang secara rekursif |
| [IVO:CLEANUP](commands/utilities/cleanup.md) | — | ✓ | Saring dan highlight objek yang cocok dengan preset |
| [IVO:SOLID2HATCH](commands/utilities/solid2hatch.md) | `IVO:S2H` | ✓ | Ubah objek SOLID menjadi hatch |
| [IVO:INITIALBLOCK](commands/utilities/initialblock.md) | `IVO:IBLOCK` | ✓ | Normalkan seleksi ke Layer 0 / ByBlock lalu buka dialog BLOCK |
| [IVO:REPLACEBLOCK](commands/utilities/replaceblock.md) | — | ✓ | Ganti instance block dengan block lain |
| [IVO:BLTSCALE](commands/utilities/bltscale.md) | `IVO:BLTS` | ✓ | Atur MSLTSCALE/PSLTSCALE di semua layout |
| [IVO:MATCHALLLAYOUTSETTINGS](commands/utilities/matchalllayoutsettings.md) | `IVO:MALS` | ✓ | Salin page setup ke seluruh layout |
| [IVO:CHANGEBASEPOINT](commands/utilities/changebasepoint.md) | — | ✓ | Ubah titik dasar block |
| [IVO:RECTANGLE](commands/utilities/rectangle.md) | — | — | Gambar rectangle column dengan snap |
| [IVO:SELECTSIMILARSPECIFIED](commands/utilities/selectsimilarspecified.md) | — | ✓ | Seleksi objek sejenis berdasarkan filter |
| [IVO:DESELECTSIMILAR](commands/utilities/deselectsimilar.md) | — | ✓ | Batalkan seleksi objek sejenis |

## Structure

| Perintah | Alias | Ribbon | Fungsi |
|:---------|:------|:------:|:-------|
| [IVO:FRAMING](commands/structure/framing.md) | — | ✓ | Gambar rantai column dan beam sekaligus, gaya LINE |
| [IVO:COLUMN](commands/structure/column.md) | — | ✓ | Gambar column di setiap titik yang ditunjuk, tanpa beam |
| [IVO:BEAM](commands/structure/beam.md) | — | ✓ | Gambar beam berikut label di setiap segmen rantai |
| [IVO:BRACING](commands/structure/bracing.md) | — | ✓ | Gambar detail bracing |
| [IVO:DIM2BRACING](commands/structure/dim2bracing.md) | `IVO:D2B` | ✓ | Ubah dimension linear menjadi bracing |
| [IVO:SCHEDULE](commands/structure/schedule.md) | — | ✓ | Rapikan isi teks tabel member schedule |
| [IVO:STRUCTURALPALETTE](commands/structure/structuralpalette.md) | — | ✓ | Buka/tutup palette Structural |
| [IVO:SHOWSTRUCTURALPALETTE](commands/structure/showstructuralpalette.md) | — | — | Tampilkan palette Structural |
| [IVO:HIDESTRUCTURALPALETTE](commands/structure/hidestructuralpalette.md) | — | — | Sembunyikan palette Structural |
| [IVO:GENCOLUMN](commands/structure/gencolumn.md) | `IVO:GC` | — | Tempatkan column di ujung setiap beam terpilih, beam dipertahankan |
| [IVO:FOOTING](commands/structure/footing.md) | `IVO:FTG` | — | Gambar garis luar footing dari garis muka luar dan garis as |
| [IVO:BOUNDARY](commands/structure/boundary.md) | `IVO:BND` | — | Susun ulang boundary dari garis cyan dan kuning terpilih |
| [IVO:BOUNDARYDUMP](commands/structure/boundary.md) | — | — | Laporkan kenapa sebuah boundary gagal, tanpa menggambar apa pun |

## Civil

| Perintah | Alias | Ribbon | Fungsi |
|:---------|:------|:------:|:-------|
| [IVO:OUTLETELEVATION](commands/civil/outletelevation.md) | `IVO:OE` | ✓ | Hitung elevasi outlet pipa dari titik yang ditunjuk |

## Detail Library

| Perintah | Alias | Ribbon | Fungsi |
|:---------|:------|:------:|:-------|
| [IVO:DETAILLIBRARY](commands/detail-library/detaillibrary.md) | — | ✓ | Buka perpustakaan gambar detail |
| [IVO:DETAILLIBRARYSETTINGS](commands/detail-library/detaillibrarysettings.md) | — | — | Atur folder dan cache Detail Library dari command line |

## Settings

| Perintah | Alias | Ribbon | Fungsi |
|:---------|:------|:------:|:-------|
| [IVO:SETTINGS](commands/settings/settings.md) | — | ✓ | Buka jendela pengaturan plugin |
| [IVO:OPENSETTINGSFOLDER](commands/settings/opensettingsfolder.md) | — | — | Buka folder tempat settings, profil, dan preset disimpan |

## Help

| Perintah | Alias | Ribbon | Fungsi |
|:---------|:------|:------:|:-------|
| [IVO:LICENSE](commands/help/license.md) | — | ✓ | Manajemen lisensi |
| [IVO:HELP](commands/help/help.md) | — | ✓ | Buka dokumentasi online ini |
| [IVO:ABOUT](commands/help/about.md) | — | ✓ | Tampilkan informasi plugin |
| [IVO:COMMANDS](commands/help/commands.md) | — | — | Tampilkan daftar perintah di command line |

---

> [!NOTE]
> Hampir semua perintah di atas membutuhkan **lisensi aktif**. Persisnya ada **tujuh** yang tidak:
>
> [IVO:LICENSE](commands/help/license.md) · [IVO:ABOUT](commands/help/about.md) · [IVO:HELP](commands/help/help.md) · [IVO:COMMANDS](commands/help/commands.md) · [IVO:SETTINGS](commands/settings/settings.md) · [IVO:OPENSETTINGSFOLDER](commands/settings/opensettingsfolder.md) · [IVO:HIDESTRUCTURALPALETTE](commands/structure/hidestructuralpalette.md)
>
> Keenam yang pertama tidak menggambar apa pun. Yang ketujuh masuk daftar karena menolak perintah *berhenti memakai sesuatu* hanya akan mengurung pemakainya bersama palette yang tidak bisa ditutup.
