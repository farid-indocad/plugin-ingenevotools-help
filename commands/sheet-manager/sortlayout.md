# IVO:SORTLAYOUT

> Mengurutkan tab layout berdasarkan nama, menaik, dengan urutan alami.

## Cara Akses

- **Ribbon:** Tab Ingenevo Tools → Panel Sheet Manager → Tombol Sort Layout
- **Command Line:** `IVO:SORTLAYOUT`
- **Alias:** —

## Cara Penggunaan

1. Jalankan perintah `IVO:SORTLAYOUT`
2. Seluruh tab layout langsung diurutkan berdasarkan namanya — **tidak ada pertanyaan apa pun**

<!-- screenshot -->

## Tips & Catatan

> [!WARNING]
> Perintah ini membutuhkan **lisensi aktif**. Jalankan [IVO:LICENSE](commands/help/license.md) untuk mengaktifkan lisensi.

> [!NOTE]
> Pengurutannya **alami (natural sort)**, bukan alfabetis murni. Artinya `SH-2` berada sebelum `SH-10`, bukan sesudahnya seperti pada pengurutan teks biasa.

> [!NOTE]
> Tab **Model** tidak ikut diurutkan — yang ditata hanya layout paper space.

> [!TIP]
> Perintah ini hanya menata urutan tab, **tidak mengubah nama layout**. Untuk menomori ulang namanya, gunakan [IVO:RENUMBERLAYOUT](commands/sheet-manager/renumberlayout.md).

## Lihat Juga

- [IVO:RENUMBERLAYOUT](commands/sheet-manager/renumberlayout.md) — menomori ulang nama layout secara berurutan
- [IVO:ADDLAYOUT](commands/sheet-manager/addlayout.md) — menambah layout dari block ViewFrame
