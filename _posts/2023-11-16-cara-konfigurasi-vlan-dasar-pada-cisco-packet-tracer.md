---
title: "Cara Konfigurasi VLAN Dasar Pada Cisco Packet Tracer"
author_profile: false
excerpt: "VLAN (Virtual Local Area Network) merupakan interface yang digunakan untuk membuat jaringan VLAN atau beberapa VLAN yang disebut inter VLAN. VLAN merupakan model jaringan yang tidak terbatas pada lokasi fisik seperti LAN."
breadcrumbs: true
header:
  teaser: "https://github.com/Julius-Ulee/School-Programs/assets/61336116/33bcb860-0670-4a23-8dae-d5d7f420f615"
last_modified_at: 2023-11-16T:00:00-01:00
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

Pada kesempatan ini izinkan saya membagikan cara konfigurasi Virtual Lan atau biasa disebut juga Vlan pada Cisco Packet Tracer, simulasi berikut ini adalah belajar vlan dasar untuk ketahap yang lebih sulit. Bagi anda yang baru mengenal cisco packet tracer mungkin akan bingung, karna vlan berbeda dengan jaringan yang biasa kita kenal yaitu lan. Dalam vlan kita dapat membagi jaringan yang besar menjadi beberapa segmen tentunya, jaringan dipecah dengan cara virtual.

Pastikan anda sudah menginstall Cisco Packet Tracer versi berapa saja, yang terpenting tidak terlalu lawas. Anda bisa melakukan login guest untuk menggunakan Cisco Packet Tracer tanpa perlu login. Setelah itu buat topologi seperti gambar dibawah ini:

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/e2f20c0d-1995-4bbb-b3d2-d0bc88c0bdd2)

Lihat lah topologi diatas, dan buatlah sama seperti gambar diatas. Jika anda ingin membuat sedikit berbeda, silahkan saja. Seperti ip untuk network yang berbeda, disini saya menggunakan ip network yaitu 192.168.20.0/24. Berikan nama untuk vlan 9 dan vlan 10 saat sudah memulai konfigurasi.

# Cara Konfigurasi VLAN Cisco Packet Tracer
Oke langsung saja ke langkah-langkahnya, disini yang paling pertama kita harus menambahkan ip address pada PC1. Tidak hanya satu pc anda harus menambahkan ip address yang berurutan di setiap pc client.

1. Klik dua kali PC1 lalu masuk ke bagian Desktop lalu IP Configuration

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/c1bc6230-3c3f-426d-87b3-d270da7b34ca)

2. Setelah itu anda akan dibawa kepengaturan konfigurasi IP, silahkan masukan ip address PC0 yaitu 192.168.20.1 dan subnet mask 255.255.255.0

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/55334da8-dd61-40f8-8fb8-7ac558f92e5a)

3. Setelah selesai pemberian ip address lakukan hal tersebut disemua pc client, tergantung ip yang dibutuhkan seperti pada gambar topologi.
4. Jika semua pc client sudah diberikan ip address, mari kita lanjutkan dengan setting vlan pada switch.

# Setting Switch
Klik dua kali switch lalu pilih CLI:

```
Switch>en #enable
Switch#show vlan #untuk melihat hasil konfigurasi vlan
Switch#conf t #untuk memuli konfiggurasi
Switch(config)#vlan ? #untuk melihat berapa alokasi vlan
Switch(config)#vlan 9
Switch(config-vlan)#name tkj1
Switch(config-vlan)#ex #exit
Switch(config)#vlan 10
Switch(config-vlan)#name tkj2
Switch(config-vlan)#ex
Switch#show vlan
```

Selanjutnya adalah memisahkan segmen vlan 9 dan vlan 10 agar tidak bisa saling terhubung, agar jaringan hanya dapat terhubung dalam satu vlan saja dan tidak bisa ke vlan lain, lanjutkan dengan perintah CLI dibawah ini:

```
Switch#conf t
Switch (config)#interface fa0/1 #untuk config fa0/1 (pc 1) agar masuk ke vlan 9
Switch (config-if)#switchport mode access
Switch (config-if)#switchport access vlan 9
Switch (config-if)#ex
Switch (config)#interface fa0/2 #untuk menambahkan ke vlan 9
Switch (config-if)#switchport mode access
Switch (config-if)#switchport access vlan 9
Switch (config-if)#ex
Switch#show vlan #untuk melihat hasilnya
```

Lakukan perintah tersebut pada sisi lainnya:

```
Switch (config)#interface fa0/3 #untuk config fa0/3 (pc 3) agar masuk ke vlan 10
Switch (config-if)#switchport mode access
Switch (config-if)#switchport access vlan 10
Switch (config-if)#ex
Switch (config)#interface fa0/4 #untuk menambahkan ke vlan 10
Switch (config-if)#switchport mode access
Switch (config-if)#switchport access vlan 10
Switch (config-if)#ex
Switch#show vlan #untuk melihat hasilnya
```

# Cek PING VLAN
Jika sudah selesai, waktunya untuk melakukan pengetesan ping antara pc lokal se vlan apakah hasilnya berhasil atau tidak. Jika sudah selesai lakukan ping antara pc beda vlan, bagaimana hasilnya. Semoga anda bisa mengerti dengan apa yang saya maksud, jika mengalami kesulitan, saya sarankan untuk meninggalkan komentar pada postingan ini. Jika kalian ping antara pc se vlan pasti success namun jika beda vlan kan failed, lihat hasilnya.
