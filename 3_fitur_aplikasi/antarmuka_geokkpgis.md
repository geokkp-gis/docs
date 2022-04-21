---
layout: default
title: Antarmuka GeoKKP-GIS
nav_order: 1
parent: Fitur Aplikasi
has_children: false
---

# Antarmuka GeoKKP-GIS

Pada bab ini akan dijelaskan mengenai antarmuka GeoKKP-GIS sebagai sebuah plugin pada QGIS. Fokus utama pembahasan ini adalah mengenai antarmuka menu-menu utama di GeoKKP-GIS. Adapun penjelasan lebih jauh akan diberikan di bab selanjutnya mengenai panel-panel kerja di GeoKKP.

Secara umum, antarmuka GeoKKP-GIS terdiri atas dua bagian:

1. Menu utama GeoKKP-GIS dalam bentuk Menu utama dan Toolbar GeoKKP

2. Panel Kerja GeoKKP-GIS

## Bagian-bagian Plugin GeoKKP-GIS

Selain kedua komponen tersebut, pada saat mode CAD diaktifkan, toolbar QAD serta panel command window juga akan turut aktif dan dapat digunakan secara bersamaan dengan plugin GeoKKP untuk penggambaran.

Berikut adalah tampilan antarmuka GeoKKP-GIS:

<img src="https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220419180717.png" title="" alt="" data-align="center">

Penjelasan untuk bagian-bagian di atas adalah:

1. **Menu GeoKKP-GIS**. Bagian menu berisi beberapa fungsi dasar yang sering digunakan pada GeoKKP-GIS, yaitu seperti gambar berikut:

<img src="https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220421013619.png" title="" alt="" data-align="center">

2. **Toolbar GeoKKP-GIS**. Toolbar berisi menu-menu utama yang digunakan
   untuk pemrosesan data persil pada GeoKKP, seperti perangkat penggambaran,
   dimensi serta validasi.

3. **Panel GeoKKP**-**GIS**.
   Panel berfungsi untuk menjadi antarmuka perantara antara pengguna dengan API
   dari server GeoKKP. Panel sendiri terdiri dari berbagai kegiatan yang dilakukan
   di tiap kantah, seperti penggambaran rutin, APBN, Unduh persil, dst.
   
   ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220421013747.png)

Panel dan toolbar dapat diaktifkan dan dinon-aktifkan dengan cara klik kanan pada bagian toolbar di QGIS, kemudian klik pada centang yang menunjukkan toolbar ("GeoKKP") maupun panel ("Panel Kerja GeoKKP-GIS"). Lokasi panel dan Toolbar ini dapat dipindah dengan cara menyeret jendela panel GeoKKP-GIS ke lokasi yang diinginkan.

![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220421014743.png)

Selain bagian-bagian tersebut, GeoKKP-GIS juga memiliki jendela tambahan ketika mode CAD diaktifkan, yaitu CAD Window yang merupakan bagian dari plugin QAD. CAD Window ini dapat digunakan untuk memanggil beberapa perintah AutoCAD ke dalam QGIS, seperti POLY, LINE, dst.

![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220421014322.png)

## Perangkat utama pada GeoKKP-GIS

Bagian ini akan membahas secara khusus mengenai toolbat GeoKKP-GIS dan perangkat yang ada di dalamnya. Berikut adalah penjelasan mengenai bagian-bagian dari toolbar GeoKKP-GIS.

![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/Desain Aplikasi - Frame 2.jpg)

Gambar di atas menunjukkan menu utama pada toolbar GeoKKP-GIS. Sebagian menu terdiri dari kelompok menu yang memiliki fungsi yang sama, misalnya untuk penggambaran dimensi. Selanjutnya akan dibahas fungsi dari masing-masing perangkat yang disebutkan di atas.