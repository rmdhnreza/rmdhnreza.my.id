---
title: 'Tutorial Install Stunnel4 di VPS Ubuntu 22.04'
date: 2022-06-18T11:30:13+07:00
description: 'Tutorial Install Stunnel4 di VPS Ubuntu 22.04'
categories: ['Linux', 'Tutorial']
tags: ['Linux', 'Tutorial']
keywords:
  [
    'Tutorial Install Stunnel4 di VPS Ubuntu 22.04',
    'Install Stunnel4 Ubuntu',
    'Install Dropbear Ubuntu',
    'Tutorial Internet Gratis',
  ]
description: 'Stunnel adalah proxy yang dirancang untuk menambahkan fungsionalitas enkripsi TLS ke klien dan server yang ada tanpa perubahan apa pun dalam kode program'
summary: 'Stunnel adalah proxy yang dirancang untuk menambahkan fungsionalitas enkripsi TLS ke klien dan server yang ada tanpa perubahan apa pun dalam kode program'
image: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgHeDpFPUJ3lnkmVU24KK7JhF-OTPh6RrjDbFhcuv54jjR_Upgq8io6_oXbAZ-aNra8TPTtmdqgYkrPTlZ-q8KRZVmZygGrUCrk8-bpKO_8s4uOOmgKc3UbQgdddhZWlYp3U-Ht315p-YtDNgwS16Xz22H2SvKgSw63eCvG77gSQyJM38b3eXJRS9f7gg_A/s80-rw/stunnel-logo.jpg
ThumbSchema: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgHeDpFPUJ3lnkmVU24KK7JhF-OTPh6RrjDbFhcuv54jjR_Upgq8io6_oXbAZ-aNra8TPTtmdqgYkrPTlZ-q8KRZVmZygGrUCrk8-bpKO_8s4uOOmgKc3UbQgdddhZWlYp3U-Ht315p-YtDNgwS16Xz22H2SvKgSw63eCvG77gSQyJM38b3eXJRS9f7gg_A/s0-rw/stunnel-logo.jpg
---

## Stunnel4
Stunnel adalah proxy yang dirancang untuk menambahkan fungsionalitas enkripsi TLS ke klien dan server yang ada tanpa perubahan apa pun dalam kode program.

Stunnel bergantung pada perpustakaan OpenSSL yang mendasari protokol TLS atau SSL, dan OpenSSL sendiri biasanya sudah terinstall otomatis di sistem operasi berbasis Linux.

{{% adsense %}}

## Install Dropbear & Stunnel4
Untuk kalian yang mengunakan aplikasi injector seperti HTTP Injector atau KPN, dll. Dropbear wajib di install di VPS sebagai pengganti OpenSSH, untuk menginstallnya kita bisa menggunakan perintah

```bash
sudo apt install update
sudo apt install dropbear stunnel4
```

## Setting Dropbear
Disini saya menggunakan editor nano, tapi kalian bisa menggunakan editor kesukaan kalian.
1. Edit file `/etc/default/dropbear`

```go
sudo nano /etc/default/dropbear
```

2. Ubah
   * `NO_START=0` menjadi `NO_START=1`
   * `DROPBEAR_PORT=` menjadi `DROPBEAR_PORT=3128`\
     **Catatan: Disini saya menggunakan port 3128 untuk port Dropbear nya.**

![Setting Dropbear](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgCNWtywn-MBZEnXbIp0W3riPg3GrcWvOUaLSLLqEHveIfWwkjMiEPYioq5lfMPrR4iCcesD4m7ld3uOkDWSfoIgXCJVgqOIxCXUvhwDHNwET9e-qnM4-aVZoDM69uRXPprDuoGKJ4ZhEPrgQSdLPYnN0Uh4bOAOoZQcjprikzvJzX3BEoLAr3cPTtzrZIL/s0-rw/rmdhnreza.my.id.install.stunnel4.1.jpg)

3. Save, untuk editor nano kita bisa menggunakan `CTRL + O` -> `Enter` -> `CTRL + X`
4. Start dropbear dengan perintah

```fish
sudo /etc/init.d/dropbear start
```

## Setting Stunnel4
Disini saya menggunakan editor nano, tapi kalian bisa menggunakan editor kesukaan kalian.
1. Edit file `stunnel.conf` yang berlokasi di `/etc/stunnel/`

```go
sudo nano /etc/stunnel/stunnel.conf
```

2. Isi dengan baris berikut

```toml
cert = /etc/stunnel/stunnel.pem
client = no
socket = a:SO_REUSEADDR=1
socket = l:TCP_NODELAY=1
socket = r:TCP_NODELAY=1

[dropbear]
connect = 127.0.0.1:3128
accept = 443
```

Catatan: pastikan pada bagian `[dropbear]` port nya sama dengan port dropbear yang sudah di setting di langkah sebelumnya!

![Setting Stunnel4](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjg-Ukv9W7Hh1u3sqJX9QuIJTYp0BkVKQ167pSndyhtDog26woI4nPlaQxb5KOkQ3aCUE5GDHX9brZ4zWjTLj7xx5Bfj6QsvDJzbnnxfgNQNqZg0DpgoKJUMfd9XKLlLlNEUgmBjGuo_DmcHaNHyJu-dfWxB1u1-Jj5AIuTIx-VOFfWDJ6sJpbSjIX0eRum/s0-rw/rmdhnreza.my.id.install.stunnel4.2.jpg)

3. Save, untuk editor nano kita bisa menggunakan `CTRL + O` -> `Enter` -> `CTRL + X`

4. Edit file `/etc/default/stunnel4` agar bisa berjalan pada saat system bootup, cukup tambahkan `ENABLED=1` diawal atau diakhir baris.

![Setting Stunnel4](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhZUk-MKaFDQczz61mP8bEZOTsdzx3ee_j3PqlnTTK9TQZPRvu_W1Q3wMSy7zyfO0-LJSlLzgR_9nxcCbb7vhN6X-WGQdcSoN4u6AL9_YVK0LFP8gpRn-UR9VDHWOtZjlygaL1iTSjoyA6h5zFCnFpTzlH4inmYjb28Vr-d5filjxcyw7O61SQMMxAG8taX/s0-rw/rmdhnreza.my.id.install.stunnel4.3.jpg)

5. Membuat `self-signed cerfiticate`, pastikan kalian masukan perintahnya satu persatu jangan sekaligus

```go
openssl genrsa -out key.pem 2048
openssl req -new -x509 -key key.pem -out cert.pem -days 1095
cat key.pem cert.pem >> /etc/stunnel/stunnel.pem
```

![Generated Certificates](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiXj9LgIEUNaPPQXt6hx-7B5YUl6hb_bnMaDD4xaaaVCDNHOFoWC1k7AuQ3lSJgBZnx1H4ZzF5JiK2pbhnExmeflReizNNqURYZi66JnDGSPiLgzHxfkRbvzy8NXFvGpRQQX0nKPuZTNdfJanLMBYMqDRUN0jr1klYsA-udkG5H7Y3pRGVpALJxzRvqnuWg/s0-rw/rmdhnreza.my.id.install.stunnel4.4.jpg)

Nanti kalian akan disuruh mengisi tempat, company, dll. Kalian bisa isi seperti ini atau cukup Enter saja (blank) tanpa di isi.

```markdown
You are about to be asked to enter information that will be incorporated
into your certificate request.
What you are about to enter is what is called a Distinguished Name or a DN.
There are quite a few fields but you can leave some blank
For some fields there will be a default value,
If you enter '.', the field will be left blank.
-----
Country Name (2 letter code) [AU]:ID
State or Province Name (full name) [Some-State]:Provinsi
Locality Name (eg, city) []:Kota
Organization Name (eg, company) [Internet Widgits Pty Ltd]:rmdhnreza.my.id
Organizational Unit Name (eg, section) []:rmdhnreza
Common Name (e.g. server FQDN or YOUR name) []:rmdhnreza
Email Address []:rmdhnreza@pm.me
```

5. Bila sudah selesai, jalankan stunnel4 nya dengan perintah

```go
sudo /etc/init.d/stunnel4 start
```

## Check Port
Untuk cek apakah dropbear & stunnel4 nya berhasil dipasang kita bisa cek dengan perintah
```go
sudo netstat -nlpt
```
Jika *command* di atas *not found* kita bisa install `net-tools` terlebih dahulu
```go
sudo apt install net-tools
```

![Check Port](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEi9gMo7FXmRHIoMf0Ew5b6MQWe53CoAkAD8Bqm3cwMSBODYpiYS-OHpnit8GUv-VhL783Li-S0gX9Itlu5SkKUKJa-X0A-F71chqZrxJgF2OmPnRkK9R-fnbe3RKxEnBrpe4AQH-hlPJ9_ZJ3Ao3HjT7ZkSHcRz5scQQIfBWQksNe5S4XP8RPtJQCeXITAA/s0-rw/rmdhnreza.my.id.install.stunnel4.5.jpg)

## Test SSH
Jika berhasil maka bisa connect seperti ini.

![HTTP Injector](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEib416k3TmZl9l79_n8sE0byUuG4PShPrSql5k8O6Kg6zr0UGWE3urX6GvcjCrr1Hiu41svDPOUq8EsRNKTSQU0E1OohDnUNSRovc7HXvFFD4JugeYg501pZUiby_gfGFBzRPcMvQ7FElG_XoEYM_YPBhdmYc01NqFZnCwJpHlNluuEqpp7k6NbJokYjRSW/s0-rw/rmdhnreza.my.id.install.stunnel4.6.jpg)
