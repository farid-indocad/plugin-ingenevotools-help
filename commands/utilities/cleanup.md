# IVO:CLEANUP

> Menyaring objek terpilih berdasarkan preset, lalu meng-highlight yang cocok. Tidak menghapus apa pun.

## Cara Akses

- **Ribbon:** Tab IngenevoTools → Panel Utilities → Tombol Cleanup
- **Command Line:** `IVO:CLEANUP`
- **Alias:** —

## Cara Penggunaan

1. Jalankan perintah `IVO:CLEANUP`
2. **Pilih objek yang ingin disaring.** Seleksi yang sudah dibuat sebelum perintah dijalankan langsung dipakai, dan langkah ini dilewati
3. Pilih **berkas preset** dari menu bernomor di command line:

```
Select a preset configuration file [1-<AVIA HOMES>/2-<DIXON>/3-<JGK>/.../11-<VERONA>]:
```

4. Pilih **preset** yang ingin dipakai dari berkas tersebut:

```
Select a cleanup preset [1-<SITE PLAN>/2-<FLOOR PLAN>/3-<ELEVATIONS>]:
```

5. Objek yang cocok dengan kriteria preset akan **ter-highlight** (menjadi seleksi aktif)
6. Command line melaporkan jumlahnya, misalnya `Successfully cleanup 15 object(s) based on the preset: FLOOR PLAN`

<!-- screenshot -->

## Tips & Catatan

> [!WARNING]
> Perintah ini membutuhkan **lisensi aktif**. Jalankan [IVO:LICENSE](commands/help/license.md) untuk mengaktifkan lisensi.

> [!NOTE]
> Perintah ini **tidak menghapus, tidak mengubah, dan tidak memindahkan apa pun.** Ia hanya menyaring lalu menyeleksi. Setelah objek ter-highlight, Andalah yang memutuskan langkah berikutnya — tekan `Delete`, ganti layer, atau apa pun.

> [!TIP]
> **Installer membawa sebelas berkas preset kantor**, satu per builder: AVIA HOMES, DIXON, JGK, MAKAAN, METRICON, ORBIT HOMES QLD, REMMUS, SIMOND, TEMPO, TICK HOMES, dan VERONA. Nama di menu adalah nama berkasnya tanpa awalan `cleanup-`.

> [!NOTE]
> Preset disimpan sebagai berkas XML di `%AppData%\IngenevoTools\Cleanup\`. Buka foldernya dengan [IVO:OPENSETTINGSFOLDER](commands/settings/opensettingsfolder.md).
>
> Kesebelas berkas kantor **ditimpa setiap kali installer dijalankan**, jadi jangan mengubahnya langsung. Kalau Anda butuh varian sendiri, simpan dengan nama lain (misalnya `cleanup-METRICON-nama.xml`) — berkas bernama lain tidak pernah disentuh installer.
>
> Kalau folder itu kosong, perintah berhenti dan **menyebutkan folder tempat preset harus ditaruh**.

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
