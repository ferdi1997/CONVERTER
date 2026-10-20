# Konverter KML/KMZ ke CSV — Homepass & Pole (V4 Drop Cable)

Aplikasi web statis untuk mengubah file KML/KMZ menjadi CSV. Pemrosesan dilakukan di browser; file tidak diunggah ke server.

## Fitur V4
- Memasukkan titik Homepass dan Pole; garis jaringan dan poligon diabaikan.
- Membaca atribut `Data`, `SimpleData`, dan `description`, termasuk namespace XML.
- Mengisi kolom `HOUSE_COMMENT_` dengan estimasi jarak `DROP CABLE: X m` untuk Homepass.
- Mencocokkan `FAT_CODE` dari popup Homepass dengan `FAT_ID_NETWORK_ID` pada popup FAT.
- Mempertahankan skema 41 kolom CSV.

## Perhitungan jarak
Jarak dihitung dari koordinat FAT ke Homepass dengan rumus geodesik garis lurus (Haversine), dibulatkan ke meter terdekat. Ini adalah estimasi jarak koordinat, bukan panjang rute kabel aktual. Jika FAT tidak ditemukan atau koordinat tidak valid, jarak tidak diisi.

## Deploy ke Vercel
1. Ekstrak ZIP ini.
2. Unggah folder ke GitHub atau impor repository di Vercel.
3. Gunakan konfigurasi static site tanpa Build Command, lalu Deploy.

## Catatan
- Untuk membaca KMZ, browser perlu internet untuk memuat library JSZip dari CDN.
- File KMZ yang hanya menunjuk ke `NetworkLink` eksternal perlu diekspor sebagai KML/KMZ mandiri.
