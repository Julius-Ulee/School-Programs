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

Penjelasan algoritma: Mula-mula masukkan nilai n misal:5, kemudian terjadi perulangan dengan i=0 sampai n. Pengulangan dikerjakan selama kondisi bernilai true. Kemudian write (i) menghasilkan keluaran 0 dst, proses
**diulang lagi sampai dengan i kurang dari nilai n.**

| Perintah | n | i=0..n | i | Output|
|:--------|:-------:|:-------:|:-------:|:-------:|
| read(n) | 5 |  |  |  |
| i=0: write(i) |  | true | 0 | 0 |
| i=1: write(i) |  | true | 1 | 1 |
| i=2: write(i) |  | true | 2 | 2 |
| i=3: write(i) |  | true | 3 | 3 |
| i=4: write(i) |  | true | 4 | 4 |
| i=5: write(i) |  | false |  |  |
{: rules="groups"}

### 2. Perulangan While
Perulangan akan terus dilaksanakan selama kondisi bernilai True/benar

**Bentuk Umur**
```
while kondisi:
  statement(s)
```

**Flowchart Perulangan While**

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/12baa978-a265-493d-abce-2b6d2310f3d4)

1. Ada instruksi yang berkaitan dengan kondisi sebelum masuk ke while sehingga kondisi ini benar (terpenuhi) dan pengulangan bisa dilaksanakan.
2. Ada suatu instruksi di antara instruksi-instruksi yang diulang yang mengubah nilai variabel perulangan agar pada saat kondisi perulangan tidak terpenuhi sehingga perulangan berhenti.

#### Menampilkan Deret Bilangan Genap
```
Algoritma deret
Deklarasi
  n, x : integer
Begin
    read(n)
    x <- 2
    while x <= n do
        write(x)
        x <- x + 2
End
```
```py
# Menampilkan Deret Bilangan Genap
n = int(input('Masukkan Nilai N: '))
x = 2
while x <= n:
    print(x, end=" ")
    x = x + 2

# Output
Massukan Nilai N : 8
2 4 6 8
```

Mula-mula inputkan nilai n = 8, kemudian x diberi nilai 2, setelah itu x dibandingkan dengan n. Jika (x<=n) bernilai benar maka x ditampilkan kemudian x ditambah 2 dan menghasilkan nilai x baru. Setelah itu data kembali keatas dan menguji (X<=N) bernilai benar, jika ya proses yang sama dgn sebelumnya dilakukan kembali. Demikian seterusnya sampai (x<=n) bernilai salah.

#### Tabel Penyimpanan Deret

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/e558bc1c-9572-4508-bf0d-184d762af652)

### Algoritma while untuk menampilkan angka 1 hingga 15
```
Algoritma Perulangan_while
{mencetak angka 1 hingga 15}
Deklarasi
angka =1

Deskripsi
  while angka <= 15:
    cetak angka
angka <- angka + 1
```
