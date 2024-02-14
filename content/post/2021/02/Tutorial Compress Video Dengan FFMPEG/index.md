---
title: "Tutorial Compress Video Dengan FFMPEG"
date: 2021-03-15T20:14:20+07:00
description: "Tutorial Compress Video Dengan FFMPEG di Linux dan Windows"
categories: ["Linux", Windows, "Tutorial"]
tags: ["Linux", Windows, "Tutorial"]
description: 'Pada kesempatan kali ini saya akan memberikan tutorial compress video menggunakan ffmpeg, ffmpeg ini biasanya program yang digunakan aplikasi untuk compress video, salah satunya handbrake.'
summary: 'Pada kesempatan kali ini saya akan memberikan tutorial compress video menggunakan ffmpeg, ffmpeg ini biasanya program yang digunakan aplikasi untuk compress video, salah satunya handbrake.'
image: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgoxnlTORd-C99ayoO1digwfSc5TAkckwCfg92GdGH2SQthGHCqQy9ak1CdyTQHbR7ELbkz_BdkKi-q-YntBmxLOAAqOyFQBVwCVRmDheDPVzNXs9RP-Li8sW6F4hoCv8bETjak1rkJVdENnP4UBQTsEIzj0NJHxDibExzSwQosab-zaHRDqI31bXt4NnBE/s80-rw/ffmpeg-logo.png
ThumbSchema: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgoxnlTORd-C99ayoO1digwfSc5TAkckwCfg92GdGH2SQthGHCqQy9ak1CdyTQHbR7ELbkz_BdkKi-q-YntBmxLOAAqOyFQBVwCVRmDheDPVzNXs9RP-Li8sW6F4hoCv8bETjak1rkJVdENnP4UBQTsEIzj0NJHxDibExzSwQosab-zaHRDqI31bXt4NnBE/s0/ffmpeg-logo.png
---

{{% adsense %}}

Pada kesempatan kali ini saya akan memberikan tutorial compress video menggunakan ffmpeg, ffmpeg ini biasanya program yang digunakan aplikasi untuk compress video, salah satunya handbrake.
Tutorial ini bisa dipakai di sistem operasi Linux dan Windows (disini saya menggunakan Linux, tetapi perintah nya sama saja mau Linux ataupun Windows)
1. Kalian install ffmpeg terlebih dahulu
   * Untuk Windows kalian bisa download di [gyan.dev](https://www.gyan.dev/ffmpeg/builds/)
   * untuk sistem operasi Linux saya sarankan menginstall ffmpeg dari snap, karena sudah support *Hardware Accelerated*, tetapi jika GPU kalian belum support NVENC kalian bisa menggunakan perintah
```bash
 sudo pacman -S ffmpeg (Arc based)
 sudo apt install ffmpeg (Debian based)
```
Jika kalian menggunakan snap bisa menggunakan perintah
```bash
 snap install ffmpeg
```
2. Jika ffmpeg nya sudah terinstall kalian bisa cek menggunakan powershell atau terminal dengan perintah ` ffmpeg` jika tidak muncul error berarti installasi selesai, jika muncul `command not found` berarti kalian belum setting **PATH** untuk ffmpeg nya,
   * Untuk setting **PATH** di Windows bisa kalian kunjungi [sulhi.id](https://sulhi.id/setting-path-environment-variable-di-windows-10/)
   * Untuk setting **PATH** di Linux kalian bisa kunjungi thread di [stackoverflow](https://stackoverflow.com/questions/14637979/how-to-permanently-set-path-on-linux-unix)
3. Sekarang kita mulai compress video nya dengan perintah
```bash
 ffmpeg -i input.mp4 -vcodec h264 -acodec aac output.mp4
```
4. Jika kalian ingin menggunakan *Hardware Accelerated*, kalian bisa gunakan perintah
```bash
 ffmpeg -hwaccel cuvid -c:v h264_cuvid -i input.mp4 -c:v h264_nvenc -cq 19 -c:a copy output.mp4
```

{{% adsense %}}

**input.mp4** ini adalah nama dan extensi video yang akan di compress sedangkan **output.mp4** adalah video yang sudah selesai di compress\
`-cq 19` **0** itu auto **19** rekomendasi **51** lossless, kalian bisa pilih 1-51.

5. Perbedaan kecepatan compress menggunakan CPU dan GPU (*Hardware Accelerated*)

![CPU](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhpJHs-qhXEBJ73rXXSQDesBqrreNm3by0ztyTrnsYSCIRFdCpCTkAjrVRKqiNIyqV9L6twgf6Yl9LL0-R1I65guDgPRN5R62I-g93tq2sX2av9QsXRlJjaIKJr_DbLa23Aln0d-tNctRYM-dP9bW-eXQcJBLo2qHE1XBsK0cc-rskq11uZOIsO480uIPKz/s0/1.jpeg) | ![GPU](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgaEm50SMOzPebMWh_vmXcW91T_Woid2zU2TuPRrKq229cnHolx3hyphenhyphenqPFa2jhnVmEV51gHRW1erXlFMCGxVOGPzBvY-NanlyHcTFpAwWRZHAoS_qvI4lZyCAG_mUTNMe52QKmqahPiqB42iUk9kZ_ijUGRnIx6egFpjN8hTgOAk_1-mcp9EyDdsbeiDPqQc/s0/2.jpeg)

6. Jika kalian ingin setting mengganti resolusi, bitrate audio & video nya kalian bisa menggunakan perintah

CPU
```bash
ffmpeg -hide_banner -i input.mp4 -vf scale="854:480" -vcodec h264 -preset slow -b:v 512k -minrate 512k -maxrate 512k -bufsize 512k -profile:v high -c:a aac -ar 44100 -b:a 64k output.mp4
```
GPU
```bash
ffmpeg -hide_banner -c:v h264_cuvid -resize 854x480 -i 1080p.mp4 -c:v h264_nvenc -preset slow -b:v 512k -minrate 512k -maxrate 512k -bufsize 512k -profile:v high -c:a aac -ar 44100 -b:a 64k -cq:v 19 -movflags +faststart 540p.mkv
```
Perintah diatas mengubah resolusi menjadi 480p, bitrate audio menjadi 64k dan bitrate video menjadi 512k

![File size](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEidXTIxHGrCI9RU_vMkJOf-LsIbjRN8GDAYYFGJDz83xp1fOdn_2k9l_kBlTfpeEN-fSspaXHcX8aGSItPibZrQW_cIFNfpgxLx13bJMpbGJRzNAjLPaTA_JlTBQOkq4fgT-Oi93T3rUxG8e5DIdoePi4X32oR1Xc1p5vS5bBAx-_Mw7nLh3pSKMyaqWIYV/s0/3.jpeg)

{{% adsense %}}
