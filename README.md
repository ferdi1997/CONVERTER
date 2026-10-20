# Konverter KML/KMZ ke CSV — Homepass & Pole (V3)

Aplikasi web statis untuk mengubah file KML/KMZ menjadi CSV. Pemrosesan dilakukan di browser; file tidak diunggah ke server.

## Perbaikan V3
- Hanya memasukkan titik yang memiliki `HOMEPASS_ID` (Homepass) atau `Pole_ID__New_` (Pole).
- Mengabaikan garis jaringan dan poligon sehingga tidak membuat baris koordinat kosong.
- Membaca atribut `SimpleData`, `Data`, dan `description` dengan dukungan namespace XML seperti `kml:SimpleData`.
- Menampilkan jumlah Homepass dan Pole yang masuk ke CSV.
- Tetap mempertahankan skema 41 kolom CSV.

## Deploy ke Vercel
1. Ekstrak ZIP ini.
2. Unggah folder ke GitHub atau impor repository di Vercel.
3. Gunakan konfigurasi static site tanpa Build Command, lalu Deploy.

## Catatan
- Untuk membaca KMZ, browser perlu internet untuk memuat library JSZip dari CDN.
- File KMZ yang hanya menunjuk ke `NetworkLink` eksternal perlu diekspor sebagai KML/KMZ mandiri.
