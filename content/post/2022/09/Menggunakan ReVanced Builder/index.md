---
title: 'Tutorial Menggunakan ReVanced Builder'
date: 2022-09-03T15:30:13+07:00
description: 'Tutorial Menggunakan ReVanced Builder'
categories: ['Linux', 'Windows', 'Tutorial']
tags: ['Linux', 'Windows', 'Tutorial']
keywords:
  [
    'Tutorial Menggunakan ReVanced Builder',
    'How to Use ReVanced Builder',
  ]
description: 'Tutorial Menggunakan ReVanced Builder'
summary: 'Tutorial Menggunakan ReVanced Builder'
image: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgRG1aqNJ299j2-lxVdxy0A5AQgPkya57k12PBkasFj1rjaG964AAkvRdqkduF5W7IsCbk-J6pdZLtzz282SsOzTE_FbYNkRA_oQzzCTl7IZre891a-n6kS2b5Ljzfsq5QuPTeuNaQ8ocTBEUtsFdt9G_6NpgKm0GW0fvozrl6MGYooetKcam6xWRa8LIdC/s80-rw/revanced-logo.jpg
ThumbSchema: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgRG1aqNJ299j2-lxVdxy0A5AQgPkya57k12PBkasFj1rjaG964AAkvRdqkduF5W7IsCbk-J6pdZLtzz282SsOzTE_FbYNkRA_oQzzCTl7IZre891a-n6kS2b5Ljzfsq5QuPTeuNaQ8ocTBEUtsFdt9G_6NpgKm0GW0fvozrl6MGYooetKcam6xWRa8LIdC/s0-rw/revanced-logo.jpg
---

{{% adsense %}}

Sebelumnya saya sudah buatkan [Tutorial Patch YouTube Android dengan ReVanced](/tutorial-patch-youtube-android-dengan-revanced/), sayangnya cara itu harus manual, seperti rename files, memasukan perintah secara manual, Android harus terkoneksi dengan PC, dll.

Sekarang ada tools dengan nama ReVanced Builder, tools ini bisa melakukan patch YouTube secara otomatis (kecuali menginstall Azul JDK).

## Aplikasi yang dibutuhkan
Aplikasi yang harus terinstall di PC kita yaitu **Azul JDK versi 17+**, kalian bisa pilih link dibawah ini sesuai dengan sistem operasi kalian untuk download dan install **Azul JDK versi 17+**.

* **Linux 32-Bit:** [Azul Zulu: 17.36.19](https://www.azul.com/downloads/?version=java-17-lts&os=linux&architecture=x86-32-bit&package=jdk)
* **Linux 64-Bit:** [Azul Zulu: 17.36.19](https://www.azul.com/downloads/?version=java-17-lts&os=linux&architecture=x86-64-bit&package=jdk)
* **Windows 32-Bit:** [Azul Zulu: 17.36.19](https://www.azul.com/downloads/?version=java-17-lts&os=windows&architecture=x86-32-bit&package=jdk)
* **Windows 64-Bit:** [Azul Zulu: 17.36.19](https://www.azul.com/downloads/?version=java-17-lts&os=windows&architecture=x86-64-bit&package=jdk)

Setelah berhasil terinstall, kalian coba buka PowerShell atau CMD (untuk Windows) dan Terminal untuk Linux, ketikan perintah berikut `java --version`, jika yang muncul seperti ini, maka penginstallan **Azul JDK versi 17+** berhasil.

1             |  2
:-------------------------:|:-------------------------:
![Install Azul JDK](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiJ6a9Zp9PJ8iSUlEELHCNhj5k2fIuY2vtnIQhKcHgAdvgVeaKqkjTpvm5ZrPJ-d2vudfYFsIQD7WXPrpAwWFbArse1X4g7-m8f9y7_ycTyqulVc9mymC_DQP0I_Kz_lCs68sP5ZqSrP7Lh_An36GmMpQ-3rEL63SQpvWSQCMtlkgmRt9yOziDiXjF5sMca/s0-rw/rmdhnreza.my.id.tutorial.revanced.builder.2.jpg) | ![Versi Java](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEg988ZrCOwLzGkO-a0SL2LvoJez7DNX3IMJxFOizigllZfLjrKCDzIFb5U5WmXOP9w2mZNneT7LLos2DVvECxamRdW12U7o80YjDj8KRqmM0JkR24BozJ8LD3ZkuPJjHN1HNRSlZxjjie9kiJ4JvJDypwlmUc3auHwn4HrClRhUVzYWbWL6Jp9ykRYD5BMf/s0-rw/rmdhnreza.my.id.tutorial.revanced.builder.3.jpg)

{{% note %}} Untuk aplikasi ADB sebetulnya optional di tutorial ini, tetapi jika kalian ingin menginstall otomatis YouTube ReVanced nya, harus terinstall ADB di PC kalian dan pada saat mengikuti tutorial ini, pastikan Android kalian terkoneksi ke PC kalian. {{% /note %}}

## ReVanced Builder

1. Download terlebih dahulu [ReVanced Builder](https://github.com/reisxd/revanced-builder/releases/latest) nya\
   Download sesuai dengan sistem operasi kalian (Linux, MacOS atau Windows)

![ReVanced Builder](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgolTQec1Z_K4SJ7F0RAK7q-U8Q8Slj_mkUOWk1Hjg6VMjvysp6s1_8B-3zs8383odiUQ4Jw69mfnNh5Ex6sGsYCusZzlraQmKIEU11EMjkN6pkYSB2KiVTPo1fGjrMPZBwfITx_ISxqEp-bMZkAhYspu1h2QqBDOeMM-B9CMoEjYcCeGMJSLYZNuF0hT3O/s0-rw/rmdhnreza.my.id.tutorial.revanced.builder.1.jpg)

{{% note %}} Versi terbaru ReVanced Builder pada saat tutorial ini dibuat yaitu versi 3.3.7 {{% /note %}}

2. Karena disini saya menggunakan Linux, jadi saya download file `revanced-builder-nodejs-linux`
3. Setelah di download buka atau eksekusi file `revanced-builder-nodejs-*` nya, maka ***default browser*** akan terbuka otomatis

![ReVanced Builder](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEie1bznpJ9YI75LcdpHbZca8_jwjEOTAmbn2VBzMX7ZrYrS56HsV_iebXFoxkDKjX9m3OJbQFYl3zYuRSB6l0ax1ADy25YF0NA9sOhOrLg-GaW5F5WBISETSYq5oprW4v4ahRwlvmgMAJDIrz00ptbPv-oKTxXY5VCdW4OMY-99S5RlYz6qZmdYZ2FSoDj0/s0-rw/rmdhnreza.my.id.tutorial.revanced.builder.4.jpg)

4. Kalian pilih YouTube lalu *Continue*

![Pilih YouTube](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgmIG3UQhcaNecHjrQyTziusr20XnqrskxCH2h5KHKFc9CXy4P7T6cHNN5gzGKPtLHKcHoCbK-5HO4-S29BmmOYmpRyqzMhy1Bg-WoZzS_9EHPs8QlWgSpbjkGOu2n0Jm8CZl-vOlzfnAj4RfP53syhTuoo_XAy_-aHTYGyfJryFq-b2AW-DVYQuyfdXSUd/s0-rw/rmdhnreza.my.id.tutorial.revanced.builder.5.jpg)

{{% note %}} Jika muncul failure seperti ini, pastikan Azul JDK versi 17+ sudah terinstall dengan benar {{% /note %}}

![Failure Azul JDK](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhhb4qBFbd1Ukz361flrAqOwXJ_8iKLLEL916uqZjilsvk_tOmMjybWHggzKIij0mGeDPI5qZFnseSdNdxCQUhA_iwdAKen04r8swjlp0wUxMct6AK5SIxo2mQ107pQYWjzS3vzgsU7l54mON9zXNmjKE8rOCl6-vqECK9oL9TWNVcmr-zNpO5LjTcuH75E/s0-rw/rmdhnreza.my.id.tutorial.revanced.builder.6.jpg)

{{% adsense %}}

5. Pilih Patch yang akan dipakai
   * Untuk pengguna **non-root** cukup klik pada bagian `Select All` untuk memakai semua patch
   * Untuk pengguna root, klik pada bagian `Select All` lalu **jangan pilih patch Hide Cast Button** sama **MicroG support**
   * Jika sudah klik *Continue*

![Pilih Patch](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhbRyV1dv4Na59sQl3Cs9Yz4ZsWM3WDll81m0CQSdVxquuYNCbQK258S0Lu-3q3G5sFOnqUXdTu46e_7VbZWcKup-45sxztVjvvhHlTtQKPf5jcBWvUiGY3lzmciFUMVfiwgz8jjLEZi2dEBnSy6XzV-E689S7KXpHuyQdMVPnQSa58udZsPdtm6fGqMaSj/s0-rw/rmdhnreza.my.id.tutorial.revanced.builder.7.jpg)

6. Pilih versi YouTube yang akan di patch.\
   Jika sudah klik pada bagian *Continue*
{{% note %}} Pilih versi yang terdapat tulisan (recommended), untuk menghindari crash dikarenakan patch nya belum tentu kompatibel dengan versi YouTube terbaru {{% /note %}}

![Pilih Versi YouTube](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgHrOamhFj9CPJyB6emZICm7nroLyCX_lGKBR2p8qHYjLYyjGntljxS3cLFTWnxbYE7u1IzrFab624sTT-q23kJ3AqHY2wh0Z_xrdtKCfyX2_O7PGNkNmoFb3sqWtuHZXKVbdX7AfVEKri2_6bawMpou2kLPeKT89uSUjNx27H1qb17qt-r87TcR12fraIA/s0-rw/rmdhnreza.my.id.tutorial.revanced.builder.8.jpg)

7. Tunggu hingga proses download aplikasi YouTube nya selesai (Cepat lambatnya tergantung koneksi internet kalian), jika sudah terdownload klik pada bagian *Continue*.

1             |  2
:-------------------------:|:-------------------------:
![Download YouTube](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiA9cplb-BxNjBAwMhunYkTiooQFw51tQI0AveU5W5NO5MLLBryBKb43z5_M317IozL6wZvYiaAS_s5wDcdchfOtSGOdtKOXmJ50tby89KDwvc3JCmgJxk6rsEnzU_tML0lZ2p9V2IeXwmoIkBE1VPdEXD2JdM5bri8X4dAz2aVb9mBE9RKmfSwp8LDMUFo/s0-rw/rmdhnreza.my.id.tutorial.revanced.builder.9.jpg) | ![Download YouTube](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgm4LWlD2blHLNaHIyx8qTqS9osUingQyVkU2xIZ17rjeTp9E4BXpHkQdTj3JdrUfU1dwrwZ7VsmeHb0zCrbdmyQyW-UHKYhEBs3um-yvqek1P8NNvcg4s5eDuab1vxNOkSE-VTWhd9o8pJjGi-TXPZwOxHztEPpSItg5Z8ymyPZmSr82jmX5Qp92kB9xwS/s0-rw/rmdhnreza.my.id.tutorial.revanced.builder.10.jpg)

8. Proses patch sedang dilakukan
{{% note %}} Proses ini, cepat lambatnya tergantung dengan spesifikasi hardware komputer kalian. {{% /note %}}

1             |  2
:-------------------------:|:-------------------------:
![Proses Patch](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEh2mt9L3XY6JeKDlLbiMv-0msI9o3qUwSjQHqRyR1lQC4RBhlTYHbVrKyCm_DJK_xXEXxcX2XsB2e-bvCiT3CZE9Lnvnup4oQJDuLT0zt6wFHVxUJy7v7Sejnzom1YgV1SYdE1SVB7ZG-h_q06AgMl-bJJnucvDti4KhOUZ2omcxGEIWSF8V66ugPOMVeSe/s0-rw/rmdhnreza.my.id.tutorial.revanced.builder.11.jpg) | ![Proses Patch](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgmrXrjbhSqFFbDlmoPmcd-0x7G6XhVpzm1hmJy52-DC-6ocW6dApipZdtmSqqwWufdvEXIPlI8FhOaI-32Krdcoll-R_lpheS1DxXODtwt69P5LqizKLCwgw-j4LOLF6JaDrQxPGspp8HO6UX-MLVLsLQLxgSpLH5MjDAh5-YeK9wokLIZnPp5L0GMk0Al/s0-rw/rmdhnreza.my.id.tutorial.revanced.builder.12.jpg)

9. Proses patch berhasil.
   * Jika kalian mengkoneksian Android kalian ke PC, **YouTube ReVanced** akan otomatis terinstall ke Android kalian.

![Patch Berhasil](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgo4mMm4oTw5IRZxClw8UtQ2Km_G1SELGId53Ie1V5O4EMR6dqRzC9Av457RVXAvVFn0oEyqomAx2IqnsTWnCbKm6zoXQhiXgZy7qrcbujJ-ZvPrT4NAGDMq-mhrZrbbXQrKnhJW6thoc0iFpEafFNEeSRfqF7Scdr4pKniKMmLmR-NMzOYQPdRKmq_w5E7/s0-rw/rmdhnreza.my.id.tutorial.revanced.builder.13.jpg)

10. Buka folder **revanced** Copy 2 file ini ke Android kalian dan install
    * ReVanced-YouTube-v17.33.42-cli_v2.9.5-patches_v2.50.4.apk
    * VancedMicroG-v0.2.24.220220-220220001.apk

![YouTube ReVanced apk](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiGwPuEMAWZhePWfLrb7BS3-JBF7z7Ds8IOqpK0u50bmtMWEItit0yX-dwNIVwvdYoIrrhO7rbDvx6bVM81N4UyP-b0XbYs8oK8nxInqwwlgwkTlCfrv7Vz7Ei6UTVF02qL8BX9f9Blm_UVEpNmAs5p04svxqSVz0M9uePLMLnMpHpKJoYO_bt6212P0wlw/s0-rw/rmdhnreza.my.id.tutorial.revanced.builder.14.jpg)

## Video

{{% adsense %}}

{{% iframe "AD6v5dy-cPlb_MoD2Im0k1OEncTbilnDE2ySdnAExivnRFi3a0xf6cpKZaQShDQucWYd7PCdtKVxqEn8ZbGEIs0xt08wkUFy0m8XbJOPBJKSCF6OHkpGorj8GbhWAT7XlLBSckO3KQ4" %}}