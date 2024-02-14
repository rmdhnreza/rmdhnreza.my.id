---
title: "Cara Install Windows Subsystem for Android™ (WSA) di Windows 11"
date: 2021-10-21T17:30:13+07:00
description: "Cara Install Windows Subsystem for Android™ (WSA) di Windows 11 Stable"
categories: ["Windows", "Windows 11", "Tutorial"]
tags: ["Windows", "Windows 11", "Tutorial"]
keywords:
  [
    "WSA",
    "Windows Subsystem for Android™",
    "Windows Subsystem for Android™ (WSA) di Windows 11",
    "Windows Subsystem for Android™ (WSA) di Windows 11 Stable",
    "Install WSA",
    "Install Windows Subsystem for Android™",
    "Install Windows Subsystem for Android™ (WSA) di Windows 11",
    "Install Windows Subsystem for Android™ (WSA) di Windows 11 Stable",
  ]
description: 'Untuk menyederhanakan banyak hal, Microsoft membuat subsistem baru (Sebelumnya Microsoft sudah membuat Subsistem Linux (WSL)) yang memungkinkan Anda menjalankan aplikasi Android di Windows sama seperti aplikasi berbasis Windows  lainnya.'
summary: 'Untuk menyederhanakan banyak hal, Microsoft membuat subsistem baru (Sebelumnya Microsoft sudah membuat Subsistem Linux (WSL)) yang memungkinkan Anda menjalankan aplikasi Android di Windows sama seperti aplikasi berbasis Windows  lainnya.'
image: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhBHtbalLnHkYsI1w5DDQGDzMKf4vPuwdyj4dKtkGaqQaw9sF9vNffHJOcFGA3lb46CfzsSI9yCDZs4lZVI_s9ZcfF7cf8ee9UxzWtbuxGEV_bZZkH9QkeT4uVCd4_FFo1y80i12pffQ_M_02u5ASx8H_AJcrUWmYrMyK4jYEAuIRDHaUJKrZmYG9K3KWiU/s80-rw/windows11-logo.png
ThumbSchema: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhBHtbalLnHkYsI1w5DDQGDzMKf4vPuwdyj4dKtkGaqQaw9sF9vNffHJOcFGA3lb46CfzsSI9yCDZs4lZVI_s9ZcfF7cf8ee9UxzWtbuxGEV_bZZkH9QkeT4uVCd4_FFo1y80i12pffQ_M_02u5ASx8H_AJcrUWmYrMyK4jYEAuIRDHaUJKrZmYG9K3KWiU/s0/windows11-logo.png
---

{{% adsense %}}

## Cara Install Windows Subsystem for Android™ (WSA) di Windows 11

## Apa itu WSA ?

Untuk menyederhanakan banyak hal, Microsoft membuat subsistem baru (Sebelumnya Microsoft sudah membuat Subsistem Linux (WSL)) yang memungkinkan Anda menjalankan aplikasi Android di Windows sama seperti aplikasi berbasis Windows  lainnya.

Aplikasi (apk) ini disediakan ke Windows 11 melalui **Amazon App Store** (Play Store jika di Android), tetapi anda juga bisa melakukan *sideload* (menginstall aplikasi dari luar Google Play baik melalui file APK ataupun dari repository lain) hampir semua file Android .APK sehingga Anda dapat menjalankan banyak aplikasi yang saat ini tidak ada di **Amazon App Store**.

WSA memiliki persyaratan sistem yang lebih tinggi daripada Windows 11 itu sendiri, jadi menginstal Windows 11 saja tidak cukup, WSA membutuhkan setidaknya

- 8 GB RAM
- Solid-State Drive (SSD), dan
- Processor yang didukung
  - Intel® Core™ i3 Generasi ke-8
  - AMD Ryzen™ 3000
  - Qualcomm® Snapdragon™ 8c
  - Atau lebih tinggi dari yang disebutkan diatas.

{{% adsense %}}

## Jadi Bagaimana Cara Menginstallnya?

Info nya sih ini:

> Saat ini WSA hanya tersedia untuk mereka yang menjalankan saluran Windows 11 Insider Beta, dan akan segera tersedia untuk mereka yang berada di saluran Dev. Jangan berharap WSA berada di versi produksi (stable) Windows 11 hingga sekitar tahun 2022. Selain itu, Amazon App Store saat ini hanya tersedia untuk mereka yang berada di AS.

Tapi tenang saja kalian bisa mengsintall WSA di Windows 11 stable, tapi memang caranya agak cukup rumit bagi orang awam karena beberapa perintah harus dijalankan menggunakan **PowerShell**

1. Download WSA .`msixbundle` yang ukurannya cukup besar yaitu sekitar 1.2GB, untuk mendownload nya kalian kunjungi
   - https://store.rg-adguard.net/
   - URL isi dengan: https://www.microsoft.com/store/productId/9P3395VX91NR
   - Channel: Slow
   - Setelah itu tekan tanda :white_check_mark:

![Download .msixbundle](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiSL66wf-Rs_aL8AGSpS9QqwFFOXZTAeIT0qrccczV5k8YjFqFUyLeONx-Ky70fUtHSXkD9Z3CyN1jY3yh5IQnvihGnFucO_sdCvAgSIx0pF7zTGKOszbcrFDHg_qxt5m1f3S5OfWED4F2p3OjI90NL2LVQUN_00jWfipADIaSUU8fOFpOcsl1cJktuKEIn/s0/rmdhnreza.my.id-wsa-3.jpeg)

2. Scroll kebawah sampai kalian lihat file yang berukuran -+ 1.2GB\

![Download .msixbundle](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEh1Xt_s3cL8pNMub_1HjQqa2-28_-7yTUNge6KEBxswn2jMdqvR3dRijALbcy0TEAqRw5EhDhgMs-2uuv00yaHL2gKOIIzDEWmXh5vZw-2UmNG-4WhOIV1DiItjUkxhGZVvdubG9Jw4mZn6B6a8LdnD0ARR2XykFZMFNAvS5U7O4h7olvZYpL7quUGRGM3k/s0/rmdhnreza.my.id-wsa-4.jpeg)

3. Saya asumsikan file `.msixbundle` nya ada di folder **Downloads**
4. Buka **PowerShell** sebagai **Admin** (**Win + X** -> Pilih Windows **PowerShell (Admin)**)
   - Arahkan PowerShell ke Folder Downloads dengan perintah

```powershell
cd Downloads
```

5. Install file `.msixbundle` dengan perintah

```powershell
Add-AppxPackage MicrosoftCorporationII.WindowsSubsystemForAndroid_1.7.32815.0_neutral_~_8wekyb3d8bbwe.msixbundle
```

![Windows Subsystem for Android](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjsSsAJv1xl63Dsyjl3NPbji03abFr5CeAto59phjHWVkGXwiQ9eFLg1MJY2cLLiO3j7FsaFsb4GzFiMzBGlR9ZU4I5uExdjDGOABFjAHj4qpbysT5GW_9QvmtycLCT4rniqnNLagSp-1jmNjiJM8qw6E6EEWbXWgZAzRTRxouQTDMzUCQ7x-EU1NN1Yxr7/s0/rmdhnreza.my.id-wsa-1.jpeg)

6. Tunggu hingga Installasi selesai

**Catatan Penting**: Jika Subsistem Windows untuk Android meminta Anda untuk mengaktifkan "Virtual Machine Platform", fitur ini dapat ditemukan di Settings:

![Enable Virtual Machine Platform](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEilHCeds8axn4tQFQglqC7U86lpj3hLWBejshCiqLgKKTAv-TIH35adqXpAWLlFLuHGh20wDNDc8xkTzTmlsrO-o5GPsMWIZeaTUdEgClRu4E00nPEhcSQLwTLauCcv8poXF47Ch-mITEfJXVY0aJDDer_IUOz2GJsUOgAqgo_S59-sUYQaWAYYFvpIWa45/s0/rmdhnreza.my.id-wsa-2.jpeg)

Sumber Tutorial untuk Installasi WSA:
  - [/r/Windows11/comments/qcqcyd/windows_subsystem_for_android_wsa_megathread/](https://www.reddit.com/r/Windows11/comments/qcqcyd/windows_subsystem_for_android_wsa_megathread/)
  - [/r/Windows11/comments/qc6z0w/windows_subsystem_for_android_for_dev_channel/](https://www.reddit.com/r/Windows11/comments/qc6z0w/windows_subsystem_for_android_for_dev_channel/)

  {{% adsense %}}
