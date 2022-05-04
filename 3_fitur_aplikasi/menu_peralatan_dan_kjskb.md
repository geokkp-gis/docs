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

Georeferencing adalah salah satu jenis operasi spasial yang digunakan untuk memberikan lokasi/koordinat khususnya dari objek berupa gambar. Operasi ini biasanya digunakan pada data masukan berupa gambar hasil scan yang belum memiliki informasi sistem koordinat, misalnya scan gambar ukur.

 Klik pada menu ini di GeoKKP-GIS akan memunculkan jendela Georeferencer QGIS serta dialog penambahan layer raster. Gunakan dialog ini untuk memanggil layer foto atau gambar ukur hasil scan:

![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220501183313.png)

Prinsip kerja dari georeferencer adalah memberikan beberapa koordinat tanah (*ground coordinate*) pada lokasi piksel yang sesuai di gambar sehingga seluruh gambar kemudian dapat di*transformasi* ke dalam posisi yang tepat. Untuk itu, sebelum melanjutkan dengan proses penambahan titik koordinat tanah sebagai titik ikat, terlebih dahulu kita lakukan pengaturan. Klik pada menu **Settings > Transformation Settings**:

![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220501234400.png)

terdapat tiga pengaturan yang penting:

1. Jenis atau tipe transformasi. Pilih **Linear** jika orientasi dan ukuran skala gambar dengan kondisi sebenarnya di lapangan tidak jauh berbeda. Pilih **polinomial 1** untuk kasus lainnya

2. Target SRS. Gunakan sistem proyeksi (CRS) yang sama seperti yang digunakan pada Project, yaitu sesuai dengan zona TM-3 di lokasi yang dimaksud

3. Muat pada QGIS ketika proses selesai. Ini untuk memudahkan operasi selanjutnya di QGIS, tanpa harus memuat ulang layer yang dihasilkan oleh transformasi.

setelah pengaturan selesai, kita dapat melanjutkan dengan memilih titik dan memasukkan koordinat tanahnya. Klik pada salah satu titik yang diketahui koordinatnya, kemudian masukkan koordinat tersebut pada kolom yang tersedia

![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220501234839.png)

Pada gambar di atas, kursor ditempatkan pada salah satu pojok persil yang terdapat pada gambar untuk menandai lokasi tersebut dengan koordinat tanah yang kita miliki. Di sini QGIS memberikan satu fungsi yang sangat berguna, yaitu mengambil koordinat dari muka peta (![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220501235047.png)). Dengan adanya tool ini, kita dapat mengenali lokasi yang terdapat pada muka peta untuk menandai lokasi yang tepat pada kanvas QGIS dengan menggunakan basemap berupa citra satelit.

![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220501235650.png)

Setelah itu, koordinat titik akan secara otomatis terisi pada kolom yang disediakan.

![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220501235807.png)

Lanjutkan pada beberapa titik yang lain. Setelah semua titik selesai, kita akan mendapatkan estimasi akurasi dari proses georeferencing yang kita lakukan dengan memeriksa nilai residu:

![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220502175354.png)

Tabel di bagian bawah gambar tersebut menunjukkan pasangan koordinat di gambar (dalam piksel) serta koordinat tanah yang dipilih. Residual menunjukkan besaran pergeseran antara kombinasi titik-titik tanah dengan posisi titik-titik pada pixel. Setelah nilai residual ini muncul, kita dapat menjalankan transformasi untuk merubah posisi gambar ke lokasi yang tepat.

Jika kita lihat lebih detil, akan muncul garis berwarna merah yang menunjukkan nilai residu:

![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220502000216.png)

Klik pada tombol  ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220502000258.png)untuk memulai transformasi. Hasil akhir dari transformasi ini adalah seperti berikut:

![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220502175739.png)

Setelah mendapatkan gambar pada posisi yang dikehendaki, kita dapat melanjutkan dengan melakukan penggambaran seperti pada contoh sebelumnya.

### Export ke CSV

Menu ini berfungsi seperti namanya, yaitu mengkonversi layer terpilih pada daftar layer menjadi file dengan format CSV. Perintah ini hanya berlaku untuk layer dengan jenis vektor, sehingga apabila layer terpilih berupa raster, akan muncul pesan kesalahan. 

![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220502203000.png)

### Pencarian Atribut

Menu pencarian atribut digunakan untuk menemukan fitur tertentu pada layer vektor yang memiliki suatu atribut tertentu pula. Sebagai contoh, kita dapat mencari persil yang memiliki nomor induk bidang tertentu. Fungsi pencarian atribut ini merupakan penyederhanaan dari fungsi serupa yang disediakan oleh **Attribute Tabel QGIS**.

Menu pencarian atribut bekerja dengan sangat sederhana. Pengguna cukup memilih layer yang akan dicari, kemudian memilih diantara kolom-kolom data dari layer tersebut. Terakhir, pengguna mengetikkan nilai fitur pada kolom yang dicari.

![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220502213317.png)

Proses pencarian fitur akan secara otomatis mengarahkan pengguna pada fitur tersebut di kanvas QGIS.

![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220502213340.png)

## Menu Persetujuan KJSKB

Menu ini hanya terdiri dari satu sub-menu yang berfungsi untuk memberikan persetujuan atas proyek yang dikerjakan oleh Kantor Jasa Surveyor Kadaster Berlisensi (KJSKB). 

![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220502213857.png)

Pengguna dapat mencari peta bidang berdasarkan atas nomor tanda terima yang diinputkan oleh KJSKB. Dengan demikian, operator dapat menentukan apakah Peta Batas Bidang tersebut diterima atau ditolak.

## Menu Pengaturan dan Bantuan

Selain CAD Mode, pada bagian kanan dari menu GeoKKP juga terdapat menu pengaturan dan bantuan. Menu pengaturan digunakan secara umum pada aplikasi GeoKKP-GIS untuk mengatur beberapa konfigurasi umum aplikasi, seperti url untuk server GeoKKP serta pengaturan daftar basemap. pengguna dapat menambahkan basemap atau daftar kantor yang terdaftar, kemudian menyimpan konfigurasi tersebut pada folder lokal untuk digunakan seterusnya pada aplikasi GeoKKP-GIS.

![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220503051501.png)

Adapun menu bantuan digunakan untuk merujuk pada halaman manual ini secara online.
