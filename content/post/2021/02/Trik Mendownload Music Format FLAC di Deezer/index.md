---
title: "Trik Mendownload Music Format FLAC Di Deezer"
date: 2021-01-08T14:47:05+07:00
description: "Trik Mendownload Music Format FLAC Di Deezer menggunakan Deemix"
categories: ["Deezer", "Tutorial"]
tags: ["Deezer", "Tutorial"]
description: 'Tutorial kali ini saya akan membagian trik mengunduh dari deezer dengan bitrate FLAC menggunakan aplikasi atau tools berbasis python.'
summary: 'Tutorial kali ini saya akan membagian trik mengunduh dari deezer dengan bitrate FLAC menggunakan aplikasi atau tools berbasis python.'
image: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjege8fXLWWu-IBbAQqfDyHI3zEcjXEaMEqrr2EaAx5bl3qu8HIlgftAd_0Zarz8EfEY_pZgGpSgo4ennwqk6yqto2OKEnWbHeLjCm-prAVtJrgfqx9_NFoPIg56E0PYrdeoCDmB9BHIU5yKVKsNeK_n9nGOOPpmCFd18xT6Brer_Pzd9eNTuYwNECPDzi7/s80-rw/deezer-logo.png
ThumbSchema: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjege8fXLWWu-IBbAQqfDyHI3zEcjXEaMEqrr2EaAx5bl3qu8HIlgftAd_0Zarz8EfEY_pZgGpSgo4ennwqk6yqto2OKEnWbHeLjCm-prAVtJrgfqx9_NFoPIg56E0PYrdeoCDmB9BHIU5yKVKsNeK_n9nGOOPpmCFd18xT6Brer_Pzd9eNTuYwNECPDzi7/s0/deezer-logo.png
---

{{% adsense %}}

Tutorial kali ini saya akan membagian trik mengunduh dari deezer dengan bitrate FLAC menggunakan aplikasi atau tools berbasis python. Jadi untuk kalian yang belum terinstall python3 di sistem operasi nya pastikan kalian install dulu python3 nya yang bisa di download di python.org/downloads/. Tips mengetahui python3 sudah terinstall di sistem operasi kalian caranya sangat mudah, untuk kalian pengguna sistem operasi Linux, MacOS kalian tinggal buka terminal saja dan untuk pengguna Windows kalian buka Powershell lalu ketikan perintah
```bash
 python3 --version
```
Hasilnya akan seperti ini, di sistem operasi saya yang terinstall python3 versi 3.6.9. Oke kita langsung saja mulai tutorialnya.
![Cek Python Version](https://1.bp.blogspot.com/-A7KDhUmMzUU/X3c5bYisZHI/AAAAAAAACq8/G7mrtAkLjYYTUcZOprTU_BEMm3Eg7Q4vQCLcBGAsYHQ/s0/python3.jpeg) alt="Cek Python Version" >}}

{{% adsense %}}

## Tanpa Git

1. Kalian download dulu source code nya dari [git.rip/RemixDev/deemix-pyweb](https://git.rip/RemixDev/deemix-pyweb) lalu extract
2. Kalian masuk ke folder **deemix-pyweb** nya lalu buka Terminal untuk sistem operasi Linux, MacOS dan Powershell untuk sistem operasi Windows lalu ketikan perintah

```bash
 python3 -m pip install -U --user -r requirements.txt
```

![Trik Mendownload di Deezer.com](https://1.bp.blogspot.com/-Jx9tty-lkkE/X3YsHLec62I/AAAAAAAACo4/wGBJGL92880guXZ9IRy-KQiPRMBijWTGgCLcBGAsYHQ/s0/3.jpeg)

![Trik Mendownload di Deezer.com](https://1.bp.blogspot.com/-uP6PfAsBDGo/X3Ysy0tEBrI/AAAAAAAACpM/D9Kl5LbEBEcJS68lsv3cuDYz7sbKOHLdwCPcBGAYYCw/s0/4.jpeg)

3. Jika semua package nya sudah terinstall kalian download **deemix-webui** dari [git.rip/RemixDev/deemix-webui](https://git.rip/RemixDev/deemix-webui) lalu extract dan rename folder nya dari **deemix-webui** menjadi **webui** setelah itu cut/pindahkan folder nya ke folder **deemix-pyweb** yang kalian download dilangkah 1. Jadinya seperti ini didalam folder **deemix-pyweb**

![Trik Mendownload di Deezer.com](https://1.bp.blogspot.com/-tru5MPm4Oo8/X_gT5cVDCHI/AAAAAAAACzw/AHXYZ2_wxW8Xn0gEmptN9u9KzcUXuGiSACLcBGAsYHQ/s0/webui.jpeg)

4. Di Terminal atau Powershell kalian ketikan perintah untuk menjalankan deemix nya

```bash
 python3 server.py
```

5. Setelah itu akan muncul link http://127.0.0.1:6595 dan kalian buka link nya di browser

![Trik Mendownload di Deezer.com](https://1.bp.blogspot.com/-3gS2ROUCwAs/X3YslVSP1dI/AAAAAAAACpE/R70y5HMCD0IvR684Q8MGflSYPek2w-XzwCLcBGAsYHQ/s0/6.jpeg)

{{% adsense %}}

## Menggunakan Git

1. Kalian clone repository dengan dengan perintah

```bash
 git clone https://git.rip/RemixDev/deemix-pyweb.git
```

2. Kalian masuk ke folder deemix-pyweb nya lalu buka Terminal untuk sistem operasi Linux, MacOS dan Powershell untuk sistem operasi Windows lalu ketikan perintah

```bash
python3 -m pip install -U --user -r requirements.txt
```

![Trik Mendownload di Deezer.com](https://1.bp.blogspot.com/-Jx9tty-lkkE/X3YsHLec62I/AAAAAAAACo4/wGBJGL92880guXZ9IRy-KQiPRMBijWTGgCLcBGAsYHQ/s0/3.jpeg)

![Trik Mendownload di Deezer.com](https://1.bp.blogspot.com/-uP6PfAsBDGo/X3Ysy0tEBrI/AAAAAAAACpM/D9Kl5LbEBEcJS68lsv3cuDYz7sbKOHLdwCPcBGAYYCw/s0/4.jpeg)

3. Jika semua package nya sudah terinstall kalian clone juga webui nya dengan perintah

```bash
 git submodule update --init --recursive
```

![Trik Mendownload di Deezer.com](https://1.bp.blogspot.com/-GcWharjIILs/X3YtwePP-VI/AAAAAAAACpY/Pc5GoMi0ihQbYTD8XYDp3vqeqvHW2L0pwCLcBGAsYHQ/s0/5.jpeg)

4. Di Terminal atau Powershell kalian ketikan perintah untuk menjalankan deemix nya

```bash
 python3 server.py
```

5. Setelah itu akan muncul link http://127.0.0.1:6595 dan kalian buka link nya di browser

![Trik Mendownload di Deezer.com](https://1.bp.blogspot.com/-3gS2ROUCwAs/X3YslVSP1dI/AAAAAAAACpE/R70y5HMCD0IvR684Q8MGflSYPek2w-XzwCLcBGAsYHQ/s0/6.jpeg)

{{% adsense %}}

## Cara Mendapatkan ARL Google Chrome / Chromium Based Browser

1. Kalian akses [deezer.com](https://www.deezer.com) dan login
2. Kalian klik **icon gembok** pada address bar dan pilih **Cookies**

![Trik Mendownload di Deezer.com](https://1.bp.blogspot.com/-YHuRX7MFkMc/X3YuLj-gBEI/AAAAAAAACpo/08Ns9cidoS0ihEn1jFbdkDhGq3N_BeTVACLcBGAsYHQ/s0/chrome1.jpeg)

3. Pilih **deezer.com** pilih **Cookies** lagi

![Trik Mendownload di Deezer.com](https://1.bp.blogspot.com/-mIC5_u7YXgA/X3YuRVH2srI/AAAAAAAACpw/C3H5OuOpnSg6SSXrt-1KpszMOX1yWU5-ACLcBGAsYHQ/s0/chrome2.jpeg)

4. Disana kalian cari **arl** dan copy **content** nya dengan cara klik 2x lalu **CTRL+C**

![Trik Mendownload di Deezer.com](https://1.bp.blogspot.com/-ukA-f1Trcs0/X3YuW9w5h5I/AAAAAAAACp0/jUvWCErHC2YMl4lZ9oXGSxrh0YARJIHxQCLcBGAsYHQ/s0/chrome3.jpeg)

{{% adsense %}}

## Cara Mendapatkan ARL Firefox / Gecko Based Browser

1. Kalian akses [deezer.com](https://www.deezer.com) dan login
2. Kalian klik kanan dan pilih **Inspect Element** atau dengan menggunakan shortcut **CTRL+SHIFT+I**

![Trik Mendownload di Deezer.com](https://1.bp.blogspot.com/-Yw3deFdtKCk/X3Yt5GLdLeI/AAAAAAAACpc/hMwz1R83Oko808p6SBXTpdzMyCh2HbVUACLcBGAsYHQ/s0/8.jpeg)

3. Masuk ke tab Storage pilih Cookies pilih https://www.deezer.com, disana kalian akan melihat **arl** dan kalian copy **value** nya dengan cara klik 2x lalu **CTRL+C**

![Trik Mendownload di Deezer.com](https://1.bp.blogspot.com/-t5a7zFAAdUM/X3Yt-_R59LI/AAAAAAAACpg/uvvZMB1vXTIxRxo_nQZyITRcmT_bg1MCwCLcBGAsYHQ/s0/9.jpeg)

{{% adsense %}}

## Mendownload Music
1. Setelah mendapatkan **ARL**, kalian **Open Settings**

![Trik Mendownload di Deezer.com](https://1.bp.blogspot.com/-ezlDk1XAx94/X3YuemqsHaI/AAAAAAAACp8/QSOi-br_bS8cyyNE3t3ZTvpii8sT3vuowCLcBGAsYHQ/s0/7.jpeg)

2. Masukan **ARL** yang kalian dapatkan tadi di kolom **ARL** nya, lalu kalian **UPDATE**, Jika tidak ada error, maka **username deezer** kalian akan muncul

![Trik Mendownload di Deezer.com](https://1.bp.blogspot.com/-_Ysj3nSD9Wc/X3Yuka9ZW7I/AAAAAAAACqA/UlR4zDCfLCY2XtxY7VxFtv2yDDStFplPQCLcBGAsYHQ/s0/10.jpeg)

![Trik Mendownload di Deezer.com](https://1.bp.blogspot.com/-3OXncrO816I/X3YuuR2wdRI/AAAAAAAACqM/3bneCqGgxocHhm2Zs4_xyjocNgT7mfaOQCLcBGAsYHQ/s0/11.jpeg)

3. Scroll kebawah sampai bagian **Downloads** lalu ubah **Preferred Bitrate** mnejadi **FLAC**

![Trik Mendownload di Deezer.com](https://1.bp.blogspot.com/-PS6RNpj9wGY/X3Yu0qlGfyI/AAAAAAAACqU/paF8xTDD5oIMWTs1lUrCwJKUymH6YLBCgCLcBGAsYHQ/s0/12.jpeg)

4. Kalian klik **Save**
5. Setelah itu kalian bisa klik **Search** untuk mendownload Music yang kalian ingin download dengan format **FLAC**

![Trik Mendownload di Deezer.com](https://1.bp.blogspot.com/-cXGrMftzm7A/X3Yu6tJfj2I/AAAAAAAACqY/caM_2uI0NOo2zns3V1sjdbi_QalaFy8WQCLcBGAsYHQ/s0/13.jpeg)

{{% adsense %}}
