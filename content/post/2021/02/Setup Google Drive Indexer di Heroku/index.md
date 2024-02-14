---
title: "Setup Google Drive Indexer di Heroku"
date: "2020-11-25"
description: "Setup Google Drive Indexer di Heroku"
categories: ["Heroku", "Google Drive", "Tutorial"]
tags: ["Heroku", "Google Drive", "Tutorial"]
description: 'Google Drive Indexer memudahkan kalian untuk share file dari akun Team Drive untuk di unduh oleh orang lain, karena Team Drive sendiri tidak support share folder maka Gdrive Indexer ini solusinya. Perlu diketahui Gdrive Indexer ini support drive dan juga Team Drive.'
summary: 'Google Drive Indexer memudahkan kalian untuk share file dari akun Team Drive untuk di unduh oleh orang lain, karena Team Drive sendiri tidak support share folder maka Gdrive Indexer ini solusinya. Perlu diketahui Gdrive Indexer ini support drive dan juga Team Drive.'
image: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhwt-aIrDfkicVex80qrbDItqFfgyBTs2wC8x83xh6zK4tHZo1DNzL78bDUJpSn3HvlHnhbzQ01IsYCqkqYqiv_BSsdZvTqYWmKPJpbC8cwPreQ7ryVzxBU1LJev9XvWudfSxA_2GFvDAmuyF-JX9jKJJ0XBCLNJ4XqZFMi2WrfBmWjJHXepFRghbbM2eF4/s80-rw/Google_Drive_logo.png
ThumbSchema: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhwt-aIrDfkicVex80qrbDItqFfgyBTs2wC8x83xh6zK4tHZo1DNzL78bDUJpSn3HvlHnhbzQ01IsYCqkqYqiv_BSsdZvTqYWmKPJpbC8cwPreQ7ryVzxBU1LJev9XvWudfSxA_2GFvDAmuyF-JX9jKJJ0XBCLNJ4XqZFMi2WrfBmWjJHXepFRghbbM2eF4/s0/Google_Drive_logo.png
---

{{% adsense %}}

Google Drive Indexer memudahkan kalian untuk share file dari akun Team Drive untuk di unduh oleh orang lain, karena Team Drive sendiri tidak support share folder maka Gdrive Indexer ini solusinya. Perlu diketahui Gdrive Indexer ini support drive dan juga Team Drive.

Pada tutorial kali ini Gdrive Indexer akan kita pasang di Heroku, jadi buat kalian yang tidak punya akun heroku harus buat dulu di heroku.com, jika kalian sudah membuat akunnya langsung saja kita mulai pemasangannya.

{{% adsense %}}

## Setup Heroku

1. Klik link berikut ini [Deploy to Heroku](https://heroku.com/deploy?template=https://github.com/patheticGeek/gdrive-index)
      * **App name** kalian bebas apa saja asal masih tersedia di heroku nya, app name ini yang akan menjadi subdomain link kalian
      * **Region** kalian bebas mau di US atau EU

![Heroku Google Drive Indexer](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgkcOUnDbn5maJ6uf6O37zX3WRNXK4fjK0eQi8mVU9ZHF4BgeI85nZeybZt8bQYsbyhsWyNNs2deRHL8zWUbkSc1d7n1ALAh4UrLX6GHp3U1jLg2diCMlaEIQ51eC9gpgCkzsPUJN0kc-1Hz2SgmIqjV9L7XsnsW-fg4utEdJ2Kdyyw4ck08IBkzbPZfMmj/s0/1.jpg)

2. Setelah semuanya selesai kalian klik Deploy app & tunggu beberapa menit sampai prosesnya selesai

![Heroku Google Drive Indexer](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjwySZk2nM7DrWlHYVmcF6FfVwGVhUieLXiMhBMxqwjbLiPLmjpQ701CgjMBLuNzg9eqeEETgWspME6zpuIw5O_ol-0414Q6fujykRhccFjV6uquhNi1w8VqSZFFNmXyXMwrWNEJH7b8M5N3ple2CscyUC17HuTv16OMJxJR4DJn2x5sA-wK4Cywnx1hAqO/s0/2.jpg)

3. Jika proses build nya sudah selesai kalian klik Manage app masuk ke bagian **Settings** dan klik **Reveal Config Vars**

![Heroku Google Drive Indexer](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhnaRGg-f1pErXXIXJf9z1d43ZjUmGylX8PLnBFi_1-14KHj5G4quvf9854REEEDuDGcHb-mlCbOGNudz_Gq03pOYURp5IK1DlNc32RlLPFa9jHhL4Gia-34t8_EESLJj6Mp_hXnFOk-zzxSe11YooC4Ur0o5Q72dgGqAAtVbX1bDwACH836_WEt35y8tNd/s0/3.jpg)

4. Isi bagian **KEY** dengan **AUTH** sedangkan **VALUE** nya kosongkan saja klik **Add**
5. Buka project kalian https://appname.herokuapp.com/setup ganti **appname** dengan **appname** yang kalian buat dilangkah pertama
6. Jika sukses maka tampilan app kalian akan seperti ini

![Heroku Google Drive Indexer](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEibJTbOrDV_0YFZzaacuL1S9okMlHn-tF9MtGHKr_5W3wlJKlPVUeAKTMdMYQY5rWh0Ypzmt2JImG5mb1ztwdFjs1orgBcEjFq9uJMNYmgKCELwP-c0DeenEYPudcWyiGzKiPPTbih0R1jFojKtKCqHyvdlt2JRaRbs42JwciU6ko1HS5Et-isdXmPZlxsc/s0/4.jpg)

{{% adsense %}}

## Membuat Client & Secret ID

7. Buka [developers.google.com/drive/api/v3/quickstart/nodejs](https://developers.google.com/drive/api/v3/quickstart/nodejs) Klik **Enable Drive API** Login dengan akun Google kalian. Jika kalian sudah masuk tinggal isi **Project Name** bebas setelah itu Next maka akan muncul **Configure your OAuth** client kalian pilih **Desktop App** jika sudah langsung klik **Create** maka kalian akan mendapatkan **Client ID** & **Client Secret**

![Heroku Google Drive Indexer](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEh-bEnnvzuJPIvLi9cYVXynsQg7mwqdl6_IrrxQ685dHCfEi-NGLngEKq7ImIXme_KEYn_4glq4YueI76xV6KgXSIifki-zcJv28qb1BdMqoATLNuR3d931HNLVqWgECMQBmtF70o_QIBiSYnMGei8hyphenhyphenpwJ1s5xO3ki_eBM8Hfp2umfLzSJT0fu8RNc2IFn/s0/enabledriveapi.jpg)
![Heroku Google Drive Indexer](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEh3EQAUoLXcbmPIad3yjaTN-rSdbkK5cGKJsS-yguRT9opRkomLE7p_6qBrWvTeMT9eYJUxcc6GmQWokqCBxB8oSfrWI6CfbFbathcv2_doX_sw6YCNXoRQs_Dp8q8qpT36xLjbSQ1FBXgq0LdGY2Hyp-TEoNFrOKUQ4viFsSlZjzBSVKwxv0Z_LJ7H4rBC/s0/enabledriveapi1.jpg)
![Heroku Google Drive Indexer](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEg-RMODCnOMW_DkzMojamgvtvsnoMalQ-ZpISsWPLA1N1ioi3N6Sp3qsFeQUl2n0JNmdL99yu2EzGi8K7pQfthCnxJdgVnRGN6YG_rwMoDjXskRQ5smHqfM-slrL0ypl1Cpy1rPnnOzmI4nu176RNJkPWUpI7yWyHGbuQE3yb_e7hkyZ-98yP_hB3MyPSkf/s0/enabledriveapi2.jpg)

8. Copy **Client ID & Client Secret** ke app kalian (langkah nomer 6) setelah itu **Get Auth Code**, akan otomatis membuka tab baru dan kalian masuk dengan akun Google kalian sampai mendapatkan code nya

![Heroku Google Drive Indexer](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEg7Ss6o_2ajFSKJ1mYEk1mW7aFEiRAY0FCRXDhSOiLT2F3e14X6u_TFkg8vdve5WLiz3LoJ7hrfBQ4AnTHbSYCFNor8gqxNIb42f3AkEQZynAkeiov53-e8kKBwXVZAGi5pWpVSOss60if-y9mweit27eJS8TlEWwhtDv5RJZCkhBILp5XyzoRkJ3hk8niP/s0/5.jpg)
![Heroku Google Drive Indexer](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjo0K61LPXdW9ngPnRwYpyuGBKRcW7w7hs5gTZADT-fuVQaDDXbYYvm7DoafPtX4bpZ6Nlao5bYJHtPuZmsTiYz1_qmH1LKR5mKmOlKaqUgqrzWzX-anyYEDv2T0uzYQufLJZJC9mBZncBkd8FSanWoNC87Umtyla6AHxXMdf_xsdshFR1gZuZC52aJBzyY/s0/enabledriveapi4.jpg)

{{% adsense %}}

9.  Paste Code pada kolom Paste auth code here lalu klik Generate token maka akan muncul akses token-nya
10. Untuk **Parent Folder ID** ini opsional tapi saya sangat sarankan untuk diisi, disini saya akan menggunakan **Shared Drive** jadi saya isi ID nya dengan ID folder shared drive saya
      * contoh: https://drive.google.com/drive/folders/**0ANKV19DAKsAKdsRUk9PVA**
      * Kalian hanya copy bagian **0ANKV19DAKsAKdsRUk9PVA** saja dan paste di Parent Folder ID
11. Untuk bagian Auth kalian boleh isi atau tidak, tapi untuk keamanan saya sarankan kalian isi.
12. Langkah selanjutnya kalian tinggal copy paste pada tabel Enviroment variables ke config app kalian (langkah nomor 4)

![Heroku Google Drive Indexer](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhYF0XzZ3I-b6m_R9yam_C1n1hqu4MetCYMycJAUTjVvUr_QnQoPAe3xZSAv80OrvqI00iPiDOkpcbIKOepPA8TtqOg-5UxzPpzadWGrfxOc9C-b_uzFdBNbsMoJvSay8E7-Z2uNl6obj_7dZL7LgRu2vp5rvUXymOq5jEOhnZlVAzrBOI8gnmNg5j8SPnS/s0/enabledriveapi5.jpg)

13. Jadinya seperti ini

![Heroku Google Drive Indexer](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEi8eRzWscH3HNY4gmxn5jlLYsWnnDOW2JDho3Of03I-5QQSBU4Pf_le8SGa8tBPzm_hnLT1mZVKMMtndI_sVWx7PrTW_nved0PNyNd0G8MsD5hdLZVVHhXN1FQiPqXu07CKg-pQJSeT6hetEuwDYRm0K3EGSAH3KsYlfW90MU9ARFnh2i4thdIxoxR5wWOi/s0/6.jpg)


14. jika sudah kalian tinggal buka https://appname.herokuapp.com

![Heroku Google Drive Indexer](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEh-DR7Sk07rjZ7B47lH3Ok_4RXVJKikEkYKBnQ-E_wcd_bC0nOSCoXXjs2jUI2bMIS6kLXhwDiQDoYYU4fGvw5SrnirSM8IBFlqZsQekSmU9PqRhqlWFSqcOG2BFBR2f6GvXvnLBbyOn6HSJPkWPJHwZmtEZnhsr_fjVWO8C2zK2NX3HlgC3k6dA5IcvDeI/s0/7.jpg)

![Heroku Google Drive Indexer](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhX9zmCjzUzqVPKTUEdbXyFzP5GgjkAtsgoek4nr4D0OElTyvJvrE4acp7GoZ9q0pYSqJX-eL6YJgEcJSkSq1aHatKSVfi81lcPLtyJ6BVjjZCFrQKSQs0fGrR6slF8ztXYGuc2uVGfTMR-NH1lkpTKMjJ7jDSDUmcjnMxQJutCBQXObEj-CymWpXy39IV-/s0/8.jpg)

15. Itulah langkah-langkah setup Google Drive Indexer di Heroku, jika kalian kesulitan dalam pemasangannya kalian bisa tanyakan di kolom komentar


{{% adsense %}}
