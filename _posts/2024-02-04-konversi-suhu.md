---
title: "Konversi Suhu dengan Python"
author_profile: false
excerpt: "Program ini digunakan untuk melakukan konversi suhu antara beberapa satuan suhu, yaitu Celcius, Reamur, Farenheit, dan Kelvin."
breadcrumbs: true
header:
  teaser: "https://github.com/Julius-Ulee/School-Programs/assets/61336116/5d588504-081b-4da7-8e83-fc3ed7af8736"
  overlay_filter: 0.5
last_modified_at: 2024-02-04T:00:00-01:00
categories:
  - Python
tags:
  - Learn
comments: true
show_date: true
---

# Pendahuluan
Program ini digunakan untuk melakukan konversi suhu antara beberapa satuan suhu, yaitu Celcius, Reamur, Farenheit, dan Kelvin.

# Input dan Output
- Program akan meminta pengguna untuk memasukkan suhu dalam satuan Celcius, Reamur, Farenheit, atau Kelvin, tergantung pada pilihan pengguna.
- Setelah menerima input, program akan menghitung dan menampilkan hasil konversi ke tiga satuan suhu lainnya.
  
# Konversi Celcius
```py
celcius = float(input('Masukan Celcius = '))
reamur = (4/5) * celcius
kelvin = celcius + 273
farenheit = (9/5) * celcius + 32
```

# Konversi Reamur
```py
input_reamur = float(input('Masukan Reamur = '))
r_celcius = (5/4) * input_reamur
r_kelvin = kelvin * (5/4) * input_reamur + 273
r_farenheit = (9/4) * input_reamur + 32
```

# Konversi Farenheit
```py
input_farenheit = float(input('Masukan Farenheit = '))
f_celcius = 5/9 * (input_farenheit - 32)
f_reamur = 4/9 * (input_farenheit - 32)
f_kelvin = 5/9 * (input_farenheit - 32) + 273
```

# Konversi Kelvin
```py
input_kelvin = float(input('Masukan Kelvin = '))
k_celcius = input_kelvin - 273
k_reamur = 4/5 * (input_kelvin - 273)
k_farenheit = 9/5 * (input_kelvin - 273) + 32
```

# Output Hasil Konversi
Setelah menghitung, program akan menampilkan hasil konversi ke layar.

# Penutup
Program diakhiri dengan menampilkan informasi pembuat program.

# Penambahan Informasi Pembuat
```py
print('-----------------------------------------')
print('-----------------from--------------------')
print('-------------- me Ulee ------------------')
```

**Catatan:** Pastikan untuk menjalankan program ini pada lingkungan Python yang sesuai.
