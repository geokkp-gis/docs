---
layout: default
title: Menu Peralatan dan Perizinan KJSKB
nav_order: 5
parent: Fitur Aplikasi
has_children: false
---

# Menu Peralatan dan Perizinan KJSKB

Pada sub-bab ini akan dibahas menu-menu pendukung yang terkumpul pada menu Peralatan. Menu peralatan ini digunakan untuk mendukung operasional GeoKKP-GIS, seperti untuk mengatur lokasi kerja, mencari lokasi, dst. Pada bagian ini juga dibahas mengenai menu perizinan Kantor Jasa Surveyor Berlisensi (KJSKB).

## Menu Peralatan

Menu peralatan terdiri dari berbagai sub-menu yang digunakan untuk mendukung penggunaan GeoKKP-GIS. Menu Peralatan terdiri dari sub-menu sebagai berikut:

![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220430032835.png)

Penjelasan untuk tiap menu adalah sebagai berikut:

### Atur Lokasi Kerja

Seperti yang telah disebutkan di bagian awal panduan ini, penggunaan plugin GeoKKP-GIS perlu melibatkan pengaturan beberapa hal terlebih dahulu, seperti misalnya pengaturan Sistem Proyeksi (CRS) dari project yang sedang aktif. Menu **Atur Lokasi Kerja** ini akan secara otomatis memberikan lokasi estimasi dari Kabupaten/Kota wilayah kerja sebagai pendekatan untuk pengaturan kantor, sekaligus memberikan pengaturan untuk sistem proyeksi Project menjadi proyeksi TM-3 yang sesuai dengan lokasi tersebut.

![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220428212440.png)

Hasilnya adalah sebagai berikut:

![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220430032716.png)

### Pencarian Alamat

Menu pencarian alamat menggunakan perangkat Geocoding (pencarian lokasi) yang terdapat pada QGIS. Pencarian ini menggunakan Nominatim, yaitu perangkat Geocoding yang berbasis pada data OpenStreetMap (OSM). Pencarian dibatasi hanya di wilayah Indonesia, sehingga hasil yang diperoleh tidak akan berupa titik di luar wilayah Indonesia.

![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220430033232.png)

Jika pencarian memberikan lebih dari satu hasil, maka akan muncul daftar yang dapat dipilih:

![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220430033703.png)

Hasil pencarian lokasi berupa layer titik baru yang menunjukkan lokasi tersebut:

![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220430033951.png)



### Menu Transformasi Koordinat

Menu transformasi koordinat digunakan untuk melakukan konversi satu arah dari koordinat lintang-bujur (*geographic*) menuju koordinat UTM dan TM3 dari koordinat tersebut. Menu ini juga sekaligus memberikan zona UTM dan TM3 dari hasil konversi koordinat ini.

![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220430220747.png) 

Hasil dari konversi koordinat kemudian dapat dicopy ke dalam clipboard untuk digunakan selanjutnya.

>  Catatan:
> 
> Perlu diingat bahwa urutan data masukan adalah **Lintang, Bujur**



### Menu Zoom To XY

Menu ini digunakan untuk memindahkan zoom kanvas ke lokasi tertentu apabila diketahui koordinat X dan Y dari lokasi tersebut pada sembarang sistem proyeksi. 

Pengguna cukup memasukkan koordinat x atau bujur serta y atau lintang pada kolom yang tersedia, kemudian memilih sistem proyeksi yang sesuai dengan koordinat tersebut. GeoKKP-GIS kemudian akan melakukan zoom pada lokasi yang dimaksud dan memberikan indikator lokasi koordinat tersebut.

![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220430221405.png)

Berikut adalah contoh penggunaan menu ini pada koordinat dengan sistem proyeksi TM3:

![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220430221538.png)



### Menu Gambar NLP

Nomor Lembar Peta (NLP) pada peta-peta yang dibuat di Badan Pertanahan Nasional disusun berdasarkan atas grid yang dibentuk pada skala yang berbeda. Menu ini memudahkan pengguna untuk mengidentifikasi nomor lembar peta di koordinat tertentu.

![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220501010603.png)

selain menentukan nomor lembar peta, menu tersebut juga akan menambahkan layer berupa batas nomer lembar peta tersebut ke dalam kanvas QGIS. Pengguna juga dapat mengcopy NLP yang dihasilkan ke dalam *clipboard* untuk digunakan di perangkat lain.

Menu ini juga akan secara otomatis mendeteksi pengaturan sistem proyeksi. Apabila dijumpai sistem proyeksi belum diatur sesuai dengan sistem koordinat TM-3, maka akan muncul peringatan untuk terlebih dahulu mengatur sistem koordinat project. Selain itu, apabila pengguna memilih lokasi TM-3 yang tidak sesuai dengan titik yang di-klik, akan muncul pemberitahuan.

![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220501011109.png)



### Menu Georeference/Rubbersheet

