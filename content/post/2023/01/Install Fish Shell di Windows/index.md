---
title: 'Install Fish Shell di Windows 10/11'
url: "install-fish-shell-di-windows-10-11"
date: 2023-01-20T15:30:13+07:00
description: 'Tutorial Install Fish Shell di Windows 10/11'
categories: ['Tutorial', 'Windows']
tags: ['Tutorial', 'Windows']
keywords:
  [
    'Install Fish Shell di Windows 10/11',
    'Tutorial Install Fish Shell di Windows 10/11',
    'Cara Install Fish Shell di Windows 10/11',
    'How to Install Fish Shell on Windows 10/11',
  ]
description: 'Tutorial Install Fish Shell di Windows 10/11'
summary: 'Tutorial Install Fish Shell di Windows 10/11'
image: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEisicyW-w1Bv23AhvpAG2W55KaQ7GAAPFZVVxQedvViaQH4h22oCvx6mXIBp3SjVc_ovqKrKD-swXYrRokbt_A0MwxGwjDkLhpaBHt_EyD4p2nbMS2qJjLT54Yv7xkQeXnmTiL7mBrGflRSHQwLBKufrsRFmEg_KTkumd-03DGjYcIIE-3dqd-lTduJjKU5/s80-rw/fish-shell-logo.png
ThumbSchema: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEisicyW-w1Bv23AhvpAG2W55KaQ7GAAPFZVVxQedvViaQH4h22oCvx6mXIBp3SjVc_ovqKrKD-swXYrRokbt_A0MwxGwjDkLhpaBHt_EyD4p2nbMS2qJjLT54Yv7xkQeXnmTiL7mBrGflRSHQwLBKufrsRFmEg_KTkumd-03DGjYcIIE-3dqd-lTduJjKU5/s0/fish-shell-logo.png
---

{{% adsense %}}

Sebelumnya saya sudah pernah bahas [Cara Install Oh My Zsh di Windows 10](https://rmdhnreza.my.id/cara-install-oh-my-zsh-di-windows-10/). Kali ini kita akan bahas lagi tutorial cara install **Fish Shell** di sistem operasi berbasis Windows. Sama seperti [Cara Install Oh My Zsh di Windows 10](https://rmdhnreza.my.id/cara-install-oh-my-zsh-di-windows-10/) tutorial ini pun menggunakan **Git for Windows**

## Install Git for Windows

1. Install [Git for Windows](https://git-scm.com/download/win) sesuai dengan sistem operasi yang kamu pakai apakah 32/64 Bit, jika kalian menggunakan [scoop](https://rmdhnreza.my.id/cara-menginstall-package-manager-scoop-di-windows-10/), kalian bisa lewati langkah ini.

## Install Pacman

2. Download [pacman](https://packages.msys2.org/package/pacman?repo=msys), [pacman-mirrors](https://packages.msys2.org/package/pacman-mirrors?repo=msys) & [msys2-keyring](https://packages.msys2.org/package/msys2-keyring?repo=msys) dari situs MSYS2. Selain itu, agar `Fish` dapat dijalankan, kalian perlu mengunduh [gcc-libs](https://packages.msys2.org/package/gcc-libs?repo=msys&variant=x86_64) karena menggunakan `msys-stdc++-6.dll`

3. File-file tersebut dalam format zst. Untuk melakukan *extract* ke format tar, bisa menggunakan [zstd versi windows](https://github.com/facebook/zstd/releases), untuk pengguna [scoop](https://rmdhnreza.my.id/cara-menginstall-package-manager-scoop-di-windows-10/) kamu bisa menggunakan perintah `scoop install zstd` untuk menginstall [zstd](https://github.com/facebook/zstd/releases) setelah aplikasinya terinstall [zstd](https://github.com/facebook/zstd/releases) nya, jalankan perintah berikut ini dari cmd/powershell `zstd -d *.zst` berhasil di *extract* akan muncul 4 file baru dengan format tar.

1             |  2
:-------------------------:|:-------------------------:
![Figure 1](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhIZH4s5ADlUHeqgAnD8qr8hhtQg3hqxfX6k4ElWiwLSrPt8q0H-laHkglkNbXH2s4F4A2MCZlFrKgSN0eK6cofScTv3ddw4thvqHKer1YGgYcJfMX6mxBeI5Ks8xEKVu89kdm9BC8TLLLuFEGdHJZi1KdQvv-MolFFY9Ql097Ss_uPn-sadqD9bWuo3lBL/s0/rmdhnreza.my.id.install.fish.shell.windows.1.jpg) | ![Figure 2](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgycPyWO2uJH7d5waC84MapP_jDSYfFTFUmZFFaWDiz7dBzgF7h7KhYdbg7gV4-ExUJWYFvMWn2AH7Jw2e3MYOCTUZ1M_EDgs51Bd1A0b0KaIPbYJaNI2OIhXnpkiTtv1fBkdHg8QIoM1cVqi2yhWaLHQfyBh8OOg49GqNXnx0MigpFBqWYZ6zfRi-7oXkZ/s0/rmdhnreza.my.id.install.fish.shell.windows.2.jpg)


4. Sekarang kita buka **Git Bash** nya dan jalankan perintah dibawah ini untuk *extract* file tar ke **Git Bash**

```md
cd /
tar -xvf ~/Downloads/msys2-keyring-1_20210213-2-any.pkg.tar
tar -xvf ~/Downloads/pacman-mirrors-20210423-2-any.pkg.tar
tar -xvf ~/Downloads/pacman-6.0.0-2-x86_64.pkg.tar
tar -xvf ~/Downloads/gcc-libs-10.2.0-1-x86_64.pkg.tar
pacman-key --init
pacman-key --populate msys2
pacman -Syu
```

{{% note %}} Pastikan PATH untuk file tar nya benar! {{% /note %}}

{{% adsense %}}

1             |  2
:-------------------------:|:-------------------------:
![Figure 3](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgUaRWxrv0G26RzPs4PpZRvGnZXHMmdRjH8IUH3Jvy7Nn5O8fuj4gEnliioAfKaZj3JZ07VYmsKsHiRmiUE_UYcjH9mYeLBlzuUaC5KGDzlGZKaUwuBemjUNO23XvF-vBobskflGRgQfTVh4c0C31-qqtYv3ndj6EEmClxAeitp9PSr2NzY6C_C_s9pDi7z/s0/rmdhnreza.my.id.install.fish.shell.windows.3.jpg) | ![Figure 4](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjAuuWP07xIKaeuZDGZcUE1ykwuzDqmnDoZ6YNrRwUbSbnaOoWMY2M3xqW6PuwsdNogjX0dCx36mCHAvJDme1EJKxlP8smtD2bUTg-R71V833dVxWST0sAillUwYu7TT-Ged0BqV4LV2qB2UQyy2uEqcG2gd0lvCALiy_nLQebjFjYeMhi5N0eb8_V8AgUD/s0/rmdhnreza.my.id.install.fish.shell.windows.4.jpg)

5. Untuk menyinkronkan file metadata, kamu perlu menjalankan perintah di bawah ini. Langkah ini memerlukan waktu beberapa menit untuk menyelesaikannya tergantung pada kecepatan internet kamu juga.

```bash
URL=https://github.com/git-for-windows/git-sdk-64/raw/main
cat /etc/package-versions.txt | while read p v; do
  d=/var/lib/pacman/local/$p-$v
  mkdir -p $d
  for f in desc files install mtree; do
    echo "$URL$d/$f" ..... $d/$f
    curl -sSL "$URL$d/$f" -o $d/$f
  done
done
```
1             |  2 | 3
:-------------------------:|:-------------------------:|:-------------------------:
![Figure 5](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgHrLG_To6XANKFxsF5Sr6Id1oH_UIq6T9EA-gwqg3ZfMIKK_d1zhxwVq6-4kzSwUcH_7837wykKlK-0ytUcm1BmF2bJx7ULWxmLiOCID1QKz7fmeFVzTHSOpiypZIoVafvXfCuBiczanRQ6nuzr2hxQ0ObZiB1iAT2jd8eij6Dnk4CD6n1aiQItbeKJpTt/s0/rmdhnreza.my.id.install.fish.shell.windows.5.jpg) | ![Figure 6](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjBRGKr6gl673r5w-ZnwzZ-Y8ptd5OsnJU1MARBmELKT9FnOuvArWEC_4ukDSRNINOdOgv9oQPUG1x_0hVjXPxDzuwoHvcNwEzgZ0O-ieuGcZXcNDh8PXV5_cNnqKMf8qjiz1kwjygcqSXXzPl95OnC96tc0LWFVzKvvBaPLZUc6rzwAvFa_S1MwuWx0CDr/s0/rmdhnreza.my.id.install.fish.shell.windows.6.jpg) | ![Figure 7](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEj0G_LKvpaUp_5fDdU002xU8EUwgIKQTfcntyggYd3Qnlbo8-HLeythEtLdGo7dtOvWg7YAbKlhCxZ8OMgomQ3ZbJNvWJPGyV9Va_gLNdccF4shffpBvr83kRGdMkQ9fP4dbcLxx5W6C1KH_j6FAnpf7R59mKJ2T5uSb6maZ7XFS-aOzE6bpR4FbGFFNJ25/s0/rmdhnreza.my.id.install.fish.shell.windows.8.jpg)

{{% adsense %}}

## Install Fish

6. Setelah pacman terinstal pada **Git Bash**, `Fish` dapat diinstal:

```bash
pacman -S fish
```

![Figure 8](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjss41lgnuLvyVR3onZB6LQBcZzMxpdF8acqSDdvYWDlp7pgUQP1iRq9OenvnPfwPqe4qsMwcBfGUAczge93Tkau_f2swr_DdsZoQOF9Aysi9pufaNtpn4eE2V4CY9V74_2auozsIKPogdma6IfGtat8gROuj3EjqRtPxWhbaBEOxZUaQ1SYlYULS74KroM/s0/rmdhnreza.my.id.install.fish.shell.windows.7.jpg)

7. Jika semuanya berjalan dengan baik dan berfungsi dengan baik, buat *file* dengan nama `.bashrc ` di `%USERPROFILE%` atau `C:\USERS\USERNAME\.bashrc` dan tambahkan baris-baris berikut untuk menjadikan `Fish` sebagai shell default:

```bash
if [ -t 1 ]; then
  exec fish
fi
```
1             |  2
:-------------------------:|:-------------------------:
![Figure 9](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjRp1c7vC6tQjbweSkNPPbPAL5c7IN_H09kcPQ4aQ-VaDwKxz2Fxtff4nU7_UQweeWCzP1IIopUoZfc723vTfTl63zdb32hUnAzL8ik0VkZhnJin_SR4DgxZoT76PIt8NFywSjQTqZ_faIKL7Pqpn-8ojN_IjdlnfgGqwwDRmkaYegzSrR_TG_I68ZqjjOf/s0/rmdhnreza.my.id.install.fish.shell.windows.9.jpg) | ![Figure 10](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjUtey_Xo2zx51vKBw5DdTIEf1r4j6Z0B-jWMfw-lKNHC4krRng06oFlapJt6IpKfysCYxgHk1X7Y1dtItLP7jnDY3WNmBowJ7rKN3Tx2lC_5fJM7LDUJWZnDWA_JjGBMAsQ-ckivKr8tEoGKgEdH6UA5k9szzYlu0ybYcYJx5V28wzBk94ESK_a9laJzD_/s0/rmdhnreza.my.id.install.fish.shell.windows.10.jpg)

8. Untuk lokasi config nya sama seperti di sistem operasi Linux yaitu di `$HOME/.config/fish`

1             |  2
:-------------------------:|:-------------------------:
![Figure 11](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhSDnvtGODKPnEasWYT4G1mJgTpc4Vaj0DiKlA4qdb30GUvH3XMJmekdT1FCk00W1OLUZPeoe61VlE8_TA5KskIrunw9yhqvpLUUsYozEtz5zhxUDShv93KsbC1Fxk0Q1ca7mUuFYpOF96Pdxx0XPyO5HJPw1TA5fL-ok3VTqVB5W5W7Dkt3lnRKtCTQzV_/s0/rmdhnreza.my.id.install.fish.shell.windows.11.jpg) | ![Figure 12](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhhnDklhmn7rSv_3WMhEV7EBZ-2CNQrn9V5IvPYz_1JcEEDvXnd5_IGjj0Kaex0wiHj-HSUl6hVMTFpPsaYZ3cbf0zbRmfkXq_gJzixaOKuceaMPJa1DbId5KyJewRj0hdZmAXztRHePJy6s1agZFncA0d-v0smXTCIbgHp7QV9HyWvBOmZXomytRsHJZuF/s0/rmdhnreza.my.id.install.fish.shell.windows.12.jpg)

Itulah tutorial [Install Fish Shell di Windows 10 atau 11](https://rmdhnreza.my.id/install-fish-shell-di-windows-10-11/) jika ada yang ditanyakan silahkan berkomentar dibawah ya!

Sumber tutorial ini diambil dari: [gist.github.com/rafaelpadovezi](https://gist.github.com/rafaelpadovezi/1cfc1026f78255458f5a2ea56291ed23)
