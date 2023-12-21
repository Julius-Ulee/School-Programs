---
title: "Konfigurasi Jaringan Komputer Cisco dengan Sistem Keamanan, DHCP Server, dan Banner MOTD pada Router."
author_profile: false
excerpt: "Implementasikan Konfigurasi Jaringan Komputer Cisco dengan Sistem Keamanan yang melibatkan enkripsi pada line console dan line vty, serta penerapan DHCP Server dengan eksklusi rentang IP, dan tambahan keamanan berupa pesan MOTD sebagai banner pada Router, dengan Interface G0/0 IP 192.168.10.1/24 dan Interface G0/1 IP 192.168.11.1/24, fungsi DHCP Server di G0/1, eksklusi IP dari 192.168.11.1 hingga 192.168.11.40 dan 192.168.11.150 hingga 192.168.11.254, menggunakan DHCP Pool bernama 'JARINGAN-KOMPUTER', serta penyesuaian kata sandi pada line console dan line vty untuk meningkatkan keamanan secara menyeluruh."
breadcrumbs: true
header:
  teaser: "https://github.com/Julius-Ulee/School-Programs/assets/61336116/f04373ef-b530-41a9-a2f5-28918dc1a15a"
last_modified_at: 2023-12-21T:00:00-01:00
categories:
  - Computer
tags:
  - Cisco
  - Network
toc: true
toc_sticky: true
comments: true
show_date: true
---

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/a9535db0-7da4-49d0-b384-55b920395553)

# A. MEMBUAT TOPOLOGI
1. Buat sebuah topologi dengan menggunakan aplikasi cisco packet tracer, lalu siapkan beberapa device seperti 1 buah router, 2 buah switch, dan 5 buah pc, kemudian susun seperti berikut:

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/376f8877-8a49-4835-acc2-0ab0690fa586)

2. Pilih kabel straight, pada menu pilihan kabel di bawah, lalu klik pada router, maka akan muncul dialog yang berisi list seperti berikut:

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/8d4b1ba7-d2b8-4731-89c1-b755abfdafdb)

Pilih **GigabitEthernet0/0/0.**

3. Kemudian klik **switch0**, lalu pilih **FastEthernet0/1:**

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/b2136ffd-9efb-44f7-963b-a1fff0eeed93)

4. Lakukan langkah nomor 2 dan 3 untuk **switch0**, bedanya pada router sekarang pilih menu **GigabitEthernet0/0/1**, dengan **FastEthernet0/1** sehingga hasilnya seperti berikut:

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/4cd71fba-e164-4790-8d2a-3e891f2ae80d)

5. Hubungkan switch0 dengan PC0, PC1, dan PC2 menggunakan kabel straight, dengan ketentuan seperti berikut:
- Klik **switch0** kemudian pilih **FastEthernet0/2** ke **PC0** lalu pilih menu **FastEthernet0.**
- Klik **switch0** kemudian pilih **FastEthernet0/3** ke **PC1** lalu pilih menu **FastEthernet0.**
- Klik **switch0** kemudian pilih **FastEthernet0/4** ke **PC2** lalu pilih menu **FastEthernet0.**
Maka hasilnya seperti berikut:

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/10e85dbb-bbf8-4f4f-af22-b75c29e69fb9)

6. Hubungkan switch yang satunya lagi yaitu **switch1**, menggunakan kabel straight ke **PC3** dan **PC4**, dengan ketentuan berikut:
- Klik switch1 kemudian pilih **FastEthernet0/2** ke **PC3** lalu pilih menu **FastEthernet0**
- Klik switch1 kemudian pilih **FastEthernet0/3** ke **PC4** lalu pilih menu **FastEthernet0**

7. Maka hasil akhir untuk menghubungkan beberapa device network akan menjadi seperti berikut:

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/1fee0dbe-a93e-4132-9222-8595214e7a0d)

# B. MEMBUAT SISTEM KEAMANAN PADA LINE CONSOLE DAN LINE VTY

## 1. Line Console

- Klik router, maka akan muncul jendela dialog lalu klik pada tab CLI
- Lalu masukkan perintah seperti pada gambar berikut:

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/a5c93e14-c302-4956-8a62-30fde9eada09)

Pada gambar diatas merupakan perintah untuk mengkonfigurasi **line console 0**, serta memberi password keamanan dengan nama **jarkom12190261.**

## 2. Line Vty
- Masih pada tab CLI yang sama, untuk mengkonfigurasi line vty, maka ketik perintah sebagai berikut:

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/e01fe90f-72fd-4052-86b0-fb4b6921b6c0)

Konfigurasi password pada **line vty 0 4**, seperti pada gambar diatas, sama seperti line console, disini juga wajib memberikan password keamanan dengan nama **jarkom12190261.**

- Untuk mengecek apakah password berhasil dibuat atau tidak, ketik perintah exit terlebih dahulu dari router, lalu masukkan password yang tadi sudah dibuat, jika berhasil login, maka akan seperti berikut:

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/011d03da-b4d2-424d-8f63-fa9fd397b630)

- Buat enkripsi pada password, dengan mengetikkan perintah berikut:

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/fb82365b-3631-4434-99c4-0f65961a96c9)

- Ketik perintah **show run**, untuk melihat bahwa password berhasil terenkripsi. Jika password berhasil dienkripsi, hasilnya seperti berikut:

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/db3b3d18-7d77-47d4-a538-6352309a8552)

Untuk melihat hasil enkripsi seperti gambar diatas, scroll ke bawah hingga ke bagian **line con 0.**

# C. MEMBUAT BANNER MOTD
- Buat banner MOTD dengan tulisan **‘SELAMAT DATANG’**, dengan mengetik perintah berikut:

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/9baae2f1-9794-43dd-9ae7-78d4dbe21a4b)

- Kemudian exit terlebih dahulu, jika banner MOTD berhasil dibuat maka akan menampilkan teks **'SELAMAT DATANG’**, seperti berikut:

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/5c7586be-63a8-400e-97f2-07a23e05ce6a)

# D. MEMBUAT INTERFACE
## 1. Router Interface G0/0
- Ketikkan perintah **interface GigabitEthernet0/0/0**, lalu set IP address dan subnet mask seperti gambar berikut:

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/587858e0-2c95-47a9-9f1e-c835711153d3)

## 2. Router Interface G0/1
- Lakukan hal yang sama seperti pada interface G0/0, ketik perintah **interface GigabitEthernet0/0/1**, lalu set IP address nya menjadi **192.168.11.1** dengan subnet mask **255.255.255.0**

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/0c0a274f-921b-4f25-b27e-940f1280b5dd)

# E. MEMBUAT DHCP SERVER PADA G0/1
Membuat DHCP server dengan jangkauan atau range yang ditentukan beserta DHCP Pool dengan nama **‘JARINGAN-KOMPUTER’**, Ketikkan perintah seperti berikut:

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/f49fb85d-ef3f-4bf7-944e-c6dbc91dcfb9)

# F. SET IP ADDRESS PADA SETIAP PC
## 1. Set IP address pada jaringan ke-1 dengan IP Static
- Klik pada **PC0**, kemudian pilih menu **IP Configuration** lalu klik tab **Desktop**
- Pada IP Configuration set IPv4 dengan **IP 192.168.10.2**
- Set Subnet mask menjadi **255.255.255.0**
- Dan default gateway menjadi **192.168.10.1**

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/abe834ad-d9ef-4c26-81ec-da512b184c9a)

Lakukan hal yang sama seperti langkah di atas dengan ketentuan berikut:
- PC1 : IPv4 192.168.10.3 255.255.255.0 & default gateway 192.168.10.1
- PC2 : IPv4 192.168.10.4 255.255.255.0 & default gateway 192.168.10.1


## 2. Set IP address pada jaringan ke-2 dengan IP DHCP
- Klik **PC3**, kemudian pilih menu **IP Configuration**, lalu pilih tab **Desktop**
- Pada interface ip configuration pilih **DHCP**, maka otomatis IP, subnet mask, dan Default gateway-nya akan terisi, berikut hasilnya:

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/3b481efa-ab85-4280-af86-e87ecca69997)

- Hal yang sama juga dilakukan pada **PC4**:

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/330b1209-1d9d-4a58-a4be-e9284bbefc5c)

- Setelah melalui beberapa langkah di atas, maka hasilnya jaringan sudah berhasil terkoneksi satu sama lain:

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/2fafe049-cb25-441a-aa30-a5cbd73980ae)

- Untuk mengecek berhasil atau tidaknya bisa dilakukan dengan tes PDU
- Klik icon amplop seperti berikut:

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/56b08f24-254b-4efc-a8ee-27ba47fa4c32)

- Kemudian , sebagai contoh klik **PC3** kemudian klik **PC4**, jika berhasil cek pada bagian scenario di kanan bawah, seperti berikut:

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/5050900e-c982-4511-98ce-6fac15fbfa05)

- Jika berhasil maka last status **successful**
- Begitu juga jika di tes ke network lain, maka hasilnya akan **successful**, seperti contoh pada **PC3** ke **PC2**, seperti berikut:

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/3091805a-b2e9-4351-8456-0b4cc22ce74d)
