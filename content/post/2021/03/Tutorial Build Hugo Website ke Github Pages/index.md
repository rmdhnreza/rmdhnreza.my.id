---
title: "Tutorial Build Hugo Website Ke Github Pages Menggunakan Github Actions"
date: 2021-03-04T16:33:19+07:00
description: "Tutorial Membuat Static Website Dengan Hugo di Hosting ke Github Pages"
categories: ["Hugo", "Github", "Tutorial"]
tags: ["Hugo", "Github", "Tutorial"]
description: 'Saya asumsikan kalian sudah mempunyai akun GitHub dan di Sistem Operasi kalian sudah terinstall Hugo.'
summary: 'Saya asumsikan kalian sudah mempunyai akun GitHub dan di Sistem Operasi kalian sudah terinstall Hugo.'
image: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjICTyl0qQlb4JHbR_VCnvHIPxC9P0Y_f0wuHQeTae_A7QoAzrjORIgC_k7tLutRQFVsGiT2Af-HQYbKL7VTcdW06tjxNCPoIAfEIOgG8bZpUlTY6UEUHL-MA4PUYfMbeTkxQNIHO0jK6UP-eMPa4ZB2quoBGyEmci4DkOGc6Pb04Evbzdnp3gSdKIJEcdT/s80-rw/github-logo.png
ThumbSchema: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjICTyl0qQlb4JHbR_VCnvHIPxC9P0Y_f0wuHQeTae_A7QoAzrjORIgC_k7tLutRQFVsGiT2Af-HQYbKL7VTcdW06tjxNCPoIAfEIOgG8bZpUlTY6UEUHL-MA4PUYfMbeTkxQNIHO0jK6UP-eMPa4ZB2quoBGyEmci4DkOGc6Pb04Evbzdnp3gSdKIJEcdT/s0-rw/github-logo.png
---

{{% adsense %}}

Saya asumsikan kalian sudah mempunyai akun [Github](https://github.com) dan di Sistem Operasi kalian sudah terinstall [Hugo](https://gohugo.io). Langsung saja ke Tutorialnya

1. Buat public repository dengan **username** github kalian ditambhakan **.github.io** jadinya seperti ini **rmdhnreza.github.io** dan ceklis *Add a README file*

![Membuat Repository Github](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEggPpu1c-nevPkWidGfMJH1-mjs1MFO2F8bN5b5ZwnCV8NEU1jnTxudlJv9jMjm7IIoPlnj65Ygxm1FLryWKez5xvB14KU7XuJ039ZU03icLgpPsbLRUfuwjsn9ehA0mY9ZK6uGDOvNdAx2-Oc6o90GlqnhNbUVBsXjCoT4HRwk5OIeohYj_2zAikLuazqe/s0-rw/1.jpeg)

2. Clone repository yang sudah kalian buat dengan perintah
```
git clone https://github.com/rmdhnreza/rmdhnreza.github.io
```
![Clone Repository](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEih0D3dH4LM6WDBXJbViOPwHzUFMz82xSamrY5ub9scUqlRF-S2KTSx_5_-ABgOLEH02b7JvzOFJtvoHXSHgqamVS2SkapvO6f6Y5AklDNc89vEmVgZMT3vjezdntF1EQTfXhspMbgaPQ8OUn74A1OcMQsMZPGeJnL92_J77dPvDe3nbRMXFxgUsOeIBLXG/s0-rw/2.jpeg)

{{% adsense %}}

3. Buat hugo website dengan perintah
```
hugo new site --force rmdhnreza.github.io
```

![Membuat Hugo Website](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEh-A0b6g70bhNYxpS9Kv7RxyShJ55MHiFJF_7YXjGtrKqOgjELCKSAz_kB5SHCLZjBFSzdxbv6j-gprTkNBbjUkoWtLsD4qxMDGNKXK32thySxCGbtiwq377DHN7zyg1bo0Hm820EmeTqD4OXCGa64Mi5IfA5WTkPGHTm783M2siEjba_v36IVdiWNxdoTY/s0-rw/5.jpeg)

**Note:** argumen --force disini untuk memberi tahu hugo jika folder nya tidak kosong

4. Masuk ke folder **root direktori** hugo kalian (rmdhnreza.gitlab.io) dan tambahkan tema yang akan kalian gunakan, disini saya menggunakan tema **Notepadium**, untuk memasang tema yang kalian inginkan kalian lihat dokumentasi tema nya.
```
git submodule add https://github.com/zwbetz-gh/vanilla-bootstrap-hugo-theme.git themes/vanilla-bootstrap-hugo-theme
```

![Menginstall Tema Vanilla](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiMyelX-RdKlfjiLW1VbMBlIYOV7J_ZDNvS01vfgDvHkoyW2F6I2OU3sHqOjTmjmLapVnMPkNe9eb9QT5GQSR3fzpnDvKMxkrfIQVoqLDyVmO7Uv3S1u6nudbq1DRq5suDGqcEoKQq8gWcq8dJ7PTs8-7li55-KyHJ8BiQAbLeYPbrc_8cWf7JELBIXc70V/s0-rw/7.jpeg)

5. Copy isi folder dari exampleSite ke **root direktori** hugo website kalian, jangan lupa jika di **exampleSite** terdapat **config.yaml** maka kalian harus **hapus config.toml** di **root direktori** hugo website kalian, begitupun sebaliknya. Karena jika ada 2 config, kemungkinan besar akan error.

![Hapus salah satu config](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEi20JYt0SM0PH-rhPds-QQLIuOuRCqv-MPrjpdsISRAk5Z2NTPnodNOtySrsVZS5QvK8pk7zE4ZNMxxX972ye14fwWo60Nbm7kHPMZQSTyYZqRmO1dGP2ZzYd6aMtiTx3RvvZAhxgbD3dQ4i9XUyiWjGcF-XFOjS0qwPaTc6Dm8yt9szWwQFKTBrTV2CMUc/s0-rw/8.jpeg)

6. Ganti **baseURL** di **config.yml** dengan **URL Website** kalian (https://rmdhnreza.github.io)

![Ganti baseURL di config hugo](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjT-Orqb-jY14wAXX7ZjfdEL2cIFdviVaMZMoCwpwntaPvmkSorGlAIXdnCJXil8QdTDgDH7jjAiwF9RuFtOOoDFGnoV9-viySq4LBHb3PvG65iwEb4tc0zvvQ_kkA8nMayIT9L-kGFBQHVgkh7c82rS_o9wdtFvm8UJYyL302tNS1DGQfyiBeOPDWo6KjV/s0-rw/9.jpeg)

{{% adsense %}}

7. Test website kalian dengan perintah `hugo server` Jika tidak ada error maka kita bisa langsung ke langkah selanjutnya

![Hugo Server tidak ada error](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEggYXC0EqU3t2dC0YgHjRSdqzO3EVAME9XT0jlYjaxvrvuKtY-L71O0lm_2sP76q_kXO2bKbv8_uHlzFZ_laqVfcbUh6DLkmyMa1ANrH8k8YTeGyeNB-jGaudivr8AnNgyImiV5cbwIcm4MkkJn016_uZ6oS4ZOYL85SyX5SlaO3RPLmbXywFW27uiVZrEw/s0-rw/10.jpeg)

8. Buat folder **.github/workflows** di **root direktori** hugo dan buat file **gh-pages.yml** di folder nya, jadi struktur foldernya seperti ini
```
.github
└── workflows
    └── gh-pages.yml
```
![Github Actions](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjUhJNs1J8qh-1zuLcCEyH86xhuyRx5b6UMbl5fpl6ElDDTh2jvdptbvqPj3UHtb8rD_ePaNEorF1PtEm6wPcxCxsjAlinhSloGUawRS_fhtOlTwblJ5xivDNjgT-9GFlVD7XQFzNrTIB3vSO-emYtTrENGP7WUf6x8k9pOabICFaJjotbvrdB_-Dxxn-p-/s0-rw/12.jpeg)

9. Isikan code berikut di gh-pages.yml
```
name: github pages

on:
  push:
    branches:
      - main
  workflow_dispatch:
    inputs:
      git-ref:
        description: Git Ref (Optional)
        required: false

jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
        with:
          submodules: recursive  # Fetch the Docsy theme
          fetch-depth: 0         # Fetch all history for .GitInfo and .Lastmod

      - name: Setup Hugo
        uses: peaceiris/actions-hugo@v2
        with:
          hugo-version: '0.81.0'
          extended: true

      - run: hugo --minify

      - name: Deploy
        uses: peaceiris/actions-gh-pages@v3
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
```
9. Jika sudah maka bisa langsung kita push ke github dengan perintah
```
git add .
git commit -m "Hugo Github Pages"
git push origin main
```
10. Sekarang di Github kalian, masuk ke bagian **Settings** lalu scroll kebawah sampai bagian **Github Pages**, disana kalian ganti **Source Branch** nya dari **main** ke **gh-pages**, setelah itu kalian **Save**

![Ganti source branch dari main ke gh-pages](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjcyG26RLWiu38_49YqWbrDNFEDiVoiAyHiuBu1Y34UwL8gkUCzMauREOi5-dvRCcuwZ7zuYv_E2_bXoHdDblCbd-HN4Wuh2CbvqDfxFFvQoF8MuL6ZRVM8xt29KX-dAWebqiRnKRMnEiHmttM-0Wz2CmBdiU9sXhADiQuF49t6m9yBkwo0wKyEITPJLM05/s0-rw/16.jpeg)

11. Kalian coba URL https://username.github.io/ apakah website nya sudah live atau belum, jika belum, kalian masuk ke bagian **Actions** lalu klik **github pages** lalu klik **run workflow** kalian klik **run workflow** lagi

![Wwbsite sudah Live dan bisa diakses](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgiClaOOuluVd-wZHAoAfCl5uGG7j8ddKqElGGTlRX7m_O-BJPAF5HsX5NTjqPoclJoeXABDq0BEjFx2Ogu0Zc0xnBEBtR4H7SPXnF1O7Mo9HLvOjkbh4LmUYVen_ZVBtZlKbSbMwGk15In86JvYv125vx8KmS5WDW3b9c64nsHfw_vZN2rAew8oqg7OHvx/s0-rw/17.jpeg)

{{% adsense %}}
