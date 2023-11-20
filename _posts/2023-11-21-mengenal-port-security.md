---
title: "Mengenal Port Security Pada Cisco"
author_profile: false
excerpt: "Port Security merupakan mekanisme keamanan yang digunakan pada switch Cisco. Dengan port security, kita bisa membatasi jumlah host yang dapat terkoneksi pada sebuah port yang ada di switch serta menentukan host mana saja yang bisa terkoneksi ke switch."
breadcrumbs: true
header:
  teaser: "https://github.com/Julius-Ulee/School-Programs/assets/61336116/bf23897a-62e2-4c72-9b4c-adfa96fdae81"
last_modified_at: 2023-11-21T:00:00-01:00
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

**Port Security** merupakan mekanisme keamanan yang digunakan pada switch Cisco. Dengan port security, kita bisa membatasi jumlah host yang dapat terkoneksi pada sebuah port yang ada di switch serta menentukan host mana saja yang bisa terkoneksi ke switch.

Prinsip dalam mengkonfigurasi port security adalah mendaftarkan mac address mana saja yang bisa atau diperbolehkan untuk terkoneksi ke switch. Sedangkan cara kerja dari port security adalah ia akan membuang paket dari host atau memblok host yang mac address nya tidak sesuai dengan konfigurasi pada port security. 

Terdapat dua macam port security pada cisco, yakni **static** dan **sticky** (dinamik). pada Port security statik, mac address host harus ditambahkan secara manual oleh administrator, sedangkan pada port security dinamik, mac address akan ditambahkan secara otomatis.

Selain itu, dalam port security dikenal istilah **violation**. Yakni tindakan yang akan dilakukan oleh port interface pada switch ketika terdapat host yang tidak terdaftar mac addressnya berusaha untuk terhubung melalui interface yang sudah disetting port security. Ada 3 macam violation yaitu :

1. Protect
2. Restrict
3. Shutdown

Interface yang menerapkan violation **protect**, akan membuang (drop) paket yang dikirim oleh host yang tidak dijinkan tadi. Jika dilihat melalui command ping, maka akan menghasilkan output **Request timed out**.

Interface yang menerapkan violation **restrict**, akan membuang (drop) paket seperti pada mode protect, namun interface akan menghitung jumlah violation ang terjadi. Sementara pada mode protect jumlah violation tidak akan dihitung. Untuk melihat jumlah violasi yang terjadi ( violation count), gunakan perintah **show port-security interface <nama_interface>**.

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/d6d71562-1393-4fa1-96e4-5b3aeb93be41){: .align-center}

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/4e42d593-a104-4be9-9171-86a0d2ab5a94){: .align-center}

Sedangkan interface yang menerapkan violation **shutdown**, akan menonaktifkan port interface yang digunakan oleh host yang tidak diijinkan tadi. Ketika host mengirim paket ke host lain seperti ping, maka seketika port akan ter-shutdwon. Apabila dilihat pada cisco packet tracer, maka link yang menghubungkan host dengan switch akan berwarna merah.

Untuk memperjelas pemahaman, berikut saya gambarkan sebuah jaringan sederhana yang menggunakan port security dengan violation shutdown sebagai contoh :

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/5664eacf-c377-42f1-af2d-c6bb06bc555c){: .align-center}

Pada topologi di atas, PC0 dan PC1 digambarkan sebagai host yang memiliki ijin untuk terhubung dengan switch. PC0 terhubung dengan port 1 pada switch, sedangkan PC1 terhubung ke port 2 pada switch. Dimisalkan port selain 1 dan 2 dalam keadaan mati sehingga tidak bisa digunakan.

Laptop digambarkan sebagai host yang tidak memiliki ijin untuk terhubung dengan switch. Namun Laptop berusaha untuk terhubung ke switch dengan cara mencabut kabel yang terhubung ke PC1 lalu menghubungkan laptop ke port 2. Apa yang terjadi ? Lihatlah gambar di bawah ini :

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/1c3a7370-f9ab-4e98-a7ef-2824dc6de209){: .align-center}

Link yang menghubungkan Laptop dengan switch seketika ter-shutdown. Meskipun Laptop memiliki ip address yang sama dengan PC1 namun laptop tetap tidak dapat terhubung ke switch karena mac address pada Laptop tidak terdaftar di switch.

Seperti itulah ilustrasi mengenai penggunaan port security pada switch cisco.  Dengan menggunakan port security, kemanan jaringan bisa lebih ditingkatkan dan ancaman dari host yang tidak dikenal dapat diminimalisir. Untuk selanjutnya akan saya bahas mengenai konfigurasi port security menggunakan cisco packet tracer. 
