---
title: 'Cara Download Komik Webtoon'
url: "cara-download-komik-webtoon"
date: 2023-12-23T00:00:00+07:00
description: "Cara Download Komik Webtoon Menggunakan PC."
categories: ['Tutorial', 'Linux', 'Windows']
tags: ['Tutorial', 'Linux', 'Windows']
keywords:
  [
    'webtoon downloader',
    'webtoon downloader pdf',
    'how to use webtoon downloader',
    'kakao webtoon downloader',
    'webtoon downloader online',
    'webtoon downloader url',
    'webtoon downloader android',
    'webtoon downloader free',
    'webtoon downloader github',
    'webtoon downloader reddit',
    'naver webtoon downloader',
    'webtoon download apk'
  ]
description: 'Cara Download Komik Webtoon Menggunakan PC.'
summary: 'Cara Download Komik Webtoon Menggunakan PC.'
image: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiX8kYZNfbt36tIy2RKS5XShkM5GgFqrQmw619pS054SLYo678uf7Zxc-3fTOXoR7Il7hyXshwVQDDkJFBGrij7TBOKMdP43fkD8eAtUjyy98FBVvrWD2wAla7ziA_vcE7pggxJZX3-0SedVg7-RohT9-NIywSqcYsXrL8ikP8ZcKjfcDme1wB4XcQO9svl/s80-rw/webtoon-logo.png
ThumbSchema: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiX8kYZNfbt36tIy2RKS5XShkM5GgFqrQmw619pS054SLYo678uf7Zxc-3fTOXoR7Il7hyXshwVQDDkJFBGrij7TBOKMdP43fkD8eAtUjyy98FBVvrWD2wAla7ziA_vcE7pggxJZX3-0SedVg7-RohT9-NIywSqcYsXrL8ikP8ZcKjfcDme1wB4XcQO9svl/s0/webtoon-logo.png
---

![Tower of God](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhQaSqkTsDDe2c5abh3Ru1ZkO-ysub07YFhXYEl3xLD4MBqV046jEVyR4bZE8X4W99mJW4nu-DPxaiMO0MOW65QuUhzUboamiYYbMOt_pCKv5hWz1KGmltQFN1Fre6YM1VXOPwWKAD1WqmLf1Sh96DaRRbegRbwknz002azGUJtI1dhEjZzdOkiqt49Lq4D/s1600/webtoon-tower-of-god.jpg)

Webtoon (ditulis dengan gaya sebagai WEBTOON) adalah sebuah portal penerbitan webtun yang diluncurkan oleh Naver Corporation di Korea Selatan pada tahun 2004. Layanan ini dikenal sebagai Naver Webtoon dalam versi Korea, Line Manga (sebelumnya XOY) dalam versi Jepang, Dongman Manhua dan Webtoon dalam versi Tionghoa, serta Webtoon dalam versi Indonesia, Inggris, Jerman, Prancis, Spanyol, dan Thai.

Layanan ini bermitra dengan pembuat konten untuk menerbitkan konten asli di bawah Webtoon Originals dan sejumlah seri lainnya melaui situs penerbitan mandiri, Canvas. Komik Webtoon dapat ditemukan melalui fungsi "sistem harian", serta dapat dibaca dan diunduh secara gratis di komputer serta perangkat iOS dan Android.

Tutorial mengunduh komik disini menggunakan PC bukan menggunakan android, karena membutuhkan beberapa tools yang hanya ada di PC bukan di smartphone.

{{% adsense %}}

## Software yang dibutuhkan
1. PC dengan sistem operasi Mac, Linux atau Windows
2. Python versi terbaru
3. Pip versi terbaru
4. Git (optional)

{{% note %}} Untuk pengguna Windows kamu harus install python, sedangkan untuk Mac & Linux python sudah terinstall otomatis {{% /note %}}

## Setting Downloader

1. Pastikan `python` sudah terinstall pada komputer kamu, untuk mengecek nya kamu bisa menggunakan perintah

```bash
python -V
```

2. Pastikan juga `pip` sudah terinstall (biasanya ini bundle dengan python untuk Windows), kamu bisa mengeceknya dengan perintah

```bash
pip -V
```

![Webtoon Downloader](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEg_uJPnEY0NNCFpaB7cnNsbMaK8D8em5eMf04JPNYSxxMiY1y-uJvDDtaiNyw1zGaNr-aAou3A5b6yG5iWTaFuo57cqJKatecbjZxJklwimDAXgQV2KtpFWtkE0lycijEHW_qj0CUeC6byIfNfaokIGGDUiBBibmc79RrzzSt9Rmx-KY0Dj4NFG49QG7TxB/s0/rmdhnreza.my.id.webtoon.downloader.1.png=s0?imgmax=0)

3. Download [webtoon-downloader](https://github.com/Zehina/Webtoon-Downloader/archive/refs/heads/master.zip). Jika kamu menggunakan `git` kamu bisa *clone* dengan menggunakan perintah

```bash
git clone https://github.com/Zehina/Webtoon-Downloader.git
```

![Webtoon Downloader](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjooKTYGtLYuFpk7pQgnmQxSCHBH4Zk-CMsMwpsXC9wArfNA4pf-lRR9qkq1TwibsmdzrNGRGD4XmYX02_R61pjzAZjIg88aG77TMH6ge3jwnRBIAwBOOX8Et9_q97J1p6T6SaPnOhWYK-4yM8Yb3X7FckHQeECQzxb3zuU_glkwCPaV0RG0GVO-EgS_bm6/s0/rmdhnreza.my.id.webtoon.downloader.2.png=s0?imgmax=0)

{{% note %}} Untuk yang download menggunakan zip kalian harus extract terlebih dahulu {{% /note %}}

4. Masuk ke folder **webtoon-downloader** nya dan buka CMD, PowerShell atau Terminal di folder nya, untuk pengguna Windows kalian bisa tekan `SHIFT + Klik Kanan` dan pilih `Open Powershell window here`
5. Install module yang dibutuhkan menggunakan pip, dengan perintah

```bash
pip install .
```

1             |  2 | 3
:-------------------------:|:-------------------------:|:-------------------------:
![Webtoon Downloader](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEj1xOk17ZSrsCYnnzyKYWmriBXpCT9LrutkFK2MQlnc2EskGgLXAgalb5EAu2XsUfelYisJWymXPW6LezgLSbBLzqrgfrrb1IXiBGAsT_A7-U3oyUBfyPuckJNlm2d2IxkA9X6CuTheWGiS7GvfkMgWwUpsaZHqCzwNWg5qXSWS9YGP62z6F-WZHO0K0Kez/s0/rmdhnreza.my.id.webtoon.downloader.3.png=s0?imgmax=0) | ![Webtoon Downloader](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEg3Ml0Jr0OxhxKAQ9gC3oc2tBj0OkH00qy5EaixPGK11-Q3g3NZeQqKtC3jA0uMtGyImaFI8wfFm8D2osCbCI_J1rG6iV5_d6fTnRbNhgi8HF1FUewI21UHxRTpFeb6zccfR3AWJrEGT8nRLL3AuxXXNwgO60_wunC4w4AZhG8tZlVvO2WSSTckPzIajdqT/s0/rmdhnreza.my.id.webtoon.downloader.4.png=s0?imgmax=0) | ![Webtoon Downloader](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEj8BUhlEgMcA4aElaAV_7Qb9uuoxLXC8pCM39fjON8SnxhU22MHzsbrwjjO1w32BGLCZ-i-mPeA3QFhPDdL1-rDGOSwFxqbHUIt1Qu21RxOeQ9Ib_mUVRmpzvRhVAOEsc0Mg8L_9U0hnbFTnMxKRfk5W91fyVOku-Ww5VFLBIGUd2KgYlbWo2Kt8d8J5u09/s0/rmdhnreza.my.id.webtoon.downloader.5.png=s0?imgmax=0)

Jika semua module nya sudah terinstall, sekarang kita bisa lanjutkan untuk download komik nya.

## Download Komik

{{% note %}} Disini saya contohkan mengunduh komik Tower of God {{% /note %}}

Downloader ini sangat *versatile* kalian bisa:

1. Mengunduh semua chapter dari judul tertentu.

```bash
$ webtoon-downloader "https://www.webtoons.com/id/fantasy/tower-of-god/list?title_no=749"
```

![Webtoon Downloader](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhmJUJkfh8Gn_0qxyZbyAM88gHxlUZVh-TyixvQgmMEa1bjdTfh34vzeyLaXX3zBH3fM0oOKhPgUnC_StDRZdl5-tE-H264pVk3Td-JfMK1ywh8OMkGXLbld7ID5zYeU6uFJvFNOSeLvioCq00au2Bvz-l4ueD-lB-iUV8PRLNp7B5YRIHkgb5MxicpQOJS/s0/rmdhnreza.my.id.webtoon.downloader.6.png=s0?imgmax=0)

2. Mengunduh semua chapter yang telah dirilis mulai dari chapter 100 hingga chapter terakhir yang dirilis

```bash
$ webtoon-downloader "https://www.webtoons.com/id/fantasy/tower-of-god/list?title_no=749" --start 100
```

![Webtoon Downloader](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgDVC7Zg_4D44xpxZUh-cwhAraeUGW5Ekyj90NxHPHASXY7NwYAEtWjCq1xMgLTPSzN54yZQ0975rj_A6a9OQaXTCy3_Bbc1W0QIcP5Wwwi4Uuol1auSIx3OOY3Ilt09mGbjcGJCNKXF0qjTV-jQI3-rdsQq-QN7TDkGk1FCFBsmR-w_TEb5VP-76EiNfqZ/s0/rmdhnreza.my.id.webtoon.downloader.7.png=s0?imgmax=0)

3. Mengunduh semua chapter yang telah dirilis hingga chapter 6.

```bash
$ webtoon-downloader "https://www.webtoons.com/id/fantasy/tower-of-god/list?title_no=749" --end 6
```

![Webtoon Downloader](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjUXLcs68otZQojr-kHMRNII57WlW5qh-g5tX5m9zMX4DQzTMLanp2RaAc90AtueERZ4ubkLhujKFe8bsDoJzPpiTdX2LVuKCsKgdkR0VFwP9cERvQjPZlDUDuk8J6yjPgld1BPfyyD4sConKrSSn6u_YMtCH7ycqLk3gEKWARmW5rQ7sS4jhwLg1BSL91N/s0/rmdhnreza.my.id.webtoon.downloader.8.png=s0?imgmax=0)

4. Mengunduh semua chapter yang telah dirilis antara chapter 35 dan chapter 67, termasuk kedua chapter ini

```bash
$ webtoon-downloader "https://www.webtoons.com/id/fantasy/tower-of-god/list?title_no=749" --start 35 --end 67
```

![Webtoon Downloader](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgSZAwleIjnRMHYv5r7IKh-3UBgPR_uQ-J-IBALCCDkP34bpJ0amtLWzm2jtatk8Ortg3d0E6KQyb8nqoqvt6bSXc9Rphi-V49VxKHw3UNqVi1VqJ4tK6Hx7f0kvhCJP2jUvOe4tbLLeTc73sIMZn8sK0MeHxLPyQyUfCYB8RoV-7q9CN8GCGf5ahQ1BqKN/s0/rmdhnreza.my.id.webtoon.downloader.9.png=s0?imgmax=0)

5. Mengunduh hanya chapter yang dirilis terbaru dengan menggunakan `-l` atau `--latest`

```bash
$ webtoon-downloader "https://www.webtoons.com/id/fantasy/tower-of-god/list?title_no=749" --latest
```

![Webtoon Downloader](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgEoeWFV2hGC624ZSVyYF9toB-IIZmen3RcbZ4rF-OXlfYLHf1C30pfhNES_K3oWTpt1iSLCvDtgrpJr632KqaIXm071-mBq0uCUWC9NNIxU84UFYovhpe8XtTb_k5aQ0E-CxE4s8aQEjsqiMwT_d03oxp0rFMw9DJgwV1jKcZn3Udk3YeeERvNsPoVyNO5/s0/rmdhnreza.my.id.webtoon.downloader.10.png=s0?imgmax=0)

{{% adsense %}}

6. Kamu dapat mengubah format gambar yang diunduh dengan argumen `--images-format`

```bash
$ webtoon-downloader "https://www.webtoons.com/id/fantasy/tower-of-god/list?title_no=749" --images-format 'png'
```

![Webtoon Downloader](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEi8_SPvS62GKZMprjEquTdAMTFV4DMrXbqwYFrsDJc1QVUdxnpnHI1fsgC_k2jSvtwCTWYZeYJE-lIC64OJGjJ3NIN5e7FuSTb87QikaTHRDJ5vk5ixYOITSiXazSQtKg_qdD5hE2YDa2r3J2kg_LQUfbROf4DqK_RF3uPHPuz3wLp0Fzvj9XrAMytyhQ9z/s0/rmdhnreza.my.id.webtoon.downloader.11.png=s0?imgmax=0)

Secara default, chapter-chapter yang diunduh akan disimpan di bawah direktori kerja saat ini dengan nama folder [seri_judul].
Sebagai contoh, mengunduh `Tower of God`, chapter 150 akan menghasilkan tampilan sebagai berikut:
```md
Tower_of_God
    │--150_001.jpg
    │--150_002.jpg
    │--150_003.jpg
    │...
```
7. Untuk mengunduh gambar-gambar ini ke dalam folder yang berbeda, kamu dapat menggunakan argumen opsional `--dest`

```bash
$ webtoon-downloader "https://www.webtoons.com/id/fantasy/tower-of-god/list?title_no=749" --dest ./path/to/parent/folder/of/downloaded/images
```

![Webtoon Downloader](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgMxjoovhugutETMjMB48K-8_gDlmlIaWD1v-JrZA_z_kRwRNKu3bW1Nqp5kLQWE7HTVK7Eq78jr1i4aRU-noyJNJDaAv_7orlsajCGwndrrZ6Zt6TSyWr3EjZ85euCJDFxfLAeMDRwrwWKEfuJrjRhVKtYUuh2OrYhH-PDU5eqkH6WNSnQAqQRgRtRybZO/s0/rmdhnreza.my.id.webtoon.downloader.12.png=s0?imgmax=0)

8. Gambar-gambar yang diunduh dari chapter secara default berada di dalam direktori [dest], namun gambar-gambar ini dapat dipisahkan ke dalam direktori yang berbeda dengan memberikan argumen `--separate`, di mana setiap direktori berhubungan dengan chapter yang diunduh.

```bash
$ webtoon-downloader "https://www.webtoons.com/id/fantasy/tower-of-god/list?title_no=749" --separate
```

![Webtoon Downloader](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhZj47sDPe3WcEYWIltzN0T7Dvm3fsQd9R5eW8Wt-8N9L2HEbkbPuSZ-V6SNgKM9GvEo16ncuMuvebEAg_O1vwq6WwgXB98HUoCrAx8A3PI9swHDnXCjxW2CSc5JIkyC9RYKRu3bIqz6HoUILueeUcCKLk58sIuLTewjSn1DOUsTalr47-FmRRehy8QsEvA/s0/rmdhnreza.my.id.webtoon.downloader.13.png=s0?imgmax=0)

Sebagai contoh, mengunduh `Tower of God`, chapter 150 hingga 152 akan menghasilkan yang berikut ini

```md
Tower_of_God
    │150
        │--150_001.jpg
        │--150_002.jpg
        │--150_003.jpg
        │...
    │151
        │--151_001.jpg
        │--151_002.jpg
        │--151_003.jpg
        │...
    │152
        │--152_001.jpg
        │--152_002.jpg
        │--152_003.jpg
        │...
```

9. Kamu juga dapat mengekspor ringkasan, judul chapter, dan catatan penulis ke dalam file teks. Kamu dapat memilih format untuk output sebagai JSON (default) atau file teks biasa atau keduanya.

```bash
$ webtoon-downloader "https://www.webtoons.com/id/fantasy/tower-of-god/list?title_no=749" --export-texts [--export-format <json|text|all>]
```

![Webtoon Downloader](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiW_1XsMeAtjpmaBg8ukrOTm_ZEHevJ2Mr97cV8VvE-Qk4n6twcGHVAK7SSszjMIOAJW3ZkOaYPt5d1bg8bXwoZKY6giq37eNzEGczbHaDH6o5E7kUlYADimQACiyZQm2h2xlxbl9DFtzVHdNNRaEoAtnQGXPojTyCINDyD7AFhnMBdVnerWrQweYJVaZEp/s0/rmdhnreza.my.id.webtoon.downloader.14.png=s0?imgmax=0)

## Penutup

Sekian untuk tutorial cara mengunduh komik dari Webtoon, dan juga aplikasi ini hanya bisa mengunduh yang bisa dilihat di web, jadi untuk komik *daily pass* tidak bisa diunduh menggunakan aplikasi ini.

{{% adsense %}}