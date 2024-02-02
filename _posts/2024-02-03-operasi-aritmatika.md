---
title: "Pengenalan Operasi Aritmatika dan Interaksi dengan Pengguna dalam Python"
author_profile: false
excerpt: "Python adalah bahasa pemrograman komputer yang serbaguna dan dapat digunakan untuk berbagai jenis program. Python dapat digunakan untuk membangun situs, software/aplikasi, mengotomatiskan tugas, dan melakukan analisis data."
breadcrumbs: true
header:
  teaser: "https://github.com/Julius-Ulee/School-Programs/assets/61336116/5d588504-081b-4da7-8e83-fc3ed7af8736"
  overlay_filter: 0.5
last_modified_at: 2024-02-03T:00:00-01:00
categories:
  - Python
tags:
  - Learn
comments: true
show_date: true
---

# Operasi Aritmatika (Matematika):

- Pengguna diminta untuk memasukkan dua angka melalui `input()`.
- Angka-angka tersebut diubah menjadi tipe data integer dengan menggunakan `int()` karena `input()` menghasilkan string.
- Dua angka tersebut kemudian dijumlahkan dan hasilnya disimpan dalam variabel `hasil`.
- Hasil penambahan tersebut ditampilkan ke layar.
  ```py
  angka1  = int(input("Masukan angka pertama : "))
  angka2 = int(input("Masukan angka kedua : "))

  hasil = (angka1+angka2)

  print("Hasil penambahan : ", hasil)
  ```

# Input Nama Pengguna:

- Pengguna diminta untuk memasukkan nama melalui `input()`.
- Nama yang dimasukkan dianggap sebagai string dan disimpan dalam variabel `nama`.
- Nama tersebut kemudian ditampilkan di layar.
  ```py
  nama = str(input("Masukan nama : "))
  print("Nama anda : " + nama)
  ```

# Operasi Perkalian (*):

- Dua angka yang dimasukkan oleh pengguna dikalikan, dan hasilnya disimpan dalam variabel `hasilkali`.
- Hasil perkalian kemudian ditampilkan ke layar.
  ```py
  hasilkali = angka1 * angka2
  print("Hasil kali nya adalah : ", hasilkali)
  ```

# Operasi Pembagian (/):

- Dua angka yang dimasukkan oleh pengguna dibagi, dan hasilnya disimpan dalam variabel `hasilbagi`.
- Hasil pembagian ditampilkan ke layar.
  ```py
  hasilbagi = angka1 / angka2
  print("Hasil baginya adalah : ", hasilbagi)
  ```

# Operator Modulus (%):

- Dua angka yang dimasukkan oleh pengguna dioperasikan dengan modulus, dan sisa hasil bagi disimpan dalam variabel `hasilmodulus`.
- Hasil sisa bagi tersebut ditampilkan ke layar.
  ```py
  hasilmodulus = angka1 % angka2
  print("Hasil sisa bagi nya adalah : ", hasilmodulus)
  ```

# Penutup:

- Menampilkan informasi penutup, dengan mencetak beberapa garis pemisah dan mencantumkan identitas pembuat kode.
  ```py
  print('-----------------------------------------')
  print('-----------------from--------------------')
  print('-------------- me Ulee ------------------')
  ```
Dengan materi ini, pengguna dapat memahami konsep dasar penggunaan operasi aritmatika dan interaksi dengan pengguna menggunakan fungsi `input()` dalam bahasa pemrograman Python. Materi mencakup penanganan input, operasi aritmatika dasar, dan tata cara penampilan hasil kepada pengguna.
