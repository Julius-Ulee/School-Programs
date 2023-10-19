---
title: "Looping"
permalink: /algoritma/looping/
author_profile: false
excerpt: "Looping dalam pemrograman adalah sebuah konsep di mana sejumlah pernyataan atau instruksi dieksekusi berulang kali selama suatu kondisi terpenuhi. Dalam bahasa pemrograman apapun, termasuk dalam bahasa pemrograman Python atau JavaScript, looping dapat dilakukan dengan menggunakan beberapa jenis pernyataan kontrol seperti `for`, `while`, atau `do-while`."
show_date: true
header:
  overlay_image: /assets/images/header/logika-dan-algoritma.jpeg
  overlay_filter: 0.5
last_modified_at: 2023-10-14T17:00:00-01:00
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

#### Algoritma while untuk menampilkan angka 1 hingga 15
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

#### Program Python Mencetak bilangan 1 sampai 15
```py
# Perulangan While
angka = 1
while angka <= 15:
  print ("Bilangan ke-: ", angka)
  angka = angka + 1
print ("Terima Kasih")

# Output
Hasil Running :
Bilangan ke-: 1
Bilangan ke-: 2
Bilangan ke-: 3
Bilangan ke-: 4
Bilangan ke-: 5
Bilangan ke-: 6
Bilangan ke-: 7
Bilangan ke-: 8
Bilangan ke-: 9
Bilangan ke-: 10
Bilangan ke-: 11
Bilangan ke-: 12
Bilangan ke-: 13
Bilangan ke-: 14
Bilangan ke-: 15
Terima Kasih
```

##### Program Python Mencetak bilangan Menurun 10 sampai 1
```py
# Perulangan While
# Mencetak bilangan 10 sampai 1
bil = 10
while bil > 0:
    print(bil)
    bil = bil - 1
print("Hasil Mencetak Bilangan Secara Menurun")

# Output
10
9
8
7
6
5
4
3
2
1
Hasil Mencetak Bilangan Secara Menurun
```

#### Program Python Menentukan Bilangan Prima atau tidak
```py
# Input bilangan
bilangan = int(input("Masukkan Bilangan: "))

# Bilangan prima harus lebih besar dari 1
if bilangan > 1:
    for i in range(2, bilangan):
        if (bilangan % i) == 0:
            print(bilangan, "bukan bilangan prima")
            print(i, "kali", bilangan // i, "=", bilangan)
            break
    else:
        print(bilangan, "adalah bilangan prima")
# Bila bilangan kurang atau sama dengan satu
else:
    print(bilangan, "bukan bilangan prima")

# Output
Masukkan Bilangan : 137
137 adalah bilangan prima

Masukkan Bilangan : 147
147 bukan bilangan prima
3 kali 49 = 147
```

#### Perintah BREAK;
Berfungsi untuk keluar dari suatu loo[ for atau while bentuk umumnya adalah:
```yml
...
...
break
...
...
```

##### Program Python Menggunakan Perintah Break
```py
# Perintah break pada perulangan for
# Program akan keluar setelah mencetak angka sampai 6 karena perintah break
bil = 6
for i in range(0, 10):
    print(i)
    if i == bil:
        break

# Output
0
1
2
3
4
5
6
```
**Note:** Looping akan dikerjakan terus sampai dipaksa keluar oleh instruksi break;
{: .notice--info}

#### Perintah Continue:
Fungsi Continue akan melakukan pengulangan mulai dari awal lagi.
```py
# Penggunaan continue pada while
bil = 0
pilihan = 'y'

while (pilihan != 'n'):
    bil = int(input("Masukkan bilangan dibawah 50: "))
    if (bil > 50):
        print("Bilangan melebihi angka 50, Silahkan diulangi.")
        continue
    print("Pangkat dua dari bilangan ini adalah: ", bil * bil)
    pilihan = input("Apakah Anda ingin mengulang kembali (y/n)? ")

# Output
Masukkan bilangan dibawah 50: 20
Pangkat dua dari bilangan ini adalah: 400
Apakah Anda ingin mengulang kembali (y/n)? y
Masukkan bilangan dibawah 50: 36
Pangkat dua dari bilangan ini adalah: 1296
Apakah Anda ingin mengulang kembali (y/n)? y
Masukkan bilangan dibawah 50: 70
Bilangan melebihi angka 50, Silahkan diulangi.
Masukkan bilangan dibawah 50: 25
Pangkat dua dari bilangan ini adalah: 625
Apakah Anda ingin mengulang kembali (y/n)? n
```
### 3. Nested Loop (Loop Bersarang)
Bentuk Umum Nested While:
```
While kondisi:
  while kondisi:
    statement(s)
  statement(s)
```

Bentuk Umum Nested For:
```
for variabel in range:
  for variabel in range:
    statement(s)
  statement(s)
```

#### Program Python Menggunakan Nested While Mencetak Bil. Prima antara 1 - 50
```py
# Program Menggunakan Nested While
# Untuk mencetak bilangan prima antara 1 sampai 50

i = 2
while(i < 50):
    j = 2
    while(j <= (i/j)):
        if not(i % j):
            break
        j = j + 1
    if (j > i/j):
        print(i, "adalah Bilangan Prima")
    i = i + 1

print("Terima Kasih")

# Output
2 adalah Bilangan Prima
3 adalah Bilangan Prima
5 adalah Bilangan Prima
7 adalah Bilangan Prima
11 adalah Bilangan Prima
13 adalah Bilangan Prima
17 adalah Bilangan Prima
19 adalah Bilangan Prima
23 adalah Bilangan Prima
29 adalah Bilangan Prima
31 adalah Bilangan Prima
37 adalah Bilangan Prima
41 adalah Bilangan Prima
43 adalah Bilangan Prima
47 adalah Bilangan Prima
Terima Kasih
```

#### Program Python
1. Membuat Program untuk mencetak bilangan genap 1 sampai 10:

```py
for i in range(2,12,2):
    print(i)

# Output
2
4
6
8
10
```

2. Membuat program menjumlahkan Bilangan 1 sampai 10
   
```py
jum = 0
for i in range(10):
    i = i + 1
    print(i)
    jum = jum + i

print("Jumlah Bilangan 1 - 10 adalah: ", jum)

#Output
1
2
3
4
5
6
7
8
9
10
Jumlah Bilangan 1 - 10 adalah: 55
```

3. Membuat program untuk menggambar segitiga siku-siku dengan melakukan masukan bilangan bulat.

**Format Masukan & keluaran:**

Masukan adalah bilangan bulat dengan range : 1 ≤ 𝑁 ≤ 100.

Keluaran program adalah karakter '*' yang menggambarkan pola segitiga siku-siku.

```py
# Meminta input bilangan bulat positif dari pengguna
n = int(input("Masukkan Bilangan Bulat Positif: "))

# Validasi input, pastikan n adalah bilangan bulat positif
if n <= 0:
    print("Masukan tidak valid. Masukkan bilangan bulat positif.")
else:
    # Melakukan perulangan nested for untuk menghasilkan pola siku-siku
    for i in range(0, n):
        for j in range(0, i + 1):
            print('* ', end='')
        print('')  # Pindah ke baris berikutnya setelah setiap baris bintang selesai

# Output
* 
* * 
* * * 
* * * * 
* * * * *
```
