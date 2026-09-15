# IVO:RENUMBERVIEWFRAME

> Menomori ulang block ViewFrame yang dipilih menurut urutan kiri ke kanan.

## Cara Akses

- **Ribbon:** Tab Ingenevo Tools → Panel Sheet Manager → Tombol Renumber Viewframe
- **Command Line:** `IVO:RENUMBERVIEWFRAME`
- **Alias:** `IVO:RVF`

## Cara Penggunaan

1. Pilih block **ViewFrame** yang ingin dinomori ulang (boleh sebelum perintah dijalankan — preselection dihormati)
2. Jalankan perintah `IVO:RENUMBERVIEWFRAME` atau `IVO:RVF`
3. Nomor baru ditulis ke atribut ViewFrame **menurut posisinya dari kiri ke kanan**

<!-- screenshot -->

## Tips & Catatan

> [!WARNING]
> Perintah ini membutuhkan **lisensi aktif**. Jalankan [IVO:LICENSE](commands/help/license.md) untuk mengaktifkan lisensi.

> [!NOTE]
> **Urutannya ditentukan posisi di model space, bukan urutan Anda memilihnya.** ViewFrame paling kiri mendapat nomor pertama, tidak peduli mana yang Anda klik lebih dulu.

> [!TIP]
> Nama atribut tujuan dan jumlah digit dibaca dari `IVO:SETTINGS` → **Sheet Manager > Viewframe** dan **Sheet Name** — perintah ini tidak menanyakannya.

> [!TIP]
> Jalankan perintah ini **sebelum** [IVO:CREATELAYOUT](commands/sheet-manager/createlayout.md) atau [IVO:ADDLAYOUT](commands/sheet-manager/addlayout.md), karena nama layout diturunkan dari nomor ViewFrame.

## Lihat Juga

- [IVO:CREATELAYOUT](commands/sheet-manager/createlayout.md) — membangun layout dari ViewFrame
- [IVO:ADDLAYOUT](commands/sheet-manager/addlayout.md) — menambah layout dari ViewFrame terpilih
- [IVO:RENUMBERLAYOUT](commands/sheet-manager/renumberlayout.md) — menomori ulang nama layout
