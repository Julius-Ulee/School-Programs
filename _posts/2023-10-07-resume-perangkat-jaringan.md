---
title: "Resume Perangkat Jaringan Repeater, Bridge, dan Network Interface Card"
author_profile: false
excerpt: "Penjelasan mengenai karakteristik **perangkat** beserta cara kerjanya."
breadcrumbs: true
header:
  teaser: "/assets/images/teaser/teaser2.jpg"
  overlay_image: /assets/images/header/network-banner.png
  overlay_filter: 0.5
last_modified_at: 2023-10-07T12:00:00-01:00
categories:
  - Learn
tags:
  - Tugas
  - BSI
  - Jaringan Komputer
toc: true
toc_sticky: true
comments: true
---

# 1. REPEATER

![image](https://github.com/azrielbsi/azrielbsi.github.io/assets/126305178/b51e71df-9171-44d4-90ba-d5d499fa2c22)


Repeater adalah alat yang berfungsi untuk memperkuat sinyal di dalam jaringan komputer.

## Karakteristik Repeater:
1. **Menguatkan Sinyal:** Repeater memiliki kemampuan untuk mendeteksi sinyal yang lemah dan menguatkannya, sehingga memungkinkan sinyal tersebut mencapai area yang lebih jauh atau melewati gangguan.
2. **Lapisan Fisik:** Repeater bekerja pada lapisan fisik (Layer 1) dalam model OSI, yang berarti ia hanya memperhatikan sinyal fisik dan tidak memiliki pemahaman tentang data yang dibawa oleh sinyal tersebut.
3. **Tidak Memiliki Alamat MAC:** Repeater tidak memiliki alamat MAC sendiri, sehingga tidak melakukan filtering atau pengambilan keputusan berdasarkan alamat MAC seperti yang dilakukan oleh bridge atau switch.


## Cara kerja Repeater:
Repeater pada umumnya diletakkan disuatu tempat ketinggian ,antennanyapun ditinggikan lagi yang biasanya diletakkan diatas tower sehingga jangkauan pancaran akan lebih jauh. Semakin tinggi letak repeater, maka akan lebih jauh pula daya jelajahnya. Seringnya repeater diletakkan disuatu lokasi yang  tinggi misalnya di puncak Gunung, atau Bukit , Antennanya pun  di instalasikan ditower yang cukup tinggi.
Memperkirakan jarak jangkau repeater, secara sangat sederhana adalah dengan melihat area dari lokasi tsb dengan mata kita, bila yang terlihat sangat luas, maka hampir dapat dipastikan, sejauh mata kita memandang, sampai sanalah  area yang dapat dicover oleh repeater itu, ( Line Of Sight ) Mengingat keterbatasan daya pandang, dapat saja coveragenya lebih jauh dari pandangan kita.
Peformance sebuah repeater dipengaruhi pula oleh ,daya pancar repeater, sensitivitas, serta sel;ektivitas dari repeater itu sendiri. Untuk meningkatkan  kekuatan pancaran, selain meletakkan repeater pada tempat yang tinggi, maka digunakan pula Antenna dengan penguatan ( gain ) yang besar.


# 2. BRIDGE

![image](https://github.com/azrielbsi/azrielbsi.github.io/assets/126305178/90ff60d9-a93b-4715-bc52-1d474c35b9a6)

Bridge adalah perangkat jaringan yang digunakan untuk memecah jaringan yang besar. Bridge bekerja pada layer data-link dari model OSI. Bridge bekerja dengan mengenali alamat MAC asal yang mentransmisi data ke jaringan dan secara otomatis membangun sebuah table internal. Tabel ini berfungsi untuk menentukan ke segmen mana paket akan di route dan menyediakan kemampuan filtering.

## Karakteristik Bridge:
1. **Menghubungkan Segmen Jaringan:** Bridge digunakan untuk menghubungkan dua segmen jaringan yang berbeda, seperti dua segmen Ethernet, dan mengatur lalu lintas data antara keduanya.
2. **Lapisan Data-Link:** Bridge beroperasi pada lapisan data-link (Layer 2) dalam model OSI, yang berarti ia memahami alamat MAC dan menggunakan informasi ini untuk mengarahkan lalu lintas data.
3. **Memiliki Alamat MAC:** Bridge memiliki alamat MAC sendiri dan dapat mengambil keputusan berdasarkan alamat MAC untuk mengirimkan atau memblokir lalu lintas.

## Cara kerja Bridge:
Bridge, juga dikenal sebagai switch layer 2, dari perngertiannya bridge adalah perangkat keras yang digunakan untuk membuat koneksi antara dua jaringan komputer yang terpisah atau untuk membagi satu jaringan menjadi dua. Kedua jaringan komputer ini biasanya menggunakan protokol yang sama; Ethernet adalah contoh dari protokol ini. Fungsi Bridge ini tidak terbatas pada Personal Komputer (PC), printer, router, switch dan hub. Perangkat yang terhubung ke jaringan melalui kartu adapter Ethernet memiliki apa yang dikenal sebagai alamat Media Access Control (MAC), juga disebut alamat fisik dari perangkat keras. Inilah yang secara unik mengidentifikasi perangkat untuk alamat yang kemudian dapat menentukan mana jaringan perangkat sedang terhubung.

Fungsi Bridge terutama untuk meneruskan data berdasarkan alamat MAC dari perangkat pengirim dan penerima. Operasi ini membantu untuk menghilangkan apa yang dikenal sebagai collision domain. Salah satu cara untuk mendefinisikan sebuah collision domain adalah jaringan di mana satu perangkat, juga disebut simpul, memaksa semua alat lain untuk menerima ketika sedang mengirim paket data. Definisi lain menyatakan bahwa domain tabrakan terjadi ketika dua atau lebih perangkat mencoba untuk mengirimkan informasi pada saat yang sama persis. Jaringan menjalankan Carrier Sense Multiple Access/Collision Detection (CSMA / CD) harus, secara teori, dilindungi dari tabrakan yang terjadi, tetapi CSMA/CD ini bisa saja gagal.

Setiap kali tabrakan terjadi, transmisi paket data yang efisien sangat dikompromikan. Semakin banyak perangkat yang berada di jaringan mencoba untuk mengirimkan data, semakin besar peluang tabrakan terjadi. Sebuah Fungsi Bridge dapat digunakan untuk segmen satu jaringan menjadi dua, sehingga mengurangi jumlah perangkat bersaing untuk hak transmisi. Misalnya, jika jaringan A memiliki 20 perangkat, ada kemungkinan bahwa dua atau lebih dari mereka akan mencoba untuk mengirimkan data pada saat yang sama dan menyebabkan tabrakan. Jika Network Bridge ditambahkan, dapat membagi jaringan A ke jaringan A dan B dengan masing-masing 10 perangkat.

Setelah Network Bridge dimasukkan, maka akan dimulai “pengaturan” transmisi data dalam perangkat pada dua jaringan. Network Bridge menyelesaikan ini dengan merekam alamat MAC dari perangkat dalam sebuah tabel yang secara otomatis dihasilkan tanpa diprogram untuk melakukannya. Ketika perangkat pertama mentransmisikan data, Network Bridge akan menambahkan alamat MAC sebagai tabel forwarding untuk referensi di masa mendatang. Network Bridge juga melihat alamat MAC dari tujuan atau perangkat penerima. Jika tidak muncul dalam tabel, Network Bridge akan menyiarkan paket data ke semua perangkat pada kedua jaringan untuk menemukan tujuan.

Tabel forwarding langsung dibangun, Network Bridge tidak harus menunggu sampai menerima transmisi dari perangkat sebelum dapat belajar dengan alamat MAC. MAC address dari perangkat penerima juga harus mempelajari saluran, pencarian lokasi tujuan. Setelah tujuan merespon, alamatnya juga ditambahkan ke tabel forwarding dari Network Bridge. Akhirnya, semua alamat MAC akan ditangkap dan data paket akan efisien dialihkan langsung ke tempat tujuan. Ini akan terjadi tanpa semua perangkat harus mengantri untuk proses transmisi.


# 3. NETWORK INTERFACE CARD (NIC)

![image](https://github.com/azrielbsi/azrielbsi.github.io/assets/126305178/78d50bdb-d49a-444e-8525-7de207dda7f1)

NIC adalah singkatan dari Network Interface Card yaitu sebuah kartu yang fungsinya sebagai jembatan dari komputer ke sebuah jaringan komputer. Cara kerja NIC adalah untuk mengubah aliran data paralel dalam bus komputer menjadi bentuk data serial sehingga dapat ditransmisikan di atas media jaringan.

## Fungsi NIC diantaranya:
1. Sebagai media yang pengirimkan data ke komputer yang lain di dalam jaringan.
2. Mengontrol data flow diantara komputer & sistem kabel.
3. Sebagai penenerima data yang dikirim dari komputer/PC lain lewat kabel & menerjemahkannya ke dalam bit yang bisa dimengerti oleh komputer.


## Kelompok 3 Kelas: 19.A4.07

![image](https://github.com/azrielbsi/azrielbsi.github.io/assets/126305178/526ffa5e-f9e2-440c-8d4f-ee868a5e5b97)

1. Azriel Fidzlie 19215261
2. M Daffa R 19215264
3. M Azhar A 19215058
4. Sigit Prastio 19215143
5. Maulana Reza Haqq 19215255
