---
title: "Cara Mendaftarkan Domain ke hstspreload.org"
date: 2021-05-31T00:30:13+07:00
description: "Cara Mendaftarkan Domain ke HSTS Preload"
categories: ["Tutorial"]
tags: ["Tutorial"]
keywords:
  [
    "HSTS",
    "HSTS Preload",
    "Daftar Domain ke HSTS Preload",
    "Daftar Domain ke HSTS Preload Wordpress",
    "Daftar Domain ke HSTS Preload Hugo",
    "Daftar Domain ke HSTS Preload Blog",
  ]
description: 'Cara yang akan share disini cukup ribet, kalian sampai harus restart Desktop/Laptop-nya dua kali, tetapi cara ini paling aman dari razia, karena saya sudah hampir pakai 2 bulan database ESET nya masih bisa update, walaupun kalian tidak bisa mengganti product ESET nya, misal dari NOD32 ke EIS kalian harus uninstall dulu NOD32 nya lalu install EIS dan ikuti lagi langkah aktivasi nya dari awal.'
summary: 'Cara yang akan share disini cukup ribet, kalian sampai harus restart Desktop/Laptop-nya dua kali, tetapi cara ini paling aman dari razia, karena saya sudah hampir pakai 2 bulan database ESET nya masih bisa update, walaupun kalian tidak bisa mengganti product ESET nya, misal dari NOD32 ke EIS kalian harus uninstall dulu NOD32 nya lalu install EIS dan ikuti lagi langkah aktivasi nya dari awal.'
image: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhTIsbQ22ElXczQHcqUEsjs0lnqCzt8yH-5ODfW3L_yuZXDEF76gVKGGXE0JZR52LIYDFPUr_i0dkXPCxIa3Pj_6cJiGDw-GnJQArU2aaYM2Go4eZbbzIXcHzQef9VLvG39e-rNSjZcq47MXIJxpuC-EEHXb0umhPNkAlPdmEdCmbsZkz4huQyM1DaDgufR/s80-rw/hsts-logo.png
thumbschema: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhTIsbQ22ElXczQHcqUEsjs0lnqCzt8yH-5ODfW3L_yuZXDEF76gVKGGXE0JZR52LIYDFPUr_i0dkXPCxIa3Pj_6cJiGDw-GnJQArU2aaYM2Go4eZbbzIXcHzQef9VLvG39e-rNSjZcq47MXIJxpuC-EEHXb0umhPNkAlPdmEdCmbsZkz4huQyM1DaDgufR/s0/hsts-logo.png
---

{{% adsense %}}

![HSTS](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhYIy0SIjwFg3j4eViTY62txVghMaFzIsVp21Mf7pHBpmZsdS7cY6cM3aYGhrODi3I2j1oTExCPiYZebUZZYv0YpzWSf2u4UiEy50sEu39PSpZOIOlDDFtKX-Stu6VD49Ia8W6uU-BOfwrx4crG-waR0X0dWFhvNmncJlurnNciwC14S1z4KgtfqUx-Kett/s0/1.jpeg)

## Apa itu HSTS

HSTS (HTTP Strict Transport Security) adalah sebuah metode dimana website memaksa browser untuk menggunakan koneksi HTTPS (Hypertext Transfer Protocol Secure) ketika melakukan pertukaran data.

HTTPS adalah protokol komunikasi antar jaringan yang memiliki keamanan lebih baik dari versi HTTP berkat adanya proteksi dari Secure Socket Layer (SSL).

Dengan metode HSTS ini, website akan jauh lebih aman. Sebab,  hanya akan melayani permintaan dari koneksi HTTPS dan menolak koneksi HTTP yang rentan serangan hacker. [Sumber: Niagahoster](https://www.niagahoster.co.id/blog/hsts-adalah/)

{{% adsense %}}

## Wordpress
* Untuk wordpress yang menggunakan **Apache** kalian bisa merubah configurasinya via **.htaccess** dengan menambahkan baris berikut
```apache
<IfModule mod_headers.c>
Header set Strict-Transport-Security “max-age=31536000; includeSubDomains; preload”
</IfModule>
```
* Untuk yang menggunakan **Nginx**, edit config **Nginx** nya dan tambahkan baris berikut
```ngix
add_header Strict-Transport-Security max-age=31536000
```

{{% adsense %}}

## Firebase Hosting
Untuk yang menggunakan firebase hosting (seperti blog saya ini) kalian cukup menambahkan beberapa baris berikut di file **firebase.json** pada bagian attribut **headers** nya.
```json
{
    "key": "strict-transport-security",
    "value": "max-age=31536000; includeSubDomains; preload"
}
```

Jadinya seperti ini, jika **firebase.json** nya masih default.

```json
{
  "hosting": {
    "public": "public",
    "ignore": [
      "firebase.json",
      "**/.*",
      "**/node_modules/**"
    ],
    "headers": [{
      "source": "/**",
      "headers": [{
        "key": "strict-transport-security",
        "value": "max-age=31536000; includeSubDomains; preload"
      }]
    }]
  }
}
```

{{% adsense %}}

## Netlify Hosting
Untuk yang menggunakan hosting netlify, kalian bisa menambahkan baris berikut di **netlify.toml**
```toml
[[headers]]
  for = "/*"
  [headers.values]
  Strict-Transport-Security = "max-age=63072000; includeSubDomains; preload"
```

## Github Pages
Sayangnya sampai artikel ini dibuat, **Github Pages masih tidak support HSTS**

## Mendaftarkan Domain ke hstspreload.org

1. Kalian kunjungi [hstspreload.org](https://hstspreload.org)

![hstspreload.org](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhYIy0SIjwFg3j4eViTY62txVghMaFzIsVp21Mf7pHBpmZsdS7cY6cM3aYGhrODi3I2j1oTExCPiYZebUZZYv0YpzWSf2u4UiEy50sEu39PSpZOIOlDDFtKX-Stu6VD49Ia8W6uU-BOfwrx4crG-waR0X0dWFhvNmncJlurnNciwC14S1z4KgtfqUx-Kett/s0/1.jpeg)

2. Masukan domain kalian yang akan di daftarkan ke HSTS preload list

![Masukan Domain Kalian](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEic7u07Dwj6RRjz5Kole4fg8FJVyu7jzHMt8QX6Jhc40GMZ625tQ3fGR3kNDD0q5JfMWlSF6I9teOoZkGieReqjli77lsx0uBpdna2dOfyLMio2X_NlPOmakF-o0Y7SUNmRpE6cPj1cUbPOcRRFvpBOUhMYAREjp4a5lnRFZjYPepKGzVtgzi4nm1jnaJ4-/s0/2.jpeg)

3. Klik **Check HSTS preload status and eligibility**

![Check HSTS preload status and eligibility](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhydRPQqbor5CH5U8wu3oYqt8YRU2qSXuNrrqMfrhKDW-WT1Ai_CR2EAZfupxRDkH-B3NkYr25A7uH98Ksde3Mi0XK6nCMNvZlIZnSfcvLYsE0NIEiG6IIyAeN8xzAIzMDerlEIt94ldRuetSNuC11ccw5Tlz3h7ptT2oQsVrb6crFegUbzeHxiIkKJL3lp/s0/3.jpeg)

{{% adsense %}}

4. Jika tidak ada error, maka akan muncul tampilan seperti ini dan kalian ceklis dua-dua nya

![Check HSTS preload status and eligibility](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgq7i3Hhe2YHkgnuQSyQ5-caG5KpjTgv7ezFdTB3XdZ4Hc6cvCIF4mqc78uSqmWIEXXepUJGU9LjywLMz6wjSG7XSxyJXQ6e9ScSGgDP5x5rna3XfPMszegIppcOlmyb7yq54ETutJeUm1lyaZIxQrAIHqY718h5PaznPNIeOKKUCQSYCxZNQX5zeWCwxso/s0/4.jpeg)

5. Klik **Submit rmdhnreza.my.id to the HSTS preload list**, maka nanti akan muncul **Success**

![Success](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhwbiS2t5j04iJnx5YJ1an1tEJJD4ALPRGLLFL6Ag4LP_cSWv_fTMonj8xSIKNPXCObcDPrtZg334XjAm4kEoC0xVmmA3xb3b2HR4dI-ZnLS4LAHuNAhDuRB9xObNZDWRM9Uu0BSSRPOstJ65bmetP-Ub8Q9gL-9C5-4gEkQaw_LqRcFLPTGAB7MOnFKMt4/s0/5.jpeg)

7. Proses ini membutuhkan waktu sampai berminggu-minggu, jadi kalian bisa cek setiap hari untuk melihat apakah domain kalian sudah terdaftar di HSTS preload list atau belum

![Tinggal menunggu](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgaHZ6dkG_6OXYyOkiepHVkZPr7twN3LL-ir7KGXqilJGaKsK5_PiWphzOClQj98gDM0OVKLug2-BrQxtYV4MspXhyBVxgcW3ZtUXaxIP9QklgR6C6cMSSDuPwRfOTDm-FOaEnk9-QahDqZTFcIr7Wb92EYtVz0SnGK3_6DE-K79cbGkV0xtsk4yBYbLSEh/s0/6.jpeg)

{{% adsense %}}
