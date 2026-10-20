# Konverter KML/KMZ ke CSV — Homepass & Pole (V5 Drop Cable + 25 m)

Aplikasi web statis untuk mengubah file KML/KMZ menjadi CSV. Pemrosesan dilakukan di browser; file tidak diunggah ke server.

## Fitur V5
- Memasukkan titik Homepass dan Pole; garis jaringan dan poligon diabaikan.
- Membaca atribut `Data`, `SimpleData`, dan `description`, termasuk namespace XML.
- Kolom `HOUSE_COMMENT_` pada Homepass diisi angka saja: jarak garis lurus FAT ke Homepass (meter) + tambahan 25 meter.
- Mencocokkan `FAT_CODE` dari popup Homepass dengan `FAT_ID_NETWORK_ID` pada popup FAT.
- Mempertahankan skema 41 kolom CSV.

## Perhitungan jarak
Jarak dihitung dari koordinat FAT ke Homepass dengan rumus Haversine, dibulatkan ke meter terdekat, lalu ditambah 25 meter. Nilai ini merupakan estimasi, bukan panjang rute kabel aktual. Jika FAT tidak ditemukan atau koordinat tidak valid, jarak tidak diisi.

## Deploy ke Vercel
1. Ekstrak ZIP ini.
2. Unggah folder ke GitHub atau impor repository di Vercel.
3. Gunakan konfigurasi static site tanpa Build Command, lalu Deploy.

## Catatan
- Untuk membaca KMZ, browser perlu internet untuk memuat library JSZip dari CDN.
- File KMZ yang hanya menunjuk ke `NetworkLink` eksternal perlu diekspor sebagai KML/KMZ mandiri.
