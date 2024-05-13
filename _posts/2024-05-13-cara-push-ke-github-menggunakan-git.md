---
title: "Cara Push Project ke Github Mengunakaan GIT"
author_profile: false
excerpt: "Pada tulisan ini kita akan belajar bagaimana caranya mengupload (push) project ke Github."
header:
  teaser: "https://github.com/Julius-Ulee/School-Programs/assets/61336116/5dfbbb25-f3de-4923-b4f8-bf67e55bd37d"
last_modified_at: 2024-05-13T17:00:02-05:00
breadcrumbs: true
categories:
  - Software
tags:
  - GIT
  - Github
toc: true
toc_sticky: true
show_date: true
---

<figure class="align-center">
  <img src="https://github.com/Julius-Ulee/School-Programs/assets/61336116/5dfbbb25-f3de-4923-b4f8-bf67e55bd37d">
</figure> 

Pada tulisan ini kita akan belajar bagaimana caranya mengupload (push) project ke Github.

> Bagi yang belum install Git silahkan install terlebih dahulu, untuk tutorialnya silahkan cek [link](https://schoolprograms.my.id/software/cara-install-git-diwindows-serta-konfigurasi/) berikut untuk cara instalasinya.

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/4943ef51-9479-4501-85f3-83436cc7f068)

# Membuat Repository GitHub
Kita perlu membuat respository di GitHub untuk menyimpan source code secara online.

- Buka [Github](https://github.com)

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/3b00511a-6cf8-4a29-857a-10fc8056891f)

- Buat repository baru dengan cara Klik tombol new disebelah kiri.

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/76dec9e9-ba82-43aa-9848-d5cf0b0ac407)

- Buat nama repository baru. Misal `praktikum-ci`. Selanjutnya isi bagian lain jika diperlukan. Jika sudah klik tombol Create Repository.

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/fdadfec2-a017-4a74-9791-05fcc185ad52)

# Inisialisasi Git (git init)
Kita perlu melakukan melakukan inisialisasi git di local.

Silahkan buka folder project yang ingin diinisiasi git. Contoh di bawah ini ingin diinisialisasi pada project blog codeigniter.

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/6eb94e4c-64a9-441d-9475-c7d423078441)

Buka terminal di project tersebut:

- Windows: klik kanan — pilih `Git Bash Here`

- Linux: klik kanan — pilih `open terminal here`. Atau bisa berpindah ke direktori project menggunakan perintah cd.

Inisialisasi git dengan menjalankan perintah:

- `git init`

# Menambahkan Perubahan ke Staging Area (git add)
Pada langkah ini, silahkan kerjakan projek, tugas, atau perubahan apapun.

Jika sudah selesai, selanjutnya kita perlu menambahkan perubahan ke staging area.

Kita bisa menambahkan setiap perubahan ke staging area, kemudian melakukan commit pada setiap perubahan (atomic commit). Atau kita bisa menambahkan semua perubahan ke staging area, kemudian langsung melakukan commit.

Buka terminal di project, sama seperti yang dilakukan pada tahapan inisialisasi git (lihat kembali langkahnya pada bagian inisialisasi git).

Kita coba untuk menambahkan semua perubahan ke staging area:

- `git add .`

> Tanda titik di sini artinya ingin menambahkan semua perubahan ke staging area. Tanda titik sama seperti tanda bintang. Tanda bintang berarti seluruh file. Artinya kita ingin menambahkan semua file ke staging area

# Menyimpan Perubahan (git commit)
Setelah kita menambahkan perubahan ke staging area, langkah terakhir adalah menyimpan perubahan. Hal ini sama seperti ketika kita sudah memasukan barang ke lemari, langkah selanjutnya adalah menguncinya atau menutupnya untuk disimpan.

Jika tidak melanjutkan dari tahapan sebelumnya, silahkan buka terminal pada folder project. Langkah yang dilakukan sama seperti di tahapan inisialisasi git.

Menyimpan perubahan:

- `git commit -m “pesan commit atau perubahan”`

Pada pesan commit, silahkan isi pesan yang mewakili pekerjaan yang dilakukan. Misal menambahkan fitur login, membuat modul tambah data untuk user, menghapus fungsi update, dll.


# Menambahkan Link Remote (git remote)
Kita belum menghubungkan project local dengan repository di github.

Kita akan menambahkan link repository ke project local agar project local dan repository github tersambung.

Buka repository github. Copy link repository (jangan lupa tambahkan .git di akhir url). Contoh: https://github.com/aufaroot18/praktikum-ci.git

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/91c2abaf-6bcb-4cbf-821a-ae12055fadc2)

Menambahkan link remote:

- git remote add origin https://github.com/aufaroot18/praktikum-ci.git

Kita menambahkan remote dengan nama origin, link-nya adalah https://github.com/aufaroot18/praktikum-ci.git

# Mengirim Perubahan ke Repository Github (git push)
Langkah terakhir adalah mengirim (upload/push) perubahan ke repository github.

Pada tahapan ini, kita akan mengirimkan kode project yang ada di local (laptop atau komputer) ke online yang ada di repository github.

Mengirim perubahan ke Repository Github:

- `git push origin main`

Kita ingin mengirim perubahan ke origin (nama remote yang sudah kita buat pada tahapan sebelumnya) di branch main (utama).

Jika terdapat error karena branch main, silahkan push ke branch master:

- `git push origin master`

Selanjutnya silahkan refresh repository github, dan project yang ada di local sudah terupload ke repository github.

Selesai, terima kasih.
