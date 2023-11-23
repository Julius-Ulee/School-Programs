---
title: "Cara Setting VOID di Simulasi Jaringan Cisco Packet Tracer (Via CLI)"
author_profile: false
excerpt: "VOIP atau kepanjangan dari Voice Over Internet Protocol adalah teknologi yang dapat membuat kita melakukan percakapan suara atau telepon melalui jaringan seperti Intranet atau Internet."
breadcrumbs: true
header:
  teaser: "https://github.com/Julius-Ulee/School-Programs/assets/61336116/93cf38a8-c32b-42a7-98d8-d232f10d8201"
last_modified_at: 2023-11-23T:00:00-01:00
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

VOIP atau kepanjangan dari Voice Over Internet Protocol adalah teknologi yang dapat membuat kita melakukan percakapan suara atau telepon melalui jaringan seperti Intranet atau Internet.

Teknologi VOIP banyak digunakan sebagai media komunikasi di perkantoran atau digunakan untuk pelayanan Costumer Service.

Kali ini kita akan melakukan simulasi sederhana untuk mengetahui bagaimana caranya merancang jaringan VOIP. Simulasi ini menggunakan software Cisco Packet Tracer. Sebaiknya pergunakan Cisco Packet Tracer versi 6 keatas agar simulasi dapat berjalan dengan baik.

# 1. Siapkan Topologi Jaringan untuk VOIP.

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/fb1624ad-93d0-4eb7-be98-2995b5f0558b){: .align-center}

Buatlah dulu Topologi seperti gambar di atas. Simulasi kali ini menggunakan 1 buah Router Cisco dengan tipe 2811, 1 buah Switch Cisco Catalyst 2960-24TT, dan 2 buah Cisco IP Phone 7960 Series.

# 2. Setting Router
Berikan IP address kepada Router dengan perintah CLI sebagai berikut :

```yml
R1>enable
R1#configure terminal
R1(config)#interface FastEthernet0/0
R1(config-if)#no shutdown
R1(config-if)#interface FastEthernet0/0.10
R1(config-subif)#encapsulation dot1q 10
R1(config-subif)#ip address 192.168.1.1 255.255.255.0
```

Setelah Router memiliki IP address, langkah selanjutnya adalah menjadikan Router sebagai DHCP server sehingga nantinya IP Phone bisa memiliki IP address secara otomatis. Gunakan perintah CLI seperti di bawah ini :

```yml
R1(config-subif)#ip dhcp pool iptelepon
R1(dhcp-config)#network 192.168.1.0 255.255.255.0
R1(dhcp-config)#default-router 192.168.1.1
R1(dhcp-config)#option 150 ip 192.168.1.1
```

TIndakan berikutnya adalah pengaturan Telephony-service agar Router bisa melakukan pelayanan telepon. Perintah CLI untuk hal tersebut adalah :

```yml
R1(dhcp-config)#telephony-service
R1(config-telephony)#ip source-address 192.168.1.1 port 2000
R1(config-telephony)#max-dn 2
R1(config-telephony)#max-ephone 2
R1(config-telephony)#auto assign 1 to 2
R1(config-telephony)#ephone-dn 1
R1(config-ephone-dn)#number 1001
R1(config-ephone-dn)#ephone-dn 2
R1(config-ephone-dn)#number 1002
```

Catatan :angka dibelakang “max-dn” dan “max-ephone” menyesuaikan jumlah Telepon yang akan dipasang. Karena simulasi ini menggunakan 2 buah IP Phone maka “max-dn 2” dan “max-ephone 2”.

# 3. Setting Switch
Jaringan VOIP biasanya membutuhkan manageable switch atau switch yang memiliki sistem operasi dan bisa dikonfigurasikan. Berikut ini perintah CLI agar switch bisa digunakan di jaringan VOIP :

```yml
SW1>enable
SW1#configure terminal
SW1(config)#vlan 10
SW1(config-vlan)#interface FastEthernet0/1
SW1(config-if)#switchport mode trunk
SW1(config-if)#interface range FastEthernet0/2-4
Sw1(config-if)#switchport voice vlan 10
```

# 4. Test IP Phone
Jika konfigurasi Router dan Switch sudah benar, IP Phone secara otomatis akan mendapatkan IP address serta Dial Number dan sudah bisa digunakan.

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/3d2540bc-e452-4fae-9005-3aec55777cf3){: .align-center}

Lakukan pengujian dengan melakukan panggilan menggunakan IP Phone 1 ke IP Phone 2 atau sebaliknya. Jika IP Phone bisa terkoneksi dan menghubungi satu sama lain maka Simulasi VOIP bisa dikatakan berhasil.

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/2f070a2a-8e54-43e2-8058-61b92be795da){: .align-center}

