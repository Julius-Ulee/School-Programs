---
title: "konfigurasi Web server Cisco Packet Tracer"
author_profile: false
excerpt: "Web server adalah perangkat lunak (software) yang berfungsi sebagai penerima permintaan yang dikirimkan melalui browser kemudian memberikan tanggapan permintaan dalam bentuk halaman situs web atau lebih umumnya dalam dokumen HTML."
breadcrumbs: true
header:
  teaser: "https://github.com/Julius-Ulee/School-Programs/assets/61336116/15248aa3-6231-44bd-882f-c3bc103a9854"
last_modified_at: 2023-11-20T:00:00-01:00
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

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/95639433-5650-4686-981e-492d99230f05){: .align-center}

Web server adalah perangkat lunak (software) yang berfungsi sebagai penerima permintaan yang dikirimkan melalui browser kemudian memberikan tanggapan permintaan dalam bentuk halaman situs web atau lebih umumnya dalam dokumen HTML.

Web server juga dikenal dengan nama HTTP server, menyediakan kemampuan untuk mengirimkan dokumen hyper-text kepada pengguna. Dokumen Hypertext itu nantinya digunakan untuk dijadikan tampilan.

Cara mengkonfigurasi HTTP server dengan menggunakan Cisco packet Tracer adalah sebagai berikut. Pertama desain topologi seperti pada gambar.

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/6c410a7f-8394-4fcb-9091-f7a38352a05e){: .align-center}

Keterangan :

>> Server generic

>> Switch 2950-24

>> PC generic

>> Kabel straight

Setting IP Address komputer server dengan masuk ke menu server, caranya klik icon **server > Desktop > IP Configuration**. Atur IP nya seperti gambar berikut.

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/1eea49db-1d69-4852-b984-799a1177ea00){: .align-center}

setelah selesai memberikan IP server, selanjutnya kita akan membuat HTTP nya. masih di menu server, **pilih services > HTTP** seperti gambar berikut. pastikan HTTP dalam posisi **On**. untuk mengedit file HTTP nya klik di index.html.

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/f4877ce7-e6b0-4b23-b971-3b3693e54a80){: .align-center}

setelah membuka index.html hapus semua HTML yang ada, kemudian kreasikan sendiri file HTML nya sesuai selera anda. contoh singkat seperti pada gambar berikut. Kemudian tutup jika sudah selesai.

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/17878b04-df90-4f88-8484-673cb692ed69){: .align-center}

Selanjutnya setting semua IP address pada PC Client yang terhubung dengan server, klik icon **PC > Desktop > IP Configuration** lalu setting seperti berikut PC0: **192.168.1.2**, PC1: **192.168.1.3**, PC2: **192.168.1.4**.

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/b0082ab4-7f17-4fe0-a2d1-7bec24fdd727){: .align-center}

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/10585e84-2fd7-4bc5-9b96-3e1c209bd35d){: .align-center}

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/a91bd786-5259-4971-a9d4-2ad01c42ef57){: .align-center}

Setelah selesai mengatur IP setiap PC, pastikan apakah PC dan dan server sudah terkoneksi dengan baik atau belum. Caranya dengan melakukan test ping dari  PC- client dengan server. Anda dapat melakukannya di command prompt **PC > Desktop > Command Prompt**.

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/6fbd517f-ade7-453d-9599-4628e12af20e){: .align-center}

Terakhir tes apakah web server berhasil atau tidak dengan cara klik pada **PC client > Desktop > Web Browser** kemudian  masukkan IP address komputer server, berikut hasilnya.

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/775ab71f-535e-4651-b3b9-e4f972e6b32c){: .align-center}

Sekian tutorial singkatnya untuk konfigurasi web server dengan Cisco Packet Tracer, semoga bermanfaat dan terimakasih.
