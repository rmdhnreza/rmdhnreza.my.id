---
title: "Trik Download Torrent Menggunakan Heroku"
date: "2020-11-26"
description: "Heroku Torrent to Google Drive"
categories: ["Google Drive", "Tutorial"]
tags: ["Google Drive", "Tutorial"]
description: 'Pada tutorial kali ini saya akan membagikan cara mengunduh atau leech file torrent dari Heroku langsung ke akun Google Drive atau Team Drive kita. Jadi kita bisa mengunduhnya via download manager seperti EagleGet, Free Download Manager, Internet Download Manager, dll.'
summary: 'Pada tutorial kali ini saya akan membagikan cara mengunduh atau leech file torrent dari Heroku langsung ke akun Google Drive atau Team Drive kita. Jadi kita bisa mengunduhnya via download manager seperti EagleGet, Free Download Manager, Internet Download Manager, dll.'
image: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEix8be1DebCxOUC3pDFO9WaUyqtBc_LDC2PTMy1ci5I1nsvxJl3gN1IsjENPocxDYXfUvgSbUZ3ObOm_8LmApu9wk_ZJDI_rIKcPhrOlUFeHrssCT88ltzB-APHHnQ5mylUYxf_FrrMwL2u2Ks3kOM7L7pfobyrE91K1l0xX2baIJqbmFE64HYib6DZAxi9/s80-rw/heroku-logo.png
ThumbSchema: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEix8be1DebCxOUC3pDFO9WaUyqtBc_LDC2PTMy1ci5I1nsvxJl3gN1IsjENPocxDYXfUvgSbUZ3ObOm_8LmApu9wk_ZJDI_rIKcPhrOlUFeHrssCT88ltzB-APHHnQ5mylUYxf_FrrMwL2u2Ks3kOM7L7pfobyrE91K1l0xX2baIJqbmFE64HYib6DZAxi9/s0/heroku-logo.png
---

{{% adsense %}}

Pada tutorial kali ini saya akan membagikan cara mengunduh atau leech file torrent dari Heroku langsung ke akun Google Drive atau Team Drive kita. Jadi kita bisa mengunduhnya via download manager seperti EagleGet, Free Download Manager, Internet Download Manager, dll.

Tutorial kali ini mirip-mirip dengan tutorial [Setup Google Drive Indexer di Heroku](https://rmdhnreza.my.id/setup-google-drive-indexer-di-heroku/) yang ada di blog ini, jika kalian sudah pernah mencoba [Setup Google Drive Indexer di Heroku](https://rmdhnreza.my.id/setup-google-drive-indexer-di-heroku/) langkah-langkahnya tidak terlalu rumit seperti membuat **Client_ID**, **Client_Secret**, dll.

Pertama-tama kalian yang tidak punya akun heroku harus buat dulu di akunnya di [heroku.com](https://heroku.com), jika kalian sudah membuat akunnya langsung saja kita mulai pemasangannya. Oke, langsung saja kita masuk ke Tutorialnya

{{% adsense %}}

## Setup Heroku

1. Klik link berikut ini [Heroku Deploy](https://github.com/patheticGeek/torrent-aio-bot)
      * **App name** kalian bebas apa saja asal masih tersedia di heroku nya, app name ini yang akan menjadi subdomain link kalian
      * **Region** kalian bebas mau di US atau EU

![Heroku Torrent to Google Drive](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEi8d9UcQDV-ePe6pfa-5TJARfquO2zgJYk2COOJjOELlgizeP8PP9b-RL980LR5-HXeD9SbD1LM2y6XdZtR3jN1Bk2jKr1j01F2i8Y1eelyp1YdB89BrDzyXbIOU95wrBmOhmuQLfDEFaj_vneEe6AZSpt7KwK8ZPTFnZWwK7kAPvE2_ayy3KUxW0GFsp3W/s0/1.jpeg)

2. Setelah semuanya selesai kalian klik **Deploy app** & tunggu beberapa menit sampai prosesnya selesai

![Heroku Torrent to Google Drive](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjzGHQZkqAxPwPFkiJ8Cpr46bjqtJp4SFum11rkwzmQLewNxPID27McAb7Zz8FQaCTHM7nc-loanyE57E0NBdCQyJy35eFi9cP-DdYabJQTF0wxMtS0l6Zesef63aNX0wH1onHkgWxWfC1Lm9fU0MDsGTFsZ7o2k7lxoEAlfcX_48S975r-fPVYdkZct4Yy/s0/2.jpeg)

3. Jika proses build nya sudah selesai kalian klik **Manage app** masuk ke bagian **Settings** dan klik **Reveal Config Vars**

![Heroku Torrent to Google Drive](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjB3wmqYfBHwYKlo9VVKZxNpUXtYQOMkBAbiZIiuZKgqFeX4ooP6t97TnXoNzT-XZlq705Q_el5bCMM2zT670dD7ddMz-QKlU56rL7yhNDwHRerucwTSnF58aQYRJCRboMz5OmVoutl8E3G-VWCSQyT63Hj14606h629uuAsEOlCXzQQwcXX_4fMl58Rufx/s0/3.jpeg)

4. Isi bagian
      * **KEY** dengan **SITE**
      * **VALUE** dengan https://appname.herokuapp.com/ (**appname** kalian ganti dengan name yang kalian buat di langkah 1)
      * Lalu klik **Add**

![Heroku Torrent to Google Drive](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEg_NvcVineNmOXwuJeSIwjgl127Sh2XkJClTAw4rZYdsBsf3_GpgsngPfhjsWFfohv3usni3DLzxgXSwzpEM3PAqHpBa7rzWQ0YsiNCTTKNfa-mFJ-Si2iqUVHKAdSokk-kC-fE72M597a-KSZNvYznvNQkX4wOdwADdVzvVHviAQ1vUbd4sKHvqqNIsTY8/s0/4.jpeg)

Sampai sini sebetulnya kalian sudah bisa mengunduh/leech torrent, tapi pasti akan error karena tempat penyimpanannya (dalam hal ini Google Drive) belum kita setting.

{{% adsense %}}

## Membuat Client & Secret ID

5. Buka [developers.google.com/drive/api/v3/quickstart/nodejs](https://developers.google.com/drive/api/v3/quickstart/nodejs) Klik **Enable Drive API** masuk dengan akun Google kalian. Jika kalian sudah masuk tinggal isi project name bebas setelah itu Next maka akan muncul **Configure your OAuth client** kalian pilih **Desktop App** jika sudah langsung klik **Create** maka kalian akan mendapatkan **Client ID** & **Client Secret**

![Heroku Torrent to Google Drive](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgymquchP5rANmjjTjeuVuSa9LQRYe8jzdgraFWKq3D5jIEXyLc_1djbcFy_5aNL-E36qCpgCxJ70COAzKrzxTGDJd-4HEC6yno6nTuL_UYU9qJMGX_B9hX73cjger2zUX5tIzhSXxPKfOYVHGcyFynLfa0P8edxp9STZi2gk49vjx6XzkgusqGPaHsAVVi/s0/6.jpeg)

6. Buka link: https://appname.herokuapp.com/drivehelp
      * Copy & Paste **Client ID** & **Client Secret** yang kalian buat dilangkah 5
7. Setelah semuanya selesai kalian klik Generate token

![Heroku Torrent to Google Drive](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjMXQ-7x8WjNm28GWRZ670KSQ8Ro1Jv34-3S-Vw-LklkYw_HFbLVvvGWtjGRw_4hiV4m0T8PClXtJAQ6rJ9za33dgF8mQJSBZ7Kmeumm3P8BJUrhymKn2KWUI2MA5JEyh27Pa_rL7REFlkJldQ0JKHZLbACwEeosgt6hFOUtsrCd_tJeQ_gkb8Ft_dfJSbu/s0/7.jpeg)

8. Kalian masuk dengan akun Google kalian, akun Google ini yang akan menjadi tempat penyimpanan unduhan torrent, jadi pastikan kalian masuk dengan akun Google yang memiliki Shared Drive atau akun Universitas (edu).
9. Setelah mendapatkan **Auth Code** paste code nya dikolom app kalian, lalu **Get auth code** maka kalian akan mendapatkan **token**

![Heroku Torrent to Google Drive](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEifPvdygSQsx0MMCNKxiPxuy4IrCYA36QYzX8Sdzlt2VybnW1lbC79aWRQKWMBedEyaIIKDOAVXlNApwUmlygSv_o0M6bFa8ggwDjH7-URMohEFN14ba1EHho3lvrWxTUFq73qzTRkgj-7NyrAHasRUzCE05svYoOwJusVy9zPOhfYBFG9Ofh2bmDTpJ5N3/s0/9.jpeg)

10. Setting config aplikasi kalian (Langkah Nomor 4) seperti berikut (KEY -> Value)
      * **CLIENT_ID** -> yang kalian dapatkan pada langkah 5
      * **CLIENT_SECRET** -> yang kalian dapatkan pada langkah 5
      * **AUTH_CODE** -> yang kalian dapatkan pada langkah 7
      * **TOKEN** -> yang kalian dapatkan 9
11. Jika kalian ingin menyimpan unduhan torrent nya di satu folder maka buat config
      * **GDRIVE_PARENT_FOLDER** -> Isi dengan ID Folder kalian

![Heroku Torrent to Google Drive](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiPQ_kkNi3LmLB-tmGUDZ8F94rRWbhKPglLatUOMbQ2laGyuTeJ6RvImXX4rzlYq3uxcTQjQ2m_RxOrGpDyx6q5tN4AG7fhRcqp8fWBIsXC7FWuH9qVYhlprH7xLrROuz1_01ZlLbTmJ8evNK54PPatc_soZHTXxQSkAlN2ZlPeqkZveu6n_CzoXPG7Blpw/s0/10.jpeg)

12.  Maka hasil akhirnya seperti ini

![Heroku Torrent to Google Drive](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhNHPx5H4qkgfI8QFracQ9voFKH424NUO6Bc_b0_kE_Rfdo4GieS0pjN82Ud7wgzC7mvozbPVSubUadFMEPhqjIjO8s5_5jOpWxjsv88i1NUv7NP5O2VW8OzkoVYWjehLhM42-wRVm9Gr2Nu98p3Bz2cNPS6KY3MZzd-hA4mBEUOk__DbZbxNxzk0Ls1Wl0/s0/11.jpeg)

13. Setelah itu kalian bisa tes download torrent jika berhasil maka hasil undukan akan langsung muncul dibagian Drive

![Heroku Torrent to Google Drive](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEil8Z8HuYvzZd-VdvSDCMKgjqmqlwYL0WAZXkpEec8i4O9ELu0VXgj2iJSWi3b4SFq1iSxdwsMduUxaAj3a3NwHGopxOwHA_H_2S00LbgLNhfrUKgXsyjOb4DJQ8FR7EemJys_Hr-tnk2yhedVHx1XvMvykUHZrQ6hgrxZs4LI5VEHQgauVya1ZGUkA2kiM/s0/14.jpeg)

![Heroku Torrent to Google Drive](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjXdZTToPtPHBAt8Gh-1DPxWxsktsLnLk_MKSOM8W_zwjLG5QHEDoD8PJpbEEX2xl7x7bLk5t7BQQk__bXdK_ujje_jX2PP6XUFAH23EeSXyRGNCXIBCuKOPiasma3DdJam24hFhx7X_WGv8lTuKqN33w1YTt-aRcBd_704ljI3ZRZWBBjDeS22HbYnvUmH/s0/15.jpeg)

Jika kalian bingung dengan langkah-langkah nya kalian bisa tanyakan di kolom komentar bingung di langkah berapa

{{% adsense %}}
