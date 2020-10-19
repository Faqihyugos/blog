---
title: "Pengenalan Sistem Terdistribusi"
date: 2020-10-19T13:48:07+07:00
draft: false
cover: "network.jpg"
useRelativeCover: true
coverCaption: "Source : Gambar oleh [Bethany Drouin](https://pixabay.com/id/users/bsdrouin-5016447/?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=2402637) dari [Pixabay](https://pixabay.com/id/?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=2402637)"
description: "Sistem Terdistribusi adalah Sekumpulan komputer otonom yang terhubung ke suatu jaringan, dimana bagi pengguna sistem terlihat sebagai satu komputer."
tags: [
  "Sistem Terdistribusi",
  "Bab 1",
  "Pengenalan"
]
disqus_title: "Sistem-terdistribusi"
---
# Pengenalan Sistem Terdistribusi

## 1. Mengapa Sistem terdistribusi ? 
- Komputer-komputer yang terdistribusi secara geografis.
- Komunikasi melalui koneksi kabel/fibre/wireless/.
- Keuntungan : interaksi, koorporasi dan pemakaian bersama sumber daya, mengurangi biaya, meningkatkan kinerja dan ketersediaan.

### Definisi Sistem Terdistribusi
Sistem Terdistribusi adalah Sekumpulan komputer otonom yang terhubung ke suatu jaringan, dimana bagi pengguna sistem terlihat sebagai satu komputer.
Komputer otonomi : walaupun komputer tidak terhubung ke jaringan,  komputer tersebut tetap dapat berjalan.
Dengan menjalankan sistem terdistribusi, komputer dapat melakukan :
1. Koordinasi Aktifitas
2. berbagi sumber daya : hardware, software dan data
Dengan definisi tersebut diatas maka internet sesungguhnya bukanlah suatu sistem terdistribusi, melainkan infrastruktur dimana sistem terdistribusi dapat di aplikasikan pada jaringan tersebut.

### Proses
- Dieksekusi secara konkuren. 
- Berinteraksi untuk mencapai tujuan umum. 
- Aktifitasnya saling koordinasi dan bertukar informasi melalui
pesan yang ditransfer melalui jaringan komunikasi.

## 2. Contoh Sistem Terdistribusi
1.  Sistem Telepon
- ISDN, PSTN

2.  Manajemen Jaringan
- Adminstrasi ke sumber jaringan

![Gambar 1.1 : Contoh sistem terdistribusi, Automatic Banking (teller machine) System](/images/gambar-bab-1.jpg "Contoh sistem terdistribusi, Automatic Banking (teller machine) System")

3.  Network File System (NFS)
- Arsitektur untuk mengakses sistem file melalui jaringan

4.  WWW (World Wide Web)
- Arsitektur client/server yang diterapkan di atas infrastruktur internet
- Shared Resource (melalui URL)

## 3. Keuntungan Sistem Terdistribusi

Keuntungan yang didapatkan dalam menerapkan sistem terdistribusi, antara lain :

- Performance : Kumpulan dari beberapa prosesor akan memberikan kinerja yang lebih baik dari pada komputer yang terpusat. Begitu juga kalau dilihat dari sisi biaya.

- Distribution.

- Reliability (Fault tolerance) : apabila salah satu komponen terjadi kerusakan, sistem tetap dapat berjalan.

- Incremental Growth : Mudah dalam melakukan penambahan komputer komponen.

- Sharing Data/Resources : Berbagi data adalah salah satu hal yang pokok pada kebanyakan aplikasi.

## 4. Permasalahan dalam Sistem Terdistribusi

Kelemahan pada sistem terdistribusi adalah :

- Kesulitan dalam membangun perangkat lunak . Kesulitan yang akan dihadapi antara lain : bahasa pemrograman yang harus dipakai, sistem operasi dll.

- Masalah Jaringan : Karena sistem terdistribusi di implementasikan dalam jaringan komputer, maka isu2 yang berkaitan dengan jaringan komputer akan menjadi pertimbangan utama dalam merancang dan mengimplementasikan sistem.

- Masalah Keamanan : Karena pada sistem terdistribusi berbagi data/sumber daya merupakan hal yang mutlak, maka muncul masalah2 yang berkaitan dengan keamanan data dll.