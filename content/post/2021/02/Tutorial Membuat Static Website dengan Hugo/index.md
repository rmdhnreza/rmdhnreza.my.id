---
title: "Tutorial Membuat Static Website Dengan Hugo"
date: 2021-01-07T18:54:45+07:00
description: "Tutorial Membuat Static Website Dengan Hugo di Hosting ke Firebase"
categories: ["Hugo", "Tutorial"]
tags: ["Hugo", "Tutorial"]
description: 'Hugo adalah Static Webite Generator yang ditulis menggunakan bahasa program Go. Hugo adalah project Open Source yang dilisensikan di bawah Lisensi Apache 2.0. Hugo mampu memuat halaman dalam hitungan detik ( <1ms per halaman) karena itu Hugo terkenal dengan "The world’s fastest framework for building websites".'
summary: 'Hugo adalah Static Webite Generator yang ditulis menggunakan bahasa program Go. Hugo adalah project Open Source yang dilisensikan di bawah Lisensi Apache 2.0. Hugo mampu memuat halaman dalam hitungan detik ( <1ms per halaman) karena itu Hugo terkenal dengan "The world’s fastest framework for building websites".'
image: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgf1oK8J4S3tNRWW330MlC17FhhksTbIfUXE49C6mbc5OQTrkhr290jKKDMwmYNiVHY-RNXhPurj7DCzzXZpw9XnEO36JnkBWIYMjEk7EEexmYw57w5KDiQVs7rFh71xCvHzMvU0wu-haVqmqgwBxnL-Y7v5lXBGASCMKsNfC-__2j6op-H9eKE6-1aSvds/s80-rw/hugo.png
thumbschema: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgf1oK8J4S3tNRWW330MlC17FhhksTbIfUXE49C6mbc5OQTrkhr290jKKDMwmYNiVHY-RNXhPurj7DCzzXZpw9XnEO36JnkBWIYMjEk7EEexmYw57w5KDiQVs7rFh71xCvHzMvU0wu-haVqmqgwBxnL-Y7v5lXBGASCMKsNfC-__2j6op-H9eKE6-1aSvds/s0-rw/hugo.png
---

{{% adsense %}}

Hugo adalah Static Webite Generator yang ditulis menggunakan bahasa program Go. Hugo adalah project Open Source yang dilisensikan di bawah Lisensi Apache 2.0. Hugo mampu memuat halaman dalam hitungan detik ( <1ms per halaman) karena itu Hugo terkenal dengan "The world’s fastest framework for building websites".

Disini saya akan men-deploy website hugo ke Firebase, selain ke Firebase kalian juga bisa hosting website kalian ke Github, Gitlab atau Netlify.

Sebelum membuat website dengan Hugo pastikan kalian menginstall Hugo nya terlebih dahulu.

1. Install hugo versi terbaru yang bisa kalian download di [github.com/gohugoio/hugo/releases](https://github.com/gohugoio/hugo/releases)
2. Saya sarankan kalian mengunduh versi extended nya, karena beberapa tema hanya support versi extended
3. Untuk pengguna Windows saya sarankan install menggunakan **scoop**, yang bisa kalian lihat tutorial nya di website ini tepat nya [Cara Menginstall Package Manager Scoop Di Windows 10](/cara-menginstall-package-manager-scoop-di-windows-10/)

![Tutorial Membuat Static Website dengan Framework Hugo](https://1.bp.blogspot.com/-dnVPw2BHVB8/X3iUG5N64hI/AAAAAAAACrc/AFjHbgjsNOAi0rEyDgG56ou8PVEpl2vTQCLcBGAsYHQ/s0-rw/2.jpeg)

4. Setelah kalian menginstall hugo nya, buka Windows Powershell untuk yang menggunakan sistem operasi Windows dan buka Terminal untuk sistem operasi berbasis Linux dan jalankan perintah ``` hugo version``` dan jika tidak ada error maka hugo sudah berhasil di install di sistem operasi kalian.

{{% adsense %}}

## Membuat Website Dengan Hugo

1. Kita harus membuat website nya dulu dengan perintah  hugo new site rmdhnreza untuk rmdhnreza kalian bisa ganti dengan nama yang kalian mau, jika sudah selesai hugo akan membuat folder baru dengan nama tadi.

![Tutorial Membuat Static Website dengan Framework Hugo](https://1.bp.blogspot.com/-onczNnB0HZs/X3iUj6JxbzI/AAAAAAAACro/76K6ioQlgYQW8cDBogDGZMg6eX5n8v5ggCLcBGAsYHQ/s0-rw/3.jpeg)

2. Masuk ke folder yang baru dibuat ``` cd rmdhnreza```
3. Download tema hugo nya yang bisa kalian dapatkan di themes.gohugo.io, disini saya akan menggunakan tema paper. Perlu kalian ketahui, setiap tema config nya pasti berbeda ada yang menggunakan format **.TOML** dan ada juga yang menggunakan format **.YML**, jadi pastikan kalian menginstallnya sesuai dengan dokumentasi tema tersebut.
4. Untuk menginstall tema paper di root folder hugo website kalian ketikan perintah perintah
```bash
 git submodule add https://github.com/nanxiaobei/hugo-paper themes/paper
```
5. Edit **config.toml** menggunakan editor, lalu ubah nama temanya

![Tutorial Membuat Static Website dengan Framework Hugo](https://1.bp.blogspot.com/-fN1BGpEngMk/X_cNJlFcnXI/AAAAAAAACzI/sgrmLg7h9yAH7-OeocEeWlOI2_pAiZnqACLcBGAsYHQ/s0-rw/9.jpeg)

{{% adsense %}}

6. kita coba jalankan hugo nya dengan perintah ``` hugo server -D``` Jika tidak ada error maka pemasangan tema berhasil **CTRL + C** untuk menghentikan proses hugo.
7. Buat post dengan perintah ``` hugo new PostPertama.md``` pastikan ekstensi **.md** (markdown) kalian tulis.

![Tutorial Membuat Static Website dengan Framework Hugo](https://1.bp.blogspot.com/-6jIwe9lsEEE/X_cOMDPE4fI/AAAAAAAACzQ/DUfo0Oqe2jEf_GkUrcovvQeznSLSBjjTgCLcBGAsYHQ/s0-rw/11.jpeg)

8. Maka akan muncul file baru di folder content, disana kalian bisa edit post nya dan pastikan **draft: false** agar nanti muncul pada saat kita hosting ke firebase
9.  Jalankan lagi hugo server dengan perintah ``` hugo server -D``` lalu buka di browser **http://localhost:1313**

![Tutorial Membuat Static Website dengan Framework Hugo](https://1.bp.blogspot.com/-S9AvWTeMM_s/X3iVGmjVP5I/AAAAAAAACr8/bIxz6ueUNJ4tJBPnXe_FxHh2eCF4Q5SwQCLcBGAsYHQ/s0-rw/13.jpeg)

10. Jika dirasa sudah cukup **CTRL + C** untuk menghentikan proses hugo, dan ketik perintah ``` hugo``` nanti akan muncul folder baru bernama **public**, nah folder ini yang nantinya akan kita hosting ke firebase

![Tutorial Membuat Static Website dengan Framework Hugo](https://1.bp.blogspot.com/-C6uWslKC3o0/X3iVMzNz7vI/AAAAAAAACsA/u4Aj-jIGLOU14DrP9R3dNAJz6LASHk7KgCLcBGAsYHQ/s0-rw/14.jpeg)

{{% adsense %}}

## Hosting ke Firebase
Sebelum kita mengupload static website kita ke Firebase pastikan kalian sudah menginstall npm package **firebase-tools** di sistem operasi kalian, jika kalian belum menginstallnya kalian download dan install **nodeJS** versi terbaru, setelah terinstall masukan perintah ``` npm install -g firebase-tools``` di Powershell, CMD ataupun terminal. Jika Kalian sudah menginstall firebase tools nya, kita langsung saja mulai hosting static website kita ke firebase

1. Login ke firebase, gunakan perintah
```bash
 firebase login
```
2. Setelah berhasil login, ketikan perintah
```bash
 firebase init
```
   * Pilih Hosting
   * Pilih project kalian jika kalian belum punya project tinggal pilih **Create a new project**
   * Beri nama & ID project kalian
   * What do you want to use as your public directory? **Enter**
   * Configure as a single-page app (rewrite all urls to /index.html)? **No**
   * File public/404.html already exists. Overwrite? **No**
   * File public/index.html already exists. Overwrite? **No**

![Tutorial Membuat Static Website dengan Framework Hugo](https://1.bp.blogspot.com/-eWXp0dNrDrg/X3icUKGHMyI/AAAAAAAACsk/wzYR9KvzYjonpc65e9siTrvXPVrTpIXjQCLcBGAsYHQ/s0-rw/16.jpeg)

{{% adsense %}}

3. Sekarang kita upload semua file yang ada di folder public dengan perintah
```bash
 firebase deploy
```
4. Jika berhasil nanti akan muncul URL nya di terminal, bisa kalian buka di browser **https://rmdhnrezamyid.web.app**
5. Edit **config.toml**, ganti bagian **baseURL** nya dengan link website kalian lalu save

![Tutorial Membuat Static Website dengan Framework Hugo](https://1.bp.blogspot.com/-04MLwZshVX8/X3icgE92o6I/AAAAAAAACss/vO8-kdBfQAY0vVY3QklY9NzuXatQm4N1gCLcBGAsYHQ/s0-rw/18.jpeg)

6. Langkah terakhir kalian ketikan perintah
```bash
 hugo
 firebase deploy
```
Sekarang buka URL kalian di browser,
![Tutorial Membuat Static Website dengan Framework Hugo](https://1.bp.blogspot.com/-LHm8DzZblIk/X3icsi-4zTI/AAAAAAAACs4/bg0soHYAn3kB9a6KKp-_opFp2D0uoVimwCLcBGAsYHQ/s0-rw/20.jpeg)

Untuk lebih lengkapnya bisa kalian kunjungi dokumentasi hugo di [https://gohugo.io/documentation/](https://gohugo.io/documentation/).

{{% adsense %}}
