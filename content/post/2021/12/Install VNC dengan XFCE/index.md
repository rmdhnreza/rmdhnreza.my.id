---
title: "Install VNC menggunakan XFCE4 di VPS Ubuntu"
date: 2021-12-28T15:30:13+07:00
description: "Tutorial Install VNC menggunakan Desktop Environtment XFCE4 di VPS Ubuntu"
categories: ["Linux", "Tutorial"]
tags: ["Linux", "Tutorial"]
keywords:
  [
    "Install VNC menggunakan XFCE4 di VPS Ubuntu",
    "Cara Install VNC menggunakan XFCE4 di VPS Ubuntu",
    "Install VNC menggunakan Desktop Environtment XFCE4 di VPS Ubuntu",
    "Tutorial Install VNC menggunakan Desktop Environtment XFCE4 in VPS Ubuntu",
    "How to Install VNC Desktop Environtment XFCE4",
    "How to Install XFCE4 in VNC VPS Ubuntu",
  ]
description: 'Virtual network computing (VNC) adalah software remote-control yang memungkinkan untuk mengontrol komputer lain melalui koneksi network'
summary: 'Virtual network computing (VNC) adalah software remote-control yang memungkinkan untuk mengontrol komputer lain melalui koneksi network'
image: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhuUEYmsjYOLpzVT37xi-ZwWRHHT8kVlCAN23hXuoZ8sHPumrALAhyO75Hf27y_cDi2rQnXo14cKF4syqJsHRiMiNDHLrZr6ujQom27BMONFS2mVASVtWS0QloFonHO8ooU28VDUvU6_GzBlznctZsvGCbzGnHc6l7K6JeCpVgwKUAvZmn7kBxMTsSQN2yL/s80-rw/vnc-logo.jpg
thumbschema: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhuUEYmsjYOLpzVT37xi-ZwWRHHT8kVlCAN23hXuoZ8sHPumrALAhyO75Hf27y_cDi2rQnXo14cKF4syqJsHRiMiNDHLrZr6ujQom27BMONFS2mVASVtWS0QloFonHO8ooU28VDUvU6_GzBlznctZsvGCbzGnHc6l7K6JeCpVgwKUAvZmn7kBxMTsSQN2yL/s0/vnc-logo.jpg
---

Virtual network computing (VNC) adalah software remote-control yang memungkinkan untuk mengontrol komputer lain melalui koneksi network. Pencetan keyboard dan mouse click dikirimkan dari satu komputer ke komputer lainnya sehingga seseorang dapat mengelola sebuah dekstop, server dan alat yang terhubung jaringan tanpa harus di lokasi yang sama.

VNC bekerja pada model client/server. Sebuah VNC Viewer (atau client) diinstall pada komputer lokal dan dihubungkan dengan server yang harus diinstall di komputer remote. Server mengirim duplikasi dari display komputer remote ke viewer (client). Server juga menerjemahkan command dari viewer dan menerapkannya pada komputer remote.

{{% adsense %}}

VNC adalah platform independent dan kompatible dengan operating system apapun. Komputer harus berada di jaringan TCP/IP dan memiliki port yang terbuka untuk traffic dari IP address suatu alat yang akan mengontrol. Sumber [yunushadisisworo.wordpress.com](https://yunushadisisworo.wordpress.com/2015/02/08/apa-itu-vnc/)

Pada tutorial ini saya menggunakan VPS menggunakan Sistem Operasi `Ubuntu 18.04`, tapi harusnya ini juga bisa digunakan di Sistem Operasi Ubuntu yang lebih baru. Tutorial ini menggunakan Desktop Environment xfce4, untuk menginstall i3wm di VNC kalian bisa lihat tutorial nya di [install-vnc-di-vps-ubuntu-menggunakan-de-i3wm](https://rmdhnreza.my.id/install-vnc-di-vps-ubuntu-menggunakan-de-i3wm/)

## Install VNC Server
1. Login ke VPS kalian sebagai root
2. Update terlebih dahulu sistem nya

```bash
sudo apt update && sudo apt upgrade
```
![](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgUJEwPRQkWNi10EZphHtESomdSY6xd3A2CYfufdDoySSC8DvMGQ5sPgbw8NUNb4s2tsunaQaRk3t5rv8uxcdIpz5dYrbYpwFHyI9vGdSF_bSbKQtPzxzvbn2Txk81ioklyLDf3HfqzsxKtC6e2tbtxL0dRKcujC8ABT8A0rFzZXuhEHucMa4U2FSN9GtmL/s0/rmdhnreza.my.id.vnc.xfce4.ubuntu.vps.1.jpeg)

3. Ketika kita menginstall VNC, tidak disarankan menggunakan user root, jadi untuk itu kita buat terlebih dahulu username yang bisa akses sudo

```bash
sudo useradd -mG sudo rmdhnreza
sudo passwd rmdhnreza
```
`-mG sudo` perintah ini untuk membuat home direktori dan menambahkan user ke group sudo

![](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiVs6gcze8MlMlc_S7_iO3WsWh4PM2k5iAwWDRkFuIBF6KY4hW5eKTflnE2c_35FhhFeMY4zRNKaMBC7lUHIEbFsm3yHJNhNHLWBHOwzw8FHXOdmHKAt4h3co-8NgRu9PsONG3NtUXnvJk8QEJvI-y4o2RjD7l3cNHwofZVnF_-VsDBK8WqYYDcF3zfbFpE/s0/rmdhnreza.my.id.vnc.xfce4.ubuntu.vps.2.jpeg)

4. Setelah membuat user & password, kita sekarang akses username yang baru kita buat

```bash
su - rmdhnreza
```

{{% adsense %}}

![](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiVbQsNvqolo6OvqLxsScHgF0O9RWtznR_29Itc0A1Xt9KV4bUKkToJsGT_X_vPZU192fiu0wfAJgoKQxtVxv42URrbe5EzVYPuRrKk-KjUcd1G0WdGUu-ORQyvqqx4atuIWIY00wxzdluzPjpgEa9w9BruskX9yYY-s_ju4hr3_4bXuSPCi8Gw4CLZQvHM/s0/rmdhnreza.my.id.vnc.xfce4.ubuntu.vps.3.jpeg)

5. Kita mulai installasi Desktop Environtent xfce4 & VNC server nya\
Tunggu beberapa saat hinggal install selesai

```bash
sudo apt install nano xfce4 xfce4-goodies tigervnc-standalone-server
```
`nano` Text Editor untuk edit file, jika kalian punya text editor lain, bagian ini bisa dihapus\
`xfce4` ini Desktop Environment nya (Wajib di Install)\
`xfce4-goodies` ini adalah default aplikasi xfce4, contoh nya terminal, thunar, dll. (Optionall, tapi disarankan untuk di install)\
`tigervnc-standalone-server` ini adalah VNC server nya, disini kita menggunakan tigerVNC

![](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgNLF_N8skTS8S2_c9UBYNTOx6vtUsN7egl1OF-kRV2RQIKVHkud-hkbLKZMjDmq3bGmET3Q3LRqodHGwd8reQv2EKfERSo0Baf64qAgiNAN_HPaND9pyhvSH9M69UyHzncOMpF3Rz702ljtRuOhMCWS4tMMLFVDpoXqUoRS2YdWVGla6rKbK9ZperoLwuj/s0/rmdhnreza.my.id.vnc.xfce4.ubuntu.vps.4.jpeg)

![](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEj1t47FdAKpXGYIcMP7GXBDYhuwVofBoc3uM5scvHJLxg4TUR_KHNawg3pVgFyQ4pc7xbHN6njV9jXh_VrzcYKS-vyotI2fPiyUz1AikgJsQXgAbZ5hVyTy9M9hUn1bwdCXg6uAJqCgbnlzqM3B8k5OBFxVbHtBITSrnNcJ4Jqi7k44pY2buVETuhsjWeTt/s0/rmdhnreza.my.id.vnc.xfce4.ubuntu.vps.5.jpeg) | ![](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgkFHuHlSqTNwKqEaFA7hkwIZKTt27w-QBjEzudRtd4i5_oiTWxCQ2pWH0S1Y4Na_sMA7cL4mVHgbnYvdyu0NSgNKpt9oJ5ADDG0AuRkYYpg58wk-MykUGMXJWwiIsSvFWhzIDBtylDhlcojgjomS3U2y_XjZ1WQgWrq2jFr5ibxTK6lokQC7f5q9-aRBKi/s0/rmdhnreza.my.id.vnc.xfce4.ubuntu.vps.6.jpeg)

6. Kita buat password untuk akses VNC, **password minimal 6 karakter**\
Would you like to enter a view-only password (y/n)? pilih n saja

```bash
vncpasswd
```
![](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjpDH60E2IV1H1KCKM80W-9j0VtgJMuy8n3dylCOpzZ62KddQduD1Eejo0VTwKvI318ygG2xwnXw89snBTV7capKPpasPwXsQK3pJ02qK2WlCd7UJOBgSNjLdOuT75Kb44MbNpJ9WJy8emmaApyZfuw6qgrhxuBtJVkYWqlWxC_5tD-mdjX1Zn5T8Lddi2E/s0/rmdhnreza.my.id.vnc.xfce4.ubuntu.vps.7.jpeg)

7. Kita buat dan edit file `xstartup` di `$HOME/.vnc/xstartup`

```bash
nano $HOME/.vnc/xstartup
```
lalu tambahkan baris berikut
```bash
#!/bin/sh
unset SESSION_MANAGER
unset DBUS_SESSION_BUS_ADDRESS
vncconfig &
exec startxfce4
```
Yang penting pada `xstartup` ini ada pada bagian `exec startxfce4`, jadi pastikan tidak salah pada bagian `exec` ini.

![](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjVubBsNwuBVr0WR5pZOravo835NzWixt2elNYA2GflUZEfpZfbn9ndtNGx3psNulLAFxPKaeZFotpik4UBlQOULrIjp8QbRCRF87g-9HE1uB8wcqLRPUZvJMVcsKbydVzRXjK3Iy1tYIWMAUdOZCnd0LXXuulBIgywvFAqNJQJz_qKDQ15HIY75oCm2aL4/s0/rmdhnreza.my.id.vnc.xfce4.ubuntu.vps.8.jpeg)

## Install VNC Viewer
Untuk akses VNC, kita harus menggunakan VNC Viewer, disini saya menggunakan tigervnc (sama seperti server nya), untuk itu jika kalian belum punya tigervnc nya kalian harus download terlebih dahulu aplikasi nya

- Ubuntu 18.04, Ubuntu 20.04, Windows OS | [Download via Sourceforge](https://sourceforge.net/projects/tigervnc/files/stable/1.12.0/)
- Arch Linux | `sudo pacman -S tigervnc`
- Fedora | `sudo dnf install tigervnc`
- OpenSUSE | `sudo zypper install tigervnc`

## Login VNC
Setelah download aplikasi vncviewer nya kita bisa langsung buka saja aplikasi nya.

1. Pada bagian VNC server kalian isikan IP VPS kalian lalu menggunakan port 5901 (Port default VNC), atau jika kalian menggunakan Local Forwarding Port 5901, kalian bisa isikan `localhost:5901`
```md
IP.V.P.S:5901
1.2.3.4:5901
localhost:5901
127.0.0.1:5901
```
2. Masukan password VNC nya, yang tadi dibuat dilangkah 6

![](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhYn61kKdx77VvCzGv8-PggcMF766ravDuLAqrNYx6efjpkffRoCOHsiCUQZHMPt9wFrSr8yGv4ExX4-l8HsxDL3ayE6snf0P02t5fHK94HUrWW_Cquah1M1R6e-ENF1AJIwOMXvZaygI8QQ-mxrtFHquzn-I06JH7RaHPCrK7PsG-fSXSiFyp2tUkPdLcT/s0/rmdhnreza.my.id.vnc.xfce4.ubuntu.vps.9.jpeg) | ![](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEifHBquP-vUObOjaov3kgRXWBPpoTexO-XVhVT6EM2LasgevCc9Vewz1A2KcS1cqP-k2VDRlJtdkOaRfRwefuArLoK36qSYX9ANxk4IaQuhX8pnkWXuwp1tMKIFvbzoJ0Ioj7C8GocpBUjEotx4rs-TBrmgddsKXN9wFSlxi5t2h7cKH0P4jRxMwAd_svsF/s0/rmdhnreza.my.id.vnc.xfce4.ubuntu.vps.10.jpeg)

3. Jika berhasil maka tampilannya akan seperti ini, kalian cukup pilih `Use default config`

![](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgoxXz7nHJba5cIUIxWzYqDstJI07cP0dWtu1Cy7hLBfioODFdfPJ7OhZv0d98dSff2t96ZM9zhYyQQrNe6qrQUxlho_oQgPwwE_pIzPaQXchQZolNsdSh_D7786tsLfd7VQxWSIs13UNa93gJOj0QiMZfeb0IpkECAWB9_ektFn-3CVwuDhyiDuhdMtAPJ/s0/rmdhnreza.my.id.vnc.xfce4.ubuntu.vps.11.jpeg)

4. Sekarang kita coba install browser Firefox dan melakukan Speedtest
5. Hasil nya seperti ini

![](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgFe3u5HWoUPCnbewElm69Q4j92s1fmK3EfECCokRwphqbFaZ5lTmjgbmQHhor6dOaGXfI9UG0h0AvxjyAKRYN1YcXocnOcA5l3SeqWnlVULTIlzTwkP_uehyphenhyphenLEv_06Ooi2flOcCtl-H48G7iPK5Kc2bM2D1Sm-x-4TT_wnLiOM-cYqS4mcTotHUSjP-WIL/s0/rmdhnreza.my.id.vnc.xfce4.ubuntu.vps.12.jpeg) | ![](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiW9p0fhbwtx4DPB3G4GO0bMz8WH-gg7TiaU-4uqJASK9jI73_9uhXrtgBAJ7PzIrQTjyFCkGCrLhEj2eQChJ9j9FAS4FvGIetjUR-8zqMh9RcTusBGsBmfqnjE6blUNVV_0WTBK_5RiMBsrBjZVsf6MPKdt50fxrimyx3Op8VSC1F-8ZWlfZdSLrv4kymx/s0/rmdhnreza.my.id.vnc.xfce4.ubuntu.vps.13.jpeg)

Itulah diatas tutorial install VNC menggunakan Desktop Environment XFCE4 di VPS Ubuntu.

{{% adsense %}}
