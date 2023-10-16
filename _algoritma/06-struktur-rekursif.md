---
title: "Struktur Rekursif"
permalink: /algoritma/struktur-rekursif/
author_profile: false
excerpt: "Rekursif adalah suatu proses dari suatu subprogram yang dapat berupa fungsi atau prosedur yang memanggil dirinya sendiri."
show_date: true
last_modified_at: 2023-10-16T17:00:00-01:00
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

**Rekursif** adalah suatu proses yang bisa memanggil dirinya sendiri.

*Contoh konsep penggunaan Rekursif*  
**Masalah** : Memotong Roti tawar tipis-tipis sampai habis  
**Algoritma** :
1. Jika roti sudah habis atau potongannya sudah paling tipis maka pemotongan roti selesai.
2. Jika roti masih bisa dipotong, potong tipis dari tepi rotitersebut, lalu lakukan prosedur 1 dan 2 untuk sisapotongannya.

# Contoh Fungsi Rekursif
1. Fungsi pangkat
2. Faktorial
3. Fibonancy
4. Menara Hanoi

# Fungsi Pangkat
Menghitung 10 pangkat n dengan menggunakan konsep rekursif.

Secara Notasi pemrograman dapat ditulis :

10<sup>0</sup> = 1 .............................. (1)  
10<sup>n</sup> 10 * 10<sup>n-1</sup> .............................. (2)

Contoh:  
10<sup>3</sup> = 10 * 10<sup>2</sup>  
  10<sup>2</sup> = 10 * 10<sup>1</sup>  
    10<sup>1</sup> = 10 * 10<sup>0</sup>  
      10<sup>0</sup> = 1

# Fungsi Pangkat
```py
# Fungsi Pangkat Secara Rekursif
def pangkat(x, y):
    if y == 0:
        return 1
    else:
        return x * pangkat(x, y - 1)

x = int(input("Masukkan Nilai X: "))
y = int(input("Masukkan Nilai Y: "))
print("%d dipangkatkan %d = %d" % (x, y, pangkat(x, y)))

# Output
Masukkan Nilai X: 10
Masukkan Nilai Y: 3
10 dipangkatkan 3 = 1000
```
