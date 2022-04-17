---
layout: default
title: Instalasi GeoKKP-GIS
nav_order: 2
parent: Persiapan GeoKKP-GIS
has_children: false
---

# Instalasi Plugin GeoKKP-GIS

Setelah melakukan instalasi QGIS, selanjutnya pada bagian ini akan dijelaskan mengenai cara instalasi plugin GeoKKP-GIS. Sebagai sebuah plugin pada QGIS, GeoKKP-GIS terdaftar pada repository resmi QGIS, dan dapat diinstall dengan berbagai cara, sama seperti plugin QGIS lain pada umumnya. Bab ini akan membahas dua buah cara yang dapat digunakan untuk melakukan instalasi plugin GeoKKP-GIS, yaitu melalui Plugin Manager serta cara manual dengan mengunduh file ***.zip** dari repository GeoKKP-GIS. 

## Ekosistem Plugin pada QGIS

Seperti yang telah kita ketahui, QGIS merupakan sebuah proyek OpenSource, dimana setiap orang bisa berkontribusi dalam pembangunan aplikasi QGIS maupun pengembangan fitur-fitur QGIS dalam berbagai bentuk. Salah satu bentuk pengembangan aplikasi pada QGIS adalah **Plugin**. Plugin dapat digunakan untuk memperkaya fitur-fitur QGIS yang belum disediakan pada bagian utama aplikasi QGIS. 

Plugin juga dapat digunakan untuk membungkus sebuah proses bisnis tertentu dan memungkinkan personalisasi antarmuka pada fungsi-fungsi yang tersedia di QGIS. Plugin QGIS berkembang sangat pesat dan memungkinkan penambahan berbagai fitur yang bahkan tidak dapat dijumpai pada perangkat lunak berbayar sekalipun. Pada saat modul ini ditulis, terdapat lebih dari 1000 plugin berbeda yang terdaftar pada *repository resmi* Plugin QGIS, dan jumlah ini terus bertambah tiap harinya. 

![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220417230558.png)

GeoKKP-GIS merupakan salah satu plugin yang dibangun di dalam ekosistem QGIS ini. Untuk itu, agar dapat menggunakan plugin GeoKKP-GIS di dalam QGIS, pengguna perlu melakukan instalasi plugin terlebih dahulu. 

## Instalasi Plugin GeoKKP-GIS pada QGIS

Instalasi seluruh plugin pada QGIS cukup sederhana. Semua plugin pada QGIS memiliki repository penyimpanan yang secara otomatis terhubung pada QGIS. Terdapat dua cara untuk instalasi plugin pada QGIS:

- Melalui **Plugin Manager**. Ini adalah cara resmi untuk instalasi plugin pada QGIS. Cara ini memerlukan koneksi internet untuk terhubung dengan repository plugin QGIS

- Pada kasus dimana koneksi internet terbatas atau tidak tersedia, instalasi plugin dapat dilakukan secara Offline melalui file ***.zip** dari plugin yang akan diinstal.

Berikut adalah penjelasan untuk kedua cara tersebut:

### Cara Pertama: Instalasi melalui Plugin Manager

1. Pada QGIS, buka menu **Plugins > Manage and Install Plugins**. Pastikan bahwa kita telah memiliki koneksi internet yang memadai untuk melakukan instalasi.
   
   ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220417231116.png)

2. Jendela **Plugin Manager** akan muncul. Plugin Manager inilah yang berfungsi sebagai repository tempat penyimpanan seluruh plugin yang terdaftar pada QGIS
   
   ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220417231150.png)

3. Selama masa pengembangan, plugin GeoKKP-GIS akan ditandai sebagai plugin ‘*experimental*’. Untuk itu, kita perlu terlebih dahulu mengaktifkan pencarian untuk plugin eksperimental. Pada menu di sebelah kanan jendela Plugin Manager, klik pada Settings, kemudian centang opsi untuk “***Show Also Experimental Plugins..***”
   
   ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220417231246.png)

4. Selanjutnya, klik kembali pada menu ‘**All**’. ketikkan ‘*geokkp*’ pada kolom pencarian. Halaman instalasi GeoKKP-GIS akan muncul.
   
   ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220417231318.png)
   
   Klik pada tombol ‘Install Experimental Plugin’ untuk melakukan instalasi plugin tersebut. Pada saat modul ini ditulis, versi terakhir dari GeoKKP-GIS adalah **versi 1.1.6**.  

5. GeoKKP-GIS telah selesai diinstall. Pada jendela utama QGIS Anda saat ini akan muncul menu, toolbar serta panel kerja untuk GeoKKP-GIS
   
   ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220417231530.png)

6. Apabila toolbar dan panel GeoKKP-GIS tidak muncul, klik kanan pada toolbar, kemudian aktifkan centang untuk panel dan toolbar GeoKKP-GIS<img src="https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220417231646.png" title="" alt="" data-align="center">

Pastikan bahwa panel dan toolbar GeoKKP-GIS telah muncul pada jendela QGIS. Dengan demikian, instalasi Plugin GeoKKP-GIS telah selesai dilakukan.



### Cara kedua: Instalasi manual melalui *.zip

Adapun cara kedua instalasi akan diberikan di bawah ini. Ingat bahwa **<mark>cara ini tidak perlu dilakukan jika cara pertama sudah berhasil</mark>**.

1. Terlebih dahulu unduh file *.zip yang tersedia dari laman https://plugins.qgis.org/plugins/geokkp-gis/ yang menyediakan source code plugin GeoKKP-GIS. Klik pada tombol **Download Latest** untuk mengunduh file *.zip dari plugin tersebut.
   
   ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220417234241.png)

2. Pada jendela Plugins Manager (*Plugins > Manage and Install Plugin*), pilih menu **Install from ZIP** dan arahkan pada file *.zip plugin yang sudah diunduh.
   
   ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220417234714.png)

3. Setelah memilih file, maka langkah selanjutnya adalah klik pada **Install Plugin**. Tunggu proses install hingga nanti akan muncul pemberitahuan bahwa proses instalasi telah berhasil.
   
   <img src="https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220417234805.png" title="" alt="" data-align="center">

Dengan demikian, kita telah menyelesaikan proses instalasi GeoKKP-GIS.Tahap terakhir adalah melakukan instalasi plugin-plugin pendukung untuk memudahkan pekerjaan kita dengan bidang penggambaran bidang tanah pada QGIS. Ini akan kita bahas pada sub-bab selanjutnya.
