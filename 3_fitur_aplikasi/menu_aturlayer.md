---
layout: default
title: Menu Pengaturan Layer
nav_order: 3
parent: Fitur Aplikasi
has_children: false
---

# Menu Utama GeoKKP-GIS

Pada sub bagian ini akan dijelaskan lebih jauh mengenai perangkat-perangkat yang terdapat pada menu utama GeoKKP-GIS. Tiap perangkat memiliki peran tersendiri dalam alur pengolahan data dengan GeoKKP. 

## Menu Login Pengguna

GeoKKP-GIS terhubung dengan layanan API pada server GeoKKP, sehingga untuk dapat mengakses berbagai perangkat yang terdapat pada menu GeoKKP-GIS, pengguna perlu untuk melakukan login terlebih dahulu. Untuk itu, pengguna cukup mengklik pada tombol "**Masuk Pengguna**", kemudian memasukkan username dan password yang sudah terdaftar pada sistem.

![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220421223655.png)

Pengguna dapat menyimpan username dan password yang digunakan untuk login dengan mencentang pada kolom "**Simpan Login**". Informasi ini akan dapat digunakan di project yang sama pada QGIS, dan akan dihapus apabila pengguna menutup QGIS atau membuka project baru untuk menghindari kebocoran data

Setelah melakukan login, pengguna perlu untuk terlebih dahulu mengatur lokasi kerja serta sistem proyeksi dari project QGIS yang sedang aktif. Untuk itu, alur login pengguna akan dijelaskan secara khusus di sub-bab selanjutnya.

## Menu Tambah Layer

Klik pada ikon ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220421224612.png) akan memunculkan daftar layer yang dapat ditambahkan pada QGIS seperti berikut:

<img src="https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220421224748.png" title="" alt="" data-align="center">

Daftar layer yang ditampilkan pada menu tersebut mengacu pada standar spasial ATR/BPN, baik kategori layer maupun nama layer. Dengan demikian, untuk mencari layer dapat dilakukan dengan mengetikkan kode atau nama layer yang dicari pada kolom pencarian yang tersedia. Sebagai contoh apabila akan dicari layer “Dimensi Pengukuran”, maka cukup ketik "*Dimensi Pengukuran*" atau "*020400*" di kolom pencarian.

<img src="https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220421225019.png" title="" alt="" data-align="center">

Centang pada layer-layer yang akan ditambahkan pada QGIS, kemudian klik **Tambah Layer**. Layer tersebut berikut dengan simbologi dan atributnya akan muncul pada daftar layer di QGIS:

<img src="https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220421225539.png" title="" alt="" data-align="center">

Setelah membuat layer melalui menu di atas, selanjutnya dapat dilakukan penggambaran. Berbagai metode penggambaran pada GeoKKP-GIS akan dibahas selanjutnya di bawah ini.

> **Catatan**:
> Berbeda dengan AutoCAD dimana penggambaran biasanya dilakukan terlebih dahulu, pada QGIS penggambaran layer perlu diawali dengan membuat layer yang akan diisi terlebih dahulu. Untuk itu, diberikan menu Ubah Layer seperti di bawah untuk memindahkan fitur yang telah di digitasi pada salah satu layer. 

## Menu Ubah Layer

Apabila menu **Tambah Layer** di atas membuat layer baru yang belum ada pada QGIS, maka menu **Ubah Layer** ini akan memindahkan fitur pada salah satu layer ke layer yang lain.    

![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220421230845.png)

Pada contoh di atas, kita ingin memindahkan hasil penggambaran (digitasi) yang pada awalnya dilakukan di layer "**Batas Persil**" ke layer baru sebagai "**Bangunan Rumah**". Apabila kita tidak mencentang "*Hanya objek terpilih*", maka seluruh fitur pada layer Batas Persil akan dipindahkan menjadi layer "**Bangunan Rumah**". Jika "*Hanya Objek Terpilih*" dicentang, maka kita perlu menggunakan tool Feature Selection pada QGIS (![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220421231417.png)) untuk memilih fitur mana yang akan dipindahkan. 

Selanjutnya, plugin akan secara otomatis membuat layer baru sesuai pilihan pada jendela **Ubah Layer**:

![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220421231529.png)

Menu ini berguna pada saat penggunaan panel, misalnya panel Partisipatif, untuk memindahkan layer yang dibuat pada saat penggambaran menjadi layer lain yang akan dikirimkan pada server GeoKKP sesuai dengan format yang telah ditentukan pada server.

## Menu Tambah Data

Menu tambah data terdiri dari beberapa sub-menu sebagai berikut:

<img src="https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220421231943.png" title="" alt="" data-align="center">

Fungsi utama menu ini adalah untuk menambahkan data baru ke dalam QGIS. Penjelasan untuk tiap menu adalah sebagai berikut:

### Tambah Data

Menu ini akan memanggil perangkat **Data Source Manager** pada QGIS. Perangkat ini digunakan untuk memanggil jenis data apapun yang dikenali oleh QGIS. Daftar lengkap data yang didukung oleh QGIS dapat dilihat [di sini](https://docs.qgis.org/3.22/en/docs/user_manual/managing_data_source/supported_data.html).

![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220421233250.png)

### Import CSV dan Import GPX

Kedua menu ini dibuat untuk memudahkan penambahan data bertipe CSV/TXT maupun GPX. Pada dasarnya, kedua jenis data ini juga dapat ditambahkan menggunakan menu "**Tambah Data**" di atas. Akan tetapi kedua menu ini digunakan untuk memudahkan pengguna menambahkan kedua jenis tipe data ini dengan lebih mudah.

Menu CSV/TXT akan membaca data dengan format Lat/Long atau X/Y secara otomatis. Format data yang digunakan sebagai masukan adalah Delimited Data seperti berikut:

```csv
317011.23664018, 941524.78167574;
317044.22393406, 941483.50243035;
317066.94761492, 941500.17142917;
317029.53821057, 941535.97905399;
```

Format data tersebut dapat diperoleh dengan mengkonversi tabel data (misalnya pada format Excel) menjadi format CSV atau Delimited TXT. SIstem akan memanggil jendela **Plot Koordinat** pada menu penggambaran, kemudian memberikan opsi untuk pemilihan sistem proyeksi untuk plotting data.

> **Catatan**:
> 
> *Ingat bahwa data teks tidak mengandung informasi sistem proyeksi, hanya koordinat saja. Apabila hal ini dapat dilakukan dengan mudah pada AutoCAD, pada GIS kita perlu mendefinisikan sistem proyeksi agar baris-baris koordinat ini dapat tergambar pada lokasi yang tepat*

![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220421233936.png)  

Sistem juga akan secara otomatis mengenali kesalahan input data pada teks atau pada file yang diimport, sehingga pengguna memiliki kesempatan untuk memperbaiki kesalahan pada data sebelum data ini ditambahkan pada QGIS.

![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220421234311.png)

Setelah semua kesalahan selesai dikoreksi, maka GeoKKP akan membuat layer baru dan secara otomatis membentuk poligon berdasarkan urutan data masukan yang diberikan:

![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220422000223.png)

> **Catatan:**
> 
> Penting untuk diingat bahwa pada saat pemilihan sistem proyeksi seperti di atas, kita juga perlu memperhatikan sistem proyeksi yang sedang aktif pada QGIS. Sistem proyeksi yang kita pilih harus sama dengan sistem proyeksi yang sedang aktif di proyek QGIS tersebut (lihat di bagian pojok kiri bawah dari jendela QGIS):
> 
> ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220422000542.png)

Adapun menu Import GPX akan secara otomatis membaca layer-layer dari file tracking GPS tersebut seperti di bawah ini:

![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220422000718.png)

Pada gambar di atas, layer *track_point*, *route_point*, *track* serta *route*dibuat secara otomatis oleh GeoKKP berdasarkan atas data yang diperoleh dari file GPX yang diinputkan.

### Import DXF/DWG

Menu Import DXF/DWG (![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220422000936.png)) akan memanggil jendela import DXF yang terdapat pada QGIS. Pada jendela ini dapat dilakukan beberapa pengaturan sebelum menambahkan layer yang diminta pada QGIS, seperti pemilihan layer dan sistem proyeksi.

![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220422001112.png)

### Menu Import Wilayah Administrasi

Menu ini pada dasarnya adalah duplikasi dari menu **IMPADM** pada GeoKKP versi AutoCAD. Menu ini memanggil data batas administrasi yang terdaftar pada server GeoKKP sehingga dapat diunduh dan digunakan pada operasi-operasi yang memerlukan batas administrasi, seperti pembuatan persil pada **Panel APBN**.

![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220422001519.png)

Karena memerlukan informasi lokasi, maka apabila pengguna belum mengatur informasi lokasi ini, akan muncul peringatan yang mengharuskan pengguna memilih lokasi kantor. Pemilihan lokasi kantor dilakukan pada **Panel Lokasi**di sebelah kanan:

 ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220422001701.png)

Klik pada kolom **Kantor**, kemudian pilih salah satu kantor yang terdaftar sesuai dengan akun pengguna. Selanjutnya, klik pada tombol "**Simpan Area Kerja**" untuk mengkonfirmasi pemilihan lokasi kantor. Akan muncul pemberitahuan bahwa  pemilihan lokasi berhasil dilakukan. 

Selanjutnya, menu IMPADM dapat digunakan sesuai dengan lokasi kantor yang terdaftar:

![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220422001943.png)

> **Catatan**:
> 
> Sekali lagi, pemilihan Zona TM-3 harus sesuai dengan lokasi kantor yang terdaftar. Kesalahan pemilihan zona (misal pada gambar di atas dimana zona untuk Papua jelas bukan TM3-46.2) akan mengakibatkan data tergambar di kanvas QGIS pada lokasi yang salah

### Tambah Basemap

Menu ini akan memunculkan daftar layer basemap yang dapat digunakan sebagai latar belakang. Pada umumnya latar yang digunakan adalah gambar citra satelit dari penyedia layanan citra, seperti Bing Satellite dan Google Satellite. Klik pada salah satu layanan basemap yang tersedia, kemudian klik "**Tambah Layer Basemap**".

![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220422005104.png)

Apabila pengguna ingin menambahkan layer baru, menu pengaturan GeoKKP-GIS dapat digunakan untuk keperluan ini.  Informasi yang diperlukan adalah link url dalam format XYZ tiles sebagai layer yang akan ditambahkan ke dalam QGIS.

> **Catatan**:
> 
> *QGIS mendukung ratusan jenis basemap yang dapat digunakan. Plugin Quick Map Services (QMS) dapat digunakan untuk menambahkan berbagai jenis layer basemap ini dengan mudah pada QGIS.*

### Tambah OpenAerialMap

OpenAerialMap merupakan layanan untuk mengunggah mosaik foto udara secara cuma-cuma. Apabila pada Kantor Pertanahan terdapat mosaik foto udara hasil pemotretan dengan PUNA (*Pesawat Udara Nir-Awak*), maka pengguna pada kantah tersebut dapat mengunggah data ke dalam OpenAerialMap, kemudian menggunakan layanan data dalam bentuk service TMS (*Tile Map Service*) atau WMTS (*Web Map Tile Service*) pada GeoKKP menggunakan menu ini. 

Pada website OpenAerialMap (http://openaerialmap.org/), klik **Start Exploring**, kemudian lakukan pencarian pada mosaik foto udara sesuai dengan lokasi mosaik foto tersebut. Klik pada kotak berwarna biru untuk menampilkan informasi detil dari foto udara yang dimaksud.

![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220422005320.png)

Kemudian, klik pada tombol WMTS untuk meng*copy* link yang dibutuhkan.

![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220422005532.png)

Setelah mendapatkan link tersebut, gunakan menu ini untuk menambahkan data pada GeoKKP-GIS. Berikan nama layer yang sesuai dan *paste* link yang telah diperoleh pada kolom Link WMTS:

![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220422005616.png)

Mosaik foto udara akan dipanggil dalam bentuk service (tidak perlu mengunduh seluruh mosaik foto) dan dimunculkan pada QGIS sehingga dapat digunakan sebagai latar belakang pada saat penggambaran.

![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220422005715.png)
