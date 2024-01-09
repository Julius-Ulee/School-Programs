---
title: "Cara Install GIT dan Konfigurasi Awal di Windows"
author_profile: false
excerpt: "Git adalah perangkat lunak yang digunakan untuk mengelola versi source code program. Git merupakan kepanjangan dari Group Inclusive Tour."
breadcrumbs: true
header:
  teaser: "https://github.com/Julius-Ulee/School-Programs/assets/61336116/5a30a928-0ced-4c67-8b09-8e3519905cf4"
last_modified_at: 2024-01-08T:00:00-01:00
categories:
  - Software
tags:
  - GIT
  - Installation
  - Konfigurasi
toc: true
toc_sticky: true
comments: true
show_date: true
---

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/24cbeba4-6433-4449-8410-755acf187f0e)

# Pengertian GIT
Git adalah sebuah version control system yang digunakan oleh para developer untuk mengembangkan software secara bersamaan. Fungsi utama dari Git adalah mengatur versi source code program dengan memberikan tanda baris serta code mana yang perlu ditambah ataupun diganti.

# Download Git
Silahkan buka website resminya Git ([git-scm.com](https://git-scm.com/)). Kemudian unduh Git sesuai dengan arsitektur komputer kita. Kalau menggunakan 64bit, unduh yang 64bit. Begitu juga kalau menggunakan 32bit.

# Langkah-langkah Install Git di Windows
Baiklah, mari kita mulai ritual instalnya. Silahkan klik 2x file instaler Git yang sudah diunduh.

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/83eb8306-5b88-4582-82a2-2132c4b260a8)

Maka akan muncul infomasi lisensi Git, klik Next > untuk melanjutkan.

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/33469c5f-b68e-4c19-98cc-9a223c53b904)

Selanjutnya menentukan lokasi instalasi. Biarkan saja apa adanya, kemudian klik Next >.

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/a7837b6d-e96b-4fae-8bfd-57e1fbea65c8)

Selanjutnya pemilihan komoponen, biarkan saja seperti ini kemudian klik Next >.

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/de0e4e8c-b56e-4fb5-a3f8-00be3e69957b)

Selanjutnya pemlilihan direktori start menu, klik Next >.

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/5a61b987-4617-4a19-93ff-dc4e25ed5511)

Selanjutnya pengaturan PATH Environment. Pilih yang tengah agar perintah `git` dapat di kenali di Command Prompt (CMD). Setelah itu klik Next >.

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/118f14c3-28ac-4cd5-8e99-0e49a1ef5409)

Selanjutnya konversi line ending. Biarkan saja seperti ini, kemudian klik Next >.

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/15f6410e-1a79-49b8-98b7-6b0f3966fd07)

Selanjutnya pemilihan emulator terminal. Pilih saja yang bawah, kemudian klik Next >.

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/4ab1b032-3603-4700-9b4a-567a7455d903)

Selanjutnya pemilihan opsi ekstra. Klik saja Next >.

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/75183986-4303-487e-81f9-84a0afec0473)

Selanjutnya pemilihan opsi ekspreimental, langsung saja klik Install untuk memaulai instalasi.

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/7106a944-1ac7-4611-827d-12a493f3485d)

Tunggu beberapa saat, instalasi sedang dilakukan.

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/0afaba16-989d-4790-ae27-5b49a389085e)

Setelah selesai, kita bisa langsung klik Finish.

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/c72f956d-6d49-460a-9efc-accfde6d8d79)

Selamat, Git sudah terinstal di Windows. Untuk mencobanya, silahkan buka CMD atau PowerShell, kemudian ketik perintah `git --version`.

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/9273b20e-bc29-4b68-86f2-36ac2062d458)

# Konfigurasi Awal yang Harus Dilakukan
Ada beberapa konfigurasi yang harus dilakukan sebelum mulai menggunakan Git, seperti menentukan name dan email.

Silahkan lakukan konfigurasi dengan perintah berikut ini.

```
git config --global user.name "Julius-Ulee"
git config --global user.email fidzlieazriel@gmail.com
```

Kemudian periksa konfigurasinya dengan perintah:

```
git config --list
```

Apabila berhasil tampil seperti gambar berikut ini, berarti konfigurasi berhasil.

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/c8f0d382-985c-4cc9-bb7a-af9449e7dc96)

Konfigurasi `core.editor` bersifat opsional. Sedangkan name dan email wajib.

Jika kamu memiliki akun Github, Gitlab, Bitbucket atau yang lainnya…

maka username dan email harus mengikuti akun tersebut agar mudah diintegrasikan.
