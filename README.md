# Konverter KML/KMZ ke CSV — Vercel

Aplikasi web statis untuk mengubah file KML/KMZ menjadi CSV. File diproses di browser pengguna; aplikasi ini tidak memerlukan backend.

## Deploy ke Vercel

1. Ekstrak ZIP ini.
2. Unggah folder proyek ke repository GitHub.
3. Di Vercel, pilih **Add New → Project**, lalu impor repository tersebut.
4. Karena ini situs HTML statis, kosongkan **Build Command** dan **Output Directory** jika diminta.
5. Klik **Deploy**.

Alternatif: gunakan Vercel CLI dari folder ini dengan `vercel`.

## Catatan

- Nama halaman utama harus tetap `index.html`.
- Pembacaan KMZ memerlukan internet untuk memuat library JSZip dari CDN.
- Jika file KMZ tidak terbaca, pastikan file KMZ valid dan berisi file KML.
- Data diproses di browser; tidak ada endpoint server untuk mengunggah data.
