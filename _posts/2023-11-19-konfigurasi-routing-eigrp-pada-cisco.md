---
title: "Konfigurasi Routing EIGRP pada Cisco"
author_profile: false
excerpt: "Enhanced Interior Gateway Routing Protocol atau disingkat EIGRP adalah salah satu routing protocol yang digunakan untuk menghubungkan jaringan antar router secara dinamik."
breadcrumbs: true
header:
  teaser: "https://github.com/Julius-Ulee/School-Programs/assets/61336116/357dd806-3e79-4eb9-83f0-21415144cda8"
last_modified_at: 2023-11-19T:00:00-01:00
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

Enhanced Interior Gateway Routing Protocol atau disingkat EIGRP adalah salah satu routing protocol yang digunakan untuk menghubungkan jaringan antar router secara dinamik. EIGRP merupakan protokol routing yang hanya dapat digunakan pada router- router cisco dan termasuk ke dalam distance vector routing protocol.

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/52bd7e1e-06dd-4129-98c2-2bee31e2d5e9){: .align-center}

Salah satu kelebihan dari EIGRP adalah adanya feasible successor atau jalur backup yang akan menggantikan jalur utama apabila terjadi kegagalan link (down) pada jalur utama tersebut. Beberapa karakteristik dari eigrp antara lain :

- Menggunakan algoritma DUAL
- Memiliki hop count sebanyak 224
- Dapat melakukan convergence secara cepat
- Mampu menonaktifkan auto-summary route
- Menggunakan composite metric

Untuk melakukan konfigurasi routing eigrp, setidaknya terdapat dua langkah yang harus dilakukan, yakni mengaktifkan routing eigrp dan mengadvertise network yang terhubung dengan router.

Untuk mengaktifkan routing eigrp menggunakan comamnd :

```
router eigrp [ASN]
```

ASN (Autonomous System Number) merupakan sebuah identifier yang digunakan router-router eigrp untuk mengenali router eigrp yang lainnya. Router eigrp hanya dapat berkomunikasi dengan router eigrp lain yang berada dalam satu ASN yang sama.

Apabila router ingin berkomunikasi dengan router lain yang terletak di ASN yang berbeda, maka harus dilakukan redistribute. Untuk saat ini kita belum akan membahas tentang redistribute ini.

Sedangkan untuk mendaftarkan (advertise) network menggunakan perintah :

```
network [network_address]
```

yang dimaksud network address pada perintah di atas adalah network yang terhubung secara langsung dengan router.

Terdapat opsi lain untuk melakukan advertise network yakni dengan menambahkan wildcard mask dibelakang network address, seperti berikut :

```
network [network_address] [wildcard mask]
```

wildcard mask di atas berfungsi untuk menentukan network tertentu (spesifik) yang harus diadvertise.

Kita juga bisa menggunakan perintah no auto-summary . Perintah ini berguna agar network address tidak disummarisasi (auto summarize). Untuk beberapa kasus, perintah ini sangat penting karena jika tidak menggunakan perintah ini, bisa-bisa routing akan menjadi kacau.

# Contoh Konfigurasi Routing EIGRP
Sekarang lihatlah topologi di bawah ini :

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/f3598c18-ccf0-4700-8d77-f958aa9bb436){: .align-center}

Topologi di atas merupakan contoh atau ilustrasi dari tiga buah router yang akan menggunakan routing eigrp. Jika masih bingung dengan ip yang digunakan oleh router dan PC di atas, silahkan lihat tabel di bawah ini :

| Device | Interface | IP Address | Subnetmask | Gateaway |
|:--------|:-------:|:-------:|:-------:|:-------:|
| R1 | FastEthernet 0/0 | 192.168.1.254 | 255.255.255.0 | N/A |
|  | Serial 2/0 | 100.100.100.1 | 255.255.255.252 | N/A |
|  | Serial 3/0 | 100.100.100.5 | 255.255.255.252 | N/A |
| R2 | FastEthernet 0/0 | 192.168.2.254 | 255.255.255.0 | N/A |
|  | Serial 2/0 | 100.100.100.6 | 255.255.255.252 | N/A |
|  | Serial 3/0 | 100.100.100.9 | 255.255.255.252 | N/A |
| R3 | FastEthernet 0/0 | 192.168.3.254 | 255.255.255.0 | N/A |
|  | Serial 2/0 | 100.100.100.2 | 255.255.255.252 | N/A |
|  | Serial 3/0 | 100.100.100.10 | 255.255.255.252 | N/A |
| PC1 | FastEthernet 0 | 192.168.1.1 | 255.255.255.0 | 192.168.1.254 |
| PC2 | FastEthernet 0 | 192.168.2.1 | 255.255.255.0 | 192.168.2.254 |
| PC3 | FastEthernet 0 | 192.168.3.1 | 255.255.255.0 | 192.168.3.254 |
{: rules="groups"}

Dan berikut adalah konfigurasi dari masing-masing router di atas,

**Konfigurasi R1 :**

```
//masuk ke mode konfigurasi
Router>enable 
Router#configure terminal

//mengubah hostname
Router(config)#hostname R1 

//konfigurasi ip address
R1(config)#interface fa0/0 
R1(config-if)#ip address 192.168.1.254 255.255.255.0 
R1(config-if)#no shutdown 

R1(config-if)#interface s2/0 
R1(config-if)#ip address 100.100.100.1 255.255.255.252 
R1(config-if)#no shutdown 

R1(config-if)#interface s3/0 
R1(config-if)#ip address 100.100.100.5 255.255.255.252 
R1(config-if)#no shutdown 

R1(config-if)#exit 

//konfigurasi eigrp
R1(config)#router eigrp 1 
R1(config-router)#network 192.168.1.0 0.0.0.255 
R1(config-router)#network 100.100.100.0 0.0.0.3 
R1(config-router)#network 100.100.100.4 0.0.0.3 
R1(config-router)#no auto-summary 
R1(config-router)#exit 

//menyimpan konfigurasi router
R1(config)#do write 
Building configuration...
[OK] 
R1(config)#
```

**Konfigurasi R2 :**

```
//masuk ke mode konfigurasi
Router>enable 
Router#configure terminal 

//mengubah hostname
R2(config)#hostname R2 

//konfigurasi ip address
R2(config)#interface fa0/0 
R2(config-if)#ip address 192.168.2.254 255.255.255.0 
R2(config-if)#no shutdown 

R2(config-if)#interface s2/0 
R2(config-if)#ip address 100.100.100.6 255.255.255.252 
R2(config-if)#no shutdown 

R2(config-if)#interface s3/0 
R2(config-if)#ip address 100.100.100.9 255.255.255.252 
R2(config-if)#no shutdown 

R2(config-if)#exit 

//konfigurasi eigrp
R2(config)#router eigrp 1 
R2(config-router)#network 192.168.2.0 0.0.0.255 
R2(config-router)#network 100.100.100.4 0.0.0.3 
R2(config-router)#network 100.100.100.8 0.0.0.3 
R2(config-router)#no auto-summary 
R2(config-router)#exit 

//menyimpan konfigurasi router
R2(config)#do write 
Building configuration...
[OK] 
R2(config)#
```

**Konfigurasi R3 :**

```
//masuk ke mode konfigurasi
Router>enable 
Router#configure terminal 

//mengubah hostname
R3(config)#hostname R3 

//konfigurasi ip address
R3(config)#interface fa0/0 
R3(config-if)#ip address 192.168.3.254 255.255.255.0 
R3(config-if)#no shutdown 

R3(config-if)#interface s2/0 
R3(config-if)#ip address 100.100.100.2 255.255.255.252 
R3(config-if)#no shutdown 

R3(config-if)#interface s3/0 
R3(config-if)#ip address 100.100.100.10 255.255.255.252 
R3(config-if)#no shutdown 

R3(config-if)#exit 

//konfigurasi eigrp
R3(config)#router eigrp 1 
R3(config-router)#network 192.168.3.0 0.0.0.255 
R3(config-router)#network 100.100.100.0 0.0.0.3 
R3(config-router)#network 100.100.100.8 0.0.0.3 
R3(config-router)#no auto-summary 
R3(config-router)#exit 

//menyimpan konfigurasi router
R3(config)#do write 
Building configuration...
[OK] 
R3(config)#
```

**Konfigurasi PC :**

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/43906d87-eae7-4a26-bd4e-e6686cad2312){: .align-center}

Setelah konfigurasi semua perangkat telah selesai, selanjutnya cek apakah masing-masing network telah terkoneksi atau belum dengan melakukan ping dari satu PC ke PC lain. Pastikan sudah terkoneksi ya, jika belum, berarti masih ada konfigurasi yang keliru.

Kita juga dapat melakukan verifikasi menggunakan perintah-perintah di bawah ini :

```
show ip route show ip route eigrp
```

Contoh verifikasi routing pada R1 :

```
R1#show ip route
Codes: C - connected, S - static, I - IGRP, R - RIP, M - mobile, B - BGP
D - EIGRP, EX - EIGRP external, O - OSPF, IA - OSPF inter area
N1 - OSPF NSSA external type 1, N2 - OSPF NSSA external type 2
E1 - OSPF external type 1, E2 - OSPF external type 2, E - EGP
i - IS-IS, L1 - IS-IS level-1, L2 - IS-IS level-2, ia - IS-IS inter area
* - candidate default, U - per-user static route, o - ODR
P - periodic downloaded static route

Gateway of last resort is not set

100.0.0.0/30 is subnetted, 3 subnets
C 100.100.100.0 is directly connected, Serial2/0
C 100.100.100.4 is directly connected, Serial3/0
D 100.100.100.8 [90/21024000] via 100.100.100.6, 00:00:37, Serial3/0
                [90/21024000] via 100.100.100.2, 00:00:08, Serial2/0
C 192.168.1.0/24 is directly connected, FastEthernet0/0
D 192.168.2.0/24 [90/20514560] via 100.100.100.6, 00:00:37, Serial3/0
D 192.168.3.0/24 [90/20514560] via 100.100.100.2, 00:00:08, Serial2/0

R1#show ip route eigrp
100.0.0.0/30 is subnetted, 3 subnets
D 100.100.100.8 [90/21024000] via 100.100.100.6, 00:00:50, Serial3/0
                [90/21024000] via 100.100.100.2, 00:00:21, Serial2/0
D 192.168.2.0/24 [90/20514560] via 100.100.100.6, 00:00:50, Serial3/0
D 192.168.3.0/24 [90/20514560] via 100.100.100.2, 00:00:21, Serial2/0

```

Demikianlah pembahasan mengenai konfigurasi routing eigrp pada router cisco. Semoga dapat memberikan pemahaman mengenai cara mengkonfigurasi routing eigrp. 
