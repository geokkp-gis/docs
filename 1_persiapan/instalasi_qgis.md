---
layout: default
title: Instalasi QGIS
nav_order: 1
parent: Persiapan GeoKKP-GIS
has_children: false
---

# Instalasi QGIS

Aplikasi GeoKKP-GIS dibuat dalam bentuk plugin di QGIS untuk memanfaatkan  kekayaan fungsi analisis dan dukungan data geospasial yang dimiliki oleh QGIS. Sebelum lebih jauh mengenal plugin GeoKKP-GIS dan melakukan instalasi, terlebih dahulu kita akan berkenalan dengan QGIS sebagai sebuah aplikasi GIS *open-source*.

## Tentang QGIS

QGIS ([http://qgis.org](http://qgis.org)) merupakan perangkat lunak bebas dan terbuka (*free and open source*) yang memiliki berbagai fungsi untuk keperluan sistem informasi geografis, termasuk untuk akuisisi, pengolahan, analisis dan visualisasi data geospasial dari berbagai sumber. Penggunaan QGIS sepenuhnya **tidak dipungut biaya**, dan unduhan QGIS dapat diperoleh secara gratis dari website resminya. Versi terbaru QGIS, yang dirilis tiap tiga bulan sekali, dapat dijumpai secara berkala dari website ini.

![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220417220532.png)

Selain itu, QGIS juga memiliki dukungan komunitas dan dokumentasi yang lengkap. Berbagai komunitas baik nasional maupun internasional memberikan dukungan untuk penggunaan QGIS yang lebih baik serta membantu penanganan masalah yang terjadi bagi pengguna baru. Komunitas QGIS di Indonesia dapat dijumpai pada [https://qgis-id.github.io/](https://qgis-id.github.io/) serta pada grup telegram [@qgisid](https://t.me/qgisindonesia).

![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220417221635.png)

Sebagai perangkat lunak bebas dan terbuka, pengembangan QGIS dapat dilakukan oleh siapapun, dan fungsi-fungsi pada QGIS dapat diperluas untuk berbagai keperluan. Kemampuan QGIS tidak terbatas pada menu utama yang Anda jumpai pada saat instalasi. Apabila Anda memerlukan suatu fungsi yang belum dijumpai pada QGIS, besar kemungkinan Anda akan dapat menemukannya sebagai ekstensi atau **plugin** QGIS yang dikembangkan oleh pengembang perangkat lunak di berbagai belahan dunia. 

Plugin-plugin ini, sama seperti QGIS, dapat Anda gunakan secara **gratis**, dan dapat Anda jumpai dengan mudah pada Plugin Manager di QGIS. Berbagai fungsi tambahan pada QGIS dapat Anda jumpai di sini.  Pada saat panduan ini ditulis, terdapat lebih dari seribu plugin yang dapat dijumpai pada repository resmi QGIS. Jumlah ini masih akan terus bertambah seiring keinginan para pengembang aplikasi untuk menambahkan berbagai fungsi yang spesifik pada QGIS.

Untuk itu, GeoKKP yang difungsikan sebagai antarmuka utama pada kegiatan pertanahan juga dikembangkan sebagai sebuah *plugin* pada QGIS. Modul ini akan menjelaskan mengenai bagaimana melakukan instalasi QGIS serta Plugin GeoKKP-GIS, berikut dengan beberapa plugin lain yang dapat membantu penggunaan GeoKKP GIS untuk melakukan pengolahan data-data pertanahan di lingkungan Kementrian ATR/BPN.

## Memahami versi rilis QGIS

Sebagai sebuah perangkat lunak bebas dan terbuka, pengembangan QGIS berjalan demikian pesatnya sehingga berbagai fitur baru terus-menerus ditambahkan pada kode dasar QGIS. Dengan demikian, kita dapat menjumpai versi baru QGIS tiap beberapa bulan sekali. 

Untuk itu, secara umum dapat kita jumpai dua jenis QGIS yang ada pada setiap siklus rilis: QGIS versi LTR dan QGIS versi terbaru. QGIS versi LTR (*Long-term Release*) biasanya lebih stabil, sedangkan versi rilis terbaru memiliki lebih banyak fitur. Plugin GeoKKP-GIS dibangun di atas **QGIS LTR**, meskipun dukungan pada QGIS versi terbaru juga sangat memungkinkan. Apabila versi QGIS Anda mengalami masalah atau belum didukung secara penuh oleh plugin GeoKKP-GIS

## Instalasi QGIS

QGIS merupakan perangkat lunak *multiplatform*. Artinya, QGIS dapat digunakan di berbagai sistem operasi berbeda: Windows, Linux, Mac, dan seterusnya. Pengembangan QGIS kini bahkan merambah ke aplikasi survey lapangan dengan menggunakan perangkat mobile (Android dan iOS). 

> *Panduan ini dan contoh-contoh setelahnya mengasumsikan penggunaan sistem operasi Windows. Untuk sistem operasi lain, silahkan mengacu pada panduan yang tersedia di website resmi QGIS.org*

Secara umum, terdapat dua buah cara untuk melakukan instalasi perangkat lunak QGIS pada sistem operasi Windows, yaitu melalui **Standalone Installer** serta melalui **OSGeo4W Installer**. Pada bagian ini hanya akan diberikan contoh instalasi melalui Standalone Installer, mengingat kemudahannya untuk pengguna pemula. 

Langkah berikut adalah panduan singkat untuk instalasi perangkat lunak QGIS:

1. Akses halaman https://qgis.org/en/site/forusers/download.html untuk mengunduh instalasi **Standalone QGIS**. Klik pada menu Download dari halaman utama untuk menuju halaman unduhan QGIS.
   
   ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220417223924.png)

2. Pada menu Installation Downloads pilih **QGIS Standalone Installer**. Pada saat panduan ini ditulis, versi terbaru adalah versi 3.22. Tunggu prosesnya hingga unduhan selesai.
   
   ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220417223952.png)

3. Jalankan installer yang sudah diunduh dalam ekstensi `.msi` untuk memasang QGIS di perangkat komputer Anda. Muncul tampilan seperti berikut, lalu klik **Next**.
   
   <img src="https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220417224045.png" title="" alt="" data-align="center">
   
   Centang pada  *I accept the terms in the License Agreement* dan klik **Next**.
   
   <img src="https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220417224432.png" title="" alt="" data-align="center">
   
   Sebelum melakukan proses install terlebih dahulu menentukan *Destination Folder*, lalu klik **Next**
   
   ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220417224807.png)

4. Klik **Install** untuk memulai proses instalasi dan tunggu sampai proses install selesai. Setelah itu, klik **Finish**.
   
   ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220417224859.png)

5. Jalankan QGIS dengan melakukan pencarian pada kolom *search* yang berada di taskbar Windows Anda.
   
   ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220417224950.png)

6. Perangkat QGIS telah dapat digunakan. Periksa apakah seluruh fungsi-fungsi pada menu QGIS dapat digunakan dengan baik sebelum melanjutkan ke panduan berikutnya. 
   
   ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220417225258.png)

Anda telah berhasil melakukan instalasi QGIS. Sebelum melanjutkan instalasi dan penggunaan *plugin GeoKKP-GIS*, Anda disarankan untuk memahami terlebih dahulu dasar-dasar penggunaan QGIS. Untuk itu, sub-bab selanjutnya akan membahas mengenai pengantar QGIS serta bagaimana  menggunakan QGIS untuk keperluan mendasar seperti digitasi dan pembuatan layout.
