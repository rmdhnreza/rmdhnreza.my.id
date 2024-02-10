---
title: "Cara Hosting atau Deploy Hugo di Gitlab"
date: 2021-03-20T00:33:19+07:00
description: "Cara Hosting atau Deploy Hugo di Gitlab"
categories: ["Github", "Tutorial"]
tags: ["Github", "Tutorial"]
description: 'Pada kesempatan kali ini saya akan share tutorial hosting atau deploy website Hugo kalian ke Gitlab.'
summary: 'Pada kesempatan kali ini saya akan share tutorial hosting atau deploy website Hugo kalian ke Gitlab.'
image: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEisMIKWE7fAZ5QUTcmC1MDT3fMLKEzrkp_U0IIs28xJXpMH3AZMegRzVvvSwVb-sK5pqfuqSGXnS2m_vw167ozXqyuCNslYOFmRQsv694U3tkT1RfhqDpOoBrxea0zDsCuzCN3MlPehcztTfkEu_SiTl5B7R06waDgfRZlRiE9jMz1FQjCKfwIkEQVcFx7s/s80-rw/gitlab-logo.png
ThumbSchema: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEisMIKWE7fAZ5QUTcmC1MDT3fMLKEzrkp_U0IIs28xJXpMH3AZMegRzVvvSwVb-sK5pqfuqSGXnS2m_vw167ozXqyuCNslYOFmRQsv694U3tkT1RfhqDpOoBrxea0zDsCuzCN3MlPehcztTfkEu_SiTl5B7R06waDgfRZlRiE9jMz1FQjCKfwIkEQVcFx7s/s0-rw/gitlab-logo.png
---

{{% adsense %}}

Pertama-tama jika kalian ingin hosting atau deploy blog hugo ke Firebase kalian bisa lihat di [Tutorial Membuat Static Website Dengan Hugo](/tutorial-membuat-static-website-dengan-hugo/) \
Jika kalian ingin hosting atau deploy ke Github kalian bisa lihat tutorial [Tutorial Build Hugo Website Ke Github Pages Menggunakan Github Actions](/tutorial-build-hugo-website-ke-github-pages-menggunakan-github-actions/)

Pada kesempatan kali ini saya akan share tutorial hosting atau deploy website Hugo kalian ke [Gitlab](https://gitlab.com/), Saya asumsikan kalian sudah mempunyai akun Gitlab dan sudah login.

1. Buat project baru dengan klik **Create a project** Pilih **Create blank project**
  - **Project name** kalian bisa isi bebas
  - **Project slug** kalian buat **username**.gitlab.io (Wajib jika tidak menggunakan ***3rd-party*** domain)
  - **Visibility Level** pilih **Public**
  - **Initialize repository with a README** kalian **ceklis**

![Create a project](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgi5OnkebA1J68PVHGbDBbhUrgyEuzq9id7LAt5WIaYQk81Z7xo5B68RynC1LCLZ-z7ho37wmzTDWAiG-7j1qsYnAs1Q8N5eQPTzMS8f-V03IppibDu1DL62hQxmlmm59la1t0QiI2qRyhUKEiRBv9s9mYAcAdhNt1CDBlsPb1mV9sRB5OOAJJKouOL2TFL/s0-rw/1.jpg) | ![Create blank project](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhfrUv12G9a37JkNMffZLHxfSvV_ZS5Wc4CTuxsrwPMKanbJ67U6lp1PI_RhvcR5_OdGEyPv4qe3KqhSxQmCKsoT9ETXFpogRl0yUnxxGUxPF-uRSs7yKqWRt6x-JVnB3JMHUqoBg25_FqC5nnUu-TUraEQP5yRhlLkueTL5VduKWZI-EJp3cFkXdJ0lBiV/s0-rw/2.jpg) | ![Project name](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhwE4SO9NCLfvv-00n0XrIRwuvvyq6up3HZ0YolokL9f8Una1INQWDdlekANHgbCi-YrvL2WHkdelP0KRJ1wDJyrOjrE-tpqj-rM1pG5VbEual4RrLtNQ2mKUB1yB5gABfsDRiOhM9O2eOkTumfGQSzKqTWx9mWnYTBexHL7Q2axD4MPdwMhABTgF7IPVb5/s0-rw/3.jpg)

2. Clone repository atau project kalian, Karena disini saya menggunakan HTTPS, jadi gitlab meminta username dan password, jika kalian sudah setting **sshKeys** di Gitlab saya sarankan clone menggunakan SSH
```bash
git clone https://gitlab.com/rmdhnreza/rmdhnreza.gitlab.io.git
```
3. Buat website hugo dengan perintah `hugo new site --force username.gitlab.io`. Note: Perintah `--force` disini untuk memberitahu hugo jika folder nya tidak kosong
```bash
hugo new site --force rmdhnreza.gitlab.io
```

![Clone repository](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEi7-eEAEE8BMUp-n7bpm7MElpbQRxi6DWlzf3pVbbRn0-i5Mg68Sk4MIn3VBdq7_ATxkAZdmqUw7hXUVJLz0pL9D3AMuwIp6AvnLcykXPZa9GaOBZghyphenhyphenPH5UAJMH0B3PugQsmd-9l86GKCYEI1p_rSX5p_Gs3jRv8OgKMThbmJoyHOs9toJkNHOnkPvuaSt/s0-rw/4.jpg)  ![Buat hugo website](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhHvBkzJraT6uFoqK81j9JQvTxgQ3QNx8pjpycCwpc4m0iemERY0NeNk_iQoNs1QusbdW8pQokQM1DqvydmCACM2jJiluKz5zLx36y0ndcQdviV3YrWSmVdOyDfz6iuv5LG_uCWLERMMG6zgFJvD_LG5-JSpU6wE6kbCA-i7zxViTytVkazwDUTH95pfnI3/s0-rw/5.jpg)

{{% adsense %}}

4. Masuk ke folder **root direktori** hugo kalian (rmdhnreza.gitlab.io) dan tambahkan tema yang akan kalian gunakan, disini saya menggunakan tema **Notepadium**, untuk setting-setting temanya kalian bisa lihat di dokumentasi tema nya.
```bash
git submodule add https://github.com/cntrump/hugo-notepadium.git themes/hugo-notepadium
```
5. Copy isi folder dari **tema/exampleSite** ke **root direktori** hugo website kalian, jangan lupa jika di **exampleSite** terdapat **config.yaml** maka kalian harus **hapus config.toml** di **root direktori** hugo website kalian, begitupun sebaliknya. Karena jika ada 2 config, kemungkinan besar akan error.

![Copy isi exampleSite](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgLIcn2wxrlN0yqjXjgxrCW8DijoTueXPBwRtJbUnVANX5E41atwscFiJp0SBbG565YwmuM7KfzqvLo0fzjFJEmYbVMxyjo4WLaChcOscwmQt1DFacddrPFj-DTxyc70S_UjrN6sMQy4ePbAdCTTB2FJDrw2240Skhnrf8Uxa-dSE2_eFe6CYvfqwSNqR4E/s0-rw/6.jpg) | ![Paste isi ExampleSite](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhEWfXgyT_ypv7lMZ1UxnH03Ty4vwBqRU7g3EIa2KFlZXmADhJchV87ZF1ekO5zW7jKkqyOvQfBVaoI7rwDUhJyvrwpkCvw3T0cuf-H2s_KQRJxoH2SDQa8WS45uYsB7Hj5bg2aWYmXjgxrzsoMp4D6_SN92pcox12A65vV2WjaO16okvIxabvEMInnIyLL/s0-rw/7.jpg)

6. Jika sudah gunakan perintah `hugo server` untuk menjalankannya secara local, saya asumsikan disini kalian tidak mendapati error.

![Jalankan website secara lokal](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEguQQvFliVLVeFx_Hnjl8rA0NT9RnFbI6riATTgWN40LsvTe9xDFa-SAur8pdxu588W9tZYQ24FoPgHb5Fv_Q7Xpjdb5airDLk8-i8UfiH5LVA5pP_QyV3mXSwJPZzL1rohRaK_gH2OfP9pu2QP5HEE2uhmQk8PbHjuVduuLQaYSeqVoKVKT6KiBSqRRziA/s0-rw/9.jpg)

7. Edit **config.toml**, ganti **baseURL** nya menjadi **https://username.gitlab.io**

![Edit baseURL](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjHWuygcA6peRWY99M3hCYtlJU8scQSR51O7hyphenhyphenzlF025zSwhoopEkXsvM64oiRQZmpEUmwX1x6NNoKXC5MZpUHMEiPLaKBkcm4S6p_t9iQ6Qfu7QroNJc3zXKXplbNWzcjVzteUqJ5zFFn8d4VElkds2D1gbl_XY1DBs9ANZeAEZGdV5YMASb0PvFAjsNeT/s0-rw/8.jpg)

{{% adsense %}}

8. Buat file baru dengan nama **.gitlab-ci.yml**, isikan konten berikut lalu Save
```yml
# All available Hugo versions are listed here: https://gitlab.com/pages/hugo/container_registry
image: registry.gitlab.com/pages/hugo:latest

variables:
  GIT_SUBMODULE_STRATEGY: recursive

test:
  script:
  - hugo
  except:
  - master

pages:
  script:
  - hugo
  artifacts:
    paths:
    - public
  only:
  - master
```

![.github-ci.yml](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgkfp_K8BqOrTxvQ8P6nntB0CCoSoPeoKNTS8oZnb24U0YItE1gRXSPhv94GN16fk_B735AyBwn7bLU80DxZoRziikZR81SYtNAhqXDeiB-ws9mPDKdiQcYfxf-CnegPQmVEoTG0racdzlszwuQt4bxkf5jyEGwFKxxL5TKLU6qmYC-p9KdEOV2HHf8cMNU/s0-rw/10.jpg)

8. Sekarang kita push ke Gitlab
```bash
git config user.name "Nama Kalian" ->> Jika kalian sudah setting ini secara global, bisa lewati langkah ini
git config user.email "Email Kalian" ->> Jika kalian sudah setting ini secara global, bisa lewati langkah ini
git add .
git commit -m "Deploy Hugo ke Gitlab"
git push origin master
```

![Kita push ke Gitlab](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEh8-WHJk2E6qFGxetK_4UJQPe3cdErYjEDBkpMc-H7mbPsXriZj4ybpfX0HjVBzQEYgXvsQtR-q_vbGGnRvieaAEiF19eWsigBDB-GA6qD2C1MF-K1GhKESgtNjObOoFnpWd_9zgvQM7jDQgTK3cgOs9ItNQjjng_yzkEHphzWuLSybAErn_ptEP5zOWTTR/s0-rw/11.jpg)

9. Tunggu beberapa saat sampai **https://username.gitlab.io** bisa diakses, pada saat tutorial ini dibuat dibawah 2 menit website yang saya hosting di Gitlab langsung bisa diakses

![Project berhasil di Push](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhMSAfNbHnhkL5N2kHjwcnxiXFC9_HHQl1vrj8udmPEgjs7xQqniDfJExMM4LimGcGkO7vZ40848uuZHzT0VfAtDQxNT6lXesx166VZG5nYob7uycih86R7irSQtrNPYdhlB01hhdHdxgJDpDaIZ_OIi-90baj_2d-gTkxnTGfZBur_zraH7_UEntlSBbww/s0-rw/12.jpg) | ![Tampilan Settings Pages](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhhtxMVedQyEc7bvmF1yco_AKR8sHsqbfuVP-GKdY5bO189dGEDZnyPeI3CC-CAlN92AoTMlOfDOg6FU-O88WxwO2JFPx7-4VWwrlwaFeaKrGXR1hvmBkKspABcnSVpIEUvYtRZILuPMPRzo88a1rS9Z2mYlftgz0RhPOMIkpiJOBeC1mdbQSZ8Ter1gpSn/s0-rw/13.jpg) | ![Tampilan website rmdhnreza.gitlab.io](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjH7btMo0lWWk6WCPFDJvYGl4-q8ktXWrRis8S1lcqjdHrc7mUng7NfcL0RPUYJr6qrSfEcVbsoHhWoA6LUqGaHFIvJGyNqqZv9TAYmepV8t_6DYr1qYPiSNskj8A1-pjSxaq8DrK68KnYTJCgIiLaLO95-zJFcMtfSIZZltwlGSUFWpfIxTwsmbN9W9DoK/s0-rw/14.jpg)

{{% adsense %}}
