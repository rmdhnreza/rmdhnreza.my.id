---
title: 'Cara Memasang Iklan Adsense di Blog Hugo'
date: 2022-05-08T10:30:13+07:00
description: 'Memasang Iklan Adsense di Blog Hugo'
categories: ['Tutorial']
tags: ['Tutorial']
keywords:
  [
    'Cara memasang iklan adsense di Blog Hugo',
    'How to install adsense on Hugo Blog',
  ]
description: 'Tidak seperti blogspot atau wordpress yang sangat mudah untuk memasang iklan Adsense, di Hugo ada beberapa tahap untuk memasang Adsense.'
summary: 'Tidak seperti blogspot atau wordpress yang sangat mudah untuk memasang iklan Adsense, di Hugo ada beberapa tahap untuk memasang Adsense.'
image: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjO5jokp6MbqNQns-3JFI8LO6ex19a_jE0HEoU5I606DwAMcnPvgAZe9-dGl0UU5aieNBJxXr0uWt39TKqJ7twV6Wlr0jbAZwjspETWZ3ECWJh7OMK54jaxi9TddyaNAkJ0_Qe4OpS4ZF0C_k81skdgjb2-NT1N5jFsauN3gdm49OFXjfZbdN64HH3vaR72/s80-rw/adsense-logo.png
ThumbSchema: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjO5jokp6MbqNQns-3JFI8LO6ex19a_jE0HEoU5I606DwAMcnPvgAZe9-dGl0UU5aieNBJxXr0uWt39TKqJ7twV6Wlr0jbAZwjspETWZ3ECWJh7OMK54jaxi9TddyaNAkJ0_Qe4OpS4ZF0C_k81skdgjb2-NT1N5jFsauN3gdm49OFXjfZbdN64HH3vaR72/s0-rw/adsense-logo.png
---

Tidak seperti blogspot atau wordpress yang sangat mudah untuk memasang iklan Adsense, di Hugo ada beberapa tahap untuk memasang Adsense.

Kita akan memasang Adsense di **homepage** secara **otomatis**, sedangkan di bagian **post** secara **manual** menggunakan *shortcode*

## Setting Dashboard Adsense

Sebelum kita memasang Adsense, pastikan website kita sudah disetuji oleh Google seperti ini.

![Situs yang sudah disetujui oleh Google](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiQ7FehFYkZq_X0PcVyKrpdXOTX5f-_BPGBCpIp6Y24Sdg9KszziZLsRJKKAiIY4hXfc2EQE9croYzJqLSHU0ymT23GnIIXfYiigbBjHvMjiIm8Iy_nyvDrk_4MQ16gJAR6eTqFRO0KZRXA65pzjj1da3ew9ebsOSMF4zCgH_jXZwl0FKzHpXw456Qz1uHa/s0-rw/rmdhnreza.my.id.adsense.hugo.2.jpg)

{{% adsense %}}

Jika website nya sudah disetujui oleh Google, kita sekarang akan membuat iklannya.

1. Masuk ke bagian Iklan
2. Pada bagian **Menurut situs** buat iklan yang **disarankan** dan **Iklan dalam Artikel**
3. Pada bagian **Setelan global** aktifkan fitur **Izinkan Google mengoptimalkan ukuran iklan seluler Anda**
4. Sekarang kita masuk ke bagian **Menurut situs** dan klik **Dapatkan Kode** dan salin code nya.\
   Kode ini yang akan kita pasang di situs hugo kita.

1             |  2
:-------------------------:|:-------------------------:
![Dashboard Adsense](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEg9HIpinb48n5fhIix228SAGasEWgOP2jJBS_xEdUrhvJj6MjopMNOYh6yNkUzBp_G_qE7Kc4UHOBqJOKE5-nPsDJ0PN2jcUcEapTG3G8UDkhgYfKq0vOBRBo_C-JcG23y5pKwgry7lfELe24ZKRMJd8rsOqJrol4zOt2gemjA6LfpaTyNS1ETGHWu1g0dK/s0-rw/rmdhnreza.my.id.adsense.hugo.3.jpg) | ![Kode Adsense](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiTKVVg9mgO3-H3VM0kXKSbEu44nLVpfqDlgfSx62mPxuFG8VjoA1uXf5GLSX2MpDU9I759P3BOwWdFKxgfHGwGPiW1PDeBtlX3Qn2Cz8HLgmXXKTYn8mMuiTbqq35CrdajIkCHvc2bTUu1r8X6l3xUlL8E21OHs0n1Oi_PvLrQzTZQXg6af13c1umyw9NV/s0-rw/rmdhnreza.my.id.adsense.hugo.4.jpg)

## Memasang kode adsense di homepage
> **Catatan**:\
> Sebelum memasang script ini perlu diperhatikan struktur tema yang kalian gunakan, disini saya memakan tema [stack](https://github.com/CaiJimmy/hugo-theme-stack).\
> Pastikan kalian memasangnya di **lokal folder** bukan di **folder tema**\
> Jadi jika kalian menggunakan tema yang sama, kalian bisa ikuti cara saya dibawah ini.

1. Saya memasang script nya di bagian **footer** bukan **header**, tapi kalian bebas dimana saja yang penting script nya ter-load oleh browser.\
   Struktur folder saya seperti ini dan **kode** tadi di pasang di **custom.html**
```toml
rmdhnreza.my.id/layouts/
├── partials
    ├── footer
        └── custom.html
```
2. Save dan coba secara lokal apakah script nya sudah ter-load oleh browser.\
   Disini kita bisa lihat bahwa script **adsbygoogle.js** sudah ter-load oleh browser.

**Catatan: Jika terdapat error**
* Pastikan kalian matikan adblocker nya
* Pastikan DNS Level Adblocker nya dimatikan juga (Adguard Home, NextDNS, Pi-Hole, Dll)

![Script berhasil ter-load oleh browser](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEifwEiBJsI_cEpDv1_WtAZmnVKkBvYwFVSIwNZsIRxHOnVAEfi_-UCj1DIwg9ze-RcKybKQcewV9NuzRgNVEsSNRci-7tZ1KDle7AhWGPsHzAc7HpQgugQQchIM2WRSv-t3OpDFk_qmcrWvXUr9snTMCdzHoTUcwq5HcNYGFyUUFl5XKPpsLqR-tViylySK/s0-rw/rmdhnreza.my.id.adsense.hugo.5.jpg)

3. Dengan ini sebetulnya Adsense sudah bisa tampil dihalaman website kita tetapi hanya pada bagian homepage nya saja.

## Memasang kode adsense di post
Untuk memasang nya secara manual di postingan kita harus membuat *shortcode* terlebih dahulu.\
Struktur folder untuk *shortcode* nya seperti ini dan diberi nama **adsense.html**
```toml
rmdhnreza.my.id/layouts
├── shortcodes
    └── adsense.html
```
1. Setting **Iklan dalam artikel** nya seperti ini jika sudah klik **Simpan dan dapatkan kode**

1             |  2
:-------------------------:|:-------------------------:
![Iklan dalam artikel](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhRC1WzgHRf6MieXHtQsvC1ZdWpwEDNpsN9XvKwiPvuYc4kK7_CTWTK67ihL0N3gxW-GRayznHbjkmslinZkaDxQ15WBDffV_TkRjylUW6bURS1vbr1WkGkOfAQeKt45nIxpc6nbR9bL1DABnN7doJ53GmitkVXp8X9YKvzIzKN0CN2Ww2Z8fTCkz6ZDq8B/s0-rw/rmdhnreza.my.id.adsense.hugo.6.jpg) | ![Iklan dalam artikel](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgp_-8rX5HohG6EBTydd7HMsFO-_nn_GYB50ixVHy_JGDw3GMZ-T2y1PSSqNKfLa5d2SXRsFHVDxSIV-AA3LCeA1C1TWGaWY2m7ZAlwQ0X-CPDIQW2eJKime41DmKAZEvExu_zYF9JwbwbgTuLQoBsUDM4TCCkjwEshdRIA7yXh32afkjQgU_QspvI8s0Or/s0-rw/rmdhnreza.my.id.adsense.hugo.7.jpg)

{{% adsense %}}

2. Salin kode nya ke **adsense.html**
3. Untuk memasang Adsense di postingan kita cukup memakai **shortcode** `{{-% adsense %-}}` (**tanpa tanda -**).

Contoh nya
```md
Paragraf 1

Paragraf 2

{{-% adsense %-}}

paragraf 3
```

Dengan kode diatas, iklan adsense akan muncul **setelah** paragraf 2 dan **sebelum** paragraf 3

**Jangan lupa hapus tanda strip (-) setelah dan sebelum kurung kurawal**

## Iklan tidak muncul

1. **Iklan tidak akan muncul di localhost**, pastikan kalian sudah hosting hugo website nya secara live
2. Matikan **Adblocker** (Extensions atau DNS-Level Adblocker)
3. Matikan juga fitur **tracking content** (Firefox, Vivaldi)
4. Matikan **Brave Shield** untuk pengguna Brave Browser
