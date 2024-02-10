---
title: 'Install v2ray Websocket TLS CDN Ubuntu 22.04'
date: 2022-08-31T15:30:13+07:00
description: 'Tutorial Install v2ray VLESS + TCP + TLS/XTLS-direct/XTLS-splice, VLESS + WS + TLS + CDN, VMess + WS + TLS + CDN, VLESS + gRPC + TLS + CDN, Trojan + TLS, Trojan + gRPC + TLS Ubuntu 22.04'
categories: ['Linux', 'Tutorial']
tags: ['Linux', 'Tutorial']
keywords:
  [
    'Tutorial Install v2ray Websocket TLS CDN Ubuntu 22.04',
    'Cara Install v2ray Websocket TLS CDN Ubuntu 22.04',
    'Tutorial Install v2ray VLESS TCP TLS/XTLS-direct/XTLS-splice Ubuntu 22.04',
    'Cara Install v2ray VLESS TCP TLS/XTLS-direct/XTLS-splice Ubuntu 22.04',
    'Tutorial Install v2ray VLESS WS TLS CDN Ubuntu 22.04',
    'Cara Install v2ray VLESS WS TLS CDN Ubuntu 22.04',
    'Tutorial Install v2ray VMess WS TLS CDN Ubuntu 22.04',
    'Cara Install v2ray VMess WS TLS CDN Ubuntu 22.04',
    'Tutorial Install v2ray VLESS gRPC TLS CDN Ubuntu 22.04',
    'Cara Install v2ray VLESS gRPC TLS CDN Ubuntu 22.04',
    'Tutorial Install v2ray Trojan TLS Ubuntu 22.04',
    'Cara Install v2ray Trojan TLS Ubuntu 22.04',
    'Tutorial Install v2ray Trojan gRPC TLS Ubuntu 22.04',
    'Cara Install v2ray Trojan gRPC TLS Ubuntu 22.04',
  ]
description: 'Install v2ray Websocket TLS CDN Ubuntu'
summary: 'Install v2ray Websocket TLS CDN Ubuntu'
image: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhsq5qCD4I90uIzNOHH1GnE1NG1ytTgb-sNPOGRPNWQl0LZk-Ndm6ew4jLXm2ELpvz0axp0nYwbgD_pYTV5eh4c8WQUXF6Cf-8H3J6scIxqyj8N4GjOpgamf5V9oWsr1-GFJ0lGt9C8xMxGVnPyLKZkONVVFFE3rsIq-wUaGtDQVHjDfb2cCkFlOZBTIJ0O/s80-rw/v2ray-logo.jpg
ThumbSchema: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhsq5qCD4I90uIzNOHH1GnE1NG1ytTgb-sNPOGRPNWQl0LZk-Ndm6ew4jLXm2ELpvz0axp0nYwbgD_pYTV5eh4c8WQUXF6Cf-8H3J6scIxqyj8N4GjOpgamf5V9oWsr1-GFJ0lGt9C8xMxGVnPyLKZkONVVFFE3rsIq-wUaGtDQVHjDfb2cCkFlOZBTIJ0O/s0-rw/v2ray-logo.jpg
---

## V2Ray
**V2Ray** adalah inti dari **Project V**, yang bertanggung jawab untuk merealisasikan protokol, fungsi jaringan, dan berkomunikasi dengan protokol **Project V** lainnya.

**Features:**
1. **Multiple inbound/outbound proxies**: one V2Ray instance supports in parallel multiple inbound and outbound protocols. Each protocol works independently.
2. **Customizable routing**: incoming traffic can be sent to different outbounds based on routing configuration. It is easy to route traffic by target region or domain.
3. **Multiple protocols**: V2Ray supports multiple protocols, including Socks, HTTP, Shadowsocks, VMess etc. Each protocol may have its own transport, such as TCP, mKCP, WebSocket etc.
4. **Obfuscation**: V2Ray has built in obfuscation to hide traffic in TLS, and can run in parallel with web servers.
5. **Reverse proxy**: General support of reverse proxy. Can be used to build tunnels to localhost.
6. **Multiple platforms**: V2Ray runs natively on Windows, Mac OS, Linux, etc. There is also third party support on mobile.

## Bahan yang harus di persiapkan

1. **Domain**: Boleh menggunakan domain gratis atau berbayar (disini saya menggunakan domain gratis dari [freenom.com](https://freenom.com))
2. **VPS**: VPS yang saya gunakan menggunakan Digital Ocean dengan Sistem Operasi Ubuntu 22.04 (Jammy Jellyfish), tapi kalian boleh menggunakan VPS dari mana saja asal bisa akses **root**
3. **Akun Cloudflare**: Untuk CDN nya.

## Menambahkan Domain ke Cloudflare

{{% note %}} Sebelum setting domain, pastikan kalian sudah mempunyai domain sendiri dan akun Cloudflare {{% /note %}}


Disini saya akan menggunakan domain gratis dari freenom yaitu `rmdhnreza.tk`

1. ***Add site*** di Cloudflare dan pilih saja ***Free Plan***

1                          | 2
:-------------------------:|:-------------------------:
![Add Site](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhOjYqgCV9KAopub95HP84de946fhQvhijebeg_uWLDFpehWIK_kNaGDnNL9ASsaYp504bcYhmKznYwlBaKebOptVyCG8N74OlxRmcZwkP1bbYpQZFpXDB90Mrh0YzfR1HGKWlVlEMuYrrWSIETdLDpkGUUdJdAbuTzmpZ5qMGJax105L9WOUKynLakTSzG/s0-rw/rmdhnreza.my.id.v2ray.websocket.tls.cdn.2.jpg) | ![Free Plan](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgDmvl4hPykoXcizof4OmoLjTdb3kJAf-fqHyL9SIZLC_Wcf1Bq1xYq4jJSr96ZQHuVhVzJdSpXbKsXd47d9oPF04twvN-qnXVi5x7rOZ7s53tkXBYFalW-i6tV9MbuYF8dj0dvsa_MRVBvAq1l5JDQGGe6s-HgOvBvfa_NhFFxqtpLH5hRKrdjO5EAhssN/s0-rw/rmdhnreza.my.id.v2ray.websocket.tls.cdn.3.jpg)

2. Untuk DNS, jika kosong seperti ini cukup klik ***Continue*** saja. Nanti akan muncul *pop up* ***Add records later*** kalian klik saja ***Confirm***

1                          |  2
:-------------------------:|:-------------------------:
![DNS Record](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEj-TXUtMZVMP0st02PMTI2kNdE3e35AUBf-zQfG0FKYMjb2caeXKgEU5rzzCS4MmLgkBd3PV_U94-nreZDRdwG0v4Km0Z2EZy1v4o1Hn6FhRcUblAiaszUY6Na3TaBh3i5e9yvpFQVVO15tRQBmBZmOr5jql28lBQ63Opln3GDq-U7yy27hGcnVO9NINprx/s0-rw/rmdhnreza.my.id.v2ray.websocket.tls.cdn.4.jpg) | ![Confirm](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjLYMOCrTBLLb3HeS1wrqlqgiCAtOiLeLlqZP1e-tbBseUabdM7R2utk818ElxLHM_mVGTiAqHd9pLT_QuGcXqxhpE-yPxHJlJ3Qh9WdGzfBxlli6tKCHfM2pwj9jF4dtZMSHOJeTFv0xr_JNtBx1jvlOMnlD3XfxTkO7hEdtBjtADf_AwMompIhlV21OF1/s0-rw/rmdhnreza.my.id.v2ray.websocket.tls.cdn.5.jpg)

3. Pointing *nameserver* dari cloudflare ke domain kalian, jika sudah klik ***Done, check nameserver***

1             |  2
:-------------------------:|:-------------------------:
![Nameserver Cloudflare](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEj8xT1NBNjeuK5Gk4-50oQ5oFW3s5pQakA1dmq_nYn1_H9uyJRjsJ11J0NqJO-qcCAhpvAKrnlfUy7q5DZmrkNvelL0zS3al3SnDgLz1R7PJSoHCw1Dg6em5ZC4JjHZ9kaUGBSFK5nuxh0Qzp72X3kAh_eMvTQ20DEBJdqBO7YVlvqjdZ0tLv7srEc2eghl/s0-rw/rmdhnreza.my.id.v2ray.websocket.tls.cdn.6.jpg) | ![Nameserver Domain](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEh760d7FaHCfLp3pSrV4K8mcKVO7YVRwMacNvdKRnR_G4ZSagfbcSKFx88Hxokqcz7LTaMnDHhgcgP7a6o6qFGfTvxDJsLTtYSVR3Y6FOlraZzb3WT710b_v12esxHJZxrg49EzOpOiY_uC3S73M8JlEw9C4Bo86LaRdrmC7vRUMqKejJ4Aa9bFfuvoBdNA/s0-rw/rmdhnreza.my.id.v2ray.websocket.tls.cdn.7.jpg)

4. Pada bagian ***Quick Start Guide*** kalian klik ***Finish later***

![Klik Finish later](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiRTj-OuYT9HTiy6HaizbZKKkmquCziedlv6TAGHXUIOIw5otR9z9Ay-31fjO2D6FK9mmvHT4X1bONGD4bgFnkP5Qrx0blQeWrfz90uyq1sQoR-zA7aC4wbpehglhnDvMHAh9Aho7Xr6v2rbpoEHKeD0yIITAEk6EKPYO9ZeFTKHEB3d2C4Esb8EiErKXYr/s0-rw/rmdhnreza.my.id.v2ray.websocket.tls.cdn.8.jpg)

5. Tunggu beberapa sampai domain kalian aktif, proses ini tidak membutuhkan waktu lama (kurang dari 10 menit). Pastikan saja langkah nomer 3 sudah benar.

1                           |  2 | 3
:-------------------------:|:-------------------------:|:-------------------------:
![Domain Pending](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEi5-cNrasZQvD7u0wiT4WA9px99NeYzm0NMZx1x0d00rP00oeiJK5_7XCyCXoGoYI0JSyJvJmx2AmHjG9-V6VUaGC-EIsBIXms0VN4qEbErPLCSrDkeIkd8YZNzwhaZQQ8QGJhkHmzALXTQUWN5k0-U_fNW-yyhJmOd_dx9rYBQnJO3nyOyMkT1n2HEHkXW/s0-rw/rmdhnreza.my.id.v2ray.websocket.tls.cdn.9.jpg) | ![Domain Pending](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgnt6MoOTlvFryAwAMf-qXCpxc0vRI3xSoATRbo6q2-sJRnNsD-A7eaY7kw4hkHT-BdFSx1vMz9-inm4AYbkpP1bfhHb6e8F6AXuOxUSVHFafi6h0ZSnW7Kmc8nmsFf4EKqNb8hKH7VvjpyNme5F9_SXfaywA3ue9cXCIk0dXZ9FZ4kMTns3xChqdSWf8xk/s0-rw/rmdhnreza.my.id.v2ray.websocket.tls.cdn.10.jpg) | ![Domain Aktif](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjcw4H-UwW5R19kZnfRSLBwjUvWMo12PAQa9aei2K0yV9_P8Uq24LwFDjObEy65x2f9RJPk1Z4ZTitoyyMW9kaFNiacEKhi65I1TQT0koL5FZxUjWgksrwF8Vd8PVhVqauJ7BTAiTTJ2wBNAV4M7SK91cNb8H75gP63JHZHnYtSaq0gZICCGfhThmVuOPzp/s0-rw/rmdhnreza.my.id.v2ray.websocket.tls.cdn.11.jpg)

6. Setelah aktif, masuk ke bagian DNS dan klik pada **Add Record**, Pointing **IP VPS** ke domain yang sudah di daftarkan, pada bagian **Proxy Status**, untuk sekarang pastikan kalian pilih **DNS Only**, tapi diakhir kita ubah ke **Proxied**

| Type  |  Name (required) | Target (required) | Proxy Status | TTL
|---|---|---|---|---|
|  A | ray | IPVPS | DNS Only | Auto

{{% note %}} Untuk "ray" kalian bisa ganti dengan apa saja. Intinya, ini adalah subdomain dan dipakai untuk host v2ray nantinya{{% /note %}}

![Pointing IP VPS](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhD9V01ELitd_m19yuRBz0pMh-Hgb4Za3MUepqC1e0YRUtEj8KfU-EV_V29V4fL4onawat4Qvf35Z723Mr7JVI0RnAeyInv16UBEwG_mbDPPDJzrPXSvjqxKtAZHf1aMDy-FJ3inVB1sMsqFSMTqCRAcUuc5xiqHvWYK8-E9ohifdZWYykoTqax8AEvEuMI/s0-rw/rmdhnreza.my.id.v2ray.websocket.tls.cdn.12.jpg)

7. Masuk ke bagian **SSL/TLS** lalu pilih **Full**

![Setting SSL/TLS](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjk6RFVu87fwcSKJPehENrtZEmHmXvLDFhCAHFCKxzeoxw5DYlcMaL-UK7h4xtcB4snQiosgE1Vf1E9B7dHPgLiTGuWL4QfiCYeXFNjUWO3lhyKAY32bn-3geZFxEr7aHk3YIWZACogh9rqRZyMyx8Hko79M6cZyv8LvOCyM56Q80kWF9G35Uc5oYk_BCSP/s0-rw/rmdhnreza.my.id.v2ray.websocket.tls.cdn.13.jpg)

8. Masuk ke bagian **Edge Certificates** lalu settings **Minimum TLS Version** ke **TLS 1.2**

![Minimum TLS Version](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjLnQ2J_u3s1ntglMztv3nWroh4uC8V1PZnZH1vf6pb-JSKoBIQ5PSrFD66wt12F6KPSWfrd8Fe2vSC6ZWL20XKUfIsSgCi4cpP7cguGr8-Yq8jDVOhA0_zRPQKdO0eFnSPR-XRFCO2d0NZbVYxfueZAfSZZHPUsPPnFuC5B-wslgMu7uWq6r-t8Oy24kko/s0-rw/rmdhnreza.my.id.v2ray.websocket.tls.cdn.14.jpg)

## Install V2Ray

{{% note %}} Untuk menghindari kegagalan dalam installasi V2Ray, saya sarankan kalian memakai VPS yang baru di buat {{% /note %}}

Disini kita akan install V2Ray menggunakan **Mack-A script** sayangnya script ini hanya berbahasa China, tetapi kalian cukup ikuti saja langkah-langkah nya.

1. Pastikan kalian login sebagai **root**, karena kita juga akan menginstall certificate dari letsencrypt.

```fish
sudo su
```

2. Update sistem nya

```fish
sudo apt update -y && sudo apt upgrade -y && sudo apt autoremove -y
```

1             |  2
:-------------------------:|:-------------------------:
![Update System](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgjdeUgJNeWOI5lRyvvJjNgWSe8bv7kYU6TQAQTqjzUyz7BvtaeODTaIW-HEfT36J_6d97xWftFhybaQC01bMdLbsWVbsVYfRlT32srnGkglYk_e4LozsdmYMwfmTJHiO1WuHqnVPb6yWftF3HOdbIj0oJCPtvjSn70clzPQQJK9Ja1Y8ayg01bIbBee8De/s0-rw/rmdhnreza.my.id.v2ray.websocket.tls.cdn.15.jpg) | ![Update System](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhy0VrS6L6FmLfp_69-l3CgxL1FPJu1KZaa7yqt7fAVEVeb8c-shDeAVCD6tOizuYgqBMBOGVzKd7vJJLsyGrvLOtwZzB5PXD2tIOEw-w83wLO0ImqI0JwhklNrHgLhkFudBMBrKFLrCgn1JNEwnG1xlu87GYUojlZLqxz-2VaGLotjFj0w646tY7fTQBqo/s0-rw/rmdhnreza.my.id.v2ray.websocket.tls.cdn.16.jpg)

3. Jika kalian melakukan update Kernel, pastikan restart terlebih dahulu sebelum menjalankan script nya

```fish
sudo reboot
```

![Update System](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgxuJjDw69oZDTvCo69PVqtb-rx4LNJGWOTRSOnuRCVQpXroEK0vHLsUKXGYBkLpI-j_CK3guE8cMXcqGMn7_IhjEF89t4hxdvbvGlED9xuolUkubiA2PfqL9YE-l1FeMgGZMdaG554Bj6pS1R5XWabLrEJgL_vPgr6f6eSy7jJGKN4Xj7ArZelQr1fkHII/s0-rw/rmdhnreza.my.id.v2ray.websocket.tls.cdn.17.jpg)

4. Download script berikut ini

```fish
wget "https://raw.githubusercontent.com/mack-a/v2ray-agent/master/install.sh"
```

5. Jalankan script nya

```fish
bash install.sh
```

![V2Ray script](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEilu00TdTU3ke0Z3FJ3bLBHh8usUeFnRMiEWYEgEFZd0fH32nxKiYfeZVeZtojWIyS4eT7JeVBXNH0B8rJ_I6cW-dbZRkA-IDBWnpWW1V9sf7ArqxJxK6QB_NEJqncDtJ5smj3aOmTLNdZ3SnzkUUxvIBsekOdLuzfRyNc06bvnWE6PSbxxsBfUxtjL0zCY/s0-rw/rmdhnreza.my.id.v2ray.websocket.tls.cdn.18.jpg)

6. Nanti muncul pilihan seperti ini dan kalian pilih nomor `1` lalu `Enter`

```fish
==============================================================
作者:mack-a
当前版本:v2.5.73
Github:https://github.com/mack-a/v2ray-agent
描述:八合一共存脚本
核心: v2ray-core[运行中]
已安装协议: VLESS+TCP[TLS] VLESS+WS[TLS] Trojan+gRPC[TLS]
            VMess+WS[TLS] Trojan+TCP[TLS] VLESS+gRPC[TLS]
==============================================================
                        推广区
AFF捐赠：https://github.com/mack-a/v2ray-agent/blob/master/documents/donation_aff.md

虚拟币捐赠：0xB08b731653515b083deE362fefFc45d5eb96c35d

推广可联系TG：https://t.me/mackaff
==============================================================
1.重新安装                 Install
2.任意组合安装             Install in any combination
3.切换Trojan[XTLS]         Toggle Trojan [XTLS]
---------工具管理--------- ---------Tool---------
4.账号管理                 Account management
5.更换伪装站               Replace the camouflage station
6.更新证书                 Update the certificate
7.更换CDN节点              Replace the CDN node
8.IPv6分流                 IPv6 offload
9.WARP分流                 WARP shunt
10.流媒体工具              Streaming Tools
11.添加新端口              Add a new port
12.BT下载管理              BT download management
13.切换alpn                Toggle alpn
14.域名黑名单              Domain Blacklist
---------版本管理--------- ---------Version---------
15.core管理                core management
16.更新脚本                Update the script
17.安装BBR、DD脚本         Install BBR, DD scripts
---------脚本管理--------- ---------Script---------
18.查看日志                View logs
19.卸载脚本                Uninstall script
==============================================================
请选择:1                   Please select:1
```

![Install V2Ray](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiF9y-UF3lFMnb6tBrzS6GL_seRasF0t7IMiGFWKaSp-3cEAQseB_R3sZCpUvx9Ze_T_vcFNmxk-MR7NXQEsQj6EsgKr3ZtchZF6qt5545tJMODVx1TlBd6-FjG59UpT2TcSv102qNb6ehs9XHR1OCRdgHZ4BDTurMcxqqxaV3e4aMCUh7wgn-f28Rl2dow/s0-rw/rmdhnreza.my.id.v2ray.websocket.tls.cdn.19.jpg)

7. Pilih **v2ray-core** nomor **2**

```fish
功能 1/1 : 选择核心安装     1/1 : Select Core Installation

========================    ===============================
1.Xray-core
2.v2ray-core
========================    ===============================
请选择:2                    Please select:2
```

![Install V2Ray](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjvWJ0zmjln5ZeTtU4D7O_EcwBgwLQUlLVJOVjnTMy8oeykEvYMpT0HhmqyFEZVrSZ_5IRKmL55ntgGHABvQCVzguAZDpqFcmvk5sZRFlUvMaqF9rwYaMijXuxOXnJLmnzQmViBLVk-2KqjNZb_7D38Px0C3J0PC9vyBNNvgrjbxaZMJFGZascqyp63bBx3/s0-rw/rmdhnreza.my.id.v2ray.websocket.tls.cdn.20.jpg)

Kita akan melihat penginstallan otomatis untuk dependency yang dibutuhkan

```fish
进度  2/13 : 安装工具
 ---> 检查、安装更新【新机器会很慢，如长时间无反应，请手动停止后重新执行】
 ---> 安装unzip
 ---> 安装socat
 ---> 安装jq
 ---> 安装binutils
 ---> 安装qrencode
 ---> 安装lsb-release
 ---> 安装nginx
Synchronizing state of nginx.service with SysV service script with /lib/systemd/systemd-sysv-install.
Executing: /lib/systemd/systemd-sysv-install enable nginx
 ---> 安装semanage
 ---> 安装acme.sh
 ```

 8. Masukan domain yang di pointing ke IP VPS kita, ada dibagian [Menambahkan Domain ke Cloudflare Langkah 6](http://localhost:1313/install-v2ray-websocket-tls-cdn-ubuntu-22.04/#menambahkan-domain-ke-cloudflare). Jika berhasil maka akan muncul IP VPS kita.

```fish
进度  3/13 : 初始化Nginx申请证书配置              Progress 3/13 : Initialize Nginx application certificate configuration

请输入要配置的域名 例: www.v2ray-agent.com --->   Please enter the domain name to be configured Example: www.v2ray-agent.com --->
域名:ray.rmdhnreza.tk                             Domain: ray.rmdhnreza.tk
 ---> Nginx启动成功                               ---> Nginx started successfully
 ---> 检查域名ip中                                ---> Check the domain name ip
 ---> Nginx关闭成功                               ---> Nginx closed successfully
 ---> 当前域名ip为:[167.172.92.148]               ---> The current domain name ip is: [167.172.92.148]
```

![Install V2Ray](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgo9r5vk2MY49w-9RxzOcfTKWflnJEPceFWWreyFAxgQRj20O-4UmjokLbnK1ooyAquUD9XPT2Js-JG8UI_s0qV2XtjmHKMNS2dhB6r5_YIco8J0A3dDhMaEDSai_ml4Tz6adrIrR5qZCipD8w3_64EjmDBVkbeX_nIY2vSWpM3tHIS8CCzfYSgMUhOfRVV/s0-rw/rmdhnreza.my.id.v2ray.websocket.tls.cdn.21.jpg)

9. Penginstallan TLS

{{% note %}} Jika gagal dalam penginstallan TLS, pastikan Menambahkan Domain ke Cloudflare Langkah 7 sudah benar {{% /note %}}

```fish
进度  4/13 : 申请TLS证书    Progress 4/13 : Apply for TLS certificate

 ---> 安装TLS证书           ---> Install TLS certificate
 ---> TLS生成成功           ---> TLS generation succeeded
 ```

10. Path untuk websocket, disini saya menggunakan `v2ray` kalian bebas isi apa saja\
   Nantinya path websocket nya seperti ini `/v2rayws`

```fish
进度  5/13 : 生成随机路径                                Progress 5/13 : Generate random paths
请输入自定义路径[例: alone]，不需要斜杠，[回车]随机路径  Please enter a custom path [Example: alone], no slashes required, [Enter] random path
路径:v2ray                                               Path: v2ray

path:v2ray                                               path:v2ray
```

![Install V2Ray](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhlV-qASMssMN4kLLUYXulIk28dAY2WDZJLjK5JbbScrN2jOnLQHLe-Vux-gArsRDtg0uFT2yiOBe_yfm78AgT_RJBDMiC5VU5AqbK3ibgAXpraqOfGQ-H5uNcrh9IYa3wK5Bt5wwlZ92b0wmqvxLaFFhfAtRlCaSKmOs859JI2um7zMWPozjHU1-4wplpE/s0-rw/rmdhnreza.my.id.v2ray.websocket.tls.cdn.22.jpg)

11. Pada bagian ini kalian pilih `www.cloudflare.com` nomor 2

```fish
进度  6/13 : 安装V2Ray
 ---> v2ray-core版本:v4.45.2
v2ray-linux-64.zip         100%[=====================================>]  13.17M  --.-KB/s    in 0.04s

进度  7/13 : 配置V2Ray开机自启
Created symlink /etc/systemd/system/multi-user.target.wants/v2ray.service → /etc/systemd/system/v2ray.service.
 ---> 配置V2Ray开机自启成功

进度 8/13 : 添加cloudflare自选CNAME

==============================================================
# 注意事项                            # Precautions

教程地址:                             Tutorial address:
https://github.com/mack-a/v2ray-agent/blob/master/documents/optimize_V2Ray.md

如对Cloudflare优化不了解，请不要使用  If you don't know about Cloudflare optimization, please don't use

 1.移动:104.16.123.96                 1. Mobile: 104.16.123.96
 2.联通:www.cloudflare.com            2. Unicom: www.cloudflare.com
 3.电信:www.digitalocean.com          3. Telecom: www.digitalocean.com
----------------------------          --------------------------------
请选择[回车不使用]:2                  Please select [Enter not used]: 2
```

![Install V2Ray](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEg2uJZKxRNHLYEia4VtUPuHMSqrn9Q4CPLDGWQV3YyAQptfZYn5FrTCEuxcGlJc9EeNdj0K8wED39WMPFExYlGwnm1jwJanPSpvkXzRkViP4DxQbvHzkd3islHvuU4A7p3WeLEgGzE3Xqy4UD3OXkvr9PCW0WsGAcvg3aF7YZfQBWRnOfw8pwrCLV8jvrlP/s0-rw/rmdhnreza.my.id.v2ray.websocket.tls.cdn.23.jpg)

12. Customize UUID, jika kalian ingin menggunakan UUID kalian, bisa pilih `y` lalu masukan custom UUID kalian, tetapi disini saya pilih `n` jadi, UUID nya diisi otomatis.

```fish
进度 9/13 : 初始化V2Ray配置     Progress 9/13 : Initialize V2Ray configuration

是否自定义UUID ？[y/n]:n        Customize UUID? [y/n]:n


进度 10/13 : 添加定时维护证书   Progress 10/13 : Add scheduled maintenance certificate

 ---> 添加定时维护证书成功      ---> Add timed maintenance certificate successfully

进度 11/13 : 添加伪装站点       Progress 11/13 : Add camouflage site
 ---> 添加伪装站点成功          ---> Add fake site successfully
 ---> V2Ray关闭成功             ---> V2Ray closed successfully
 ---> V2Ray启动成功             ---> V2Ray started successfully
 ---> Nginx启动成功             ---> Nginx started successfully

进度 12/13 : 验证服务启动状态   Progress 12/13 : Verify service startup status
 ---> 服务启动成功              ---> Service started successfully
```

13. Jika berhasil, maka akan muncul config V2Ray nya.

{{< spoiler text=" Config" >}}

```fish
===================== VLESS TCP TLS/XTLS-direct/XTLS-splice ======================


 ---> 帐号:ray.rmdhnreza.tk_VLESS_TLS-direct_TCP

 ---> 通用格式(VLESS+TCP+TLS)
    vless://41b11314-61c4-95a5-7412-f18ce65162d2@ray.rmdhnreza.tk:443?security=tls&encryption=none&host=ray.rmdhnreza.tk&headerType=none&type=tcp#ray.rmdhnreza.tk_VLESS_TLS-direct_TCP

 ---> 格式化明文(VLESS+TCP+TLS/xtls-rprx-splice)
    协议类型:VLESS，地址:ray.rmdhnreza.tk，端口:443，用户ID:41b11314-61c4-95a5-7412-f18ce65162d2，安全:tls，传输方式:tcp，账户名:ray.rmdhnreza.tk_VLESS_TLS-splice_TCP

 ---> 二维码 VLESS(VLESS+TCP+TLS)
    https://api.qrserver.com/v1/create-qr-code/?size=400x400&data=vless%3a%2f%2f41b11314-61c4-95a5-7412-f18ce65162d2%40ray.rmdhnreza.tk%3a443%3fsecurity%3dtls%26encryption%3dnone%26host%3dray.rmdhnreza.tk%26headerType%3dnone%26type%3dtcp%23ray.rmdhnreza.tk_VLESS_TLS-direct_TCP


================================ VLESS WS TLS CDN ================================


 ---> 帐号:ray.rmdhnreza.tk_VLESS_WS

 ---> 通用格式(VLESS+WS+TLS)
    vless://41b11314-61c4-95a5-7412-f18ce65162d2@www.cloudflare.com:443?encryption=none&security=tls&type=ws&host=ray.rmdhnreza.tk&sni=ray.rmdhnreza.tk&path=/v2rayws#ray.rmdhnreza.tk_VLESS_WS

 ---> 格式化明文(VLESS+WS+TLS)
    协议类型:VLESS，地址:www.cloudflare.com，伪装域名/SNI:ray.rmdhnreza.tk，端口:443，用户ID:41b11314-61c4-95a5-7412-f18ce65162d2，安全:tls，传输方式:ws，路径:/v2rayws，账户名:ray.rmdhnreza.tk_VLESS_WS

 ---> 二维码 VLESS(VLESS+WS+TLS)
    https://api.qrserver.com/v1/create-qr-code/?size=400x400&data=vless%3A%2F%2F41b11314-61c4-95a5-7412-f18ce65162d2%40www.cloudflare.com%3A443%3Fencryption%3Dnone%26security%3Dtls%26type%3Dws%26host%3Dray.rmdhnreza.tk%26sni%3Dray.rmdhnreza.tk%26path%3D%252fv2rayws%23ray.rmdhnreza.tk_VLESS_WS

================================ VMess WS TLS CDN ================================


 ---> 帐号:ray.rmdhnreza.tk_vmess_ws

 ---> 通用json(VMess+WS+TLS)
    {"port":443,"ps":"ray.rmdhnreza.tk_vmess_ws","tls":"tls","id":"41b11314-61c4-95a5-7412-f18ce65162d2","aid":0,"v":2,"host":"ray.rmdhnreza.tk","type":"none","path":"/v2rayvws","net":"ws","add":"www.cloudflare.com","allowInsecure":0,"method":"none","peer":"ray.rmdhnreza.tk","sni":"ray.rmdhnreza.tk"}

 ---> 通用vmess(VMess+WS+TLS)链接
    vmess://eyJwb3J0Ijo0NDMsInBzIjoicmF5LnJtZGhucmV6YS50a192bWVzc193cyIsInRscyI6InRscyIsImlkIjoiNDFiMTEzMTQtNjFjNC05NWE1LTc0MTItZjE4Y2U2NTE2MmQyIiwiYWlkIjowLCJ2IjoyLCJob3N0IjoicmF5LnJtZGhucmV6YS50ayIsInR5cGUiOiJub25lIiwicGF0aCI6Ii92MnJheXZ3cyIsIm5ldCI6IndzIiwiYWRkIjoid3d3LmNsb3VkZmxhcmUuY29tIiwiYWxsb3dJbnNlY3VyZSI6MCwibWV0aG9kIjoibm9uZSIsInBlZXIiOiJyYXkucm1kaG5yZXphLnRrIiwic25pIjoicmF5LnJtZGhucmV6YS50ayJ9

 ---> 二维码 vmess(VMess+WS+TLS)
    https://api.qrserver.com/v1/create-qr-code/?size=400x400&data=vmess://eyJwb3J0Ijo0NDMsInBzIjoicmF5LnJtZGhucmV6YS50a192bWVzc193cyIsInRscyI6InRscyIsImlkIjoiNDFiMTEzMTQtNjFjNC05NWE1LTc0MTItZjE4Y2U2NTE2MmQyIiwiYWlkIjowLCJ2IjoyLCJob3N0IjoicmF5LnJtZGhucmV6YS50ayIsInR5cGUiOiJub25lIiwicGF0aCI6Ii92MnJheXZ3cyIsIm5ldCI6IndzIiwiYWRkIjoid3d3LmNsb3VkZmxhcmUuY29tIiwiYWxsb3dJbnNlY3VyZSI6MCwibWV0aG9kIjoibm9uZSIsInBlZXIiOiJyYXkucm1kaG5yZXphLnRrIiwic25pIjoicmF5LnJtZGhucmV6YS50ayJ9


=============================== VLESS gRPC TLS CDN ===============================


 --->gRPC处于测试阶段，可能对你使用的客户端不兼容，如不能使用请忽略

 ---> 帐号:ray.rmdhnreza.tk_VLESS_gRPC

 ---> 通用格式(VLESS+gRPC+TLS)
    vless://41b11314-61c4-95a5-7412-f18ce65162d2@www.cloudflare.com:443?encryption=none&security=tls&type=grpc&host=ray.rmdhnreza.tk&path=v2raygrpc&serviceName=v2raygrpc&alpn=h2&sni=ray.rmdhnreza.tk#ray.rmdhnreza.tk_VLESS_gRPC

 ---> 格式化明文(VLESS+gRPC+TLS)
    协议类型:VLESS，地址:www.cloudflare.com，伪装域名/SNI:ray.rmdhnreza.tk，端口:443，用户ID:41b11314-61c4-95a5-7412-f18ce65162d2，安全:tls，传输方式:gRPC，alpn:h2，serviceName:v2raygrpc，账户名:ray.rmdhnreza.tk_VLESS_gRPC

 ---> 二维码 VLESS(VLESS+gRPC+TLS)
    https://api.qrserver.com/v1/create-qr-code/?size=400x400&data=vless%3A%2F%2F41b11314-61c4-95a5-7412-f18ce65162d2%40www.cloudflare.com%3A443%3Fencryption%3Dnone%26security%3Dtls%26type%3Dgrpc%26host%3Dray.rmdhnreza.tk%26serviceName%3Dv2raygrpc%26path%3Dv2raygrpc%26sni%3Dray.rmdhnreza.tk%26alpn%3Dh2%23ray.rmdhnreza.tk_VLESS_gRPC

==================================  Trojan TLS  ==================================


 ---> 帐号:ray.rmdhnreza.tk_trojan_tcp
 ---> Trojan(TLS)
    trojan://41b11314-61c4-95a5-7412-f18ce65162d2@ray.rmdhnreza.tk:443?peer=ray.rmdhnreza.tk&sni=ray.rmdhnreza.tk&alpn=http/1.1#ray.rmdhnreza.tk_Trojan

 ---> 二维码 Trojan(TLS)
    https://api.qrserver.com/v1/create-qr-code/?size=400x400&data=trojan%3a%2f%2f41b11314-61c4-95a5-7412-f18ce65162d2%40ray.rmdhnreza.tk%3a443%3fpeer%3dray.rmdhnreza.tk%26sni%3dray.rmdhnreza.tk%26alpn%3Dhttp/1.1%23ray.rmdhnreza.tk_trojan_tcp


================================  Trojan gRPC TLS  ================================


 --->gRPC处于测试阶段，可能对你使用的客户端不兼容，如不能使用请忽略

 ---> 帐号:ray.rmdhnreza.tk_trojan_gRPC

 ---> Trojan gRPC(TLS)
    trojan://41b11314-61c4-95a5-7412-f18ce65162d2@www.cloudflare.com:443?encryption=none&peer=ray.rmdhnreza.tk&security=tls&type=grpc&sni=ray.rmdhnreza.tk&alpn=h2&path=v2raytrojangrpc&serviceName=v2raytrojangrpc#ray.rmdhnreza.tk_trojan_gRPC

 ---> 二维码 Trojan gRPC(TLS)
    https://api.qrserver.com/v1/create-qr-code/?size=400x400&data=trojan%3a%2f%2f41b11314-61c4-95a5-7412-f18ce65162d2%40www.cloudflare.com%3a443%3Fencryption%3Dnone%26security%3Dtls%26peer%3dray.rmdhnreza.tk%26type%3Dgrpc%26sni%3dray.rmdhnreza.tk%26path%3Dv2raytrojangrpc%26alpn%3Dh2%26serviceName%3Dv2raytrojangrpc%23ray.rmdhnreza.tk_trojan_gRPC
```

{{< /spoiler >}}

![Install V2Ray](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEghADPvgfq9usmLiJfyt1O5gZzQPMU5w1grBZcYgQFxHBHd16BPygLhIGCUmpNhYSlfhIWFBbmuSJjl90gJefqL7XPtvdiythf6FAQQlA0IqZndy0rHSiyjCkcOCoWe5-BOkxTGv1VIb0pgcX3rjuqKN9SNGnp5UNMjc4mN61jNL2HQCxUh7sLwgpvKmPA1/s0-rw/rmdhnreza.my.id.v2ray.websocket.tls.cdn.24.jpg)

14. Kita pindah ke Cloudflare lagi, sekarang ubah Langkah 6 di Menambahkan Domain ke Cloudflare dari **DNS Only** menjadi **Proxied** dan **Save**.

![Minimum TLS Version](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhTqxcty1rQM4M6mWaTjsi5Kw8TxDzxfjeX30kFiQMrAThSB2eg4HuMQivcesMX5H_JTMCZ5cjnC_CfQFVoHlw5a8rqdHXoCdkI3IROf7vMc4BHW7ar1EshI2K0JqnTumJ6w9BmDiDfVWHGFiWjRDerzNzKkrSBxdkuLJVpB2dAwrlJ72HIrat4X7x_D-6h/s0-rw/rmdhnreza.my.id.v2ray.websocket.tls.cdn.25.jpg)

15. Jika berhasil, ketika kita buka `ray.rmdhnreza.tk` maka yang muncul adalah ***fake website***

![Minimum TLS Version](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhOq6QN-nR2rFeHLZsgtyFbkvHFOyG_pW2jNl_quBNcDQgzbvJzzjD4LlwKVEVHlYHHCiDQ3D4btBebxN94G3gtk0BYQdeyEod6NBcJwXUq35WDTbJmMB-PA6S_y-oeTTXybfOwo3I0DnYRxiQYAz9GjOWVlg-K0J4SSFBTS9d3VIhy1uYsecI8jWSB2diS/s0-rw/rmdhnreza.my.id.v2ray.websocket.tls.cdn.26.jpg)

## Test V2Ray
Disini saya test akun **V2Ray** nya di Android menggunakan aplikasi **v2rayNG** memakai config `VMess WS TLS CDN`

1. Kalian cukup buka URL qrcode nya agar mudah [VMess WS TLS CDN](https://api.qrserver.com/v1/create-qr-code/?size=400x400&data=vmess://eyJwb3J0Ijo0NDMsInBzIjoicmF5LnJtZGhucmV6YS50a192bWVzc193cyIsInRscyI6InRscyIsImlkIjoiNDFiMTEzMTQtNjFjNC05NWE1LTc0MTItZjE4Y2U2NTE2MmQyIiwiYWlkIjowLCJ2IjoyLCJob3N0IjoicmF5LnJtZGhucmV6YS50ayIsInR5cGUiOiJub25lIiwicGF0aCI6Ii92MnJheXZ3cyIsIm5ldCI6IndzIiwiYWRkIjoid3d3LmNsb3VkZmxhcmUuY29tIiwiYWxsb3dJbnNlY3VyZSI6MCwibWV0aG9kIjoibm9uZSIsInBlZXIiOiJyYXkucm1kaG5yZXphLnRrIiwic25pIjoicmF5LnJtZGhucmV6YS50ayJ9)
2. Scan qrcode nya menggunakan aplikasi v2rayNG
3. Edit config nya
4. Pada bagian host ganti `www.cloudflare.com` menjadi `ray.rmdhnreza.tk` (Domain kalian) lalu Save.
5. Sekarang test config nya.

1             |  2
:-------------------------:|:-------------------------:
![v2rayNG](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhkw-nLN9ptzt1_DiygZjMCq_lrh5V9D0uGdOMBm5JQF8yFpDsE2bXVbGBFpQvyKMp89ysWu3cJ6hiebeXpjhT-pvFP1SZuYjkHKQm0JgMhoRjh9254RvFqGaHw-1_0TJ3g3J3-U1eV7FQG9MtaFYSSR_JpvD2byyNU5qNMbBoaoE3n7_KPvIKzz_B7hGLO/s0-rw/rmdhnreza.my.id.v2ray.websocket.tls.cdn.27.jpg) | ![v2rayNG](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhoxIGGsBfoHyewEJFHIsXhi4sCdwKp5kECnTY9BdOGQklSldV_fwqwkuUCwVzEFD-XVRmgv5xCrlPiuFMO2ue2aQb01La3BAN-VWoJ17GkDZaY_8m9qbW3fAQtfpiZ2evHwvX4ko1pf5eeR06yw6LURsrCpWlS0JsXz1GNynUkuAjeoUcTmxs4haTUqIMr/s0-rw/rmdhnreza.my.id.v2ray.websocket.tls.cdn.28.jpg)

1             |  2
:-------------------------:|:-------------------------:
![v2rayNG](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhGi1g9RTHgUvro7zDlLWh7EVYcKAmmrOTFb3ItNftqVwFCGBrnXmxm_Gg000u4JzKQs66zsQhyuFGMRMFn2vzO9oeqHSWjYXTbhATzU_HcI5Y_iR5zRw5IeDrwWWXcg10_CFfbD6sKe7Iz3-ojG9Oqi8J6o6yZ4NfVgCrYQ0fhVGrVK6_gadczb1mF6JK6/s0-rw/rmdhnreza.my.id.v2ray.websocket.tls.cdn.29.jpg) | ![v2rayNG](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiH0juU05vaWTleslpc6tztQuC9ktZEkOoq88QEq9qs-TFUtxX3uYeP4U9gflFMUIv1wjdhwZvo5YLx8erTeXFBg4OzvWI7m40RZQYp6GWQf5ShkQgQ2UicDtKHoLt7TFhffe_DOEFNEBpe6DhorWtuS5NGGCOERNvlbPGltjwdRy23YQwUvvuVfB9GTchz/s0-rw/rmdhnreza.my.id.v2ray.websocket.tls.cdn.30.jpg)

1             |  2
:-------------------------:|:-------------------------:
![v2rayNG](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhPdXR1Yf8odlLoZ9Zyz2tl8h-KkG2ndwKfT4NDjTwhXCn8aK0NHtg9strQgqPCyAxNScHUhiaFiqsxHfWP15QV-lj5vXPSporq9jG0YgVRmURcIaIr64fZf7Vb_PViZNceqyhfPaE8OIfxu5Cajzv0Tsph2ntgomn3ichxBAmJ7pe0jFtDsV0VA8SiMpJb/s0-rw/rmdhnreza.my.id.v2ray.websocket.tls.cdn.31.jpg) | ![v2rayNG](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEi4tIRr2_B6-6Z_Fo7zPiu2VzNoNQQ9Pvo4glFrHU6y0r9hyphenhyphenZ3OfrZbnMHk4SAlXUmMT7r_ktdREoUTipbQmyDAqSN9mT2BMkaJPGNFtRHNDy_VKBCZJmXXWSSTR219EL1BSgKtnQgHOvDbHIAVIUCNLiaz-SZ6sSwburvW54U1Vv3aedfaqBzKlRu5-o1I/s0-rw/rmdhnreza.my.id.v2ray.websocket.tls.cdn.32.jpg)

## Melihat Akun
Untuk melihat akun kita bisa download lagi script nya

```fish
wget "https://raw.githubusercontent.com/mack-a/v2ray-agent/master/install.sh"
bash install sh
```

Pilih nomor 4 dan pilih lagi nomor 1.
