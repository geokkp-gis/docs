---
layout: default
title: Menu Penggambaran dan Dimensi
nav_order: 3
parent: Fitur Aplikasi
has_children: false
---

# Menu Penggambaran dan Dimensi

Sub-bab ini melanjutkan penjelasan mengenai menu utama pada toolbar GeoKKP-GIS, meliputi menu penggambaran dan pembuatan dimensi pada GeoKKP-GIS.

## Menu Penggambaran

Menu penggambaran terdiri dari sub-menu sebagai berikut:

![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220422051117.png)

penjelasan untuk tiap menu di atas adalah sebagai berikut:

### Penggambaran Manual

Menu penggambaran manual dibuat untuk memudahkan penggambaran, khususnya pada layer Batas Persil. Berbeda dengan menu digitasi pada QGIS, menu penggambaran manual ini akan secara otomatis melakukan pengecekan topologi sehingga layer yang dihasilkan tidak akan mengalami kesalahan topologi seperti dangling atau overlap. Untuk menggunakan perangkat ini, lakukan sebagai berikut:

1. Tambahkan layer "**(020100) Batas Persil**" menggunakan menu **Tambah Layer**.
   
   ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220422051814.png)
   
   > **Catatan**:
   > 
   > Sekali lagi perlu diingat untuk melakukan pengaturan sistem proyeksi Project pada QGIS sebelum menambahkan layer. Pengaturan ini dapat dilakukan melalui Panel Lokasi seperti yang telah dijelaskan sebelumnya. 

2. Aktifkan layer Batas Persil dengan memilih/menyorotnya pada bagian Daftar Layer
   
   ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220422052230.png)

3. Aktifkan menu gambar manual (![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220422052257.png)), kemudian lakukan digitasi seperti biasa pada batas persil yang dimaksud
   
   ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220422052522.png) 

4. Gunakan klik kanan untuk mengakhiri digitasi. Jendela pengisian atribut akan muncul. Fitur baru akan terbentuk pada layer Batas Persil setelah di klik **OK**.
   
   ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220422052643.png)
   
   Hasilnya adalah:
   
   ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220422052741.png)

5. Menu digitasi ini secara otomatis akan menghindarkan dari adanya overlap data. Apabila kita menambahkan persil baru di tetangga persil tersebut kemudian terjadi overlap:
   
   ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220422052911.png)
   
   Maka menu ini secara otomatis akan mengabaikan bagian yang overlap dan memotong persil tepat pada batas antara kedua bidang tersebut tanpa adanya overlap atau sliver polygon.
   
   ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220422053025.png)

Menu gambar manual ini juga akan secara otomatis mengaktifkan Advanced Digitizing pada QGIS:

![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220422053230.png)

Mode penggambaran dengan **Advanced Digitizing** ini memungkinkan pengguna untuk melakukan digitasi dengan:

* Input koordinat X dan Y serta sudut dan jarak secara beruntun dengan metode COGO (*Coordinate Geometry*)

* Input koordinat, jarak, serta sudut tertentu. Cukup dengan mengetikkan huruf 'a' (= sudut), 'd' (=jarak), 'x' (=koordinat X) serta 'y' (=koordinat Y) pada saat melakukan digitasi untuk mengaktifkan input manual pada tiap bagian tersebut

* Penggambaran dengan metode radial dengan mengunci koordinat masukan X dan Y. Penguncian dapat dilakukan satu kali (tombol satu kunci) maupun terus menerus (tombol dua kunci). Penguncian juga dapat dilakukan

* Penggambaran parallel dan tegak lurus

* Snapping pada sudut tertentu 
  
  ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220422054157.png)

Melalui metode penggambaran dengan Advanced Digitizing ini, pengguna juga mendapatkan keuntungan dari pengaturan topologi otomatis, sehingga kesalahan topologi pada hasil editing dengan tool ini juga akan dikoreksi secara otomatis.

![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220422053653.png)

 Terakhir, menu ini juga dapat digunakan untuk penggambaran dengan metode CAD, sehingga penggambaran yang dilakukan dengan GeoKKP dapat dilakukan dengan sangat rinci sekaligus menggunakan pengecekan topologi otomatis

### Plot Koordinat

Menu plot koordinat telah kita bahas sebelumnya pada penggunaan menu Import CSV/TXT. Menu ini akan menampilkan jendela dimana penggambaran dapat dilakukan berdasarkan atas urutan data dari pasangan titik Lat/Long atau X/Y.

![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220422094919.png)

Pengguna selanjutnya perlu mengatur sistem proyeksi dari data agar data yang diplot tergambar di lokasi yang sesuai.

### Penggambaran dengan Trilaterasi

Mode penggambaran dengan trilaterasi akan memberikan petunjuk lokasi titik dari dua atau tiga buah titik koordinat yang diketahui. Menu ini digunakan bersamaan dengan menu penggambaran manual untuk mendapatkan bentuk persil yang diinginkan. 

Berikut adalah langkah untuk melakukan penggambaran dengan trilaterasi:

1. Buka menu penggambaran dengan trilaterasi
   
   ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220422095621.png)

2. Isi koordinat tersebut dengan cara mengklik tombol **Titik 1**, lalu klik lokasi yang dimaksud yang ada pada QGIS, maka koordinat dari titik tersebut akan langsung terinput ke dalam formulir. 

3. Isi jarak dari titik tersebut, lalu dari titik yang dibuat akan muncul lingkaran dari titik tersebut yang berjarak sesuai dengan jarak yang dimasukkan.
   
   ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220422101913.png)

4. Lakukan hal yang sama untuk titik kedua dan ketiga
   
   ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220422102422.png)
   
   ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220422102445.png)

5. Setelah memasukkan koordinat titik, klik tombol **OK**, maka titik perpotongan antar radius tersebut akan muncul. Titik ini dapat digunakan sebagai titik *snapping* pada penggambaran metode manual

Fitur Trilaterasi tidak wajib menggunakan 3 titik; input data 2 titik pun sudah cukup menghasilkan titik perpotongan. Akan tetapi hasilnya akan berupa 2 titik perpotongan dan pengguna hanya perlu menghapus titik yang tidak perlu.

![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220422102653.png)

### Penggambaran dengan Triangulasi

Penggambaran dengan triangulasi memiliki prinsip yang sama seperti penggambaran dengan trilaterasi. Pengguna cukup memasukkan nilai koordinat (melalui klik pada titik 1 dan titik 2) serta nilai azimuth pada titik baru yang merupakan perpotongan kedua titik tersebut.

![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220422103251.png)

Setelah kedua titik dan azimuth titik selesai dibuat, akan muncul garis perpotongan dari kedua titik tersebut yang menghasilkan sebuah titik baru. Titik ini dapat digunakan dalam kegiatan penggambaran dengan menu penggambaran manual.

![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220422212505.png)

### Penggambaran dengan Azimuth-Jarak

Penggambaran dengan azimuth dan jarak menggunakan prinsip pengukuran poligon terbuka dan tertutup yang biasanya dilakukan menggunakan alat berupa Total Station. Berbeda dengan metode penggambaran yang dapat dilakukan menggunakan perangkat Advanced Digitizing sebelumnya, penggambaran dengan menu ini dapat dilakukan dengan menambahkan koreksi hitungan poligon, baik berupa poligon terbuka maupun poligon tertutup.

![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220422214508.png)

Penjelasan untuk penggunaan menu ini adalah sebagai berikut:

1. Pilih antara poligon terbuka atau tertutup sesuai ukuran di lapangan

2. Masukkan koordinat titik awal poligon. Ini dapat dilakukan dengan memilih titik pada peta (koordinat akan terisi secara otomatis) atau memasukkan nilai X dan Y pada kolom yang tersedia. Pada versi GeoKKP-GIS ini, koreksi ketinggian belum diberikan, sehingga nilai Z selalu diisi dengan nol
   
   > **Catatan**:
   > 
   > Sebelum memilih titik pada peta atau memasukkan koordinat, terlebih dahulu pastikan bahwa sistem proyeksi Project telah diatur sesuai dengan lokasi yang dimaksud. 

3. Buka daftar titik dalam format CSV untuk diimport ke dalam tabel hitungan atau simpan data yang sudah diimport ke dalam tabel hitungan menjadi file CSV

4. Tabel hitungan untuk memasukkan data. Apabila hitungan bowditch dilakukan, maka tabel secara otomatis akan menambahkan kolom-kolom koreksi dy dan dx untuk mendapatkan nilai koordinat akhir dari poligon yang dimaksud

5. Tombol untuk menambahkan titik (baris) baru atau menghapus salah satu titik terpilih 

6. Tombol untuk memulai hitung koordinat untuk menghitung nilai koordinat serta menghitung koreksi bowditch apabila dikehendaki

7. Plot titik untuk menggambar poligon hasil hitungan secara otomatis pada kanvas QGIS

Menu-menu penggambaran di atas mewadahi berbagai kemungkinan penggambaran persil dari metode-metode akuisisi data yang berbeda, seperti pengukuran lapangan dengan Total Station atau daftar koordinat GPS dari perangkat CORS. 

## Menu Dimensi

Menu dimensi digunakan untuk menggambar dimensi ukuran pada persil yang tergambar. Menu dimensi terdiri dari beberapa sub-menu sebagai berikut:

![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220422220053.png)

Seluruh menu dimensi memerlukan layer dimensi "**(020400) Dimensi Pengukuran**" telah ditambahkan pada daftar layer QGIS, sehingga sebelum menggunakan tiap menu tersebut, pastikan bahwa layer dimensi telah ditambahkan melalui menu Tambah Layer, seperti berikut ini:

![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220422221553.png)

Berikut adalah penjelasan untuk masing-masing menu di atas:

### Dimensi Jarak

Dimensi jarak akan menampilkan panjang pada sisi persil tertentu. Berikut adalah langkah untuk penggambaran dimensi persil:

1. Klik pada tombol Dimensi Jarak. Maka kursor akan berubah menjadi penanda berwarna merah. Tempatkan penanda tersebut pada salah satu titik yang akan diukur panjangnya.
   
   ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220422222021.png)

2. Klik pada titik lain untuk membentuk panjang dimensi. Tarik garis yang terbentuk sedikit menjauhi sisi persil yang akan diberi dimensi
   
   ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220422222128.png)

3. **Klik kiri** sekali lagi untuk mengunci penempatan dimensi, kemudian **Klik kanan** untuk mengakhiri editing dimensi
   
   ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220422222249.png)

> **Catatan**:
> 
> Selalu ingat bahwa pada QGIS, klik kanan akan mengakhiri digitasi

Maka dimensi jarak akan tergambar pada sisi tersebut. Dimensi ini tidak hanya berlaku untuk sisi, tetapi juga untuk diagonal ukuran, misalnya, pada saat pembuatan Gambar Ukur.

![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220422222557.png)

### Dimensi Sudut

Dimensi sudut digunakan untuk menampilkan besaran sudut, baik sebuah sudut dalam maupun sudut luar. Penggunaannya sama seperti pada saat pembuatan dimensi jarak, yaitu sebagai berikut:

1. Klik pada menu Dimensi Sudut. Kursor pada kanvas akan berubah menjadi penanda berwarna merah.

2. Total Anda perlu melakukan enam kali klik untuk membuat sebuah dimensi sudut. Klik yang pertama pada titik sudut yang akan diukur
   
   ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220422223647.png)

3. Klik kedua untuk menentukan besar lengkungan dimensi
   
   ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220422223806.png)

4. Klik ketiga dan keempat untuk menentukan sisi yang akan diukur sudutnya
   
   ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220422223904.png)

5. Klik kelima untuk menentukan sudut dalam atau sudut luar yang akan diberi dimensi
   
   ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220422224009.png)

6. Dan **klik kanan** untuk mengakhiri pembuatan dimensi sudut
   
   ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220422224126.png)

7. Baik sudut luar maupun sudut dalam dapat digambarkan melalui menu dimensi ini, seperti pada gambar berikut:
   
   ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220422224539.png)

8. Seluruh informasi sudut dan jarak ini akan disimpan sebagai fitur pada layer Dimensi Pengukuran. Dengan demikian, kita dapat mengatur simbologi maupun nilai dari sudut yang diperoleh tersebut melalui editing pada Tabel Atribut untuk layer Dimensi Pengukuran.
   
   ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220422225039.png)

### Dimensi Titik

Dimensi titik berguna untuk menambahkan informasi koordinat suatu titik. Penggunaannya cukup sederhana: Klik pada lokasi titik yang akan diberikan keterangan koordinat, seperti berikut:

![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220422225421.png)

### Titik Batas Persil

Menu ini akan menampilkan koordinat dari seluruh titik batas layer persil yang aktif. Menu ini bersifat *toggle*, yang artinya dapat dinyalakan dan kemudian dimatikan kembali.

![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220422225849.png)

Layer dimensi digunakan sebagai pelengkap untuk penggambaran, khususnya pada saat pembuatan layout. Untuk itu, layer dimensi juga akan ditambahkan pada saat pembuatan layout, misalnya, pada Gambar Ukur.
