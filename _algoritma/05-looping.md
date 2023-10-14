---
title: "Looping"
permalink: /algoritma/looping/
author_profile: false
excerpt: "Looping dalam pemrograman adalah sebuah konsep di mana sejumlah pernyataan atau instruksi dieksekusi berulang kali selama suatu kondisi terpenuhi. Dalam bahasa pemrograman apapun, termasuk dalam bahasa pemrograman Python atau JavaScript, looping dapat dilakukan dengan menggunakan beberapa jenis pernyataan kontrol seperti `for`, `while`, atau `do-while`."
show_date: true
last_modified_at: 2023-10-14T17:00:00-01:00
categories:
  - Learn
tags:
  - Logika
  - Algoritma
  - Materi
toc: true
toc_sticky: true
comments: true
---

# Looping 
Instruksi pengulangan (repetition) adalah instruksi yang dapat mengulangi pelaksanaan sederetan instruksi lain berulangkali sesuai dengan persyaratan yang ditentukan. Struktur instruksi perulangan pada dasarnya terdiri atas:
1. Kondisi perulangan. Suatu kondisi yang harus dipenuhi agar perulangan dapat terjadi
2. Badan (body) perulangan. Deretan instruksi yang akan diulang-ulang pelaksanaannya
3. Pencacah (counter) perulangan. Suatu variabel yang nilainya harus berubah agar perulangan dapat terjadi dan pada akhirnya membatasi jumlah perulangan yang dapat dilaksanakan.

## Bentuk Perulangan pada Python
1. Perulangan For Perulangan yang mengerjakan “bagian pernyataan yang sama” secara berulang-ulang berdasarkan syarat atau kondisi yang ditentukan.
2. Perulangan While Perulangan yang mengerjakan perintah selama kondisinya bernilai benar.
3. Loop bersarang (Nested Loop) Perulangan di dalam perulangan.

### 1. Perulangan For
**Bentuk Umum**
```
For variable in range:
  statements
```

**Flowchart - For**

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/be5b9831-bd45-4b1d-a89a-b18faeeb2ccd)

#### Menampilkan Deret Bilangan
```
Algoritma deret
Deklarasi
  n, i : integer
Begin
  read(n)
  for i in range n
    write(i)
End
```
```py
# Menampilkan Bilangan Deret
n = int(input('Banyak Data: '))
for i in range(n):
    print(i)

# Output
Banyak Data : 5
0 1 2 3 4 
```
**Note:** pada Python perulangan dengan fungsi Range dimulai dari 0
{: .notice--info}
