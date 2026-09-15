# IVO:RENUMBERLAYOUT

> Menomori ulang seluruh layout paper space secara berurutan, dengan pratinjau dan konfirmasi.

## Cara Akses

- **Ribbon:** Tab Ingenevo Tools → Panel Sheet Manager → Tombol Renumber Layout
- **Command Line:** `IVO:RENUMBERLAYOUT`
- **Alias:** —

## Cara Penggunaan

1. Atur format penomoran lebih dulu di `IVO:SETTINGS` → **Sheet Manager > Sheet Name**
2. Jalankan perintah `IVO:RENUMBERLAYOUT`
3. Command line menampilkan **pratinjau** nama lama dan nama barunya
4. Muncul konfirmasi:

```
Apply renumbering? [Yes/No] <Yes>:
```

5. Tekan **Enter** untuk menerapkan, atau jawab **No** untuk membatalkan

<!-- screenshot -->

## Tips & Catatan

> [!WARNING]
> Perintah ini membutuhkan **lisensi aktif**. Jalankan [IVO:LICENSE](commands/help/license.md) untuk mengaktifkan lisensi.

> [!NOTE]
> **Perintah ini tidak menanyakan format penomoran di command line.** Prefix, jumlah digit, dan aturan lainnya dibaca dari settings yang tersimpan — sehingga seluruh drawing dalam satu proyek memakai format yang sama tanpa perlu diingat-ingat tiap kali.

> [!TIP]
> Bacalah pratinjaunya sebelum menjawab Yes. Itulah kesempatan terakhir melihat nama baru setiap layout sebelum diterapkan.

> [!TIP]
> Setelah penomoran ulang, jalankan [IVO:SORTLAYOUT](commands/sheet-manager/sortlayout.md) agar urutan tab-nya ikut mengikuti nama baru.

## Lihat Juga

- [IVO:SORTLAYOUT](commands/sheet-manager/sortlayout.md) — mengurutkan tab layout berdasarkan nama
- [IVO:RENUMBERVIEWFRAME](commands/sheet-manager/renumberviewframe.md) — menomori ulang block ViewFrame di model space
- [IVO:SETTINGS](commands/settings/settings.md) — tempat format penomoran diatur
