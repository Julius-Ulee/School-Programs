---
title: "Pemahaman dan Penggunaan Type Data Dictionary (Tuple) dalam Python"
author_profile: false
excerpt: "Python adalah bahasa pemrograman yang memungkinkan penggunaan berbagai tipe data yang beragam untuk memenuhi kebutuhan pengembangan perangkat lunak. Salah satu tipe data yang sering digunakan adalah dictionary."
breadcrumbs: true
header:
  teaser: "https://github.com/Julius-Ulee/School-Programs/assets/61336116/5d588504-081b-4da7-8e83-fc3ed7af8736"
  overlay_filter: 0.5
last_modified_at: 2024-02-07T:00:00-01:00
categories:
  - Python
tags:
  - Learn
comments: true
show_date: true
---

# 1. Pengantar:
Python adalah bahasa pemrograman yang memungkinkan penggunaan berbagai tipe data yang beragam untuk memenuhi kebutuhan pengembangan perangkat lunak. Salah satu tipe data yang sering digunakan adalah dictionary. Dictionary adalah struktur data yang memungkinkan kita untuk menyimpan data dalam bentuk pasangan key-value. Key digunakan untuk mengidentifikasi dan mengakses nilai yang terkait, sedangkan value adalah data yang disimpan. Dictionary sangat berguna dalam menyimpan data yang kompleks dan dapat diakses dengan cepat berdasarkan kunci (key) tertentu.

# 2. Contoh Kode:
Berikut adalah contoh kode yang mengilustrasikan penggunaan dictionary dalam Python:

```py
# Belajar type data dictionary (tuple)

# Inisialisasi dictionary
data = {"Nama": "Agus Kurniawan", "Umur": "20", "Kerjaan": "Chairman of Coconut", "Asal": "Depok"}

# Memasukkan data ke variabel nama dengan memanggil data["Nama"]
nama = data["Nama"]

# Meminta input untuk menambahkan data tambahan
tambah = int(input("\nMasukkan berapa data yang ingin ditambah: "))
for a in range(0, tambah):
    key = str(input("Masukkan key: "))
    value = str(input("Masukkan value: "))
    data[key] = value

# Mengubah data
data["Umur"] = "21"

# Menampilkan key dari data
print("\n--Untuk memunculkan key dari data--")
for key in data:
    print(key)

# Menampilkan key dan value dari data
print("\n--Untuk memunculkan key dan value dari data--")
for key in data:
    value = data[key]
    print(key, " : ", value)

# Menampilkan nilai key value dari data dengan method items
print("\n--Menampilkan nilai key value dari data dengan method items--")
print(data.items())

# Menghapus key value dari data
hapus = str(input("Masukkan Key yang ingin dihapus: "))
del data[hapus]

# Menampilkan key dan value dari data dengan metode tuple
print("\n--Untuk memunculkan key dan value dari data dengan metode tuple--")
for key in data.items():
    print(key[0], " : ", key[1])
```

# 3. Penjelasan Lebih Lanjut:
## a. Inisialisasi Dictionary:
Kita mulai dengan mendefinisikan dictionary yang bernama `data`. Dictionary ini berisi beberapa pasangan key-value yang sudah ditentukan sebelumnya, seperti "Nama", "Umur", "Kerjaan", dan "Asal".

## b. Memasukkan Data Tambahan:
Pengguna diminta untuk memasukkan jumlah data tambahan yang ingin ditambahkan ke dalam dictionary. Selanjutnya, kita menggunakan perulangan `for` untuk mengiterasi sebanyak jumlah data yang dimasukkan oleh pengguna. Setiap iterasi, kita meminta input untuk key dan value dari data tambahan tersebut, kemudian menambahkannya ke dalam dictionary menggunakan syntax `data[key]` = `value`.

## c. Mengubah Data:
Data pada key "Umur" diubah menjadi "21" menggunakan syntax `data["Umur"]` = `"21"`.

## d. Menampilkan Key dari Data:
Key dari dictionary ditampilkan menggunakan perulangan `for` untuk mengiterasi setiap key dalam dictionary `data`.

## e. Menampilkan Key dan Value dari Data:
Menggunakan perulangan `for`, kita menampilkan setiap pasangan key dan value dalam dictionary `data`.

## f. Menampilkan Nilai Key-Value dari Data dengan Method `items()`:
Kita menggunakan method `items()` untuk mendapatkan pasangan key-value dari dictionary `data` dan menampilkannya.

## g. Menghapus Key-Value dari Data:
Pengguna diminta untuk memasukkan key yang ingin dihapus. Kemudian, kita menggunakan keyword `del` untuk menghapus pasangan key-value tersebut dari dictionary.

## h. Menampilkan Key dan Value dari Data dengan Metode Tuple:
Terakhir, kita menggunakan perulangan `for` untuk menampilkan pasangan key dan value dari dictionary dengan metode tuple. Dalam loop, setiap item dalam dictionary diakses sebagai tuple menggunakan method `items()`.
