---
title: "Cara Lengkap Membuat Paragraf di HTML"
author_profile: false
excerpt: "Setelah belajar tentang apa itu HTML, Tag, Elemen, dan Atribut. Berikutnya, kita akan belajar tentang elemen-elemen dasar pada HTML yang sering digunakan dalam membuat web."
header:
  teaser: "/assets/images/teaser/teaser-html.png"
last_modified_at: 2024-04-14T17:00:02-05:00
breadcrumbs: true
categories:
  - HTML
tags:
  - paragraf
  - web
toc: true
toc_sticky: true
show_date: true
---

<figure class="align-center">
  <img src="{{ site.url }}{{ site.baseurl }}/assets/images/teaser/teaser-html.png" alt="html">
</figure> 

Setelah belajar tentang apa itu HTML, Tag, Elemen, dan Atribut. Berikutnya, kita akan belajar tentang elemen-elemen dasar pada HTML yang sering digunakan dalam membuat web.

Mari kita mulai dengan mengenal elemen paragraf.

**Pada tutorial kali ini, kita akan belajar beberapa tag:**

- `<p>` untuk membuat paragraf;
- `<hr>` untuk membuat garis lurus;
- `<br>` untuk membuat baris baru;
- `<div>` untuk membuat paragraf di luar artikel atau layaout;
- `<pre>` untuk membuat paragraf dengan format yang sudah ditentukan.

# Membuat Paragraf di HTML
Paragraf adalah kumpulan dari beberapa kalimat. Pada web, Paragraf biasanya digunakan untuk menampilkan teks atau artikel.

Paragraf pada HTML dibuat dengan tag `<p>`. Selain tag ini, ada juga tag pendukung lain seperti `<div>`, `<hr>`, `<br>`, dan `<pre>`.

Contoh:
```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <title>Tutorial Paragraf di HTML</title>
    </head>
    <body>
        <p>Ini adalah sebuah paragraf yang berisi beberapa kalimat.
        Saya sedang belajar HTML melalui SPADA UNIKAMA. Saat ini sedang belajar tentang paragraf.</p>
        <p>Paragraf adalah kumpulan dari beberapa kalimat yang saling
        mendukung. Punya ide pokok sebagai dasar dari paragraf itu sendiri.</p>
    </body>
</html>
```

# Atribut untuk Paragraf
Biasanya paragraf ditambahkan dengan beberapa atribut seperti `align`, `id`, `class`, dll.

Contoh:
```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <title>Tutorial Paragraf di HTML #2</title>
    </head>
    <body>
        <p align="center">Ini adalah sebuah paragraf yang berisi beberapa 
        kalimat. Saya sedang belajar HTML di SPADA UNIKAMA. Saat ini Sedang,
        Belajar tentang paragraf.</p>
        <p align="right">Paragraf adalah kumpulan dari beberapa kalimat yang 
        saling mendukung. Paragraf dibuat dengan menentukan ide pokok terlebih
        dahulu. Lalu diikuti dengan kalimat-kalimat pendukung.</p>
    </body>
</html>
```

Atribut `align` merupakan atribut yang digunakan untuk perataan teks pada paragraf. Namun, menurut validator W3C.. penggunaan tag ini sebaiknya diganti dengan CSS.

Mengapa demikian?

Karena atribut `align` dapat merubah tampilan dari web. Ini sebenarnya tigas dari CSS. Tugas utama dari HTML adalah membuat struktur dasar dari web.

Contoh perataan menggunakan CSS:
```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <title>Tutorial Paragraf di HTML #2</title>
    </head>
    <body>
        <p style="text-align: justify">Ini adalah sebuah paragraf yang berisi 
        beberapa kalimat. Saya sedang belajar HTML di SPADA UNIKAMA. Saat ini 
        Sedang, Belajar tentang paragraf.</p>
        <p style="text-align: center">Paragraf adalah kumpulan dari beberapa 
        kalimat yang saling mendukung. Paragraf dibuat dengan menentukan ide 
        pokok terlebih dahulu. Lalu diikuti dengan kalimat-kalimat pendukung.</p>
    </body>
</html>
```

# Tag `<br>` untuk Membuat Paragraf
Tag `<br>` sebenarnya bukanlah tag untuk membuat paragraf. Tapi tag ini, biasanya digunakan untuk membantu tag `<p>`.

Fungsi utama tag `<br>` adalah untuk membuat baris baru.

Contoh:

Misalkan kita ingin menampilkan pantun, bisa saja kita buat seperti ini di dengan tag `<p>`.
```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <title>Tutorial Paragraf di HTML #3</title>
    </head>
    <body>
        <p>Rambut berantakan tak pernah di sisir
           Orang melihat tertawa kesenangan
           Pengangguran berserakan seperti pasir
           Kurang usaha dan keterampilan</p>
    </body>
</html>
```

Meskipun pada kode HTML kita sudah menulis tiap bait pantun dalam baris yang baru. Tapi ia akan tetap ditampilkan seperti baris.

Di sinilah saatnya kita harus menggunakan tag `<br>`. Maka, kode di atas.. bisa kita perbaiki menjadi seperti ini:
```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <title>Tutorial Paragraf di HTML #3</title>
    </head>
    <body>
        <p>Rambut berantakan tak pernah di sisir <br />
           Orang melihat tertawa kesenangan <br />
           Pengangguran berserakan seperti pasir <br />
           Kurang usaha dan keterampilan</p>
    </body>
</html>
```

Oh iya, tag `<br>` adalah tag yang tidak memiliki pasangan penutup. Cara menutupnya, tambahkan saja garis miring seperti ini `<br />`.

Tag `<br>` boleh ditutup, boleh juga tidak. Namun, sebaiknya ditutup agar valid menurut validator W3C.

# Tag `<hr>` untuk Membuat Garis
Sama seperti tag `<br>`, tag `<hr>` juga bukanlah tag untuk membuat paragraf.

Tag `<hr>` merupakan tag yang digunakan untuk membuat garis lurus secara horizontal (horizontal rule). Biasanya digunakan untuk memisahkan beberapa konten atau paragraf.

Contoh:
```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <title>Tutorial Paragraf di HTML</title>
    </head>
    <body>
        <p>Ini adalah sebuah paragraf yang berisi beberapa kalimat.
        Saya sedang belajar HTML di SPADA UNIKAMA. Saat ini Sedang,
        Belajar tentang paragraf.</p>
        <hr />
        <p>Paragraf adalah kumpulan dari beberapa kalimat yang saling
        mendukung. Punya ide pokok sebagai dasar dari paragraf itu sendiri.</p>
    </body>
</html>
```

# Tag `<pre>`
Pada kasus tertentu, kita ingin menampilkan paragraf dengan format yang lebih spesifik. Contohnya seperti pantun dan puisi yang paragrafnya diulis dengan garis baru dan juga indentasi.

Hal ini bisa dilakukan dengan bantuan tag `<br>`. Namun ada juga tag lain yang bisa jadi alternatif, yakni tag `<pre>`.

Tag `<pre>` (preformatting) merupakan tag yang digunakan untuk menampilkan teks atau paragraf dalam format yang sudah kita tentukan di HTML.

Contoh:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Tutorial Paragraf di HTML</title>
</head>
<body>
<h1>Hujan Bulan Juni</h1>
<p>oleh Sapardi Djoko Damono</p>
<pre>
tak ada yang lebih tabah
dari hujan bulan Juni
dirahasiakannya rintik rindunya
kepada pohon berbunga itu

    tak ada yang lebih bijak
    dari hujan bulan Juni
    dihapusnya jejak-jejak kakinya
    yang ragu-ragu di jalan itu

tak ada yang lebih arif
dari hujan bulan Juni
dibiarkannya yang tak terucapkan
diserap akar pohon bunga itu
</pre>
</body>
</html>
```

# Tag `<p>` vs Tag `<div>`
Tag `<p>` dan Tag `<div>`, memiliki perilaku yang hampir sama. Tapi tag `<div>` sebenarnya bukanlah tag untuk membuat paragraf, melainkan tag untuk membuat layout web.

Kadang tag `<div>` sering ‘disalahgunakan’ untuk membuat paragraf.

Contoh:
```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <title>Tutorial Paragraf di HTML</title>
    </head>
    <body>
        <div>Ini adalah sebuah paragraf yang berisi beberapa kalimat.
        Saya sedang belajar HTML di SPADA UNIKAMA. Saat ini Sedang,
        Belajar tentang paragraf.</div>
        <div>Paragraf adalah kumpulan dari beberapa kalimat yang saling
        mendukung. Punya ide pokok sebagai dasar dari paragraf itu sendiri.</div>
    </body>
</html>
```

Ini boleh-boleh, saja. Tapi hasilnya tidak akan sama seperti tag `<p>`.

Paragraf yang dibuat dengan tag `<div>` tidak akan memiliki jarak margin antar paragraf.
Tag `<div>` biasanya digunakan untuk membungkus teks yang ada di luar artikel. Contoh seperti teks pada footer, header, sidebar, dll.

Contoh:
```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <title>Tutorial Paragraf di HTML</title>
    </head>
    <body>
        <p>Ini adalah sebuah paragraf yang berisi beberapa kalimat.
        Saya sedang belajar HTML di SPADA UNIKAMA. Saat ini Sedang,
        Belajar tentang paragraf.</p>
        <p>Paragraf adalah kumpulan dari beberapa kalimat yang saling
        mendukung. Punya ide pokok sebagai dasar dari paragraf itu sendiri.</p>
        <hr />
        <footer>
            <div>&copy; 2020 Belajar HTML by Petani Kode</div>
        </footer>
    </body>
</html>
```
