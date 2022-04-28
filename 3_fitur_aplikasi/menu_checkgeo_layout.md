---
layout: default
title: Menu Check Geometry dan Layout
nav_order: 4
parent: Fitur Aplikasi
has_children: false
---

# Menu Cek Geometri dan Layouting

Pada bagian ini akan dibahas mengenai metode pengecekan topologi serta pembuatan layout. Cek geometry merupakan pengganti perangkat "Reclean" pada AutoCAD, sedangkan pembuatan layout menggantikan fungsi layouting pada AutoCAD.

## Menu Pengecekan Geometri dan AutoAdjust

Plugin GeoKKP-GIS menyediakan menu untuk koreksi topologi serta pengaturan otomatis untuk batas persil untuk menjaga konsistensi data bidang tanah yang terdapat pada server. Di menu utama GeoKKP-GIS, dapat ditemukan dua buah pengaturan pengecekan geometri, yaitu cek geometri dan autoadjust. 



### Menu Cek Geometri

Pada dasarnya, pembuatan layer persil yang menggunakan menu penggambaran seperti yang telah dijelaskan sebelumnya akan secara otomatis menghindarkan pembuatan persil dari kesalahan topologi. Meskipun demikian, menu check geometry diberikan sebagai perangkat pengecekan topologi menyeluruh untuk menghindari kesalahan pada saat pembuatan layer persil dan layer lainnya.

Pengecekan geometry dilakukan terhadap layer vektor, dan akan memeriksa kesalahan topology sebagai berikut:

1. **break** (*break lines at intersection*). 
2. **snap** (*snap lines to vertex in threshold*). 
3. **rmdangle** (*remove dangles*)
4. **chdangle** (*change the type of boundary dangle to line*)
5. **rmbridge** (*remove bridges connecting area and island*)
6. **chbridge** (*change the type of bridges connecting area and island or 2 islands from boundary to line*)
7. **rmdupl** (*remove duplicate geometry features*)
8. **rmdac** (*remove duplicate area centroids*)
9. **bpol** (*break or topologically clean polygons*)
10. **prune** (*remove vertices in threshold from lines and boundaries*)
11. **rmarea** (*remove small areas*)
12. **rmline** (*remove all lines or boundaries of zero length*)
13. **rmsa** (*remove small angles between lines at nodes*)

Ketika dijalankan, menu ini akan mendeteksi dan secara otomatis mengkoreksi kesalahan-kesalahan di atas. Menu ini juga akan memberikan laporan proses pembersihan topology sehingga pengguna dapat memeriksa kesalahan yang terdeteksi dan yang telah dikoreksi.

![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220426213308.png)

Berikut adalah contoh kesalahan geometri yang dideteksi oleh tool ini serta hasil koreksinya:

![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220426230747.png)

Dapat dilihat bahwa menu ini mengkoreksi kesalahan gap (rmarea/*small area*) serta snapping dari titik-titik batas persil. Adapun kesalahan lain seperti overlap telah terkoreksi secara otomatis pada saat digitasi menggunakan perangkat digitasi GeoKKP-GIS. 

### Menu Auto Adjust

Menu **Auto Adjust** ini digunakan untuk memudahkan editing pada layer persil yang berbatasan. Pada kasus dimana sebuah layer persil dibuat di sebelah persil baru yang berbatasan, menu auto adjust akan mengkoreksi secara otomatis gap antar layer sehingga titik batas bidang tepat berada di lokasi yang sesuai. 

Pada saat menu ini dijalankan, akan muncul kotak dialog seperti berikut:

![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220427003723.png)

Pada gambar di atas, persil berwarna abu-abu diperoleh dari hasil unduh persil dari server GeoKKP, sedangkan persil berwarna kuning adalah persil yang saat ini sedang diedit. Menu Adjust otomatis akan menyesuaikan hasil digitasi dari persil yang saat ini aktif untuk disesuaikan dengan persil tetangga yang tersimpan di server GeoKKP.

Untuk memulai adjustment, pilih bidang tanah yang akan diadjust sampai muncul jumlah yang tepat pada jendela "*Adjust Persil Otomatis*". Masukkan nilai toleransi, yaitu jarak maksimal antar titik persil untuk dapat dilekatkan satu dengan yang lain. Satuan toleransi ini mengikuti satuan project, yang dalam hal ini adalah dalam satuan **meter**.

Sebagai contoh, hasil dari penggunaan menu ini adalah sebagai berikut:

*Sebelum*:

![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220427003459.png)

*Sesudah*:

![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220427011450.png)

Perbedaan antara kedua menu ini adalah sebagai berikut:

| Reclean                                                            | AutoAdjust                                                           |
|:------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| Menggunakan satu layer masukan                                     | Menggunakan dua layer masukan                                        |
| Dapat digunakan untuk berbagai jenis layer titik, garis dan luasan | Hanya untuk layer Batas Persil saja                                  |
| Berguna untuk mengkoreksi kesalahan-kesalahan topologi             | Berguna untuk menempelkan batas antar persil                         |
| Berlaku untuk seluruh fitur pada satu layer                        | Hanya berlaku pada fitur atau fitur-fitur yang terpilih saja         |
| Menghasilkan layer baru hasil koreksi                              | Fitur yang di-adjust akan secara otomatis digantikan oleh fitur baru |

Dengan demikian, pengguna perlu memahami kapan menu cek geometry ('reclean') digunakan serta kapan menu AutoAdjust digunakan pada saat editing.



## Menu Layoutting



 
