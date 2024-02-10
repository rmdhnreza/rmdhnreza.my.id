---
title: "Install VNC di VPS Ubuntu menggunakan DE i3WM"
date: 2021-05-21T00:30:13+07:00
description: "Tutorial install VNC server di VPS Ubuntu menggunakan Desktop Environment i3WM"
categories: ["Linux", "Tutorial"]
tags: ["Linux", "Tutorial"]
keywords:
  [
    "VNC",
    "I3WM",
    "Install VNC Server di VPS Ubuntu",
    "Install VNC di VPS Ubuntu",
    "Install VNC di VPS Ubuntu menggunakan DE i3WM",
  ]
description: 'Squoosh adalah aplikasi web kompresi gambar yang memungkinkan Anda menggunakan opsi lanjutan yang disediakan oleh berbagai *compressor* gambar (jpg, MozJPEG, AVIF, dll).'
summary: 'Squoosh adalah aplikasi web kompresi gambar yang memungkinkan Anda menggunakan opsi lanjutan yang disediakan oleh berbagai *compressor* gambar (jpg, MozJPEG, AVIF, dll).'
image: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhuUEYmsjYOLpzVT37xi-ZwWRHHT8kVlCAN23hXuoZ8sHPumrALAhyO75Hf27y_cDi2rQnXo14cKF4syqJsHRiMiNDHLrZr6ujQom27BMONFS2mVASVtWS0QloFonHO8ooU28VDUvU6_GzBlznctZsvGCbzGnHc6l7K6JeCpVgwKUAvZmn7kBxMTsSQN2yL/s80-rw/vnc-logo.jpg
thumbschema: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhuUEYmsjYOLpzVT37xi-ZwWRHHT8kVlCAN23hXuoZ8sHPumrALAhyO75Hf27y_cDi2rQnXo14cKF4syqJsHRiMiNDHLrZr6ujQom27BMONFS2mVASVtWS0QloFonHO8ooU28VDUvU6_GzBlznctZsvGCbzGnHc6l7K6JeCpVgwKUAvZmn7kBxMTsSQN2yL/s0-rw/vnc-logo.jpg
---

{{% adsense %}}

## Pertama-tama
Saya disini menggunakan VPS menggunakan Sistem Operasi Ubuntu 18.04, tapi harusnya ini juga bisa digunakan di Sistem Operasi Ubuntu yang lebih baru. Tutorial ini menggunakan Desktop Environment (DE) i3WM, bukan Gnome ataupun KDE, jadi jika kalian misalnya belum familiar dengan DE i3WM saya sarankan jangan mengikuti tutorial ini.

## Tutorial Install VNC

1. Kalian login ke VPS kalian

![VPS](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhiDUAggc9JS_lsz98lV7kfhd3ubEJIfUDkz2jHNJJgkR9-5b2JS3PXc6-QTLpgxbOUFA2nkq4swHIPJeM8s5TqiE6ld84qkj9vH4lJl_5BP-mh-gEmz4-wJ1-PA1OwfXPIkv727GutZ0FJelVZWn2W1NHjaaXQgdmApGeS2G_zhAwn0XUOtD905Z8JWR6f/s0-rw/vnc-1.jpeg)

2. Jalankan perintah berikut untuk menginstall **vncserver** nya, disini saya juga menginstall aplikasi lain supaya bisa langsung dipakai pada saat kalian sudah selesai menginstall **vncserver** nya
```bash
sudo apt install dialog xorg xinit dbus-x11 x11-xserver-utils i3 pcmanfm xarchiver hsetroot xsel fonts-mplus fonts-firacode xsettingsd lxappearance tigervnc-standalone-server tigervnc-common tigervnc-xorg-extension tigervnc-viewer apache2 iputils-ping zsh nano netbase fonts-roboto fonts-nanum ttf-ancient-fonts fonts-wqy-zenhei imwheel zenity firefox apt-transport-https dconf-cli uuid-runtime clipit renameutils rar unrar libpci3 libpci-dev mediainfo gtk2-engines-murrine gtk2-engines-pixbuf libglib2.0-dev libxml2-utils konsole fonts-fantasque-sans gnupg aria2 breeze-gtk-theme breeze-icon-theme breeze-cursor-theme -y
```

![Install vncserver](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgpJmsdEIqZlY7fydIr_zeB1wsPVejsyfWZGwuJ7lXK8u1Hu3Mu_-uV-2MZLzQd_DLY1SkBvITVvv31D4JJS2FxZkTKr3fZhta_NZ2eILCOAhR6WRuk3NHAmmgDNrocy0CjNwV5LLO_ABngTf5aZ8BSyCc1BmR2PWCnOzyZvHGjNtHfdMWJmRCJJPAa1Dak/s0-rw/vnc-2.jpeg)

{{% adsense %}}

3. Tunggu proses download dan installasi hingga selesai, untuk VPS tidak lebih dari 2 menit harus nya

![Proses Download dan Installasi](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhM-8WxqmXMpn6j9tmT_Hr5NWUrgWZ4viJJFhGWbebzzxLDOvdpQkU1wACFXX2Wfe-y40KZbgkjKn2V2IFFsCjen3fDscK4KwHvv1zxQH5Eovpics45kDWMGS9gWxmaCIlj2PKNEeCDvzYHkogH5dzB6aUm9dxj2XTc0qjVnhWaGB8UlhCXw2XjLSLLs_t9/s0-rw/vnc-3.jpeg) | ![Proses Download dan Installasi Selesai](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiUyl7OOZ1bjASG5I2hw-MSL7vMtDV739GZMcYH26dzf5uBEgOFlXW-kiLwq2gnfwB8osO7OWQFx38agaoT194p6OAj3cObicJV5G7GViD6CYGBJeyGGPKiU_xd8jDelRkV99Xb2RKC2jbe83_2VEUj46AVpe17vm1dVTGccrmYFhiVLRyd7FKKQ8_jTakZ/s0-rw/vnc-4.jpeg)

4. Jalankan perintah  `vncserver`
5. Nanti kalian disuruh untuk memasukan password, password ini untuk login ke **VNC** nya dan minimal 6 karakter
6. *Would you like to enter a view-only password (y/n)*  Kalian bisa pilih **Y** atau **N** bebas

![vncserver](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhzw8QihDWKVaYmewVCjyV5XFe77-a_tguhSgbXG2wVRDo5OMMMvPpY-5IZhIa6K6pbXdR7S7rIclNK8zds97aDz0s-b_7iA-3XmRJLs_z2bj0FcKSYk2pSW3JL1fiMSabetRuPvbPaIGR9v7h4LrqLGfk4tdxyBGpiu51v3Hko50Af0ggPI8MP20OUvDwi/s0-rw/vnc-5.jpeg)

{{% adsense %}}

7. Jalankan perintah `vncserver -kill :1` *kill* proses *VNC*
8. Masukan perintah dibawah untuk start i3WM nya
```bash
cat > .vnc/xstartup <<EOL
#!/bin/sh
xrdb $HOME/.Xresources
dbus-launch --exit-with-session i3 &
exec i3
EOL
```
9. Kalian juga bisa set resolusi & DPI dengan memasukan perintah
```bash
cat > .vnc/config <<EOL
geometry=1366x768
dpi=96
EOL
chmod u+x ~/.vnc/xstartup
```
10. Kalian jalankan lagi perintah `vncserver && pkill -9 vncconfig` untuk menjalankan **VNC** nya
  * **Note:** Jika kalian tidak *kill* proses **vncconfig** nya, biasanya background nya menjadi warna abu-abu, jadi saya sarankan kalian *kill* proses **vncconfig** nya, lalu jalankan manual pada saat sudah login ke **VNC** nya

![Config VNC](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEisdQESnRpQQeVsM0j5z6QRyHZtzG0QseK2Fk5XNQRF7bzhQqIqlmXttR7mzj21LMLL9ChcXJzIDhDpQZpVQ34d6peif9RPnYQkz0xjQD1l-Xz4kSGTxV_tq4DukCzM5bkVEFpD5ryDpPLuE22eh-yIzoSO4xlhZ8vB5G-FgizEvi8J0m1_Tzj1vS_tWb6M/s0-rw/vnc-6.jpeg)

{{% adsense %}}

11. Kalian tinggal login ke VNC nya menggunakan **VNC Viewer**, disini saya menggunakan **TIgerVNC** kalian juga boleh menggunakan **VNC Viewer** yang lain.
12. Masukan IP VPS nya dengan port 5901 jadinya `IPVPS:5901` lalu masukan password yang tadi kalian buat di langkah nomor 5

![VNC Viewer IP](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhr7whsOHRRblGSaB8BkTuM-7UW1uvmfSgAdvOE352plhmnMaeT9FD_g-KBJMf814wZijpYkhQLrMfgAuv6YJzJEUTu3yQPjkWZ-1F3FMMEZ8HVzHpwCyEZ13Oq3pItNS0xwLXN6L_z54lxJj5UmAscMtOxNT4FiuHmad3lLp0dVzZZiBhwdK-ZwP5d9XiA/s0-rw/vnc-7.jpeg) | ![VNC Viewer IP Password](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhRAiOGvG0QEed118_PebgUkZBEAbfHMmxlkRh0fLbWm7Cs_lU3AXYsqCNmXEkkNqiAhQOnbzmOp_P-9NHs72jpjncsaGwkzAdmUNXQeqr5DGVIPZowaOWIF4glFtUcLedWaagcTQScQRRi8hgDamGQRnBoXPUZuLlraZL6iJt29hjSYX0cHllTXs-r3oue/s0-rw/vnc-8.jpeg)

13. Awal tampilan i3WM seperti ini kalian tinggal `<Enter>` dan pilih `<Alt>`, Jika pilih `<Win>` takutnya nanti bentrok dengan tombol Windows di Desktop kalian

![I3WM Desktop](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEj0IoLA7pCwpv99K3tFs5swZdo7Z8Dx75JBsh8Pyh2CjbJfBpdBRam7da6KbYbaa0NvyISKL1nR942pb0y4Byx6tRcFZs7L4L7962-JZvTHUsx5JrfLns8yUvJlCahFwu5qK4h5xeS8KQAZFwtfZnFd67UY0_OONMPYwTo6m4S4RHfrkqXhdiW_e0q32Qlt/s0-rw/vnc-9.jpeg) | ![I3WM Desktop](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhUnsKBLYzdqORfnMj-u_ZfabGs4SBQ1TzpJzfxnZNAsuF_c_FIm14oI6euuNENDZ1TPQRIYD2RtcJMfTC5ti6CzM4839f30Ve0K7P2Lreuai9PqCehWdg7KhFuKnt-dsSQE92vgS6pzl1tRC80dQQF6vW-g1GVolw5p6Qruhs-RIbWh3sv8M5phaYbQXzh/s0-rw/vnc-10.jpeg)

14. Tekan shorcut `Alt + D` untuk membuka d-menu
15. Menjalankan browser Firefox

![Firefox](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjOdQ6cfIbAE7wxwopgj-bke9lH7aBjIxkq1XYg7ITfb8TsxPDNpfOL6WJliEo9Im6DdeSGoNLAX8Vtwk_Af0_Qupa7v1_NAtb5L-NgcyTqpquFfBWxK1iOkb-nf9-eMwwd28fNrepqVKWnrjjhIiHVjoiV7uNYedu6Ax9VqXvRQc_gbMdgqv4E5TNlYgNX/s0-rw/vnc-11.jpeg) | ![Firefox](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhD4kpLtIu61RCce5ccjk3rKgVj5R1NgQq_y7_7ELXLANS9kJlNPqHunWDAjkaI27C5JqWduIhojrz3a2EWIy8QV1RV3ESBITTvrRYhs4jIs4ZIOBv5xnrJicjORVQ14vgDFQl6v4cwqrCy8EzSoxE9J260677kEcLBHvCkRjjc7d37JbQnqcCSd_10RZgM/s0-rw/vnc-12.jpeg)

Itulah tutorial cara menginstall VNC dengan Desktop Environment i3WM di VPS Ubuntu

{{% adsense %}}
