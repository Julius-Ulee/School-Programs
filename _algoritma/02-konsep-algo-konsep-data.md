---
title: "Konsep Algoritma & Konsep Data"
permalink: /algoritma/konsep-algoritma-data/
author_profile: false
excerpt: "**Konsep Algoritma** adalah upaya dengan urutan operasi yang disusun secara logis dan sistematis untuk menyelesaikan suatu masalah untuk menghasilkan suatu output tertentu, sementara **Tipe Data** adalah atribut yang berkaitan dengan data yang akan memberi tahu sistem komputer."
show_date: true
header:
  overlay_image: /assets/images/header/logika-dan-algoritma.jpeg
  overlay_filter: 0.5
last_modified_at: 2023-10-12T17:00:00-01:00
toc: true
toc_sticky: true
comments: true
---

# Konsep Algoritma
## 1. Algoritma Pe-ubah
Adalah Variabel yang nilainya BUKAN konstanta (selalu berubah – sesuai dengan kondisi Variabel ter**KINI**)

Sintaks : P = Q

Algoritma : P <- Q

Arti : Bahwa Nilai P diberi harga Nilai Q Nilai P akan SAMA DENGAN nilai Q, & Nilai Q TETAP

## 2. Algoritma Pertukaran
Berfungsi mempertukarkan masing-masing isi Variabel sedemikian sehingga Nilai dari tiap Variabel akan berubah/bertukar.

###  Contoh Soal Algoritma
#### Soal
Diketahui P=10, Q=15 dan R=5. Diberikan Algoritma P=Q,Q=R, mk Nilai P,Q,R sekarang?
#### Jawaban
1. **P = Q:** Dalam langkah ini, nilai Q (15) akan disalin ke dalam variabel P. Sehingga, P sekarang bernilai 15.
2. **Q = R:** Dalam langkah ini, nilai R (5) akan disalin ke dalam variabel Q. Sehingga, Q sekarang bernilai 5.

   Hasil akhirnya adalah:
   
- Nilai P adalah 15
- Nilai Q adalah 5
- Nilai R tetap 5 (tidak berubah dalam algoritma yang diberikan)

# Analisa Algoritma
1. Sekumpulan lidi yang berjumlah 12 dapat membentuk kotak seperti di bawah ini. Pertanyaan pindahkanlah dua buah lidi tersebut agar membentuk empat buah kotak.

    ![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/931e212a-ab64-4324-80f6-65d92502f6e3)

    Dengan memindahkan dua buah lidi yang ada pada bagian bawah, seperti dibawah ini

    ![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/c548f18e-896f-433a-a398-a5cedd8be5ea)

2. Ada tiga batang lidi dibawah ini, bagaimana caranya untuk membentuk angka 6 tanpa mematahkannya

    ![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/02196098-e247-48de-8c4f-864d9b45c9bf)

    Jawab: Ketiga buah lidi tersebut akan membentuk angka 6 romawi

    ![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/576d7fe7-a46f-4dbf-8601-8ce2c0aca674)

3. Budi tidak pernah bolos dalam kelasnya, tetapi dia tidak pernah mengerjakan tugas selama setahun ini. Kerjanya cuma bicara dan Budi juga tidak pernah mengikuti ujian semester, Budi juga bukan murid yang berprestasi. Kenapa Budi tidak pernah mendapat peringatan dari pihak sekolah? (menurut Anda apa jawabannya)

   Jawabannya: Karena Budi adalah Seorang guru.

   Penjelasan: Budi tidak pernah mengerjakan tugas namun membuat tugas, kerjanya cuma bicara menjelaskan materi pelajaran dalam kelas sehingga Budi tidak akan pernah mengikuti ujian semester.

4. Berapa banyaknya garis minimal untuk menutup seluruh titik-titik yang ada dibawah ini dengan syarat bahwa untuk membuat garis tersebut tidak boleh terputus :
   
   ![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/efb38600-5426-41f2-a51d-7e6a482a6b44)

5. Algoritma Pertukaran Isi Bejana Untuk Latihan Uji Coba Pertukaran Mahasiswa Membawa 2 Gelas air yang berbeda warnanya dan 1 gelas Kosong

   Diberikan dua buah bejana, A dan B; bejana A berisi larutan berwarna merah, bejana B berisi larutan berwarna biru

   **Buatlah pseudocode** untuk menukarkan isi kedua bejana itu sedemikian sehingga bejana A berisi larutan berwarna biru dan bejana B berisi larutan berwarna merah.

   ![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/9b2bb3b5-976f-496a-9a0e-54f562beef1e)

DESKRIPSI :
- Tuangkan larutan dari bejana A ke dalam bejana C.
- Tuangkan larutan dari bejana B ke dalam bejana A.
- Tuangkan larutan dari bejana C ke dalam bejana B.
   
   ![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/5a15370e-6ac5-4cae-b9da-147a14210a66)

# Tipe Data Pada Python

| Tipe Data | Keterangan |
|:--------|:-------:|
| Boolean   | Mempunyai dua nilai yaitu true bernilai 1 dan false bernilai 0   |
| String   | Terdiri dari karakter/kalimat berupa huruf, angka, dll (diapit tanda " atau ')   |
| Integer   | Menyatakan bilangan bulat   |
| Float   | Menyatakan bilangan yang mempunyai koma   |
| Complex   | Menyatakan pasangan angka real dan imajiner   |
| List   | Data untaian yang menyimpan berbagai tipe data, isinya dapat berubah-ubah   |
| Tuple   | Data untaian yang menyimpan berbagai tipe data, tapi isinya tidak dapat berubah-ubah   |
| Hexadecimal   | Menyatakan bilangan dalam format heksa   |
| Dictionary   | Data untaian yang menyimpan berbagai tipe data berupa pasangan penunjuk dan nilai
{: rules="groups"}

## Contoh tipe data pada python

```py
#tipe data Boolean
print(True)
#tipe data String
print("Belajar Python menyenangkan...")
#tipe data Integer
print(20)
#tipe data Float
print(3.14)
#tipe data Complex
print(5j)
```
```yml
Hasil Running:
True
Belajar Python menyenangkan...
20
3.14
5j
```

# Tipe Data list
Adalah sebuah array yang berisi kumpulan tipe yang tidak sejenis.
```py
#tipe data list
kata = ["Belajar", "Python", "di", "School Programs"]
angka = [10, 50, 100, 1000]
campur = ["Belajar", 100, 7.99, True]

#cetak
print(kata)
print(angka)
print(campur)
```
```yml
Hasil Running:
['Belajar', 'Python', 'di', 'School Programs']
[10, 50, 100, 1000]
['Belajar', 100, 7.99, True]
```

# Tipe Data Tuple
Tipe data tuple hampir sama dengan list, perbedaanya anggotanya tidak bisa diubah setelah dideklarasikan. Tuple menggunakan kurung biasa dan dipisahkan dengan koma untuk anggota.
```py
#tipe data tuple
kata = ("Belajar", "Python", "di", "School Programs")
angka = (10, 50, 100, 1000)
campur = ("Belajar", 100, 7.99, True)

#cetak
print(kata)
print(angka)
print(campur)
```
```yml
Hasil Running:
('Belajar', 'Python', 'di', 'School Programs')
(10, 50, 100, 1000)
('Belajar', 100, 7.99, True)
```

# Tipe Data Dictionary
Bentuk umum tipe data dictionary pada pemrograman python: Nama_variabel = {“ key1”: “value1”, “key2”: “value2”, “key3”: “value3” }
```py
#Tipe data dictionary
data = {1:"Belajar",
2: ["C++", "Python"],
"Di Kampus": "School Programs",
"menyerah" : False,
"Tahun": 2021}
print(data)
```
```yml
Hasil Running:
{1: 'Belajar', 2: ['C++', 'Python'], 'Di Kampus': 'School Programs', 'menyerah': False,
'Tahun': 2021}
```

# Operator Aritmatika & Matematika

| Operator | Keterangan |
|:--------|:-------:|
| +   | Penjumlahan  |
| -   | Pengurangan  |
| *   | Perkalian   |
| /   | Pembagian   | 
| %   | Modulus (sisa bagi) |   
| **   | Pemangkatan |
| //   | Pembagian dimana hasilnya bilangan bulat 
{: rules="groups"}

## Contoh Operator Aritmatika dan Matematika 

```py
>>> 1+2
3
>>> 8-12
-4
>>> 4*5
20
>>> 42/7
6.0
>>> 9%2
1
>>> 5**2
25
>>> 10//3
3
```

# Operator Perbandiangan

| Operator | Keterangan |
|:--------|:-------:|
| >   | Lebih besar dari   |
| <   | Lebih kecil dari   |
| ==   | Sama dengan   |
| !=   | Tidak sama dengan   |
| <=   | Lebih kecil sama dengan   |
| >=   | Lebih besar sama dengan   
{: rules="groups"}

## Contoh Operator Perbandingan

```py
>>> 10>5
True
>>> 8<6
False
>>> 10==10
True
>>> 5!=6
True
>>> 6<=6
True
>>> 8>=3
True
```

# Operator Bitwise

| Operator | Keterangan |
|:--------|:-------:|
| &   | AND   |
|  l  | OR   |
| ~   | NOT   |
| ^   | XOR   |
| <<   | Geser bit ke kiri   |
| >>   | Geser bit ke kanan   
{: rules="groups"}

# Operator AND
Operator AND akan bernilai false (0) apabila nilai semua operandnya atau salah satu bernilai false (0), dan akan bernilai true (1) apabila kedua operand bernilai true (1).

| Operand 1  | Operand 2  | Output |
|:--------|:-------:|--------:|
| 0   | 0   | 0   |
| 0   | 1   | 0   |
| 1   | 0   | 0   |
| 1   | 1   | 1   
{: rules="groups"}

# Operator OR
Operator Or akan menghasilkan output: Jika salah satu operand atau kedua operand bernilai true (1) akan menghasilkan output true (1), jika kedua operand bernilai false (0) maka akan menghasilkan output false (0).

| Operand 1  | Operand 2  | Output |
|:--------|:-------:|--------:|
| 0   | 0   | 0   |
| 0   | 1   | 1   |
| 1   | 0   | 1   |
| 1   | 1   | 1   
{: rules="groups"}

# Operator XOR
Hasil operasi menggunakan operator XOR, yaitu:
- Apabila bit yang dibandingkan nilainya berbeda misalnya 1 (true) dan 0 (false) maka outputnya adalah 1 (true).
- Apabila bit yang dibandingkan nilainya sama misalnya 1 (true) dan 1(true) atau 0 (false) dan 0 (false) maka outputnya adalah 0 (false).

| Operand 1  | Operand 2  | Output |
|:--------|:-------:|--------:|
| 0   | 0   | 0   |
| 0   | 1   | 1   |
| 1   | 0   | 1   |
| 1   | 1   | 0   
{: rules="groups"}

# Menggabungkan Nilai string
Pada Pemrograman Python untuk menggabungkan nilai string pada program adalah sebagai berikut:

```py
#Penggabungan dua string
kata1 = "Belajar Bahasa Pemrograman Python "
kata2 = "Sangat Menyenangkan"

# Menampilkan nilai dari kata1 dan kata2
print(“Kata1: “,kata1)
Print(“Kata2: “,kata2)

# Menggabungkan kata1 dan kata2
gabung = kata1 + kata2
print(“Hasil Penggabungan kata1 dan kata2”)
print(gabung)
```
```yml
Hasil Running:
Belajar Bahasa Pemrograman Python Sangat Menyenangkan
```

# Fungsi Len
Untuk menghitung jumlah karakter digunakan fungsi len()
```py
#Fungsi Len
#Untuk Menghitung Panjang Karakter
kata = "Belajar Bahasa Pemrograman Python"
jumlah_karakter=len(kata)
print(jumlah_karakter)
```
```yml
Hasil Running:
33
```

# Fungsi index()
Untuk mengetahui posisi karakter dalam kalimat.

```py
#fungsi index
kata = 'Aisah Zahra'

#dimana posisi karakater Z
print (kata.index('Z'))

#dimana posisi karakter r
print (kata.index('r'))
```
```yml
Hasil Running:
7
10
```
