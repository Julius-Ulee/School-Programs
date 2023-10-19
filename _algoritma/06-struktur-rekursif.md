---
title: "Struktur Rekursif"
permalink: /algoritma/struktur-rekursif/
author_profile: false
excerpt: "Rekursif adalah suatu proses dari suatu subprogram yang dapat berupa fungsi atau prosedur yang memanggil dirinya sendiri."
show_date: true
header:
  overlay_image: /assets/images/header/logika-dan-algoritma.jpeg
  overlay_filter: 0.5
last_modified_at: 2023-10-16T17:00:00-01:00
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

10<sup>0</sup> = 1 ................................................ (1)  
10<sup>n</sup> 10 * 10<sup>n-1</sup> .............................. (2)

Contoh:  
10<sup>3</sup> = 10 * 10<sup>2</sup>  
  10<sup>2</sup> = 10 * 10<sup>1</sup>  
    10<sup>1</sup> = 10 * 10<sup>0</sup>  
      10<sup>0</sup> = 1

## Program Fungsi Pangkat
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

- Fungsi pangkat akan memanggil dirinya sendiri, yaitu setiap nilai x dan y di input akan dikirim ke fungsi pangkat() melalui parameter variabel x dan y.
- Selama nilai y bukan 0 maka fungsi pangkat() akan terus memanggil dirinya sendiri, dan nilai y akan selalu berkurang 1 (y-1) sampai kondisi terpenuhi dan perulangan dihentikan

# Faktorial
0! = 1  
N! = N x (N-1)! Untuk N > 0

Secara notasi pemrograman dapat ditulis sebagai :  
FAKT (0) = 1 .............................................. (1)  
FAKT(N) = N * FAKT (N-1) .................................. (2)  

Contoh:  
FAKT(5) = 5 * FAKT(4)  
FAKT(4) = 4 * FAKT(3)  
FAKT(3) = 3 * FAKT(2)  
FAKT(2) = 2 * FAKT(1)  
FAKT(1) = 1 * FAKT(0)  

## Perhitungan Faktorial Secara Rekursif
Hitung 5!, maka dapat dilakukan secara rekursif dengan cara : 5! = 5 * 4!

Secara rekursif nilai dari 4! Dapat dihitung kembali dengan 4 * 3!, sehingga 5! Menjadi : 5! = 5 * 4 * 3!

Secara rekursif nilai dari 3! Dapat dihitung kembali dengan 3 * 2!, sehingga 5! Menjadi : 5! = 5 * 4 * 3 * 2!

Secara rekursif nilai dari 2! Dapat dihitung kembali dengan 2 * 1, sehingga 5! Menjadi : 5! = 5 * 4 * 3 * 2 * 1 = 120.

## Program Faktorial
```py
# Fungsi Pangkat secara Rekursif
def faktorial(a):
    if a == 1:
        return a
    else:
        return a * faktorial(a - 1)

bil = int(input("Masukkan Bilangan: "))
print("%d! = %d" % (bil, faktorial(bil)))

# Output
Masukkan Bilangan : 5
5! = 120

Masukkan Bilangan : 6
6! = 720
```

## Fungsi Faktorial
- Fungsi Faktorial adalah fungsi rekursif karena memanggil fungsinya sendiri.
- Pada saat dijalankan program akan meminta "memasukkan bilangan" pada variabel bil, kemudian bilangan tersebut akan dikirim ke fungsi faktorial() lewat parameter a.
- Selama nilai a tidak sama dengan 1 maka fungsi faktorial akan terus memanggil dirinya sendiri. Perulangan akan berhenti ketika nilai =1

# Fibonancy
Deret Fibonancy : 0,1,1,2,3,5,8,13,.........

Secara notasi pemrograman dapat ditulis sebagai :  
Fibo (1) = 0 & Fibo (2) = 1 ........................................ (1)  
Fibo (N) = Fibo (N-1) + Fibo (N-2) ................................. (2)  

Contoh:  
Fibo(5) = Fibo(4) + Fibo(3)  
Fibo(4) = Fibo(3) + Fibo(2)  
Fibo(3) = Fibo(2) + Fibo(1)  

## Program Deret Fibonancy
```py
def fibonacci(n):
    if n == 0 or n == 1:
        return n
    else:
        return fibonacci(n - 1) + fibonacci(n - 2)

x = int(input("Masukkan Batas Deret Bilangan Fibonacci: "))
print("Deret Fibonacci:")
for i in range(x):
    print(fibonacci(i), end=' ')

# Output
Masukan Batas Deret Bilangan
Fibonacci : 5
Deret Fibonacci
0 1 1 2 3

Masukan Batas Deret Bilangan
Fibonacci : 8
Deret Fibonacci
0 1 1 2 3 5 8 13
```

## Fungsi Fibonancy
- Fungsi fibonancy merupakan fungsi rekursif yang memanggil dirinya sendiri.
- Bilangan fibonancy adalah bilangan yang memiliki suku awal 0 dan 1, dan suku berikutnya adalah penjumlahan dari dua suku sebelumnya.
- Fungsi fibonancy akan terus memanggil dirinya ketika (nilai n) bukan bernilai 0 atau 1 dengan melakukan proses penjumlahan (fibonacci(n-1) + fibonacci(n-2))

# Konsep Menara Hanoi

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/f3244951-ad5c-478f-a868-f5a32be55da3)

- Jika n=1, maka langsung pindahkan saja piringan dari tiang A ke tiang C & selesai.
- Pindahkan n-1 piringan yg paling atas dari tiang A ke tiang B.
- Pindahkan piringan ke n (piringan terakhir) dari tiang A ke tiang C
- Pindahkan n-1 piringan dari tiang B ke tiang C

Langkah pemindahan tersebut diatas dapat diubah dengan notasi sebagai berikut:

**Menara (n,asal,bantu,tujuan)**

- Untuk jumlah piringan n>1 dapat dibagi menjadi 3 notasi penyelesaian
- Menara (n-1, Asal,Tujuan, Bantu);
- Menara (n, Asal, Bantu, Tujuan); atau Asal -> Tujuan;
- Menara (n-1, Bantu, Asal, Tujuan);

## Langkah-Langkah Pemindahan Piringan
1. **MENARA(1, A, C, B)**  
Pindahkan cakram dari tiang A ke tiang B: A → B

2. **MENARA(2, A, B, C)**  
Pindahkan dua cakram dari tiang A ke tiang C: A → C  
Pindahkan satu cakram dari tiang A ke tiang B: A → B  

3. **MENARA(1, B, A, C)**  
Pindahkan cakram dari tiang B ke tiang C: B → C

4. **MENARA(3, A, C, B)**  
Pindahkan tiga cakram dari tiang A ke tiang B: A → B  
Pindahkan satu cakram dari tiang A ke tiang C: A → C  
Pindahkan dua cakram dari tiang A ke tiang B: A → B  

5. **MENARA(1, C, B, A)**  
Pindahkan cakram dari tiang C ke tiang A: C → A

6. **MENARA(2, C, A, B)**  
Pindahkan dua cakram dari tiang C ke tiang B: C → B  
Pindahkan satu cakram dari tiang C ke tiang A: C → A

7. **MENARA(1, A, C, B)**  
Pindahkan cakram dari tiang A ke tiang B: A → B

8. **MENARA(1, A, C, B)**  
Pindahkan satu cakram dari tiang A ke tiang C: A → C

9. **MENARA(4, A, B, C)**  
Pindahkan empat cakram dari tiang A ke tiang B: A → B  
Pindahkan satu cakram dari tiang B ke tiang C: B → C  
Pindahkan dua cakram dari tiang B ke tiang A: B → A  
Pindahkan satu cakram dari tiang C ke tiang B: C → B  
Pindahkan tiga cakram dari tiang A ke tiang C: A → C  
Pindahkan satu cakram dari tiang A ke tiang B: A → B  
Pindahkan dua cakram dari tiang A ke tiang C: A → C  
Pindahkan satu cakram dari tiang B ke tiang A: B → A  
Pindahkan satu cakram dari tiang B ke tiang C: B → C  
Pindahkan satu cakram dari tiang A ke tiang B: A → B  
Pindahkan satu cakram dari tiang C ke tiang A: C → A  

10. **MENARA(1, B, A, C)**  
Pindahkan cakram dari tiang B ke tiang C: B → C

Ilustrasi diatas menghasilkan 15 langkah penyelesaian dari permasalahan konsep menara Hanoi dengan jumlah piringan sebanyak 4 buah 18

Untuk Video konsep menara hanoi dapat dilihat pada:  
[Link](https://www.mathsisfun.com/games/towerofhanoi.html)

**Rumus Langkah Pemindahan :**  
2<sub>N</sub> - 1  
**N = Jumlah Piringan**
