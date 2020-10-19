---
title: "Karakteristik Sistem Terdistribusi"
date: 2020-10-19T14:48:07+07:00
draft: false
cover: "network.jpg"
useRelativeCover: true
coverCaption: "Source : Gambar oleh [Bethany Drouin](https://pixabay.com/id/users/bsdrouin-5016447/?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=2402637) dari [Pixabay](https://pixabay.com/id/?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=2402637)"
description: "Sistem Terdistribusi adalah Sekumpulan komputer otonom yang terhubung ke suatu jaringan, dimana bagi pengguna sistem terlihat sebagai satu komputer. Ada beberapa hal yang harus diperhatikan dalam membangun sistem terdistribusi."
tags: [
  "Sistem Terdistribusi",
  "Bab 1",
  "Karakteristik Sistem Terdistribusi"
]
disqus_title: "Sistem-terdistribusi"
---

## Ada beberapa hal yang harus diperhatikan dalam membangun sistem terdistribusi, yaitu :

1. Transparency (Kejelasan)
2. Communication (Komunikasi)
3. Performance & Scalability (Kinerja dan Ruang Lingkup)
4. Heterogeneity (Keanekaragaman)
5. Opennes (Keterbukaan)
6. Reliability & Fault Tolerancy (Kehandalan dan Toleransi Kegagalan)
7. Security (Keamanan)

### 1. Transparency (Kejelasan)
- Access transparency : Sumber daya lokal dan remote di akses dengan menggunakan operasi yang sama.

- Location transparency : Pengguna sistem tidak tahu mengetahui keberadaan hardware dan software (CPU, file dan data).

- Migration (Mobility) transparency : Sumber daya (baik berupa Hardware dan/atau software) dapat bebas berpindah tanpa mengubah sistem penamaan.

- Replication transparency : Sistem bebas untuk menambah …le atau sumber daya tanpa diketahui oleh user (dalam rangkan meningkatkan kinerja)

- Concurency transparency : User tidak akan mengetahui keberadaan user lain dalam sistem, walaupun user tersebut menggunakan sumber daya yang sama.

- Failure transparency : Aplikasi harus dapat menyelesaikan proses nya walaupun terdapat kegagalan pada beberapa pada komponen sistem.

- Performance transparency : Beban kerja yang bervariasi tidak akan menyebabkan turunnya kinerja sistem, hal ini dapat di capai dengan melakukan automatisasi kon…gurasi terhadap perubahan beban.

### 2. Communication (Komunikasi)

Komponen2 pada sistem terdistribusi harus melakukan komunikasi dalam suatu urutan. Sebagai berikut :
- Infrastruktur jaringan (interkoneksi dan software jaringan)
- Metode dan Model komunikasi yang cocok

Metode komunikasi :

- Send

- Receive

- Remote Procedure Call

Model Komunikasi :

- client - server communication : pertukaran pesan antara dua proses : dimana satu proses (client) menggunakan / meminta layanan pada server dan server menyediakan hasil dari proses tersebut.

- groupmulitcast : target dari pesan yang dikirimkan adalah gabungan dari proses, yang berasal dari suatu grup.

### 3. Performance & Scalability (Kinerja dan Ruang Lingkup)

Ada beberapa faktor yang mempengaruhi kinerja (performance) dari pada sistem terdistribusi :

- Kinerja dari pada personal workstations

- Kecepatan infrastruktur komunikasi

- Fleksibilitas dalam membagi beban kerja : contoh, apabila terdapat prosesor (workstation) yang idle maka dapat dialokasikan secara otomatis untuk mengerjakan tugas - tugas user.

- Scalability : Sistem tetap harus memperhatikan efesiensi walaupun terdapat penambahan
secara signifikan user atau sumber daya yang terhubung :

- Cost (biaya) penambahan sumber daya (resources) harus reasonable.

- Penurunan kinerja (performance) diakibatkan oleh penambahan user atau sumber daya harus terkontrol.

### 4. Heterogeneity (Keanekaragaman)

Aplikasi yang terdistribusi biasa berjalan dalam keberagaman :

- Hardware : mainframes, workstations, PC’s, server dll.

- Software : UNIX, MS Windows, IMB OS/2, LINUX dll.

- Devices : teller machine, robot, sistem manufacturing dll.

- Network dan Protocol : Ethernet, FDDI, ATM, TCP/IP dll

Melihat keanekaragaman di atas maka salah satu solusi yang bisa di terapkan adalah Middleware : berfungsi sebagai jembatan untuk komunikasi dan proses.

![Gambar 1.2 : Arsitektur software pada sistem terdistribusi](/images/gambar-2-bab-1.jpg "Arsitektur software pada sistem terdistribusi")

### 5. Opennes (Keterbukaan)

Salah satu hal terpenting yang harus dimiliki oleh sistem terdistribusi adalah opennes (keterbukaan) dan flexibility (fleksibilitas) :

- Setiap layanan (services) harus dapat di akses oleh semua user.

- Mudah dalam implementasi, install dan debug services;

- User dapat membuat dan menginstall service yang telah dibuat oleh si user tersebut.

Aspek kunci pada opennes :

- Interface dan Protocol yang standard (seperti protokol komunikasi di internet)

- Support terhadap keanekaragaman. ( denganmembuatmidleware seperti CORBA)

### 6. Reliability & Fault Tolerancy (Kehandalan dan Toleransi Kegagalan)

Salah satu tujuan dalam membangun sistemterdistribusi adalah memungkinkan untuk melakukan improvisasi terhadap kehandalan sistem.

Availability : kalau mesin mati (down), sistem tetap harus berjalan dengan jumlah layananan yang tersisa.

- Dalam sistem terdistribusi componen yang sangat vital (critical resources) berjumlah se minimal mungkin. Yang dimaksud dengan critical resources adalah komponen yang harus ada untuk menjalankan sistem terdistribusi.

- Masing - masing Software dan Hardware harus di replikasi : kalau terjadi kegagalan / error maka yang lain akan menangani.

Data dalam sistem tidak boleh hilang, copy dari file tersebut disimpan pada secara redundan pada server lain, tapi tetap harus dijaga konsistensi datanya.

Fault Tolerance : Sistemharus bisa mendeteksi kegagalan dan melakukan tindakan dengan dasar sebagai berikut :
- Mask the fault (menutupi kegagalan) : tugas harus dapat dilanjutkan dengan menurunkan kinerja tapi tanpa terjadi kehilangan data atau informasi.

- Fail Gracefully : membuat suatu antisipasi terhadap suatu kegagalan ke suatu prosedur yang telah di rencanakan dan memungkinkan untuk menghentikan proses dalam waktu yang singkat tanpa menghilangkan informasi atau data.

### 7. Security (Keamanan)

- Confidentiality : keamanan terhadap data yang di akses oleh user yang tidak di perbolehkan (unauthorizes user)

- Integrty : keamanan terhadap kelengkapan dan autentikasi data.

- Availability : Menjaga agar resource dapat selalu di akses.

Sistem terdistribusi harus memperbolehkan komunikasi antara program/user/resources pada computer yang berbeda, maka resiko keamanan akan muncul apabila memberlakukan free access.

Dan ada hal lain juga yang harus dijamin dalam sistem terdistribusi, yaitu : penggunaan rerources yang tepat oleh user yang berlainan.