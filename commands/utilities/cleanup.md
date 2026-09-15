# IVO:CLEANUP

> Menyaring objek terpilih berdasarkan preset, lalu meng-highlight yang cocok. Tidak menghapus apa pun.

## Cara Akses

- **Ribbon:** Tab Ingenevo Tools → Panel Utilities → Tombol Cleanup
- **Command Line:** `IVO:CLEANUP`
- **Alias:** —

## Cara Penggunaan

1. Pilih objek yang ingin disaring (boleh sebelum perintah dijalankan — preselection dihormati)
2. Jalankan perintah `IVO:CLEANUP`
3. Pilih **berkas preset** dari menu bernomor di command line:

```
Select a preset configuration file [1-<structural>/2-<mep>]:
```

4. Pilih **preset** yang ingin dipakai dari berkas tersebut:

```
Select a cleanup preset [1-<Remove Dimension Lines>/2-<Remove Red Lines>]:
```

5. Objek yang cocok dengan kriteria preset akan **ter-highlight** (menjadi seleksi aktif)
6. Command line melaporkan jumlahnya, misalnya `Successfully cleanup 15 objects based on the preset: Remove Dimension Lines`

<!-- screenshot -->

## Tips & Catatan

> [!WARNING]
> Perintah ini membutuhkan **lisensi aktif**. Jalankan [IVO:LICENSE](commands/help/license.md) untuk mengaktifkan lisensi.

> [!NOTE]
> Perintah ini **tidak menghapus, tidak mengubah, dan tidak memindahkan apa pun.** Ia hanya menyaring lalu menyeleksi. Setelah objek ter-highlight, Andalah yang memutuskan langkah berikutnya — tekan `Delete`, ganti layer, atau apa pun.

> [!TIP]
> Preset disimpan sebagai berkas XML di `%AppData%\IngenevoTools\Cleanup\`. Buka foldernya dengan [IVO:OPENSETTINGSFOLDER](commands/settings/opensettingsfolder.md). Kalau folder itu masih kosong, plugin menyalin contoh preset ke sana secara otomatis saat perintah pertama kali dijalankan.

> [!NOTE]
> Satu preset bisa berisi **beberapa filter sekaligus**, dan logikanya adalah **OR** antar filter, **AND** di dalam satu filter. Contoh preset dengan dua filter:
>
> ```
> Filter 1: entityType=LINE, layer=0, linetype=Continuous
> Filter 2: entityType=LINE, layer=Defpoints
> ```
>
> Objek cocok kalau ia LINE di layer `0` dengan linetype `Continuous`, **atau** LINE di layer `Defpoints`.

> [!NOTE]
> Perbandingan teks bersifat **case-insensitive** dan **tanpa wildcard** — `defpoints` sama dengan `Defpoints`, tetapi `Dim*` tidak akan cocok dengan apa pun.

## Lihat Juga

- [IVO:SELECTSIMILARSPECIFIED](commands/utilities/selectsimilarspecified.md) — menyeleksi objek sejenis berdasarkan filter properti
- [IVO:DESELECTSIMILAR](commands/utilities/deselectsimilar.md) — membatalkan seleksi objek sejenis
