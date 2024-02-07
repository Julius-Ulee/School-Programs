---
title: "Pengenalan Penggunaan List Argument dalam Fungsi Pembuatan HTML"
author_profile: false
excerpt: "Pada materi ini, kita akan mempelajari cara menggunakan list argument dalam fungsi-fungsi pembuatan HTML. List argument memungkinkan kita untuk membuat fungsi yang lebih fleksibel dan dapat menerima sejumlah besar argumen dengan cara yang terstruktur."
breadcrumbs: true
header:
  teaser: "https://github.com/Julius-Ulee/School-Programs/assets/61336116/5d588504-081b-4da7-8e83-fc3ed7af8736"
  overlay_filter: 0.5
last_modified_at: 2024-02-08T:00:00-01:00
categories:
  - Python
tags:
  - Learn
comments: true
show_date: true
---

Pada materi ini, kita akan mempelajari cara menggunakan list argument dalam fungsi-fungsi pembuatan HTML. List argument memungkinkan kita untuk membuat fungsi yang lebih fleksibel dan dapat menerima sejumlah besar argumen dengan cara yang terstruktur.

# Metode Tanpa Atribut

```py
def Buat_html(tag, text):
    buathtml = f"<{tag}>{text}</{tag}>"
    return buathtml
```

Fungsi `Buat_html` mengambil dua argumen: `tag` yang menunjukkan jenis tag HTML yang akan dibuat dan `text` yang merupakan teks di dalam tag tersebut. Fungsi ini kemudian mengembalikan string HTML yang sesuai.

Contoh penggunaan:

```py
html = Buat_html("HTML","This html")
print(html,"\n")

html = Buat_html("Title","Japanese hub")
print(html,"\n")

html = Buat_html("Body","This Body")
print(html,"\n")
```

# Metode dengan Atribut

```py
def Buat_Atribut(tag,text, **atribut):
    html = f"<{tag}"

    for key,value in atribut.items():
        html = html + f" {key}='{value}'"

    html = html + f">{text}</{tag}>"
    return html
```

Fungsi `Buat_Atribut` juga mengambil dua argumen utama: `tag` dan `text`, tetapi juga menerima sejumlah argumen lainnya yang berupa atribut-atribut yang ingin ditambahkan ke tag HTML. Dengan menggunakan `**atribut`, fungsi ini dapat menerima sejumlah besar argumen tambahan tanpa harus menentukan mereka secara eksplisit.

Contoh penggunaan:

```py
html = Buat_Atribut("a1","Header", style="Underline")
print(html,"\n")

html = Buat_Atribut("p","Belajar python sangat asyik",color="#ffff",textstyle="bold")
print(html,"\n")
```

Dengan menggunakan list argument, kita dapat membuat fungsi-fungsi yang lebih serbaguna dan mudah digunakan dalam pembuatan elemen-elemen HTML dengan berbagai atribut.
