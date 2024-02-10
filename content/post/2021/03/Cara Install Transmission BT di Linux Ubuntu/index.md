---
title: "Cara Install Transmission BT 3.0 di Linux Ubuntu"
date: 2021-03-13T00:16:23+07:00
description: "Tutorial Install Client Transmission Bittorent 3.0 di Linux Ubuntu dengan Mudah"
categories: ["Linux", "Tutorial"]
tags: ["Linux", "Tutorial"]
description: 'Pada kesempatan kali ini saya akan share tutorial Cara Install Transmission BT 3.0 di Linux Ubuntu. Transmission adalah klien BitTorrent gratis yang tersedia untuk Linux.'
summary: 'Pada kesempatan kali ini saya akan share tutorial Cara Install Transmission BT 3.0 di Linux Ubuntu. Transmission adalah klien BitTorrent gratis yang tersedia untuk Linux.'
image: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEh9Mm0Jyo_yu5VO2cmlTu9Gd8h6R5j6x6Tvxdia06U_HjKRSFVNBGi2NOADu3Y1FMEkwrIONpgH4YJ22Xp3E1bPTUz0_DFJaOCTJPaPhadoC2h81X97280I1khHc_2L8oTZ0XiZPIEfcH37OzRQ-l5ICAhyphenhyphenkbh42-eTyyJZJUdYqsfwEwxR-EU-leDoVvlU/s80-rw/transmission-icon.png
ThumbSchema: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEh9Mm0Jyo_yu5VO2cmlTu9Gd8h6R5j6x6Tvxdia06U_HjKRSFVNBGi2NOADu3Y1FMEkwrIONpgH4YJ22Xp3E1bPTUz0_DFJaOCTJPaPhadoC2h81X97280I1khHc_2L8oTZ0XiZPIEfcH37OzRQ-l5ICAhyphenhyphenkbh42-eTyyJZJUdYqsfwEwxR-EU-leDoVvlU/s0-rw/transmission-icon.png
---

{{% adsense %}}

Pada kesempatan kali ini saya akan share tutorial Cara Install Transmission BT 3.0 di Linux Ubuntu. Transmission adalah klien BitTorrent gratis yang tersedia untuk Linux. Transmission ini menggunakan sumber daya yang sangat sedikit dibandingkan dengan klien BitTorrent lainnya. Aplikasi klien Transmission tidak tersedia di repositori Ubuntu 20.04. Namun, kalian dapat menginstallnya melalui repositori PPA eksternal. Pada saat tutorial ini ditulis, versi Transmission terbaru adalah 3.00.

## Install Transmission 3.0 Ubuntu 18.04 & 20.04
1. Tambahkan ppa berikut ini dan jalankan perintah untuk menginstall transmission nya
```bash
sudo add-apt-repository ppa:transmissionbt/ppa -y && sudo apt install transmission-daemon
```

![Add ppa dan install transmission](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhznykXQ0BAH5szhgZQYeMQG-Veg60RdhFBF4FzklUss-4mzWWn8Nf_Y2_TX7ivFsCme7a2E3ogjk3034PT04gPViYjok7Zuix4tofzCLAGlodgzHBZMHy-7d8GCeoUMa31cl8KhQMRNmg_X2I2HJAuEPCkzlw-qgmQNahcxFHeWQu88TI4ESzLxDtyR8ZV/s0-rw/transmission-1.jpeg)

2. Setelah terinstall jalankan perintah berikut ini untuk menjalankan trasnmission nya dan agar kita bisa setting config nya
```bash
sudo service transmission-daemon start
```
3. Edit config **settings.json** yang terdapat di `/etc/transmission-daemon/settings.json`
```bash
sudo nano /etc/transmission-daemon/settings.json
```

![Start transmission dan edit settings.json](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhTDEHKa_T27k-X0q_q-gYkiBr9zPDMZ3Ql0PS9VVEAOjAqrOHgdizas7ZZvkCsymw3YFm9QDqy-ZSWw86nn_Zf0jmxF7xn5T9XAxthu7WkM_3SRKqjqV0A5DHMoaScuCh3hI_uihfUlUO3xZQWX_Pj3NZYlbYQY5c8CFq4KTqjdpTzAkCzWAp9zmP6iCUK/s0-rw/transmission-2.jpeg)

4. Ubah bagian yang kalian perlukan, disini saya hanya mengubah bagian ini saja, setelah selesai edit kalian bisa simpan dengan cara `CTRL + O` `Enter` `CTRL + X` untuk editor `nano`
```json
{
    "download-dir": "/home/rmdhnreza/Downloads", // <- Ubah direktori download torrent nya sesuai keinginan kalian
    "rpc-authentication-required": true, // <- Ubah ke false jika kalian tidak ingin menggunakan username/password untuk Login
    "rpc-password": "rmdhnreza", // <- Password untuk login, jika  "rpc-authentication-required": true
    "rpc-port": 9091, // <- Port bisa kalian ubah sesuai keigininan kalian, asal port nya belum terpakai oleh aplikasi lain
    "rpc-url": "/rmdhnreza/", // <- Ubah sesuai keinginan kalian, URL nya jadi seperti ini http://localhost:9091/rmdhnreza/web
    "rpc-username": "rmdhnreza", // <- Username untuk login, jika  "rpc-authentication-required": true
    "rpc-whitelist": "*", // <- Ubah dari 127.0.0.1 ke *
}
```
5. Reload config dan restart transmission-daemon
```bash
sudo service transmission-daemon reload && sudo service transmission-daemon restart
```

![Reload dan restart transmission](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhVQ3bsHpwFjkrmYzuMvQR4k2vU9Tz-KteVBpEz06UrTPDWyHFjLcyLyH36C69IL2yIhLNcDzar3p0sGrxmCB2-cy8PjAPiT3RmVus_z66ZRoMWCk-qQp1JYNaURBIJiMRXlVhsdEJON_gkmUbs0RgRf_U2Q_HQx7X_1y2zzzg2boS-fbbnbASvlYXEmHJe/s0-rw/transmission-3.jpeg)

{{% adsense %}}

6. Buka web address, disini saja menggunakan local computer jadi ip nya 127.0.0.1 atau localhost, jika kalian menggunakan VPS kalian masukan IP nya
```
http://127.0.0.1:9091
http://localhost:9091
http://ip.v.p.s:9091
```
7. Jika berhasil maka akan ada prompt untuk memasukan username & password, dengan catatan di config nya kalian set `"rpc-authentication-required": true`, jika `"rpc-authentication-required": false` maka tidak akan muncul prompt ini

![Prompt username dan password](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhcJHnt7IXTRPrs6YVTjX2kNDmbO_xY46ebS0UyUZ7j6RS5-VhUIljp-NyF4BokBu8dmitsQPL7jyndRmo1lR8glV8cOviDnrXMONnG71SfjNPMghslb0fdNcjvifa9FoV39D5MLupElqjDcTeKVOznast_Re1E6oBqJybYZNswB9f0btV8f82ZMv6UcbCp/s0-rw/transmission-4.jpeg)

8. Sekarang kalian bisa langsung add torrent file atau magnet link

![Add torrent yang akan kalian download](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEivKAFjQiAooY8pLnENXCdKXanDOxh6Z93iq1w2DTo9OQ1MLWwBx2epwF5-Gvew9pSgZ34Kc201KJ1CoM2P_S4HvG_yFcGKqhH3DTW84FYLf1QQofPka9swjyCBOZWcd5jWvk8GIjXDwY6wHUItnfgzlhJGMpUQdyrQze79ccp9Wf8gscQY_EXPj0AY2Txh/s0-rw/transmission-5.jpeg)

9.  Jika pada saat download kalian mendapati error `Permission Denied`, kalian bisa ubah permission `"download-dir": "/home/rmdhnreza/Downloads"` nya dengan cara
```bash
chmod 777 /home/rmdhnreza/Downloads
```

![Error permission denied](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgHp9GURbobPZbTqQClqehlsgUARVoqYKzrDlBnI_HOVppNJOdTpVSdgA17OIcJ3oMRHyUapNI3syYfoHRRiWg8-2pXjn3-XG3AJnpaAtB6izqb8pO-jheZ6nRczeQ7PL8Vuz0n1dWlx3WGT7beLm1fzU-LD23NQNnUY5zycWN2MCwWnEFkhU4dr1Ttj1Zh/s0-rw/transmission-6.jpeg) | ![Ubah permission folder Downloads](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgLfZCjX6xcJ5SjoI03Kqf7rJBzALYCjkRiUD-uuEMQv8YnJkz6I79AV5S9PY1X3E_54g8BzmUMjQUTzOqJvh_Zydm-bIR1yrRqLyPgLSuCZbXPoosX5PdGP4OVxsooiribbFk4L3wEc1XnyBy_v_SPlnHdZ853yA0Ys7DUh6P0ag4yL7fVTxGzrDIa9CS9/s0-rw/transmission-7.jpeg)

{{% adsense %}}

10. Add lagi torrent yang kalian download, sudah pasti sekarang tidak akan mendapati error `Permission Denied`

![File torrent sedang di download](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEg2JmOdd7B3lhtF6cFzlKouOWg1UxrTasZa8NflsFnMlZTJEiA6CJtKUWH1uLuKNyJfpxmYxekwjDKWUtMWHV1oZwzIfxKKxiT-X-oDZFPGyhIK_xHozv8Cpn2kkgsQkDfpz2Pk6n_UiaMhFkKxyxhHzx5gXCXtPFEyxSL-fMfoySxj-n5yWBEIDNWiKdtl/s0-rw/transmission-8.jpeg)

11. Jika torrent sudah selesai cek folder download nya

![Torrent berhasil di Download](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEj_q2ucWPiWBXivZITjn780550XLm9iSVPWHqH1to9XV3-c57JWOatsb4C8-IPo1FDo819zVIqXXAmXEzp_3XLcr3yPVSFBK7u9Og0akXg6r35yp_ZdXPtoz4yoEliGOv_RYoha603Hc_kw-go5t2jrBnmzrtuER8VgYmxI87eXxLnRIE3EmWUGbhQfVcPr/s0-rw/transmission-10.jpeg)

{{% adsense %}}

## Untuk pengguna VPS
1. Kalian install terlebih dahulu apache2
```bash
sudo apt install apache2
```
2. Jalankan apache2 nya dengan perintah
```bash
sudo service apache2 start
```
3. Buat symlink directory download ke `/var/www/html`
```bash
sudo ln -s /home/rmdhnreza/Downloads /var/www/html
```
4. Buka di browser `http://ip.v.p.s/Downloads` jika kalian edit port apache2 nya menjadi 5000 (misalnya), maka `http://ip.v.p.s:5000/Downloads`

![Torrent yang berhasil di Download di VPS](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhujk90XjfVw10WSAfdyDbeMNK8o4HNGBPCPufvxu_4SgXij2Q8YeaOagvJZFEgeJMgWCY8uxyzsGBIkjx-gopCVocqbvYH8EbT-uy4sqk7wgUYJ2Dh5HiIVBR6DQ7LiQchZYpF4Uj0tcsVno1PXkbdFSwTjpZJ-2CwRkI0HHAOT4vXnN-1fXDzH-ywkT7g/s0-rw/transmission-9.jpeg)

{{% adsense %}}
