---
title: "Cara Buat Jaringan Client Server Menggunakan Cisco Packet Tracer"
author_profile: false
excerpt: "Jaringan komputer Client-Server adalah konektivitas antara komputer client dan komputer server dengan fungsi utamanya yaitu client sebagai peminta data dan server memberikan respon data terhadap permintaan tersebut."
breadcrumbs: true
header:
  teaser: "https://github.com/Julius-Ulee/School-Programs/assets/61336116/5bb69dbd-b5d0-4421-a31a-80bcdbfd908d"
last_modified_at: 2023-11-17T:00:00-01:00
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

Jaringan komputer Client-Server adalah konektivitas antara komputer client dan komputer server dengan fungsi utamanya yaitu client sebagai peminta data dan server memberikan respon data terhadap permintaan tersebut.

Model jaringan Client-Server banyak diterapkan mulai dari jaringan lokal satu ruangan (local area network) sampai jaringan yang lebih besar antar negara (wide area network).

Contoh penerapan Client-Server adalah layanan video streaming seperti Youtube dan Netflix. Perangkat client meminta data termasuk berkas video ke server, selanjutnya server merespon dan mengirim data video ke client untuk ditonton oleh pengguna.

Kali ini kita akan coba buat topologi dan simulasi sederhana jaringan Client-Server menggunakan aplikasi Cisco Packet Tracer.

# Buat Topologi
Gambarkan tiga unit Komputer PC, sebuah Switch dan sebuah PC Server, hubungkan kesemuanya menggunakan kabel Straight seperti gambar berikut.

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/a1363b2a-bc74-42c5-b081-968557fd44fd){: .align-center}

# Konfigurasi Client dan Server
Masukkan IP Address dan Subnet Mask pada PC Client dan PC Server dengan data sebagai berikut:

## Server0
- IP Address: 192.168.1.1
- Subnet Mask: 255.255.255.0

## PC0
- IP Address: I92.168.1.2
- Subnet Mask: 255.255.255.0
- Default Gateway: 192.168.1.1

## PC1
- IP Address: I92.168.1.3
- Subnet Mask: 255.255.255.0
- Default Gateway: 192.168.1.1

## PC2
- IP Address: I92.168.1.4
- Subnet Mask: 255.255.255.0
- Default Gateway: 192.168.1.1

Masukkan data tersebut dengan cara **Klik PC** → **Desktop** → **IP Configuration**.

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/0d838a12-b8a9-45ae-aa16-81a992952e3a){: .align-center}

# Test Ping
Konfigurasi sudah selesai dilakukan. Selanjutnya kita perlu test koneksi dengan cara test PING dari PC Client ke PC Server dengan cara:

**Klik PC Client** → **Desktop** → **Command Prompt** → Ketikkan **"ping 192.168.1.1"**. Jika Reply berarti PC Client dan PC Server sudah dapat saling berkomunikasi.

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/8f53c4b0-182d-4e22-a8d3-9605a586bfaf){: .align-center}
