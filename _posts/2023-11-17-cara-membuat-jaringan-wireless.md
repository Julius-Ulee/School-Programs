---
title: "Cara Membuat Jaringan Wireless Cisco Packet Tracer"
author_profile: false
excerpt: "Tutorial kali ini kita akan membuat jaringan wireless menggunakan 1 access point Linksys dengan 2 Tablet PC sebagai client."
breadcrumbs: true
header:
  teaser: "https://github.com/Julius-Ulee/School-Programs/assets/61336116/d3adf50a-729d-4154-9525-d62a17690bac"
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

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/796af71b-353d-4786-8f66-1354f6560c24){: .align-center}

# Langkah Pertama. Konfigurasi Access Point
- Klik Wireless Devices
- Masukkan Linksys

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/ef0afc54-b077-466b-ad72-bb313c932e88){: .align-center}

- Klik Linksys yang sudah dimasukkan untuk melakukan konfigurasi access point
- Klik tab GUI
- IP Address 192.168.0.1
- Subnet Mask 255.255.255.0

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/e2723b81-aa02-4484-93c3-5a4d33960979){: .align-center}

- Aktifkan DHCP Server, Enabled
- Start IP Address, IP DHCP mulai dari 192.168.0.100
- Maximum number of Users = jumlah maksimum IP DHCP
- Save Settings

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/f7d3c013-d5ed-4a20-b4a2-f1aaf737b78b){: .align-center}

- Klik menu Wireless->Basic Wireless Settings
- Beri nama SSID = Linksys
- Save Settings

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/5063287b-3752-41f7-998e-e98530fa3e10){: .align-center}

- Klik menu Wireless->Wireless Security
- Security Mode memakai WPA2 Personal
- Encryption AES
- Passphrase 12345678
- Save Settings

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/45907c91-2579-4791-acf7-076d91242804){: .align-center}

# Langkah Kedua. Konfigurasi Client
- Tambahkan 2 PC Tablet
- Klik End Devices, Wireless Tablet

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/97e92048-a06a-49b4-8d21-f9b31abc5639){: .align-center}

- Konfigurasi Tablet PC pada tab Config
- SSID = Linksys
- Authentication = WPA2-PSK
- Pass Phrase = 12345678

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/ff4003b6-d67c-4a9b-aa39-0661bd2a0793){: .align-center}

- IP menggunakan DHCP
- Jika PC Tablet berhasil terkoneksi dan DCHP Server aktif maka akan tampil nomor IP

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/22aedf56-22c4-42c8-aea3-bfce2e9ea3f7){: .align-center}

- Konfigurasikan hal yang sama pada PC Tablet yang ke-2

# Langkah Ketiga. Pengujian
- Pada PC Tablet, tab Desktop->Command Prompt
- Ping IP Access Point 192.168.0.1
- Ping IP PC Tablet ke-2

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/c76a0808-fa87-46d4-a73a-460088189d36){: .align-center}

Silahkan dipraktikan 🤗
