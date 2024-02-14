---
title: "Tutorial Menggunakan Rclone Untuk Upload & Download File Ke Dropbox"
date: 2021-03-11T15:36:16+07:00
description: "Tutorial upload dan download file menggunakan rclone ke dropbox dengan mudah"
categories: ["Linux", "rclone", "Tutorial"]
tags: ["Linux", "rclone", "Tutorial"]
description: 'Sebelumnya, ditutorial ini saya menggunakan Linux Ubuntu 18.04 dalam menggunakan perintahnya. Tapi tenang saja untuk Windows pun perintahnya sama hanya saja file rclone nya saja yang berbeda, jadi nanti kalian unduh file rclone nya sesuai dengan sistem operasi yang kalian pakai sekarang.'
summary: 'Sebelumnya, ditutorial ini saya menggunakan Linux Ubuntu 18.04 dalam menggunakan perintahnya. Tapi tenang saja untuk Windows pun perintahnya sama hanya saja file rclone nya saja yang berbeda, jadi nanti kalian unduh file rclone nya sesuai dengan sistem operasi yang kalian pakai sekarang.'
image: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEj69VMTLlXFZILr6JYR6ZN4iGMsSAEZztwGomFw_jb2o3lcAEbwo6vfBAWXNYdECI3im2LAIzVDomgOIEHhDbOPbxj5bC9cowHf4Ar8QeNTOg2YdePMVQzqfrnu7upSOA3ZMvG88R0XPp0aoSgnDoCKNj-GoEvz5DWV-NDeciLLtJD2xVEYEFEyNttnZ-G1/s80-rw/rclone-logo.png
ThumbSchema: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEj69VMTLlXFZILr6JYR6ZN4iGMsSAEZztwGomFw_jb2o3lcAEbwo6vfBAWXNYdECI3im2LAIzVDomgOIEHhDbOPbxj5bC9cowHf4Ar8QeNTOg2YdePMVQzqfrnu7upSOA3ZMvG88R0XPp0aoSgnDoCKNj-GoEvz5DWV-NDeciLLtJD2xVEYEFEyNttnZ-G1/s0/rclone-logo.png
---

{{% adsense %}}

Sebelumnya, ditutorial ini saya menggunakan Linux Ubuntu 18.04 dalam menggunakan perintahnya. Tapi tenang saja untuk Windows pun perintahnya sama hanya saja file rclone nya saja yang berbeda, jadi nanti kalian unduh file rclone nya sesuai dengan sistem operasi yang kalian pakai sekarang.

## Install rClone Sistem Operasi berbasis Linux
1. Untuk pengguna sistem operasi berbasis Linux, saya sarankan menggunakan perintah ini untuk menginstall nya, karena biasanya lebih up-to-date dibanding dengan versi apt (untuk Debian based)
```bash
curl https://rclone.org/install.sh | sudo bash
```
2. Kalian masukan password lalu Enter
3. Tunggu hingga proses installasi selesai

![Install rclone Linux](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhE7-XQX0vOgadbewu3Sr6KCxpeLxachUmodw0iZ8tpFgcSTphD_EotAvWqBcvTGNaJgVshfvtSIgipNm7KaTLZUVxQhYNfgepsOnXyM4m8s7-LaUavdG4BfnZkVTS2RGW2htAun6-9hqOxRKJPNq7OATzywxPkK2kDULzp5RqRJwM3v7EMtOZPEpFe-rIT/s0/rclone-install-1.jpeg)

## Install rClone Sistem Operasi Windows
1. Saya sarankan kalian menginstall scoop terlebih dahulu yang bisa kalian lihat di [Cara Menginstall Package Manager Scoop Di Windows 10](/cara-menginstall-package-manager-scoop-di-windows-10/)
2. Gunakan perintah ini untuk menginstall rclone
```powershell
scoop install rclone
```

![Install rclone Windows dengan scoop](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjDvOg1jZS_jdIseYJdr4Lt8WIWRuUSY7pdgPqJ2noSgN4hsjBCHr5KOzzrOxguJSfqz_xnUeev71spF66C0DFe37ilw4vs6JThkdqWiX37_rgX6XcmQz2pMIQSJjgKYgnBlycWw061Pg61eiY75eIIhhbq8sfUpKzuDDKExXw8yp8P8gq_Gt9GlGHqzoQP/s0/rclone-install-2.jpeg)

{{% adsense %}}

## Setup rClone
1. Kalian jalankan perintah
   * `rclone config`
   * Pilih `n`
   * Isi nama remote, disini nama remote saya yaitu **dropbox**
   * Enter
2. Pilih Storage, karena disini kita akan menggunakan storage dropbox, maka kalian isi nama storage nya **`dropbox`** (nomor 10)

![rclone config](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhDirKtO_XQjTdCIE2OYnnYsN7cHRgXKErHs73HB4aytN8LeSYAeDnsLAaNg0LTpo9mHib3vSWrbgkr75BuNYRCctVZ427jreU4RAsARc05rN8jeiwGdyAnCLZn8hH8v8huotlHwubIFXM8kv4D2INvARSqXi9PXNnGVi_3EEtDgtDOSSZsNeARfdGyBlXe/s0/rclone-config-1.jpeg)

3. **OAuth Client Id & Secret**, sebetulnya bisa **dikosongkan** jika kalian tidak mau ribet, tapi disini saya menggunakan **Client ID & Secret** saya sendiri caranya

{{% adsense %}}

## Membuat Client ID & Secret Dropbox
{{< spoiler text="Klik Untuk Membuka Spoiler" >}}

1. Kalian kunjungi [Dropbox App Console](https://www.dropbox.com/developers/apps/create)
2. Create App

![Dropbox Developer](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEidz3DCaRkusk4cfCNXxCwQ8laYkccabXGqGjmO-3y3GXGe0Yy_5dwwENThSznhh03qNi0unFBHOTCPRlBVvydUhzuuxih4CRO-ogR90umznSp77gUfzZ6VHw_bzsZu4N2CVDZ9_iycPOOo9y4_NbH3G-ZxQbtL5QsUioRpmm_nXjcsdtN9GwTP4uHlcv4a/s0/dropbox-api-1.jpeg)

3. **Choose an API** pilih **Scoped access**
4. **Choose the Type** of access you need pilih **Full Dropbox**
5. Name your app isi Bebas asal masih bisa dipakai
6. Create App

![Dropbox Developer](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhJ1ia4W_3m8FLeLSC06mMLhgxDsnEKcArAjCEX1LDO0MXGQEC5FYzhU1u3pknGZIJ4EgIR2WHGfqms_78b8p4Xe8j8ozCTSt8t12O0TmEzsalBeyuRBEf5RqA2k4OgIb4ghX1OrwdVhYOcpJKtEjUtfx0xhrxUikOmQO11r1X1mHXwDdKv612whxZ4bx6O/s0/dropbox-api-2.jpeg)

7. Dibagian Settings
   * Copy App key & App secret
   * Isi Redirect URIs dengan **http://localhost:53682**

![Dropbox Developer](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiGQgpmhCxBsg1Z2TKYsjizJ_ZOksvIAC-ig9t3y7QQrz8cA9VMGJptTvjYfHV4VbSQNFEWprSA4_LWW_RfRMihof_-pxCFpV0dd-2U302INlw-CnKjsFJfSzNBZFHLtd9prTijyKLP0z2znhlG638lcZ-zyTGDUn86OEe6b4c2UbtsiNVbZCqRTr_Tv3m2/s0/dropbox-api-3.jpeg)

8. Masuk ke tab Permissions, Kalian ceklis semua lalu Submit

![Dropbox Developer](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhRGsb3xdfpORn3XOevA9gBTxN0yt0Q8cjElKfeMScQRAjTz4Mmxh7I5my-EUJM1Vi87kevU7xRWnkg7QDm3FfU8Z3NLCCuzxt2GHlsAI18Vu6TqI1HhNkNBvIZAneipVX2TSX7CxiWjxfMIQRDvidPY2GJibvNI97YEEX-52vNxz4_vTdWuN5soBYgnt01/s0/dropbox-api-4.jpeg)

{{< /spoiler >}}

4. Isikan **client_id** dengan **App key** dan **client_secret** dengan **App secret**, sekali lagi ini hanya **optional**, kalian boleh kosongkan bagian ini

![rclone config](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhBSQWaTfj4zew_hDTbn7CcvdCFHRwpOZMFaeaVKivUoyxbFFbZYfMmRKLjPYEhKWJbDwKrU91qt8OREcBYwGjjXN6QwA8EK3oZ4XJEoshRQSPux5IW80VCFNVpa5lZfWJd1TlvwRFR7S0IU5rH0UtbeFKUGs57dibcmtYHZZKG9vYxHOlYG0DPszJgErXj/s0/rclone-config-2.jpeg)

5. Edit advanced config pilih `n) No (default)`
6. Kalian copy dan eksekusi perintah yang diberikan oleh aplikasi rclone di terminal atau powershell yang baru

![rclone config](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjEPvVNrYFzGDMSEM0qrlgAdTXEHuTfYIX42ehqbdmWAFxL5nlRKsfxiGwnGHi5omPpieCb4rzanx3UrK730k_y5eMS9tiBAonR8sIzntLly6O6k4C0L25q3MJGZwrYbIcz9S7nmqXN60G9tQpQY7GnwVO78uPWhZhnItCe9fsJeHdWEFt-g3JXuSRo6xO_/s0/rclone-config-3.jpeg) | ![rclone config](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjobFyOkaNyTdZtSdfeIa73SJuMWq2t4dicbeQ_lXZ_gd90J_c8yZtJid8qhYvqPwNAJdUR_Mf8B_8bG2wsOdEyQVDDCzeaMMWAs2Wv5p5BQlwbgAMJuEBO6xIuHKGzplAUf3ZIvmTGM5y157atiC_AA3Lz_HkhILK4tLVy18jz4DmcRyvUIggxqK-rdeyn/s0/rclone-config-4.jpeg)

7. Nanti kalian akan diberikan link local yang harus kalian buka di browser, buka link nya di browser
   * Kalian klik Continue
   * Klik Allow
   * Copy dan Paste Access Token (Lihat yang saya blok) ke Terminal yang pertama tadi lalu klik Enter

![rclone config](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEihvEEGI6vRZ1Ry6bdtdy0ythWTvO7VC8tLyijk3Te_lqLn6G-JuHW5dVRTLociv6HsxZigdZWvAasG-7DKSGIDxpkwQXJNu_3uOfnp15-o4E_mA_8msPhSQl7tuQsxEjpjCpB0XbJwtuR93ilauyLbCAEEJxQue1zxwwPLWNLkBMHQQFqXUiLgeJFLoato/s0/rclone-config-5.jpeg) | ![rclone config](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjBDwuTDGdfC45l1jD1lmNCETL245v12uOikyI-FK-J68WWpvM6XeJdJDBNYD4n6ja_4xOl1ktPw9cmfw_NrfuMPHjt7c1WoOk3gpf45dYUxRvPr7JiXHcnL5lfeC1I_gyUnchaJ_bKDVFSdi6ygnPVsMrihpdqck7hQXYIKmYKOUb9DRjzKtW6N2avxA2d/s0/rclone-config-6.jpeg) | ![rclone config](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEi3WPfeoxUGt0zx8tV77wtmPKskikaIpJ5NOW-dNWmWpYW2ZFrzh4b_qdVYO6jZmcR5N9VV0V6eGqIoNYVWQ0sVlaa11Od8kyo-Lmhl-aZ2Tsp2vr0FmSKehPJGYRyDRTyziwPd_tm-A9fMysYwBJZ_oocEqAGCr7tVn80Tn2tshivSf8ujUVKgIvq-hlCv/s0/rclone-config-7.jpeg)

8. Jika berhasil kalian tinggal pilih `y) Yes this is Ok (default)` dan Enter

![rclone config](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEg8E2XY8b_n1zB83u2c_-hoA_pIxQ8oSwWYAUlZXqyOS_2wsu-KOgGElKIUxem0UlicYoJRxJcLVnIymWKlTqTZbyuf8QQV3FXrGS8-algSXQwuzO4PXdqw81UygQjLIU_lNCRIawMYXSLJGjzJB2zuFBkkx7MXAWKktLrl0S-BxAC6ipP47yU6LRbmJx-m/s0/rclone-config-8.jpeg)

9.  Ketik `q` untuk keluar dari config rclone

![rclone config](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEj83baiFGHQgQl3o-eW22KamAhLSKixvJKVdY6xxoLRTuEqrT8ggj-vLgP5a0TR8WH2Fv3bf5kKBNVCuRh1bNsXkqa0rX1Sp7h8Zgd_6u6198xRwXGcALynORvheVyLabSc9c6ntBlOcM4JhngfEh0SBC4Ss-Rj-cfenXUhjGV2DY0o3w0nkVi4a2spkspf/s0/rclone-config-9.jpeg)

{{% adsense %}}

## Download & Upload file dengan rClone ke Dropbox
## Perintah rclone untuk upload
```bash
rclone copy --progress /path/file/ namaremote:path/file/di/dropbox
```
Disini saya contohkan akan upload file **Win10.ISO** yang path nya di **/home/rmdhnreza/Win10.ISO** ke **Folder WindowsISO** yang ada di **Dropbox**
Jadi, perintahnya seperti ini
```bash
rclone copy --progress /home/rmdhnreza/Win10.ISO dropbox:WindowsISO
```

![rclone upload file local ke dropbox](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiXdHtt0lvIFeiA07VmvXObEY2cPrU9bNj9tg7YA5Vwg17YyYGSjdlSeOVRLM3kAzGAF8-48nqG3Ot_cO6eUvGhXFmF1e32CyK_eSwziEPJk7tS4mB-8lnJMzboYdLkIEQXi3AQhipChL_m-6uYwzkVAfOOip9IWnugUt0LgaOc-fMWs86VdyrGYodpbsAm/s0/rclone-download-1.jpeg)

{{% adsense %}}

## Perintah rclone untuk Download
```bash
rclone copy --progress namaremote:path/file/di/dropbox /path/file/
```
Disini saya contohkan akan download file **Win10.ISO** yang path nya di **dropbox > WindowsISO/Win10.ISO** yang ada di **Dropbox** ke **Folder Home Directory saya**
Jadi, perintahnya seperti ini
```bash
rclone copy --progress dropbox:WindowsISO/Win10.ISO /home/rmdhnreza/Win10.ISO
```

![rclone download file dropbox ke local](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEisa9N7sqeEwl27xJWGmwUZqynTC0Qt07D-TCthwOq8ai8xu5sGa3NLhIbfdEx80SoZgaHohZREbISbqTnhCHr-6JctUIqm9mBmeoBQ2jWflTdxhAvKV5WQbx9Zout3wYD2pFvLIc1rHX1by7lEoFPOu9SLJkZAnN3TzucOMpIxNmzaC23J_hk5o4ZeLHKU/s0/rclone-download-2.jpeg)

Itu tadi adalah cara mudahnya download dan upload file menggunakan rclone ke dropbox, jika kalian masih bingung dengan perintah-perintah nya kalian bisa lihat langsung di [Rclone Wiki](https://github.com/rclone/rclone/wiki) untuk lebih lengkapnya.

{{% adsense %}}
