---
title: "Tutorial Cara Copy File dari Team Drive ke Google Drive"
date: "2020-11-24"
description: "Tutorial Cara Copy File dari Team Drive ke Google Drive Menggunakan rClone"
categories: ["Google Drive", "Tutorial"]
tags: ["Google Drive", "Tutorial"]
description: 'Pada tutorial kali ini saya akan membagikan cara copy file dari Team Drive ke Akun Google Drive, seperti yang kita ketahui sekarang Google Drive tidak bisa melakukan copy file secara langsung ke akun Google Drive kita sebagai gantinya hanya dijadikan shorcut saja alih-alih filenya dicopy ke akun Google Drive.'
summary: 'Pada tutorial kali ini saya akan membagikan cara copy file dari Team Drive ke Akun Google Drive, seperti yang kita ketahui sekarang Google Drive tidak bisa melakukan copy file secara langsung ke akun Google Drive kita sebagai gantinya hanya dijadikan shorcut saja alih-alih filenya dicopy ke akun Google Drive.'
image: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhwt-aIrDfkicVex80qrbDItqFfgyBTs2wC8x83xh6zK4tHZo1DNzL78bDUJpSn3HvlHnhbzQ01IsYCqkqYqiv_BSsdZvTqYWmKPJpbC8cwPreQ7ryVzxBU1LJev9XvWudfSxA_2GFvDAmuyF-JX9jKJJ0XBCLNJ4XqZFMi2WrfBmWjJHXepFRghbbM2eF4/s80-rw/Google_Drive_logo.png
ThumbSchema: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhwt-aIrDfkicVex80qrbDItqFfgyBTs2wC8x83xh6zK4tHZo1DNzL78bDUJpSn3HvlHnhbzQ01IsYCqkqYqiv_BSsdZvTqYWmKPJpbC8cwPreQ7ryVzxBU1LJev9XvWudfSxA_2GFvDAmuyF-JX9jKJJ0XBCLNJ4XqZFMi2WrfBmWjJHXepFRghbbM2eF4/s0/Google_Drive_logo.png
---

{{% adsense %}}

Pada tutorial kali ini saya akan membagikan cara copy file dari Team Drive ke Akun Google Drive, seperti yang kita ketahui sekarang Google Drive tidak bisa melakukan copy file secara langsung ke akun Google Drive kita sebagai gantinya hanya dijadikan shorcut saja alih-alih filenya dicopy ke akun Google Drive.

Disini saya akan menggunakan aplikasi bernama rclone untuk melakukan copy dari Team Drive ke Google Drive, perlu diketahui rclone ini bisa dijalankan pada Linux, Mac OS & Windows. Perlu diketahui disini saya menggunakan Sistem Operasi Linux. Oke langsung saja.

{{% adsense %}}

1. Download aplikasi rclone terlebih dahulu di official website nya [rclone.org](https://rclone.org)
2. Untuk pengguna Linux, Mac OS saya sarankan menggunakan perintah
```bash
curl https://rclone.org/install.sh | sudo bash
```
3. Untuk Pengguna Windows Saya sarankan kalian menginstall scoop terlebih dahulu yang bisa kalian lihat di [Cara Menginstall Package Manager Scoop Di Windows 10](/cara-menginstall-package-manager-scoop-di-windows-10/)
   * Gunakan perintah ini untuk menginstall rclone

```powershell
scoop install rclone
```

4. Jika proses installasi rclone berjalan lancar kalian bisa ketikan
```bash
rclone config
```
5. Jika tidak muncul error maka bisa langsung lanjut ke langkah selanjutnya

![Tutorial Copy File dari Team Drive ke Google Drive](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgx04PKdh0D8wFZHnsYJgeAfLag6HwahOXCARG4I05KSuHJ-eDHUOXAjfTjfZ4M2ep9Gvh4Ko87nQVzWS9nR34Ij06VPU8WYfiNXfFWwoB89wK2bjO9_DmwpoTYUXb1El7QRusON9VBjbWEiIKCaW8C8kDg7i3UxEkgidCpeOkSsNQ_FVl2wDwJq-dIyr67/s0/rcloneconfig1.jpeg)

{{% adsense %}}

## Konfigurasi TeamDrive
1. Ketikan perintah Lalu Enter
```bash
rclone config
```
2. **No remotes found - make a new one** > kalian pilih **n** untuk membuat remote
3. **name** > kalian buat nama remote kalian bebas, tapi saya sarankan jangan memakai spasi, disini nama remote yang akan saya gunakan **TeamDrive**

![Tutorial Copy File dari Team Drive ke Google Drive](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhlCnw6UXn2b7T3eD4ubJrMj-TfeXH-5gLosw_UKhAafTBAD-C0hlD6jxOkvbvgr0cw2TGpbSKSx8cjWZQRGtUvSzOD6WnVo_AX-Fkg8g8JjVe2DWW93eDLPpbLhf832HnONORHAsVfHglWt9ih_Ko7LcZ7Wc_ed3povwyaTJjmwLGJ23lR9oUuHta0v99_/s0/rcloneconfig2.jpeg)

4. **Storage** > kalian ketik "**drive**" (tanpa tanda "")
5. **client_id**, **client_secret**, kalian kosongkan saja
6. **Scope** > Kalian pilih nomor **1** (Full Access)
7. **root_folder_id**, **service_account_file** kalian kosongkan saja
8. Edit advanced config? pilih **N** atau bisa Enter langsung
9.  Use auto config?
    * Jika kalian pilih Y maka rclone akan otomatis membuka URL dan kalian tinggal masuk saja dengan akun Google yang memiliki Shared Drive
    * Jika kalian pilih N maka akan muncul URL di terminal dan kalian harus copy paste manual ke browser lalu masuk dengan akun Google yang memiliki Shared Drive setelah itu kalian copy code yang muncul di browser lalu paste di Terminal
    * Kesimpulan: Kalian bebas pilih yang mana saja yang menurut kalian paling mudah.
10. Configure this as a team drive? kalian pilih **Y**, ini adalah hal yang paling penting dalam konfigurasi akun Team Drive di rclone. jika kalian pilih N, Shared Drive kalian tidak akan muncul di rclone
11. Pilih Akun TeamDrive yang akan di copy filenya
12. Setelah itu kalian tinggal Enter dan Enter lagi, maka rclone akan kembali ke perintah 1

{{% adsense %}}

## Konfigurasi Google Drive
1. Sama seperti langkah Konfigurasi Team Drive, yang harus dibedakan adalah nama pada langkah nomor 3 disini saya menggunakan nama MainDrive dan Langkah nomor 10 kalian harus pilih **N**
2. Jika konfigurasi telah selesai kalian ketik q lalu Enter untuk Quit

![Tutorial Copy File dari Team Drive ke Google Drive](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiEWtrxwwRli6_zNKixEtWK06kS95kv0EatWN93hPhgeWqG7e4JNagE3Jf4bfWY74X9442WJu88FBZjyxUIPh13P5ufBq1TyHqGPr-h87MPzPPsKjXPsgk-Xb7JszbTmHOB5xuAY9KJlcao_iseT5G8ygVjZFreDCikvq4kuyxF-aoa_LeX6K1HqvtGfTGH/s0/path.jpeg)

{{% adsense %}}

## Melakukan copy dari remote TeamDrive ke MainDrive
1. Yang harus kalian lakukan pertama kali adalah share file (karena Team Drive untuk sekarang tidak bisa share folder) dari akun Team Drive kalian ke akun Google Drive yang akan meng-copy jika kalian tidak melakukan ini maka dipastikan akan error pada saat melakukan copy dengan rclone
2. Saya akan melakukan copy Video Running Man tahun 2010 di Folder (Perhatikan **PATH** nya) **RunningMan/2010**  ke Folder **2010** di Akun Google Drive

![Tutorial Copy File dari Team Drive ke Google Drive](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgpdkgOD2Ny_QwkfhaQ0bSZVbvbEaozptswpG9Ojh-6dQqIoJSB6DfwXtswhEmCQ_bX7qeHtMj-bgvsn6KUvasIzKEn_hf7VdWl_dox25XjfwToh9DEDZDuuohYo4D8U81CJAlIKzX9NPvfHPsBiAslPSDUsQYScCdL_EYLdH2mq2l_cajI7fRVIG-GjvNN/s0/rcloneconfig3.jpeg)

3. Jika sudah di Share langsung buka cmd, PowerShell atau terminal nya lalu ketikan perintah
```bash
rclone copy --progress --drive-server-side-across-configs NamaRemoteTeamDriveKalian:Folder/Yang/Akan/Di/Share NamaRemoteGoogleDriveKalian:NamaFolder
```
4. Dalam kasus saya perintahnya
```bash
rclone copy --progress --drive-server-side-across-configs TeamDrive:RunningMan/2010 MainDrive:2010
```

![Tutorial Copy File dari Team Drive ke Google Drive](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgz-cd7gwdytGOcOpTkiDZJTNpZM3vO9YNjCSzC4DvKh4c-mf_JhYhctKFoSfB1tNg_1J-B8EX2zaIfow0KduchLsRywljNGTxJ2OlQzZr-QHElz1snLmUm5A4NMHN82ss1WHmjAWPAnsNuqPbeMy1-Cge7blDHJ6q_4iiFZKKtwHq3_A8S-PnwkSaZ5X0j/s0/rcloneconfig4.jpeg)

5. Jika berhasil maka tidak ada error yang muncul dan kalian akan melihat progress copy filenya

![Tutorial Copy File dari Team Drive ke Google Drive](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEi3TW8jZBq-tOVPO0x174sPrNh7cwH2qiNxH8LjpjVHA5G41TWcWZVc93Tby5w4k77hrj22cv1RunD8JKJ9N-PpTzAXnf9724dj2UMR1eTrUgvv_kcYIJPhu7neXiyeCm9YVcBge5bLIutMQjPdIm849X2osuzFCyzjqdvjjarLOT7JA8u6NVySc_YnWG3w/s0/rcloneconfig.jpeg)

Jika kalian masih kebingungan kalian bisa tanyakan di kolom komentar, bingungnya dibagian mana, sebisa mungkin nanti saya akan bantu

{{% adsense %}}
