---
title: "Cara Menambahkan Audio pada HTML"
author_profile: false
excerpt: "HTML audio berfungsi untuk menyematkan file suara dalam halaman web. Yuk, ketahui cara menambahkannya beserta contoh lengkap!"
header:
  teaser: "/assets/images/teaser/teaser-html.png"
last_modified_at: 2023-10-19T17:00:02-05:00
breadcrumbs: true
categories:
  - Articles
tags:
  - Audio
  - HTML
toc: true
toc_sticky: true
show_date: true
---

![image-center](/assets/images/teaser/teaser-html.png){: .align-center}

HTML audio telah merevolusi cara kita berinteraksi dengan konten web, membuka pintu bagi pengalaman multimedia yang lebih dinamis.

Dari menyajikan background musik sampai menyematkan podcast informatif, fitur ini memungkinkan developer berkomunikasi dengan audiens lebih dari sekadar teks dan gambar.

Di artikel ini, kita akan membahas tentang HTML audio. Cari tahu bagaimana kamu bisa memanfaatkan fitur ini untuk mengubah cara audiens berinteraksi dengan website-mu!

# Apa Itu Tag Audio di HTMl?
HTML audio adalah salah satu fitur yang berfungsi untuk menyematkan file suara dalam halaman web. Proses ini dilakukan dengan menggunakan tag < audio > yang diperkenalkan dalam HTML5.

HTML audio membantu dalam menyajikan konten audio seperti musik, wawancara, atau efek suara lainnya langsung dalam browser.

Tak hanya meningkatkan interaksi dan pengalaman pengguna, HTML audio juga membuka peluang kreatif dalam desain web. Dari situs musik sampai platform pendidikan, HTML audio memungkinkan developer menyajikan konten audio secara langsung kepada audiens, membuat website lebih menarik.

# Cara Menambahkan Audio di HTML
Berikut cara menggunakan elemen < audio > di HTML:

- **Pilih file audio yang ingin ditambahkan:** pastikan kamu memiliki file audio yang ingin disematkan dalam format yang didukung oleh browser, seperti MP3, WAV, atau OGG.
- **Tambahkan tag < audio >:** di dalam kode HTML, tambahkan tag < audio > di tempat kamu ingin pemutar audio muncul.
- **Gunakan atribut src untuk menentukan sumber audio:** atribut src dipakai untuk menunjukkan lokasi file audio. Contoh: < audio src= "musik.mp3" >< /audio >.
- **Tambahkan atribut controls jika diperlukan:** jika kamu ingin menampilkan kontrol pemutaran seperti tombol play, pause, dan volume, tambahkan atribut controls. Contoh: < audio src= "musik.mp3" controls>.
- **Sediakan format audio alternatif:** untuk memastikan kompatibilitas lintas browser, tambahkan elemen < source > dengan format audio yang berbeda. Contoh:

```html
<audio controls>
  <source src="musik.mp3" type="audio/mpeg">
  <source src="musik.ogg" type="audio/ogg">
  Browser kamu tidak mendukung tag audio ini.
</audio>
```
- **Uji di berbagai browser:** setelah menambahkan audio, pastikan untuk mengujinya di berbagai browser agar memastikan semua audiens dapat mendengarkannya.
- **Kustomisasi lebih lanjut (Opsional):** kamu juga bisa menambahkan CSS dan JavaScript untuk mengkustomisasi tampilan dan fungsionalitas pemutar audio sesuai keinginan.

# Format Audio yang Didukung
Elemen < audio > di HTML mendukung berbagai format audio yang memungkinkan kamu menyematkan file suara dalam berbagai jenis. Beberapa format audio yang umum didukung oleh elemen ini adalah:

- **MP3 (MPEG Audio Layer III):** format ini sangat populer dan didukung oleh hampir semua browser modern. MP3 menawarkan kompresi yang baik tanpa kehilangan kualitas yang signifikan.
- **WAV (Waveform Audio File Format):** WAV adalah format tanpa kompresi yang menawarkan kualitas suara sangat tinggi. Namun, kekurangan format ini adalah ukuran file-nya bisa sangat besar.
- **OGG (Ogg Vorbis):** OGG adalah format yang menawarkan ukuran file lebih kecil dibandingkan WAV namun tetap memerhatikan kualitas suara. Format ini adalah alternatif yang bagus untuk MP3.

## Pentingnya menyediakan beberapa format audio
Tidak semua browser mendukung setiap format audio. Oleh karena itu, sangat penting untuk menyediakan beberapa format audio berbeda untuk memastikan konten audio dapat diakses semua audiens, terlepas dari browser yang mereka gunakan.

Contohnya, kamu bisa menambahkan beberapa elemen < source > di dalam tag < audio > untuk menyediakan beberapa format audio, seperti ini:

```html
<audio controls>
  <source src="musik.mp3" type="audio/mpeg">
  <source src="musik.ogg" type="audio/ogg">
  Browser kamu tidak mendukung tag audio ini.
</audio>
```

Dengan cara di atas, browser akan memilih format yang didukung agar bisa memutar audionya. Jika tidak ada format yang didukung, akan muncul pesan sesuai yang sudah kamu atur di awal.

# Tambahan Atribut Loop, Mute, dan Autoplay Audio HTML
Selain atribut **src** dan **controls**, ada beberapa atribut lain yang dapat digunakan untuk mengontrol pemutaran audio, yaitu **autoplay**, **loop**, dan **muted**.
- **Atribut autoplay:** atribut ini memungkinkan audio untuk mulai diputar secara otomatis begitu halaman web dimuat. Contoh penggunaannya adalah . Harap diingat bahwa beberapa browser mungkin membatasi atau memblokir **autoplay** untuk menghindari gangguan bagi audiens.

Hal lain yang perlu dipahami adalah **autoplay** hanya bisa digunakan jika audio tersebut diberi property **muted** terlebih dahulu.
- **Atribut loop:** atribut ini membuat audio berulang terus-menerus setelah selesai diputar. Hal ini bisa berguna untuk web yang memiliki background musik atau efek suara berulang. Contoh penggunaannya adalah **< audio src="musik.mp3 " loop>**.
- **Atribut muted:** atribut ini menyebabkan audio dimainkan dalam keadaan bisu. Pilihan ini bisa berguna jika kamu ingin audio dimulai tanpa suara dan memberi audiens pilihan untuk mengaktifkan suaranya. Contoh penggunaannya adalah **< audio src="musik.mp3" muted>** .

Semua atribut di atas dapat digabungkan sesuai kebutuhan, seperti **< audio src="musik.mp3" autoplay loop muted> < /audio>** yang akan memainkan audio secara otomatis, berulang, dan dalam keadaan bisu.

Penggunaan atribut-atribut ini memberi kamu kontrol lebih besar atas bagaimana audio diputar di website. Namun, penting untuk menggunakan atribut-atribut ini dengan bijak dan mempertimbangkan pengalaman pengguna.

# Penutup
HTML audio memberikan kemampuan untuk menyematkan dan mengontrol file audio langsung dalam halaman web.

Melalui penggunaan tag < audio >, berbagai atribut seperti **src**, **controls**, **autoplay**, **loop**, dan **muted**, serta dukungan untuk format audio yang berbeda seperti MP3, WAV, dan OGG, HTML audio menawarkan fleksibilitas dan kontrol yang lebih besar.
