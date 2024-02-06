---
title: "Pemahaman Mendalam tentang Operasi Logika dan Boolean dalam Python"
author_profile: false
excerpt: "Dalam pemrograman, seringkali kita perlu membandingkan nilai-nilai atau mengevaluasi kebenaran suatu kondisi. Python menyediakan operator perbandingan dan operator logika yang memungkinkan kita untuk melakukan tugas-tugas tersebut dengan mudah."
breadcrumbs: true
header:
  teaser: "https://github.com/Julius-Ulee/School-Programs/assets/61336116/5d588504-081b-4da7-8e83-fc3ed7af8736"
  overlay_filter: 0.5
last_modified_at: 2024-02-06T:00:00-01:00
categories:
  - Python
tags:
  - Learn
comments: true
show_date: true
---

# Komparasi dan Logika pada Python
Dalam pemrograman, seringkali kita perlu membandingkan nilai-nilai atau mengevaluasi kebenaran suatu kondisi. Python menyediakan operator perbandingan dan operator logika yang memungkinkan kita untuk melakukan tugas-tugas tersebut dengan mudah.

## 1. Komparasi (Perbandingan)
Komparasi dilakukan untuk membandingkan dua nilai dan menghasilkan nilai kebenaran (True atau False) berdasarkan hubungan antara kedua nilai tersebut.

### Contoh 1: Komparasi Kurang dari dan Lebih dari

```py
inputuser = float(input('Masukan angka yang bernilai \n -- Kurang Dari tiga \n -- Lebih dari sepuluh ='))

# Pengecekan apakah angka kurang dari tiga dengan operator <
cekkurangdari = (inputuser < 3)
print('Angka Kurang dari tiga =', cekkurangdari)

# Pengecekan apakah angka lebih dari 10 dengan operator >
ceklebihdari = (inputuser > 10)
print('Angka Lebih dari sepuluh =', ceklebihdari)
```

## 2. Operator Logika
Operator logika digunakan untuk menggabungkan beberapa kondisi dan menghasilkan nilai kebenaran berdasarkan kondisi-kondisi tersebut.

### Contoh 2: Menggunakan Operator OR

```py
# Pengecekan angka sekaligus 2 variabel agar disatukan (OR)
cekangka = cekkurangdari or ceklebihdari
print('Angka yang dimasukkan adalah =', cekangka)
```

### Contoh 3: Menggunakan Operator AND

```py
inputuser = float(input('Masukan angka yang bernilai \n -- Lebih Dari tiga \n -- Kurang dari sepuluh ='))

# Pengecekan apakah angka lebih dari 3 dengan operator >
lebihtiga = inputuser > 3
print('Angka lebih dari tiga =', lebihtiga)

# Pengecekan apakah angka kurang dari 10 dengan operator <
kurangsepuluh = inputuser < 10
print('Angka Kurang dari sepuluh =', kurangsepuluh)

# Pengecekan angka sekaligus 2 variabel agar disatukan (AND)
cekangka = lebihtiga and kurangsepuluh
print('Angka yang dimasukkan = ', cekangka)
```

# Penutup
Dengan menggunakan operator komparasi dan logika, kita dapat dengan mudah melakukan pengecekan kondisi dan mengontrol alur program dengan tepat sesuai kebutuhan.

**Catatan:** Contoh-contoh di atas disajikan dalam Python 3.x.
