# IVO:ADDLAYOUT

> Menambah layout untuk block ViewFrame yang Anda pilih, tanpa menghapus layout yang sudah ada.

## Cara Akses

- **Ribbon:** Tab Ingenevo Tools → Panel Sheet Manager → Tombol Add Layout
- **Command Line:** `IVO:ADDLAYOUT`
- **Alias:** `IVO:ADL`

## Cara Penggunaan

1. Pilih block **ViewFrame** yang ingin dibuatkan layout (boleh sebelum perintah dijalankan — preselection dihormati)
2. Jalankan perintah `IVO:ADDLAYOUT` atau `IVO:ADL`
3. Jendela progress muncul selama layout dibangun — ada tombol **Cancel** di sana
4. Command line melaporkan jumlah layout yang dibuat, berikut rincian berapa frame yang diklaim tiap tipe ViewFrame:

```
[IngenevoTools] Total Layouts Created: 6.
[IngenevoTools] Viewframe types — A1 Plan: 4, A3 Detail: 2.
```

<!-- screenshot -->

## Tips & Catatan

> [!WARNING]
> Perintah ini membutuhkan **lisensi aktif**. Jalankan [IVO:LICENSE](commands/help/license.md) untuk mengaktifkan lisensi.

> [!NOTE]
> **Tidak ada konfirmasi, dan itu memang tidak diperlukan** — perintah ini hanya menambah, tidak pernah menghapus. Kalau Anda menekan Cancel di tengah jalan, layout yang sudah terbuat **dipertahankan**.

> [!TIP]
> Perintah ini tidak menanyakan paper size, prefix, maupun title block. Semuanya dibaca dari `IVO:SETTINGS` → **Sheet Manager**.

> [!IMPORTANT]
> Baris **Viewframe types** layak dibaca setiap kali. Pola tipe ViewFrame yang terlalu longgar tidak menghasilkan error — ia menelan frame milik tipe lain dan menghasilkan sheet pada skala yang salah. Hasilnya terlihat benar sampai ada yang membuka satu sheet dan membaca viewport-nya. Angka per tipe inilah satu-satunya tanda di layar.

> [!TIP]
> Untuk membangun ulang **seluruh** layout dari nol, gunakan [IVO:CREATELAYOUT](commands/sheet-manager/createlayout.md) — tapi perhatikan bahwa perintah itu menghapus semua layout yang ada lebih dulu.

## Lihat Juga

- [IVO:CREATELAYOUT](commands/sheet-manager/createlayout.md) — membangun ulang semua layout dari nol
- [IVO:RENUMBERVIEWFRAME](commands/sheet-manager/renumberviewframe.md) — menomori ulang ViewFrame sebelum layout dibuat
- [IVO:SORTLAYOUT](commands/sheet-manager/sortlayout.md) — mengurutkan tab layout
