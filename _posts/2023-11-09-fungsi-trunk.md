---
title: "Fungsi Trunk Yang Harus Kamu Ketahui"
author_profile: false
excerpt: "Fungsi dari trunk adalah untuk menjadi penghubung antara dua switch yang telah terkonfigurasi VLAN."
breadcrumbs: true
header:
  teaser: "https://github.com/Julius-Ulee/School-Programs/assets/61336116/52bee60b-7176-4570-a10d-3d7a4563ff76"
last_modified_at: 2023-11-09T:00:00-01:00
categories:
  - Article
tags:
  - Vlan
  - Cisco
toc: true
toc_sticky: true
comments: true
show_date: true
---

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/0cb67e4f-a76e-481a-a039-f118469a0fb1)

Fungsi dari trunk adalah untuk menjadi penghubung antara dua switch yang telah terkonfigurasi VLAN. Trunk dapat diibaratkan sebagai batang pohon yang berfungsi menghubungkan ranting-ranting pada pohon. Sementara ranting-ranting tersebut adalah VLAN pada konsep trunk ini. Selain menjadi penghubung, fungsi lain dari trunk adalah untuk membatasi akses antar jaringan, sehingga tidak sembarang komponen dapat melakukan pengaksesan terhadap komponen lain di dalam jaringan lain.
Dalam VLAN ada dua mode yang digunakan, salah satunya ialah trunk link. Trunk link pada VLAN (Virtual Local Area Network) merupakan port yang melakukan konfigurasi untuk dilalui beberapa VLAN. Port switch yang menggunakan mode trunk link mampu membawa banyak VLAN. Port pada mode ini nantinya akan menjadi trunk link apabila port yang ada pada switch lawan telah di set ke mode trunk atau dynamic trunking protocol.

Mode trunk link ini umumnya digunakan untuk menghubungkan switch dengan switch, switch dengan router, atau ketika Anda ingin menghubungkan switch dengan server. Mode ini mampu mendukung teknologi fast ethernet yaitu 100Mbps dan gigabite yaitu 1000Mbps. Dalam istilah berbeda, trunk link ini disebut juga dengan tagged vlan.
