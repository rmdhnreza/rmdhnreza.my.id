---
title: "Install qBittorrent di Ubuntu Server"
date: 2021-12-28T15:30:13+07:00
description: "Tutorial Cara Install qBittorrent di Ubuntu Server tanpa GUI menggunakan Terminal"
categories: ["Linux", "Tutorial"]
tags: ["Linux", "Tutorial"]
keywords:
  [
    "Install qBittorrent di Ubuntu Server",
    "Cara Install qBittorrent di Ubuntu Server",
    "Install qBittorrent di VPS Ubuntu",
    "Install qBittorrent tanpa GUI",
    "How to Install qBittorrent Headless",
    "How to Install qBittorrent VPS Ubuntu Server",
  ]

description: 'Apa itu qBittorrent? qBittorrent adalah perangkat lunak sumber terbuka (open source) gratis yang membantu kita bertukar file dengan orang lain di seluruh dunia melalui protokol P2P Bittorrent.'
summary: 'Apa itu qBittorrent? qBittorrent adalah perangkat lunak sumber terbuka (open source) gratis yang membantu kita bertukar file dengan orang lain di seluruh dunia melalui protokol P2P Bittorrent.'
image: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEg8yK5M06H4EmPY-5_SrnQjuaHvi_EH3wBdX0R4k36q0NmHg-vw1jV8J1Fdf_Z_2aRUyDoulxW3kgMe2odfAhd_ZmoJcZFecSXI9ppUX0BoODQXN8D245f8EwZ0dXKtvtL7vzt3OFGjJLBJJUx-T0A0cmKAafILgzDKAwFOTVhYsg3i29mBpvDqrJV97uTi/s80-rw/qb-logo.png
thumbschema: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEg8yK5M06H4EmPY-5_SrnQjuaHvi_EH3wBdX0R4k36q0NmHg-vw1jV8J1Fdf_Z_2aRUyDoulxW3kgMe2odfAhd_ZmoJcZFecSXI9ppUX0BoODQXN8D245f8EwZ0dXKtvtL7vzt3OFGjJLBJJUx-T0A0cmKAafILgzDKAwFOTVhYsg3i29mBpvDqrJV97uTi/s0-rw/qb-logo.png
---

Apa itu qBittorrent? qBittorrent adalah perangkat lunak sumber terbuka (*open source*) gratis yang membantu kita bertukar file dengan orang lain di seluruh dunia melalui protokol P2P Bittorrent.

Aplikasi ini merupakan alternatif yang sangat baik untuk aplikasi serupa seperti uTorrent atau Bittorrent karena\
bersifat *cross platform*, jadi bisa di install di sistem operasi Linux, MacOS & Windows.

Pada kali ini kita akan menginstall qBittorrent di sistem operasi berbasis Linux yaitu Ubuntu, langsung saja kita ke tutorialnya.

{{% adsense %}}

## Install qBittorrent

Catatan: pastikan perintah dibawah ini kalian menggunakan `sudo`

1. Add official PPA qbittorrent dan install `qbittorrent-nox`\
`qbittorrent-nox` ini adalah qbittorrent tanpa X server.
```bash
add-apt-repository -y ppa:qbittorrent-team/qbittorrent-stable -y
apt install qbittorrent-nox
```
![Add PPA](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgA3vqlSnMmMtA4JNUFXqnwvaVtpjbfeYaM9SvFyfyz-u9mmEAzMPkiNvB8iVSuKltopjfn_2Ji0ujxupcDdo_d_mfVwDPZv4YR2QWSw8tYH5ySgDFhAni8pENAJRtIzh4LgJE-ebsZYZEOQ65I9IqUl5pvEx9I47gKuVCuXogp_tqZFHG_CwK6giQahvpO/s0-rw/rmdhnreza.my.id.qbittorrent.nox.1.jpg) | ![Install qBittorrent](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgnwvxJE7BH7_S3KFYSv6oz9yPt53JqW__qQTLo-RYyLPG4rgbNJ7OsZONESQy6UcIkMmnQ8bevi8_EaAJSz6YtBCHc_xSNyTwVkjbKWgAKCFEywoU7kNUUlDHSnhtC7r2XvslmOOoV8lCCy88Xrg75c48yJ-pIvgoMcSf82yirbznL9b-dqWOJSHi5OIIV/s0-rw/rmdhnreza.my.id.qbittorrent.nox.2.jpg)

2. Jika sudah terinstall kalian coba jalankan perintah
```bash
qbittorrent-nox
```
**jika terdapat error pastikan perintah nya menggunakan `sudo`**

3. sekarang kita jalankan `qbittorrent-nox` di belakang layar dan set port nya dengan perintah
```bash
qbittorrent-nox -d --webui-port=8000
```
Catatan:
- `-d` untuk menjalankan qbittorrent di belakang layar
- `--webui-port=8000` port yang digunakan oleh qbittorrent-nox\
disini saya menggunakan port 8000, pastikan port ini tidak konflik dengan port lain.

![jalankan qbittorrent-nox](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhfZT-979Yf-1FMn16nRhLYYJhsgX3mw3EcuCyh1yg_tW5WtxtsAzMPchL7kpMbcDBmOmLDgOUFZLDW0SzWPjaoXEUfryfbypjfsiPW3dIRD3H7OHGbB1ejTlIg-v_fypcb64w-RGZjPtChyvnJOZ3npLNxUNDo_amEh4-pDQ_3SdcroXoe4XtceM2Ijfqn/s0-rw/rmdhnreza.my.id.qbittorrent.nox.3.jpg)

4. Setelah itu kita buka browser dan kunjungi halaman qbittorent, disini menggunakan port 8000, jadi kunjungi halaman `localhost:8000`

1             |  2
:-------------------------:|:-------------------------:
![Tampilan web qbittorrent](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgXtFxUl3uxRlJ-QHCEYEQRiRl3tNn4YF8514vymysTnJe7xOzq56NaOLE9ifzZ1UMTdxG2jMF4ix5cBn68tIRdQ6pcctmxV-GkfKyTPiiH7-V4_Mu_9Ayejdew737ZrmuieYZz7plkSgA22gvS8QA1X6_qn5ZEAdHOsE6qehzOQLiydyWk0Lh-urVXn1Kx/s0-rw/rmdhnreza.my.id.qbittorrent.nox.4.jpg) | ![Tampilan qbittorrent setelah login](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhgTjggQqEgVgTpP2JpFEy1afHDfJmPCi4rCBeBepIkX2sqIhKqXHTgRjaEBglC0ARfCRjHjiSsNxxx-CycjlX-DvwoX0wA1EOJqfYf0xZ49TOWrlvpZJHr_YK4FG30p-b-wZbhQCTloOevRNvmdTyoTdf4Tw7E9uZlyQjb88NRygNLv851keAgmXel2mgv/s0-rw/rmdhnreza.my.id.qbittorrent.nox.5.jpg)

5. Jika tampil seperti ini maka berhasil, default username & password nya yaitu
```yaml
username: admin
password: adminadmin
```
6. Setelah berhasil login, pastikan kalian ganti username & password nya! Caranya masuk `Settings` pilih bagian `WebUI`

![Setting username password](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgyEg8K46FQbQm3xoLz0YChmWiLBnf7KPm4d19Fkk5hAnssNm2VJYsRZiqpczCY0KxiDVhlPa6bSRqIhacD9h1OU_7HD1IGqwNn6h7E8wN6V2eDDhk9vKgW-jLhESvHOYJ7CGrOkk-CtmP6pI468cxJ_vh2wYuJ57JqcC36kHSd9EBgBckWDit45NBoPGlh/s0-rw/rmdhnreza.my.id.qbittorrent.nox.6.jpg)

7. Sekarang kita coba download file torrent nya, disini saya coba download ArchLinux ISO via magnet link dan disimpan di folder `$HOME/Downloads`

1             |  2
:-------------------------:|:-------------------------:
![Tambahkan torrent yang akan di download](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiUc0ebS8DZ8_3h3bqobhkJ2p5qyRLn8Kr612Z51JxcJQ4EQPwBrm9cS6kVoIx3KtvLKrLWy-N9nb1t2GUT2ndhnF1dWiNhKiOyLaTfbQCrsbdu-hrmJNfL_puAkoSW6LZQmz1VIcEfBr0tkxdO3XpaqKG6mqLrX86ppvH3V18t-WqWDwoaYjYFapvEiFb2/s0-rw/rmdhnreza.my.id.qbittorrent.nox.7.jpg) | ![Download sedang berlangsung](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEh81OMeGO33Fe66-rW9AvW3DUBsheUHYm8BsXBG9X-B26XUhm8iABDL4aYfAacLaghZAdK9ZNDNHc60-Nkyq0pkQRIa8XbaPE6oTBDEENidy6zzqoBRkMeoSHX604L6iPBxnu6mseu-6Ypr6sJ8NYuJUC0v2489Sz-LqfWvyFYQKIEy-MxzAjKUXNL5t9OP/s0-rw/rmdhnreza.my.id.qbittorrent.nox.8.jpg)

{{% adsense %}}

## Install Webserver
Untuk webserver yang saya gunakan yaitu apache2, tapi kalian juga bisa menggunakan lighttpd, nginx atau webserver lainnya.

1. Install apache2
```bash
apt install apache2
```

![Install Apache Webserver](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiFjIffONW1igJEXU4bYs5E63F0042VpFiJGbgLtOUxmVyJpGbP01q75IXZ9eenp6FB4ymEhHitlsJwunh_fVBzf98Hw4-0hU9QHm9JThmqSrs4D7u37SuXT3N2hLWHfu_rZ9T5detEnHpDONKiJ3YYzqe-j_E-pRleI4evk-DD8_s7-BZlFFwttOr5xcTb/s0-rw/rmdhnreza.my.id.qbittorrent.nox.10.jpg)

2. Karena ini bukan untuk website disarankan untuk diganti port apache nya, saya ganti port apache nya menggunakan port `5000`
```bash
nano /etc/apache2/ports.conf
```
Catatan: untuk editor `nano` save menggunakan `CTRL` + `O` lalu `CTRL` + `X`

1             |  2
:-------------------------:|:-------------------------:
![Mengubah Port Apache Webserver](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhI5XDdnHmTnwLTS8cXaGir5O5DgdBSNIzGlGpxqhL5gSWV-K7pR3Wnd-qSEOAkWYvCywNpJFPHhPfbGCxryx8_4iVUdYkEv2lVfdfsfSbNGRfqqJ_UiizaTSvronASJVt5T10tQbC52AdjeDSAkW4r7OI5DAZdt9udIHjRK5qCa-zsTjvOjFu49Yim99uU/s0-rw/rmdhnreza.my.id.qbittorrent.nox.12.jpg) | ![Mengubah Port Apache Webserver](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjiBN_Pc0SIu4awtdsbo5rQWdBB7yIeEWDaGaMFhSi-X_AMGX5VLQfeg78V1M958b42rBKFALmlVIbRe_cakDYZGMhjTM0E05XC6Qu_8U722cA7FAHCKCbTkk2SqJru2ASYZWh2qqw4ci0aKbxbs0BSrgw0FYvoZZ1Bjp8uGEsYu12j-Lt2oG9RtDpNlxoD/s0-rw/rmdhnreza.my.id.qbittorrent.nox.13.jpg)


3. Jalankan service apache2 nya
- sysvinit
```bash
service /etc/init.d/apache2 start
```
- systemd
```bash
systemctl start apache2.service
```

![Start Apache2 Webserver](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjrarfiSS_uDCGAMPybIpgoRcHewT0TxdtI3i26-Y8cmdxHz1xZv-e9xiGXXl7teoSeByhxEee0o88MwxnOnj56ZxdT8WePe0y_TfXEmc2G-XsFUw36em6aG7aRL8Gev7O_t2mg-rMD65UqjVVnaj84pFhn14bcEMYg_CeV_ts02wBig4MFE91vI5uHvcRT/s0-rw/rmdhnreza.my.id.qbittorrent.nox.11.jpg)

4. Kita buka halaman `localhost:5000`, jika berhasil maka tampilannya seperti ini

![Buka Halaman Apache2 Webserver](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEg63NSNfUBZ5wE7WnAUOq878ltyxTA8ADgb6_-2xL6QL3eZx7SFUBsToIzKEWAEIMBKa5F5piiTilRbGq73LhsEN4u6MPjv2FJhuMJxOt9C8dYqtwFPgyBD2yyWgA6pOupfler-F6H6NDAVQxZE8mB1lXpb40fNQ7fZ_mpMJNnbg1dlXGyG11QJbplH0RSB/s0-rw/rmdhnreza.my.id.qbittorrent.nox.14.jpg)

5. Kita buat symlink folder `Downloads` ke `/var/www/html`

```bash
ln -sf $HOME/Downloads /var/www/html
```
![Membuat symlink download di apache](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiEsg6iF_8irMjBA3XJTrqdduhrGKGt1aJqCecnWKHmhpCMxXi2ICkdOl4M4g14BAcjSbCSO9vtmtyry89Ycjeu81sW8SzD700F46LHEbTGEM30DV7BafP-5AEyg0rxtEWAO1z_SZ9SfFWcfgIkLsSW9KfpmS9TqRViDBISgrVrWHZTT4XGDb0Bor0ucUKI/s0-rw/rmdhnreza.my.id.qbittorrent.nox.16.jpg)

6. Kita buka halaman `localhost:5000/Downloads`, jika berhasil maka akan muncul hasil download menggunakan bittorrent tadi.

![Halaman Download apache2](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEj5LrRh7F5bUG0YeTgqUQJ4vMrYRqxFQTiwYB_8vywuTWSbDBWD-p82A1bicOrGxks_ZV76K1ViyZk2jYdik-S5nK1oQp5fD9UvaUUV5WL23KdZAJxRt3YzS99AzKhA4u_FEJ3CQqSln_I_OGWoBmZLUTRTIKN519JgIgdZ-knjnVXirbXqbx1pmtCOIKxH/s0-rw/rmdhnreza.my.id.qbittorrent.nox.15.jpg)

{{% adsense %}}
