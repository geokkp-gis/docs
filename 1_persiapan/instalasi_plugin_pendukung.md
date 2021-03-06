---
layout: default
title: Instalasi Plugin Pendukung
nav_order: 3
parent: Persiapan GeoKKP-GIS
has_children: false
---

# Instalasi Plugin Pendukung

Sebagai sebuah aplikasi GIS, QGIS dilengkapi dengan kemampuan penggambaran yang sangat komplit. Meskipun demikian, pengguna yang terbiasa menggunakan perangkat penggambaran berbasis CAD mungkin akan mengalami kesulitan pada saat menggunakan QGIS. Untuk itu, GeoKKP-GIS menggunakan tambahan plugin untuk memungkinkan penggambaran berbasis CAD di lingkungan QGIS. Pada bagian ini akan dibahas mengenai prosedur instalasi plugin tersebut.

## Instalasi Plugin QAD

GeoKKP-GIS telah dilengkapi dengan berbagai fungsi penggambaran yang memudahkan penggunaannya ketika berhubungan dengan bidang tanah. Meskipun demikian, QGIS juga dilengkapi dengan ribuan plugin gratis yang dapat membantu mempermudah pekerjaan kita untuk berbagai jenis operasi terkait dengan data geospasial. Secara khusus, GeoKKP-GIS menggunakan **Plugin QAD** sebagai tambahan untuk melakukan editing data persil dengan tampilan yang sama seperti pada perangkat CAD lainnya (misalnya, AutoCAD). Ini bertujuan untuk memudahkan pengguna yang telah terbiasa menggunakan perangkat CAD untuk beralih pada lingkungan GIS. 

Sama seperti prosedur Instalasi QGIS sebelumnya, petunjuk instalasi QAD adalah sebagai berikut:

1. Buka menu Plugins > Manage and Install Plugins. Setelah itu, memastikan bahwa repository telah terkoneksi dengan internet untuk dapat melakukan proses install tools yang belum tersedia.

2. Cari plugin QAD pada kolom pencarian di jendela **Plugin Manager**. Selanjutnya install plugin QAD dengan cara klik **Install Plugin**.
   
   ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220418062102.png)

3. Untuk menampilkan tools QAD yang sudah di-install, klik kanan pada sisi kanan toolbar panel, kemudian pilih tools yang ingin ditampilkan.
   
   ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220418062355.png)

4. Plugin QAD berhasil diinstall, dan akan muncul sebagai rangkaian menu serta jendela perintah (Command Window) yang serupa dengan yang ada pada AutoCAD.
   
   ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220418062443.png)

Dengan demikian, kita telah menginstall QAD, dan fungsi penggambaran pada AutoCAD seperti POLY, LINE, dst akan dapat kita panggil cukup dengan mengaktifkan plugin ini.

## Plugin-plugin Pendukung

Seperti yang sudah dibahas, QGIS memiliki ribuan plugin yang dapat digunakan untuk berbagai fungsi yang bahkan tidak dimiliki oleh perangkat lunak berbayar. Berikut adalah beberapa contoh plugin yang dapat Anda gunakan untuk mempermudah pekerjaan dengan QGIS:

- **QuickMapServices**. Dengan plugin ini kita dapat menambahkan ratusan layer basemap pada QGIS dengan mudah, seperti Google Hybrid atau Bing Satellite.
  
  ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220418062613.png)

- **QGIS2Web**. merupakan plugin yang berguna untuk pembuatan web dari data QGIS yang dimiliki. Plugin ini mengkonversi secara langsung data dari QGIS untuk ditampilkan secara online dalam sebuah WebGIS, baik menggunakan OpenLayers, LeafletJS maupun Mapbox.
  
  ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220418062658.png)

- **Shape Tools**. Plugin ini berguna untuk menggambar berbagai bentuk geometri yang sulit dilakukan dengan perangkat digitasi biasa.
  
  ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220418062808.png)

- **Split Polygon**. Plugin ini berguna untuk membagi sebuah polygon (misalnya, persil tanah) menjadi beberapa bagian dengan berbagai metode pembagian, misalnya dengan membagi menjadi luasan yang sama.
  
  ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220418062833.png)

- **Another DXF Importer**. Plugin ini merupakan tambahan fungsi untuk melakukan Import data dari DXF dengan beberapa perbaikan, seperti fungsi untuk georeferencing dan konversi label. Sebagai catatan, plugin GeoKKP-GIS sendiri telah memiliki fungsi import DXF
  
  ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220418063421.png)

- **Input**. Plugin ini (https://inputapp.io/) merupakan bagian dari perangkat survey lapangan untuk QGIS. Pengguna di lapangan dapat melakukan survey dengan menggunakan perangkat mobile, baik dalam bentuk titik atau garis, kemudian mengunggah hasilnya secara hampir realtime pada server untuk diolah pada QGIS.
  
  ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220418063514.png)
  
  Plugin Input ini dapat dimanfaatkan, misalnya, untuk melakukan kegiatan cek plot secara langsung agar data dari lapangan dapat segera dikonfirmasi di kantor menggunakan QGIS.

Demikian adalah beberapa plugin pada QGIS yang mungkin dapat digunakan dalam kegiatan pertanahan. Masih banyak lagi plugin lain yang dapat membantu pekerjaan terkait dengan digitasi, analisis serta penyajian peta bidang tanah dan data geospasial lainnya.

Setelah berkenalan dengan QGIS dan melakukan instalasi plugin yang diperlukan, pada bab selanjutnya kita akan membahas mengenai dasar QGIS untuk pengolahan data geospasial. Demikian pula, akan diberikan sedikit pengantar mengenai bagaimana penggambaran dengan Plugin QAD dilakukan pada QGIS.
