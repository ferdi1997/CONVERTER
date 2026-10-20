# Konverter KML/KMZ ke CSV — V6

Versi ini mempertahankan fitur V5: hanya titik Homepass dan Pole, estimasi drop cable pada kolom `HOUSE_COMMENT_` berupa angka saja dengan tambahan 25 meter, dan CSV dengan 41 kolom.

## Pembaruan V6
Enam kolom koordinat (`Latitude`, `Longitude`, `BUILDING_LATITUDE`, `BUILDING_LONGITUDE`, `Coordinate__Lat__NEW`, `Coordinate__Long__NEW`) diformat dengan tepat 6 angka di belakang titik desimal. Contoh: `-6.200000`, `106.800000`.

## Deploy ke Vercel
1. Upload isi folder ini ke repository GitHub.
2. Import repository tersebut di Vercel.
3. Deploy sebagai situs statis.

Semua pemrosesan file dilakukan di browser pengguna.
