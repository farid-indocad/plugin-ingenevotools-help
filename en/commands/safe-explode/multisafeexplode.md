# IVO:MULTISAFEEXPLODE

> Meng-explode block bersarang secara rekursif sampai menjadi objek primitif.

## How to Access

- **Ribbon:** Ingenevo Tools Tab â†’ Panel Safe Explode â†’ Button Multi Safe Explode
- **Command Line:** `IVO:MULTISAFEEXPLODE`
- **Alias:** `IVO:MSX`

## How to Use

1. Jalankan perintah `IVO:MULTISAFEEXPLODE` atau `IVO:MSX`
2. Pilih satu atau lebih block reference yang ingin di-explode
3. Tekan **Enter** untuk konfirmasi
4. Block akan di-explode secara rekursif hingga semua sub-block menjadi objek primitif (LINE, ARC, CIRCLE, dll.)

<!-- screenshot -->

## Tips & Notes

> [!WARNING]
> Perintah ini bersifat rekursif â€” semua nested block akan di-explode sepenuhnya. Pastikan ini yang Anda inginkan sebelum menjalankan.

> [!NOTE]
> Sama seperti [IVO:SAFEEXPLODE](commands/safe-explode/safeexplode.md), block pada layer terkunci akan di-skip secara otomatis.

