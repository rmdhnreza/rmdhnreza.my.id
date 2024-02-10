---
title: "Tutorial Convert Video YouTube Ke Audio FLAC Menggunakan yt-dlp"
date: 2021-01-09T22:09:10+07:00
categories: ["Linux", "Windows", "Tutorial"]
tags: ["Linux", "Windows", "Tutorial"]
description: 'Tutorial kali ini saya akan share cara convert video atau music dari youtube ke format FLAC menggunakan yt-dlp.'
summary: 'Tutorial kali ini saya akan share cara convert video atau music dari youtube ke format FLAC menggunakan yt-dlp.'
image: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEg3Enk7pEPNbHs3Nc_3AGoI0EvDyWh5wMJaRdp42bg0omn9ADFBtTVTKHb_-FfmiUp7pkDK33ip9ZZLLJ585ihKcKoOjkqdv5vT4FBdela_sNCmLBXFbPWxF3DD_9kS3U8qTNUWKu90X-m1jz_Lp3uN3b6Kq8_7q1N69lYQPZJgQ9JFIxCFkTO80iXcOeob/s80-rw/yt-dlp.png
ThumbSchema: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEg3Enk7pEPNbHs3Nc_3AGoI0EvDyWh5wMJaRdp42bg0omn9ADFBtTVTKHb_-FfmiUp7pkDK33ip9ZZLLJ585ihKcKoOjkqdv5vT4FBdela_sNCmLBXFbPWxF3DD_9kS3U8qTNUWKu90X-m1jz_Lp3uN3b6Kq8_7q1N69lYQPZJgQ9JFIxCFkTO80iXcOeob/s0-rw/yt-dlp.png
---

{{% adsense %}}

Tutorial kali ini saya akan share cara convert video atau music dari youtube ke format FLAC menggunakan **yt-dlp**.
Pastikan di sistem operasi kalian sudah terinstall ffmpeg, jika belum terinstall, silahkan install terlebih dahulu agar tidak error.

#### Tutorial Installasi di Sistem Operasi Linux
1. Download terlebih dahulu yt-dlp nya, untuk sistem operasi Linux kalian bisa menggunakan **curl**
```bash
 sudo curl -L https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp_linux -o /usr/local/bin/yt-dlp
 sudo chmod a+rx /usr/local/bin/yt-dlp
```
Atau menggunakan **wget**
```bash
 sudo wget https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp_linux -O /usr/local/bin/yt-dlp
 sudo chmod a+rx /usr/local/bin/yt-dlp
```
2. Jika di sistem operasi kalian sudah terinstall **python3** kalian bisa menggunakan perintah
```bash
 sudo pip3 install --upgrade yt-dlp
```

{{% adsense %}}

#### Tutorial Installasi di Sistem Operasi Windows
1. Download [yt-dlp.exe](https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp.exe) dan copy ke `C:\Windows`, Jika kalian mendapati error kalian install [Microsoft Visual C++ 2010 Redistributable Package (x86)](https://www.microsoft.com/en-US/download/details.aspx?id=5555) terlebih dahulu.
2. Jika di sistem operasi kalian sudah terinstall **python3** kalian bisa menggunakan perintah
```powershell
 pip3 install --upgrade yt-dlp
```
3. Jika di sistem operasi kalian sudah terinstall **scoop** kalian bisa menggunakan perintah
```powershell
scoop install yt-dlp
```

{{% adsense %}}

#### Convert Video ke Audio Format FLAC
1. Kalian cari Video atau Music yang akan kalian convert, disini saya akan convert music dari channel NCS `https://www.youtube.com/watch?v=AnF_VOliv0E`
2. Jika kalian sudah siap, kalian buka `CMD` / `Powershell` untuk Windows, dan `Terminal` untuk Linux
3. Masukan perintah berikut
```bash
 yt-dlp -x --audio-format flac  "https://www.youtube.com/watch?v=AnF_VOliv0E"
```
`-x` adalah kependekan dari `--extract-audio`
![yt-dlp](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjpG62ytzVlHN52dS8dwoPAI3tiTlFK6MlIlTd8ohvYsx0tBKVPC5udOl6rEClyhWrmYPxmBk2J31UJ739LdjHWSZhXWSwTezwP5h7ElxrEO_nSlrsFeXwSlnV-oyMEdCLfuq_f9LJYqnVRy0Ogu5eWuIgWwb_oQx7k-YQH_g92mC4RoB9upz1b84maXSDC/s1600/youtube-dl-1.jpeg)
![yt-dlp](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiQaxgDgO94WmGnK9XpiuMBq4iA_Sg9s_12Na_BWao80mrLOOoLhPAGGTxtcla48-bC90Yq8BWfRGKhHhFHveWYhHvEGKr4YYqhyIrbaVMonUbVzQo6UhhidHd3mlGZb7JE1ImesOY5yb_wdm2YECcWyAMERlKEq-T3Cdof8IFjdj0kejZssG_0k_4yvnWY/s1600/youtube-dl-2.jpeg)

{{% adsense %}}
