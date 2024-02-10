---
title: "Pengelolaan Data dengan Python Menggunakan Perulangan (Loop)"
author_profile: false
excerpt: "Program ini memperlihatkan cara mengelola data menggunakan Python dengan bantuan perulangan (loop). Dalam program ini, Anda dapat melakukan operasi seperti menampilkan data, menambah data baru, mengedit data yang sudah ada, menghapus data, dan mencari data tertentu dalam list."
breadcrumbs: true
header:
  teaser: "https://github.com/Julius-Ulee/School-Programs/assets/61336116/5d588504-081b-4da7-8e83-fc3ed7af8736"
  overlay_filter: 0.5
last_modified_at: 2024-02-10T:00:00-01:00
categories:
  - Python
tags:
  - Learn
toc: true
toc_sticky: true
comments: true
show_date: true
---

# Pendahuluan
Program ini memperlihatkan cara mengelola data menggunakan Python dengan bantuan perulangan (loop). Dalam program ini, Anda dapat melakukan operasi seperti menampilkan data, menambah data baru, mengedit data yang sudah ada, menghapus data, dan mencari data tertentu dalam list.

# Materi
## 1. Inisialisasi Data Awal:
- Program dimulai dengan inisialisasi data awal yang disimpan dalam bentuk list Python.

```py
nama = ["Agus kurniawan","Andri","Karmila","Sari ulfa","Wahid","Subhan sidiq","Hartina"]
```

## 2. Menampilkan Data:
- Untuk menampilkan data, program menggunakan perulangan for loop untuk mencetak setiap elemen dalam list.

```py
for a in range(0,len(nama)):
    print("Nama : ",nama[a])
```

## 3. Menambah Data:
- Pengguna diminta untuk memasukkan berapa banyak data yang ingin ditambahkan.
- Setelah itu, program menggunakan perulangan for loop untuk meminta input nama sejumlah data yang diinginkan, dan menambahkannya ke list nama.

```py
for b in range(0,berapa_data):
    input_data = str(input(" -- Masukan nama : "))
    nama.append(input_data)
```

## 4. Mengedit Data:
- Pengguna diminta untuk memilih indeks data yang ingin diedit.
- Kemudian pengguna diminta untuk memasukkan nama baru.
- Program kemudian mengganti data lama dengan data baru menggunakan indeks yang dipilih.

```py
index = int(input("\n -- Index ke berapa yang ingin di edit : "))
edit = str(input(" -- Masukkan nama baru : "))
nama[index] = edit
```

## 5. Menghapus Data:
- Pengguna diminta untuk memasukkan nama yang ingin dihapus.
- Program kemudian menggunakan metode remove() untuk menghapus nama tersebut dari list.

```py
index = str(input(" -- Masukan nama yang ingin di hapus : "))
nama.remove(index)
```

## 6. Mencari Data:
- Pengguna diminta untuk memasukkan indeks data yang ingin dicari.
- Program kemudian mencetak nama yang sesuai dengan indeks yang dimasukkan pengguna, jika ditemukan.

```py
if nama[cari]:
    print(" -- Nama nya adalah : ",nama[cari])
else:
    print(" -- Index tidak di dapat")
```

### Contoh:

```py
print("\n -- Program Data Struchture -- \n")

# menginilialisasi variabel list di python
nama = ["Agus kurniawan","Andri","Karmila","Sari ulfa","Wahid","Subhan sidiq","Hartina"]

print(" --1 Menampilkan Data -- ")
print(" --2 Menambah Data -- ")
print(" --3 Mengedit Data -- ")
print(" --4 Menghapus Data -- ")
print(" --5 Mencari Data -- \n")

program = str(input(" -- Masukan nomor : "))

if program == "1":
    print("\n -- Menampilkan Data -- ")
    
    # Program ini me looping data sehingga tampilannya agak kelihatan rapi dan tidak berformat JSON
    for a in range(0,len(nama)):
        print("Nama : ",nama[a])

elif program == "2":
    print("\n -- Menambah Data -- ")

    berapa_data = int(input(" -- Berapa banyak data yang ingin di tambah : "))

    # Program akan looping sesuai berapa banyak data yang ingin di tambah
    for b in range(0,berapa_data):
        input_data = str(input(" -- Masukan nama : "))
        nama.append(input_data)

    # lalu memunculkannya kembali
    for a in range(0,len(nama)):
        print(" -- Nama : ",nama[a])

elif program == "3":
    print("\n -- Mengedit Data -- ")
    print(" -- ",nama," -- ")

    index = int(input("\n -- Index ke berapa yang ingin di edit : "))
    edit = str(input(" -- Masukkan nama baru : "))

    nama[index] = edit

    # lalu memunculkannya kembali
    for a in range(0,len(nama)):
        print(" -- Nama : ",nama[a])

elif program == "4":
    print("\n -- Menghapus Data -- ")
    print(" -- ",nama," -- \n")
    index = str(input(" -- Masukan nama yang ingin di hapus : "))
    nama.remove(index)
    
    # lalu memunculkannya kembali
    for a in range(0,len(nama)):
        print(a," -- Nama : ",nama[a])

elif program == "5":
    print("\n -- Mencari Data -- ")
    print(" -- ",nama," -- \n")

    cari = int(input(" -- Masukan index untuk mencari data : "))

    if nama[cari]:
        print(" -- Nama nya adalah : ",nama[cari])
    else:
        print(" -- Index tidak di dapat")

else:
    print(" -- Program Keluar -- ")
```

### Kesimpulan:
Program ini memberikan pengalaman praktis dalam menggunakan Python untuk mengelola data menggunakan perulangan (loop). Dengan program ini, Anda dapat dengan mudah menambah, mengedit, menghapus, dan mencari data dalam list Python.
