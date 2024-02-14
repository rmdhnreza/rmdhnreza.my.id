---
title: "Memperkecil Video dengan FFMPEG Menggunakan NVENC"
date: 2021-12-25T18:30:13+07:00
description: "Tutorial Memperkecil Video dengan FFMPEG Menggunakan NVENC"
categories: ["Windows", "Linux", "Tutorial"]
tags: ["Windows", "Linux", "Tutorial"]
keywords:
  [
    "Memperkecil Video dengan FFMPEG Menggunakan NVENC",
    "Cara Memperkecil Video dengan FFMPEG Menggunakan NVENC",
    "Compress Video FFMPEG Menggunakan NVENC",
    "Cara Compress Video FFMPEG Menggunakan NVENC",
    "How to Compress Video FFMPEG use NVENC",
    "Compress Video FFMPEG with NVENC",
    "Compress Video FFMPEG using NVENC",
  ]
description: 'Hardware accelerated encoding mulai menjadi tren di kalangan produsen hardware komputer di era 2010an. Intel misalnya, mulai melengkapi processor keluaran mereka dengan teknologi yang disebut Intel Quick Sync Video sejak generasi Sandy Bridge.'
summary: 'Hardware accelerated encoding mulai menjadi tren di kalangan produsen hardware komputer di era 2010an. Intel misalnya, mulai melengkapi processor keluaran mereka dengan teknologi yang disebut Intel Quick Sync Video sejak generasi Sandy Bridge.'
image: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgoxnlTORd-C99ayoO1digwfSc5TAkckwCfg92GdGH2SQthGHCqQy9ak1CdyTQHbR7ELbkz_BdkKi-q-YntBmxLOAAqOyFQBVwCVRmDheDPVzNXs9RP-Li8sW6F4hoCv8bETjak1rkJVdENnP4UBQTsEIzj0NJHxDibExzSwQosab-zaHRDqI31bXt4NnBE/s80-rw/ffmpeg-logo.png
ThumbSchema: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgoxnlTORd-C99ayoO1digwfSc5TAkckwCfg92GdGH2SQthGHCqQy9ak1CdyTQHbR7ELbkz_BdkKi-q-YntBmxLOAAqOyFQBVwCVRmDheDPVzNXs9RP-Li8sW6F4hoCv8bETjak1rkJVdENnP4UBQTsEIzj0NJHxDibExzSwQosab-zaHRDqI31bXt4NnBE/s0/ffmpeg-logo.png
---

## Apa itu NVENC

Hardware accelerated encoding mulai menjadi tren di kalangan produsen hardware komputer di era 2010an. Intel misalnya, mulai melengkapi processor keluaran mereka dengan teknologi yang disebut Intel Quick Sync Video sejak generasi Sandy Bridge. AMD juga menciptakan teknologi serupa dengan nama Video Coding Engine (VCE), mulai generasi Radeon HD 7900. Sementara NVIDIA memperkenalkan teknologi NVIDIA Encoder (NVENC) sejak GeForce seri 600 generasi Kepler. Sumber [gimbot.com](https://www.gimbot.com/mengenal-nvenc-teknologi-nvidia-untuk-youtuber-streamer/)

Yang akan dibahas disini adalah menggunakan ffmpeg untuk encode video dengan hardware accelerated yaitu NVENC, sebelum kita lanjut ke tutorial nya kita tidak bisa menggunakan NVENC dengan ffmpeg versi biasanya, tapi harus menggunakan ffmpeg yang support ffmpeg, untuk cek ffmpeg support codec NVENC kita bisa ketikan peritah `ffmpeg` di terminal dan lihat output nya, jika ada `--enable-nvenc` berarti ffmpeg kalian bisa menggunakan NVENC dalam encode videonya.

![](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiwwjMeZhZncSBlZxOy8GTB_6yKs56CAIuHf8RscfJp6VCwitm68MyFPdTp9f9_Inm-XcypmF_yBnstWn83jsGiZtRJoUfnty-IumS520g4mxTwf06FoenWL7FN4G9SM8sI-d1eoUdC20fXTUncyK4-WEaerWE0qr5B99eIKfXiUVHHGULfxWC1Ej533M3B/s0/rmdhnreza.my.id.ffmpeg.nvenc.3.jpeg)

{{% adsense %}}

Pastikan juga driver NVIDIA kalian sudah versi paling terbaru, minimal versi 450 atau yang lebih tinggi, untuk cek versi driver NVIDIA kalian bisa menggunakan perintah `nvidia-smi` di terminal dan lihat `Driver Version`-nya, jika yang muncul `Driver Version: 460.32.03` berarti kalian menggunakan driver versi 460.

## Mulai Encoding

Setelah kalian memenuhi persyaratan diatas, kita lansung ke tutorial encoding nya.

1. Kita lihat terlebih dahulu bitrate video yang akan kita compress, disini bitrate videonya yaitu `2.830` kb/s dengan resolusi 720p dan ukurannya 1.59 GiB, untuk memperkecil ukuran video nya kita ubah bitrate nya, disini saya ubah menjadi 1024 kb/s atau 1M, atau menjadi lebih kecil dari bitrate asalnya, perintah yang saya gunakan yaitu seperti ini.

![](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEg2yUu4uaYTyZI-fC0KCpP2aJU1vZRK183jV1IpvyAjF99Lj_TgEUoE8X9IKz7PyBbO9go2VxXHLDU87tpnpdN38WY_0-USRV25YNBsnTU5S3og7a5SFdQGvmzR2CMI4lzjk7ontfrTzdIv5DumM_mXhtMOr-O4UFbsIDlwhmwjES8nUV4xBenKdwstqN7n/s0/rmdhnreza.my.id.ffmpeg.nvenc.4.jpeg)

```bash
ffmpeg -c:v h264_cuvid -i demoVideo.mp4 \
-c:v h264_nvenc -preset slow -b:v 1M -minrate 1M -maxrate 1M -bufsize 1M -profile:v high \
-c:a aac -b:a 128k -cq:v 18 demoVideoOuyt-720p.mp4
```

{{% adsense %}}

`-c:v h264_cuvid` decoder yang digunakan\
`-i demoVideo.mp4` video yang akan kita kecilkan ukurannya\
`-c:v h264_nvenc` encoder yang digunakan\
`-preset slow` encoding menjadi lama tapi kualitas lebih baik dan ukurannya juga menjadi lebih kecil\
`-b:v 1M -minrate 1M -maxrate 1M -bufsize 1M` *strict* setting bitrate menjadi 1M atau 1024 kb/s\
`-profile:v high` Untuk kualitas dan ukuran file terbaik tetapi menggunakan resource GPU yang banyak dalam decode dan encode\
`-c:a aac -b:a 128k` mengubah codec audio menjadi aac dan bitrate audio menjadi 128 kb/s\
`-cq:v 18` fungsi -cq ini untuk mengatur kualias video `0` otomatis `18-23` rekomendasi `51` paling buruk\
`demoVideoOuyt-720p.mp4` nama file yang sudah di encoding

2. Tunggu sampai proses encoding selesai, biasanya aka memakan banyak waktu, tergantung durasi video nya juga.

![](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgQKyVYjOBTp2mksmSYQIeHaZY9QvJcSCtPkPscnbQNGqqcOFG9bbXCedyjBAmkd5AMiuXffZyOX_nG87hmZwnRQ9KUHeYTdjNkv_O8_nWmSz94ZiCDVGpWkX0ephm4AyQmQ5Lh8SQytuyglvj9ExW4l1QvTm4s98sZ2xsUvvi3XyS9V-gzptXx2zkCvgj_/s0/rmdhnreza.my.id.ffmpeg.nvenc.6.jpeg)

3. Jika terdapat error seperti ini bisa diabaikan saja, saya juga tidak tau penyebabnya apa, tapi video tidak corrupt dan juga tidak ada masalah dengan audionya.

![](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgUXzLNychxSpwcZVEFTTNxpsKVCoFf0s8IPvMpzEisqDBH70aizlKblCkSw74diUa4_cz9RbZLVs8vNsqy7Otafn34iXsetCQCS1hATaJHGRh2dpY1uxtJY7Rzo6cDG2M8sMGUum2JXxf0j2ReIb_v0KYzTJIHQPGtoIsx2uFVMYngCxeYIEb76MCwsUyo/s0/rmdhnreza.my.id.ffmpeg.nvenc.7.jpeg)

4. Ini perbedaan ukuran video asli dengan hasil encoding mengunakan NVENC

![](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhZ9SclvLwgZ4J3m0w2uQkNcFRgL0jiE5hWCgM_t3R9w1dATj5v1VjyOerUXk7ws9tdg1GVZ6BYEAKMXksJGmC9tqbkqTZLwg3NTMNZWQHrynLZX3Qs0AXjOSTE4pxmrxFv0x07bt_gNhcxvM3Q_pDQnxtuqERU21rGdhVOQGxSb-tcAUKG22sVO-OhiHt6/s0/rmdhnreza.my.id.ffmpeg.nvenc.5.jpeg) | ![](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgriaZs98Km-w15U9qYjf4hfGvwbMsnjSMAmvlIXaeUHKOjzkOYZ4yW8SAQwSYzQhB_kNecI41mm2S8BTorSWlElicuxWxVxctA1ob3GFMIk8TzT7w2GPkUlagF5rPFcR0eq447KV_lddzlnH6BiGQ9MnVbCvBhAfxrDNzSz9Z6yZQgriW2_GJPBqPB10Fi/s0/rmdhnreza.my.id.ffmpeg.nvenc.8.jpeg)

{{% adsense %}}
