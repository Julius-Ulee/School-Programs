---
title: "Cara Membuat Garis di HTML"
author_profile: false
excerpt: "Dalam melakukan desain web, kami seringkali membutuhkan garis untuk memisahkan konten, menambahkan estetika, atau memberikan fokus pada elemen tertentu. HTML menyediakan tag sederhana yang dapat digunakan untuk menggambar garis. Tutorial ini akan membantu kamu memahami bagaimana membuat garis di HTML."
header:
  teaser: "/assets/images/teaser/teaser-html.png"
last_modified_at: 2023-10-20T05:00:02-05:00
breadcrumbs: true
categories:
  - Learn
tags:
  - HTML
toc: true
toc_sticky: true
show_date: true
---

Dalam melakukan desain web, kami seringkali membutuhkan garis untuk memisahkan konten, menambahkan estetika, atau memberikan fokus pada elemen tertentu. HTML menyediakan tag sederhana yang dapat digunakan untuk menggambar garis. Tutorial ini akan membantu kamu memahami bagaimana membuat garis di HTML.

Jangan khawatir jika kamu baru dalam pemrograman web. Panduan ini ditulis dalam bahasa yang mudah dipahami dan dapat langsung diaplikasikan. Yuk, langsung saja kita mulai!

# Tag `<hr>`

Untuk membuat garis horizontal di HTML, kamu dapat menggunakan tag `<hr>`. Tag `<hr>` atau horizontal rule adalah tag HTML yang digunakan untuk menampilkan garis horisontal pada halaman web. Contoh penggunaan tag `<hr>` adalah sebagai berikut:

```html
<p>Paragraf di atas garis</p>
<hr>
<p>Paragraf di bawah garis</p>
```

Dalam contoh di atas, tag `<hr>` digunakan untuk memisahkan dua paragraf. Hal ini sangat berguna jika kamu ingin memisahkan konten atau menambahkan space antara dua elemen.

Kamu juga bisa menyesuaikan tinggi dan lebar garis dengan menambahkan atribut `width` dan `height` pada tag `<hr>`.

```html
<hr width="50%" height="2px">
```

# Membuat Garis Vertikal
Membuat garis vertikal di HTML sedikit lebih rumit karena tidak ada tag HTML khusus untuk garis vertikal. Tapi jangan khawatir, kamu dapat mencapainya dengan HTML dan CSS.

Berikut ini cara membuat garis vertikal menggunakan HTML dan CSS:

```html
<div style="border-left: 1px solid black; height: 500px;"></div>
```

Pada contoh di atas, kita menggunakan `div` dengan style border-left dan tinggi tertentu untuk membuat garis vertikal. Border-left dengan nilai 1px dan solid black membuat garis vertikal berwarna hitam dengan lebar 1px. Dan height 500px adalah tinggi dari garis vertikal tersebut.

# Kesimpulan
Membuat garis di HTML baik itu garis horizontal atau vertikal sebenarnya sangat mudah. Kamu hanya perlu memahami penggunaan tag dan style CSS yang tepat. Jangan takut untuk eksperimen dengan atribut dan nilai yang berbeda untuk mendapatkan hasil yang diinginkan. Selamat mencoba!
