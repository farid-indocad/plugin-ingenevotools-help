# IVO:SAFEEXPLODE

> Meng-explode block reference terpilih satu level dengan validasi (skip layer terkunci).

## Cara Akses

- **Ribbon:** Tab Ingenevo Tools → Panel Safe Explode → Tombol Safe Explode
- **Command Line:** `IVO:SAFEEXPLODE`
- **Alias:** `IVO:SX`

## Cara Penggunaan

1. Jalankan perintah `IVO:SAFEEXPLODE` atau `IVO:SX`
2. Pilih satu atau lebih block reference yang ingin di-explode
3. Tekan **Enter** untuk konfirmasi
4. Block akan di-explode satu level — sub-block di dalamnya tetap utuh

<!-- screenshot -->

## Tips & Catatan

> [!NOTE]
> Perintah ini lebih aman dari EXPLODE bawaan karena:
> - Otomatis melewati (skip) block pada layer yang terkunci
> - Hanya meng-explode satu level, tidak rekursif

> [!TIP]
> Untuk explode rekursif sampai menjadi objek primitif, gunakan [IVO:MULTISAFEEXPLODE](commands/safe-explode/multisafeexplode.md).
