# IVO:FOOTING

> Menggambar garis luar footing dari garis muka luar dan garis as yang dipilih.

## Cara Akses

- **Ribbon:** — (tidak ada tombol ribbon)
- **Command Line:** `IVO:FOOTING`
- **Alias:** `IVO:FTG`

## Cara Penggunaan

1. Buka palette **Structural** → tab **Footing**, lalu isi kedua nilai offset yang akan dipakai
2. Di drawing, pilih garis muka luar dan garis as yang menggambarkan footing
3. Jalankan perintah `IVO:FOOTING` atau `IVO:FTG`
4. Footing digambar langsung — **tidak ada prompt sama sekali**
5. Pesan keberhasilan **menyebutkan offset yang benar-benar dipakai**, misalnya:

```
[IngenevoTools] Footing created — outer 300, inner 150.
```

<!-- screenshot -->

## Tips & Catatan

> [!WARNING]
> Perintah ini membutuhkan **lisensi aktif**. Jalankan [IVO:LICENSE](commands/help/license.md) untuk mengaktifkan lisensi.

> [!NOTE]
> **Perintah ini tidak bertanya apa-apa, dan tidak membuka palette.** Kedua offset diambil dari tab Footing di palette Structural, yang nilai awalnya berasal dari settings — jadi perintah ini tetap bekerja walaupun palette-nya belum pernah Anda buka.
>
> Palette sengaja tidak ditampilkan oleh perintah ini: Anda menjalankannya di atas seleksi yang baru saja dibuat, dan palette yang tiba-tiba muncul di atas drawing adalah cara paling mudah kehilangan seleksi itu.

> [!TIP]
> Karena tidak ada prompt, **satu-satunya bukti di layar tentang offset mana yang dipakai adalah pesan keberhasilannya.** Biasakan membacanya — footing yang tergambar dari nilai palette yang basi terlihat persis sama dengan yang tergambar dari nilai yang benar.

> [!NOTE]
> Garis sumber **tidak diubah, tidak dipindah, dan tidak dihapus** — perintah ini hanya menambah. Seluruh hasilnya adalah satu langkah undo.

> [!NOTE]
> Kalau salah satu nilai offset di palette tidak valid, perintah menolak berjalan dan menampilkan pesan kesalahan yang sama dengan yang ditampilkan tombol **Create** di palette.

> [!TIP]
> Tab **Footing** tidak punya perintah pembukanya sendiri — bukalah palette Structural dengan [IVO:STRUCTURALPALETTE](commands/structure/structuralpalette.md), lalu klik tab Footing.

## Lihat Juga

- [IVO:BOUNDARY](commands/structure/boundary.md) — perintah asal yang menurunkan IVO:FOOTING, dengan offset tetap
- [IVO:STRUCTURALPALETTE](commands/structure/structuralpalette.md) — membuka palette tempat offset footing diatur
