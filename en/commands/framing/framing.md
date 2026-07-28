# IVO:FRAMING

> Menggambar rangkaian LINE-like chain sekaligus: column di setiap vertex dan beam di setiap segmen.

## How to Access

- **Ribbon:** Ingenevo Tools Tab â†’ Panel Framing â†’ Button Framing
- **Command Line:** `IVO:FRAMING`
- **Alias:** â€”

## How to Use

1. Jalankan perintah `IVO:FRAMING`
2. Klik titik pertama (vertex pertama) â€” column akan ditempatkan di sini
3. Klik titik berikutnya â€” beam akan digambar di segmen, column di vertex
4. Lanjutkan mengklik titik-titik berikutnya untuk membentuk chain
5. Tekan **Enter** atau **klik kanan** untuk mengakhiri perintah

## Options / Parameters

Tipe column yang digunakan dapat diatur melalui `IVO:SETTINGS` â†’ **Structure > Column**.

| Parameter | Deskripsi |
|:----------|:----------|
| **Column Type** | Tipe kolom yang digambar di setiap vertex (diatur di Settings) |

<!-- screenshot -->

## Tips & Notes

> [!TIP]
> Jika Anda hanya membutuhkan column tanpa beam, gunakan [IVO:COLUMN](commands/framing/column.md). Jika hanya membutuhkan beam tanpa column, gunakan [IVO:BEAM](commands/framing/beam.md).

> [!NOTE]
> Perintah ini bekerja seperti LINE â€” klik titik-titik secara berurutan membentuk chain. Column otomatis ditempatkan di setiap titik dan beam di setiap segmen antar titik.

