---
layout: default
title: Panel Invent
nav_order: 4
parent: Panel GeoKKP-GIS
has_children: false
---

# Panel Invent

Sama seperti panel lainnya, penggunaan panel invent memerlukan pengaturan sistem proyeksi dan lokasi kerja terlebih dahulu. Selanjutnya, panel ini dapat digunakan untuk membuat Peta Bidang Tanah seperti berikut:

1. Klik tombol Buat Peta untuk membuat peta bidang baru
   
   ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220511183315.png)

2. Pilih kegiatan yang diinginkan, kemudian klik Proses
   
   ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220511183342.png)

3. Akan muncul pemberitahuan bahwa peta bidang baru telah selesai dibuat. Daftar pencarian peta bidang juga akan menunjukkan hasil dari pembuatan PBT tersebut
   
   ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220511183636.png)

4. Selanjutnya, kita dapat melakukan penggambaran pada kanvas QGIS. Penggambaran dimulai dengan menambahkan layer rincikan dari daftar layer:
   
   ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220511234513.png)

5. Setelah layer rincikan ditambahkan pada daftar layer QGIS, selanjutnya lakukan editing pada layer tersebut menggunakan tool editing pada QGIS:
   
   ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220511235548.png)
   
   > Catatan:
   > 
   > Menu editing geometry pada GeoKKP (tombol ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220511235626.png)) didesain untuk secara otomatis mengkoreksi topologi dan meniadakan penambahan atribut **khusus pada layer batas persil**. Dengan demikian, untuk editing geometri layer lain termasuk layer rincikan ini, sebaiknya digunakan menu editing dari QGIS (Tombol ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220511235812.png))

6. Setelah melakukan editing geometri, akan muncul isian untuk tabel atribut. Kolom yang penting untuk diisi adalah kolom **Label** serta **Pemilik**.![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220512000059.png)

7. Klik OK untuk mengakhiri digitasi. Maka persil yang kita petakan akan muncul dengan label yang telah diinputkan pada kolom atribut sebelumnya:
   
   ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220512000230.png)

8. Apabila kita menambahkan rincikan lainnya, maka perlu diingat untuk mengisikan label sesuai dengan urutan rincikan yang dimasukkan. Contoh di bawah ini memberikan isian label serta nama pemilik pada digitasi rincikan baru:
   
   ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220512000344.png)

9. Hasil akhir digitasinya adalah seperti berikut:
   
   ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220512000517.png)

10. Jangan lupa untuk mengakhiri digitasi pada QGIS dengan menon-aktifkan tombol Editing kembali (gambar pensil di rangkaian icon editing: <img src="https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220512000659.png" title="" alt="" width="135">). Klik **Save** pada dialog yang muncul untuk menyimpan hasil editing pada file lokal di QGIS:
    
    ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220512000804.png)

11. Jangan lupa untuk melakukan clean topology melalui menu  ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220512001409.png) apabila diperlukan

12. Selanjutnya klik tombol **Simpan** pada panel kerja Invent untuk mengunggah data PBT tersebut ke dalam server GeoKKP:
    
    ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220512000944.png)

13. Akan muncul dialog Desain PBT seperti berikut. Lakukan validasi dengan mengetikkan jumlah bidang tanah yang telah diedit, kemudian klik tombol **Validasi**:
    
    ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220512001045.png)
    
    Klik tombol **Proses** setelah memasukkan jumlah bidang tanah serta zona TM3 yang sesuai. 
    
    ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220512001615.png)
    
    Jawab konfimasi untuk integrasi PBT ke dalam server GeoKKP:
    
    ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220512012900.png)

14. Apabila penyimpanan berhasil, maka akan muncul pemberitahuan seperti berikut:
    
    ![](https://cdn.jsdelivr.net/gh/geokkp-gis/images@main/20220512012945.png)
15. 