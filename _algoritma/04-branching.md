---
title: "Branching"
permalink: /algoritma/branching/
author_profile: false
excerpt: "Branching adalah membuat cabang dari repositori utama dan melanjutkan melakukan pekerjaan pada cabang yang baru tersebut tanpa perlu khawatir mengacaukan yang utama."
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

# Struktur Branching
Struktur Percabangan dalam pemrograman python, yaitu:
1. Struktur Percabangan if
2. Struktur Percabangan if else
3. Struktur Percabangan if elif else
4. Struktur Percabangan nested if

## 1. Struktur Percabangan if
Struktur percabangan if digunakan untuk satu pilihan keputusan. Jika kondisi True/benar maka statement dikerjakan, Jika kondisi False/salah maka statement tidak dikerjakan.


**Bentuk Umum**
```
if kondisi:
  statement
```

diagram alir if: 

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/80078244-25f5-4b60-b9a2-104ac848da27)

### Contoh kondisi id
Jika Nilai Ujian >= 70, maka cetak "Selamat Anda Lulus Ujian". Penulisan kode program python sbb:

```py
# struktur Percabangan if
Nilai = input('Masukan Nilai Anda: ')
if Nilai >= '70':
print('Selamat Anda Lulus Ujian')

# Output
75
Selamat Anda Lulus Ujian
```
## 2. Struktur Percabangan if else
Percabangan if ... Else akan menyeleksi kondisi jika bernilai True/benar maka statement1 dijalankan, jika kondisi bernilai False/salah maka statement2 dijalankan.

**Bentuk Umum:**
```
if kondisi:
  statement1
else:
  statement2
```

Diagram alir percabangan if else 

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/8540a970-0319-4810-b0d3-3716d2dc9ce6)

### Menentukan Bilangan Genap atau Ganjil
**Soal:** Membuat algoritma untuk menentukan suatu bilangan termasuk bilangan genap atau ganjil.

**Identifikasi Masalah:**

**Input:** Bilangan bulat (integer)

**Output:** Bilangan "Ganjil" atau "Genap".

```
algoritma bilangan_ganjil_genap
Deklarasi
Bil: integer
Ket: string
Begin
  Read (bil)
  If bil mod 2 = 0 then
    ket  ‘genap’
  Else
    ket  ‘ganjil’
  Write (ket)
end
```

Mula-mula diinputkan variabel (bil), misal 5. karena kondisi (bil mod 2 = 0) bernilai salah’, maka variabel ket adalah yang setelah else yaitu ‘ganjil’ sehingga perintah write (ket) nya sebagai output adalah ganjil.

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/7c5b502e-cdf1-4a45-a86a-97a92e01120c)

### Flowchart Bilangan Genap/Ganjil
![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/10b6732e-03f0-4217-aafc-591b3cff020c)

### Contoh Program if Else Menentukan Bilangan Ganjil atau Genap

```py
#struktur Percabangan if ... else
bilangan = int(input('Masukan Sebuah Bilangan: '))
if bilangan % 2 == 0:
    print("Bilangan {} adalah genap.".format(bilangan))
else:
    print("Bilangan {} adalah ganjil .".format(bilangan))
```
```yml
Hasil Running:
Masukan Sebuah Bilangan: 9
Bilangan 9 adalah ganjil.

Masukan Sebuah Bilangan: 6
Bilangan 6 adalah genap.
```

## 3. Struktur Percabangan if elif else
Digunakan untuk menguji lebih dari 2 kondisi, bila kondisi1 benar maka statement1 dikerjakan, bila salah menuju ke kondisi2 . Bila kondisi2 benar maka statement2 dikerjakan, jika salah maka statemen3 dikerjakan.

**Bentuk umum:**
```
if kondisi1:
  statement1
elif kondisi2:
  statement2
else:
  statement3
```

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/e95d562a-91f7-4da7-9381-c2b0c229b82d)

### Contoh Program if elif else
```py
#Struktur Percabangan if ... elif ... else
Nilai = input('Masukan Nilai Akhir : ')
if Nilai >= 80:
  print('Grade = A')
elif Nilai >= 70:
  print('Grade = B')
elif Nilai >= 60:
  print('Grade = C')
elif Nilai >= 40:
  print(Grade = D)
else:
  printf(Grade = E)
```
```yml
Hasil Running:
Masukan Nilai Akhir : 70
Grade = B
>>>

Masukan Nilai Akhir : 90
Grade = A
>>>

Masukan Nilai Akhir : 65
Grade = C
>>> 
```

## 4. Struktur Percabangan Nested if
**Nested if (if bersarang)**

Kondisi nested If adalah suatu konfisi if didalam kondisi if.

**Bentuk umum:**
```
if kondisi1:
  if kondisi 1.1:
    statement 1.1
  elif kondisi 1.2:
    statement 1.2
  else:
    statement 1.3
elif kondisi2:
  if kondisi 2.1:
    statement 2.1
  elif kondisi 2.2:
    statement 2.2
  else:
    statement: 2.3
  else:
    statement3
```

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/6e79b99b-240b-4351-9edb-7e60c3dc0e16)

### Contoh Program Nested if
```py
# Struktur Percabangan Nested If
# Merk Baju Polo/Alisan/StYess
Merk = input('Merk Baju P/A/S: ')

if Merk == 'P':
    print('Merk Polo')
    ukuran = input('Ukuran L/M/S: ')
    if ukuran == 'L':
        print('Harga = 300000')
    elif ukuran == 'M':
        print('Harga = 225000')
    else:
        print('Harga = 175000')
elif Merk == 'A':
    print('Merk Alisan')
    ukuran = input('Ukuran L/M/S: ')
    if ukuran == 'L':
        print('Harga = 275000')
    elif ukuran == 'M':
        print('Harga = 200000')
    else:
        print('Harga = 150000')
elif Merk == 'S':
    print('Merk StYess')
    ukuran = input('Ukuran L/M/S: ')
    if ukuran == 'L':
        print('Harga 250000')
    elif ukuran == 'M':
        print('Harga = 175000')
    else:
        print('Harga = 125000')
else:
    print('Merk tidak valid')

```
```yml
Hasil Running:
Merk Baju P/A/S: P
Merk Polo
Ukuran L/M/S: L
Harga = 300000
Merk Baju P/A/S: A
Merk Alisan
Ukuran L/M/S: S
Harga = 150000
```

**Note:** Merk Baju dan Ukuran di input dengan Huruf Besar.
{: .notice--info}
