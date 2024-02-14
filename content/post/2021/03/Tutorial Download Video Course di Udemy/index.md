---
title: "Tutorial Download Video Course di Udemy"
date: 2021-03-14T15:36:16+07:00
description: "Tutorial Download Video Course di Udemy"
categories: ["Tutorial"]
tags: ["Tutorial"]
keywords: ["Udemy", "Download Course Udemy", "Cara Download Kursus di Udemy", "Download Video Udemy"]
description: 'Saya asumsikan kalian sudah mempunyai akun GitHub dan di Sistem Operasi kalian sudah terinstall Hugo.'
summary: 'Saya asumsikan kalian sudah mempunyai akun GitHub dan di Sistem Operasi kalian sudah terinstall Hugo.'
image: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhc52kK2qefl1_4BaHcxNWj2aFuJdDfzQDwLwUODVl2eQVzVAnag5n2VYig-UKEy7gi8MpIywSveXrJk3JqgA7X-CAHJjcJv576DMAkufu_IGK3pPosWI56XNTzKkDu6PPXRyiQquOArkXZh-1fB9mwOFMpf_wFzsh3JU6GjQmdmhPep_HR0-ihtTGSBQtH/s80-rw/udemy.png
ThumbSchema: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhc52kK2qefl1_4BaHcxNWj2aFuJdDfzQDwLwUODVl2eQVzVAnag5n2VYig-UKEy7gi8MpIywSveXrJk3JqgA7X-CAHJjcJv576DMAkufu_IGK3pPosWI56XNTzKkDu6PPXRyiQquOArkXZh-1fB9mwOFMpf_wFzsh3JU6GjQmdmhPep_HR0-ihtTGSBQtH/s0/udemy.png
---

{{% adsense %}}

Udemy adalah pasar global untuk belajar dan mengajar secara online sehingga siswa dapat menguasai keterampilan baru dan mencapai tujuan mereka dengan belajar dari perpustakaan ekstensif dengan lebih dari 55.000 kursus yang diajarkan oleh instruktur ahli. Setiap orang dapat menjadi instruktur atau pengajar di udemy dengan mendaftar pada akun udemy.com.

## Sebelumnya kalian harus membeli terlebih dahulu kursus yang akan di download

Jika kalian sedang kursus di udemy dan malas untuk streaming, ditutorial ini kita akan mendownload video dari udemy agar bisa ditonton secara offline menggunakan video player kesukaan kalian. Langsung saja ke tutorialnya

1. Pastikan **python 3** sudah terinstall di sistem operasi kalian, untuk cek apakah **python 3** sudah terinstall atau belum kalian bisa menggunakan perintah dibawah ini untuk cek versi **python 3 nya**
```python
python3 -V
```
Untuk sistem operasi linux seharusnya python3 sudah default terinstall sedangkan untuk sistem operasi Windows kalian bisa download pythond di [situs resminya](https://www.python.org/downloads/windows/), atau install menggunakan [scoop](/cara-menginstall-package-manager-scoop-di-windows-10/) dengan perintah
```powershell
scoop install python
```
2. Clone (jika di sistem operasi kalian sudah terinstall git) atau Download & Extract repository berikut ini [github.com/r0oth3x49/udemy-dl](https://github.com/r0oth3x49/udemy-dl)
```bash
git clone https://github.com/r0oth3x49/udemy-dl.git
```
3. Kalian masuk ke folder **udemy-dl** dan install *dependencies* yang dibutuhkan dengan perintah
```python
pip3 install --user -r requirements.txt
```
![Download atau Clone](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEglwcOVnu4_pRKiPv6D-WG3Jv-6dgDW4VdQZEbVzMPPqkoR1JNoH3g8dW1zS5zhHE1-HoP-KfNShyphenhyphenLz1o0H5J_SE8_03aUuy-W2LK_mH9LrxKXk121UzKbdSuYZGntjEF0K5AVMBZam31bz87CFbj-8KVnJl_Lf3S43gGxWgnKfdZ9KvJYzu4waiRqzv6MR/s0/udemy-dl-1.jpeg) | ![Install requirements](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjSWGDfH0EXVAIOIzUg3rxYfAvPD7YbaFTAxXsksroLLF-bV2ZKKGGMxEFSUzQj9udCPLJqMW_fxcODAc8aZziqo16zDYS9E3-_6B5hFi-QKK1pofS7yGQT1_6ZtDEdokdNXsbuSwH6NoNAOqrjruF3pE_L_4UzITme4MGE260FTWNLl7OT9MQGwUqDrM02/s0/udemy-dl-2.jpeg) | ![Install requirements](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjPk_HjThE50Rs4OrXpH4KtD3xkelKy5ao0KI-AGZcsJCA5N-MwL50-dyBHjiBJlPi2pwGHEeSsfk2wGJmRFVjOrWhG1Z6nRLCG1seLPjW6RCqxMaxohoqQVWzaw7RF32nl-OaQkEfFZ90X1W8BQiVqX1FwzTRB8pCIJzoqN37iPtB02BG9b4gHnkZjT1u_/s0/udemy-dl-3.jpeg)

4. Login ke [udemy.com](https://www.udemy.com/) dengan akun kalian untuk mendapatkan akses token

{{% adsense %}}

## Mendapatkan Akses Token di Google Chrome
{{< spoiler text=" Klik Untuk Membuka Spoiler" >}}

1. Klik icon gembok
2. Pilih Cookies
3. Klik tanda panah pada **www.udemy.com**
4. Klik tanda panah lagi pada **Cookies**
5. Cari **access_token** dan copy **Content** nya

![Access Token Google Chrome](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEigfCg0tN-P1cvotkcgYOlITgkoYFGpbTQCQsaN_1jpz2vlzkw_k60Tvfy2RVMscNhHAFvC6VNxeiPlRmUHwoESYRPArqGhUSgce9GfasNzpQQMqWwnu6klt9bN5c4BIz74MPPRZY5j6rfd68IGbvJKY-8oua4mkpYBQdw1RrWMaCxFpX7ybAhKhWUQpmg5/s0/udemy-dl-4.jpeg)
{{< /spoiler >}}

{{% adsense %}}

## Mendapatkan Akses Token di Mozilla Firefox
{{< spoiler text=" Klik Untuk Membuka Spoiler" >}}

1. Klik kanan dan pilih **Inspect Element**
2. Masuk ke tab **storage**
3. Pilih **Cookies**
4. Cari **access_token** dan copy **Value** nya

![Access Mozilla Firefox](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjWwGqXyuR1KeyL76U-q3lACamWuFsyrgNiB0sZEkrahZ-dHL7LiAb8qjS43dISdavrD0_S1j2stf2YEXz4B692lK_qXPujGeQ6GKZjJnvvjnFacSluBJdgwy_n7zaS9E3Evx4Ekk6jxzl53z93p-yZ0CMiyHBdSIAzTXlpRGYXe7vSEVDwRMnL7jd1FJRq/s0/udemy-dl-5.jpeg)
{{< /spoiler >}}

5. Setelah kalian mendapatkan akses token nya, kalian buat file dengan nama **cookies.txt** dan isi dengan akses token kalian menggunakan format berikut lalu save
```
access_token=AKSESTOKENKALIAN
```
![Cookies.txt](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEj1yguDegyTz8H42D4kfodngzQbaV45ah-SQTLCI6GLZkmIEFxmJNeJpzggq1EUM9K7d4ZcmtwCLTA7hpAHUMMde41TYh6QkLkS4ctc-AW7TEMh5hBc_Z5BArxZlzq8uRnRdhzsQnztIRCdSUT8wkmO-qPRYOsEv7F0Cwy7FYWay6gggsHABEzoWEIJFNfD/s0/udemy-dl-6.jpeg)

6. Sekarang kita akan download video nya, disini saya contohkan download kursus ini [https://www.udemy.com/course/diversity-at-workplace-t/learn/lecture/25380564](https://www.udemy.com/course/diversity-at-workplace-t/learn/lecture/25380564), maka perintahnya
```bash
python3 udemy-dl.py --cookies cookies.txt https://www.udemy.com/course/diversity-at-workplace-t/learn/lecture/25380564 --quality 720 --output /home/rmdhnreza/Udemy\ Video
```
**Note:**
   - **--cookies cookies.txt** untuk memberi tahu jika kita login menggunakan cookies
   - **--quality 720** Kualitas video yang akan kita download resolusi nya 720p
   - **--output /home/rmdhnreza/Udemy\ Video** yaitu file yang kita download akan disimpan di folder /home/rmdhnreza/Udemy\ Video, jika kalian tidak setting ini maka hasil download akan disimpan di folder udemy-dl
   - Untuk syntax lainnya kalian bisa lihat di [README.md](https://github.com/r0oth3x49/udemy-dl/blob/master/README.md)

![Proses Download](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiBab9ePQPdMoLxMVnJkbfsnCJL-XqqXSLw1p5gAmSc9_6q8TKD88X9ladiFp6uShExYAntzrrdIT9EycpEAddcLCyJpjuQddRBSMu6PnPJV_NxBUrhgC-VBMz2SosHaHVHpwOiozLTxOPsmjOLbzGdbmGLuiJRN_bsW7u6f0H_aimuBPnNab-hGPzCsY4c/s0/udemy-dl-7.jpeg)

7. Video berhasil di download

![Hasil Download](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEh1oODROYKLHr4BAxg1-7vWVsHNyy_CZWc24Va3SOfKadxC7fu5aEVESfNUBc3IhQ9qZpjO6oc2NO7ObMUvAvrM2GUXnJccvSWNP2UsqtqRfmEcqY5EHF8Ut_p02bdmTkXbxx-uPAx8iREZi587qXTySRmLtmXxWFOWDOff-nMHrBUGTzg4z4VJZihGGoyl/s0/udemy-dl-8.jpeg)

{{% adsense %}}
