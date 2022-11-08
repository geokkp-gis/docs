---
layout: default
title: Panduan Kontribusi
nav_order: 5
has_children: false
---

# Panduan Kontribusi

## Pembangunan aplikasi

Untuk berkontribusi pada plugin ini, silahkan melakukan komunikasi dengan Pusdatin ATRBPN di [support.pusdatin@atrbpn.go.id](mailto:support.pusdatin@atrbpn.go.id)

## Prosedur untuk Release

Berikut adalah tahapan untuk melakukan release versi baru GeoKKP-GIS.

1. *Merge branch* develop ke *master*
2. Pastikan versi di metadata.txt sudah diperbaharusi, misalnya `version=1.0.1`
3. *Checkout master branch*. Contoh: `git checkout origin/master`
4. Buat *tag* pada *master branch* tersebut dengan versi sebagai tag-nya. Misal untuk versi 1.0.1 menggunakan tag `version-1_0_1`. Contoh: `git tag version-1_0_1`
5. Push *tag* tersebut ke Github. Contoh: `git push version-1_0_1`
6. Buat release baru di Github: [Release Baru](https://github.com/danylaksono/GeoKKP-GIS/releases/new), dengan menggunakan tag tersebut.
7. Berikan keterangan pada release versi tersebut (Changelog)
8. Tekan tombol *Publish release*
9. Github akan membuat berkas terkompresi dari plugin ini
10. Unduh berkas terkompresi tersebut, dan *extract* isinya
11. Ubah nama folder menjadi GeoKKP-GIS, dan kompres kembali
12. Upload berkas terkompresi tersebut ke [Plugin QGIS](https://plugins.qgis.org/) agar pengguna bisa mengunduhnya.
