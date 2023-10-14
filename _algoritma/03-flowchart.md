---
title: "Flowchart"
permalink: /algoritma/flowchart/
author_profile: false
excerpt: "Flowchart."
show_date: true
last_modified_at: 2023-10-12T17:00:00-01:00
categories:
  - Learn
tags:
  - Logika
  - Algoritma
  - Materi
toc: true
toc_sticky: true
comments: true
---

# Flowchart
Adalah suatu diagram yang menggambarkan susunan logika suatu program Simbol simbol yang digunakan adalah sebagai berikut :

| Simbol | Nama Simbol | Keterangan |
|:--------|:-------:|:-------:|
| ![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/cf7235ce-1c08-44ab-a8c1-657c293b27ce) | Terminal  | sebagai awal (berisi ‘Start’/’Mulai’) dan sebagai akhir (berisi ‘End’/’Stop’/’Selesai’). | 
| ![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/f66b90ce-cc91-4cce-9f55-0d4d4ed7a4b6) | Input/Output | Membaca masukan (input) atau menampilkan keluaran (output). | 
| ![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/60c038be-569f-4900-a085-34bcc1852c67) | Proses/Prosessing | Mengolah data melalui operasi aritmatika dan logika. |
| ![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/027e9bb5-d4c7-4e9f-971d-3deb2c0b6144) | Decision/(kotak keputusan) | Berfungsi untuk memutuskan arah/percabangan yang diambil sesuai dengan kondisi yang dipenuhi, yaitu Benar/Salah. |
| ![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/67f504bb-af2c-42e3-9ba0-4cdd7e506a9c) | Subroutine/subrutin | Untuk menjalankan proses suatu bagian (sub program) atau prosedur. |   
| ![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/556bad8a-b0ad-404a-bbdd-b34d4ebfac87) | On page Connector | untuk menghubungkan diagram alur yang terputus dimana bagian tersebut masih berada pada halaman yang sama. |
| ![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/10c2c73d-ec2f-493c-98dc-aea3fe225d7a) | Flowline/Alur data | Bagian arah instruksi yang dijalankan. | 
| ![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/6c86a7d1-a01c-4234-a252-8855ecc482e5) | Off page Coneector | Menghubungkan sambungan dari bagian flowchart yang terputus dimana sambungannya berada pada halaman lain. |
| ![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/b0cfa1d8-4198-4c59-bf8b-dd37f710830d) | Preparation | Digunakan untuk pemberian harga awal. |
{: rules="groups"}

# Diagram Alir Program Komputer
Pada dasarnya suatu program komputer umumnya terdiri atas :
1. Pembacaan / pemasukan data ke dalam komputer
2. Melakukan komputasi/perhitungan terhadap data tersebut
3. Mengeluarkan / mencetak/ menampilkan hasilnya.

## Flowchart terdiri dari tiga struktur
1. Struktur Sequence / Struktur Sederhana Digunakan untuk program yang instruksinya sequential atau urutan

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/90b56940-ede4-4e76-b562-3a9a7da3fa8c)

## Contoh Flowchart Struktur Squence Menghitung Luas Segitiga

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/3d2f9001-dfe1-437a-b5b3-ccbb37f4ac1e)

### Menggunakan Tabel Penyimpanan
Tabel 1. Media Penyimpanan Sequence 1

| Perintah | A | B | Output|
|:--------|:-------:|:-------:|:-------:|
| A <- 10 | 10 |  |  |
| A <- 2*A | 20 |  |  |
| B <- A |  | 20 |  |
| Write(B) |  |  | 20 |
{: rules="groups"}

Tabel 2. Media Penyimpanan Sequence 2

| Perintah | X | Y | Z | Output|
|:--------|:-------:|:-------:|:-------:|:-------:|
| X <- 100 | 100 |  |  |  |
| Y <- X-25 |  | 75 |  |  |
| Z <- Y/5 |  |  | 15 |  |
| X <- X/(Z+5) | 5 |  |  |  |
| Write(X,Y,Z) |  |  |  |  |
{: rules="groups"}

# Menjumlahkan Dua Bilangan Positif
1. Membuat flowchart untuk menjumlahkan dua bilangan bulat positip dan mencetak hasilnya Algoritmanya:
  - Masukkan bilangan a
  - Masukkan bilangan b
  - Jumlahkan bilangan a dan b
  - Cetak hasil jumlahnya

  ![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/474620bc-5a3d-4291-a73b-725820deed8c)

2. Struktur Branching Digunakan untuk program yang menggunakan pemilihan atau penyeleksian kondisi.(contoh menentukan bilangangenap/ganjil)
   
  ![image-right](https://github.com/Julius-Ulee/School-Programs/assets/61336116/06cbf6c1-4252-4f36-abf8-aaf614dfa7c2)

