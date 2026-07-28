# Instalasi

Panduan memasang plugin IngenevoTools di BricsCAD.

## Prasyarat

- **BricsCAD** V20, V21, V22, V23, V24, V25, atau V26
- Sistem operasi **Windows** (64-bit)

## Metode 1: NETLOAD (Direkomendasikan untuk Development)

Metode paling cepat untuk memuat plugin secara manual.

1. Buka BricsCAD
2. Ketik perintah `NETLOAD` pada command line
3. Pilih berkas assembly output:

```
bin\Debug\<Versi>\BricsCadPlugin.App.dll
```

> [!NOTE]
> Ganti `<Versi>` dengan versi BricsCAD Anda (misalnya `V23`).

4. Plugin akan langsung aktif. Tab **Ingenevo Tools** akan muncul di Ribbon.

## Metode 2: APPLOAD (Persisten per Sesi)

Plugin akan dimuat otomatis setiap kali BricsCAD dibuka.

1. Ketik perintah `APPLOAD` pada command line BricsCAD
2. Klik tombol **Add** dan pilih `BricsCadPlugin.App.dll`
3. Tambahkan ke **Startup Suite** agar plugin dimuat secara otomatis

## Metode 3: Registry DemandLoad (Kebutuhan Produksi)

Untuk distribusi produksi ke banyak komputer.

1. Buka berkas `deploy/registry/register-plugin.reg`
2. Sesuaikan jalur folder instalasi plugin
3. Impor file `.reg` ke registri Windows (double-click atau `regedit`)

> [!WARNING]
> Pastikan path dalam file `.reg` sesuai dengan lokasi instalasi plugin di komputer target.

## Verifikasi Instalasi

Setelah plugin dimuat, verifikasi dengan cara:

1. Periksa tab **Ingenevo Tools** muncul di Ribbon
2. Ketik `IVO:COMMANDS` untuk melihat daftar perintah
3. Ketik `IVO:ABOUT` untuk melihat informasi versi plugin

<!-- screenshot -->
