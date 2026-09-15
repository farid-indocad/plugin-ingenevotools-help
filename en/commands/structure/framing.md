# IVO:FRAMING

> Menggambar rangkaian LINE-like chain sekaligus: column di setiap vertex dan beam di setiap segmen.

## How to Access

- **Ribbon:** Ingenevo Tools Tab → Panel Framing → Button Framing
- **Command Line:** `IVO:FRAMING`
- **Alias:** —

## How to Use

1. Jalankan perintah `IVO:FRAMING`
2. Klik titik pertama (vertex pertama) — column akan ditempatkan di sini
3. Klik titik berikutnya — beam akan digambar di segmen, column di vertex
4. Lanjutkan mengklik titik-titik berikutnya untuk membentuk chain
5. Tekan **Enter** atau **klik kanan** untuk mengakhiri perintah

## Options / Parameters

Tipe column yang digunakan dapat diatur melalui `IVO:SETTINGS` → **Structure > Column**.

| Parameter | Deskripsi |
|:----------|:----------|
| **Column Type** | Tipe kolom yang digambar di setiap vertex (diatur di Settings) |

<!-- screenshot -->

## Tips & Notes

> [!TIP]
> Jika Anda hanya membutuhkan column tanpa beam, gunakan [IVO:COLUMN](commands/structure/column.md). Jika hanya membutuhkan beam tanpa column, gunakan [IVO:BEAM](commands/structure/beam.md).

> [!NOTE]
> Perintah ini bekerja seperti LINE — klik titik-titik secara berurutan membentuk chain. Column otomatis ditempatkan di setiap titik dan beam di setiap segmen antar titik.

