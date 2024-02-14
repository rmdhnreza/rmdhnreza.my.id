---
title: "Cara Menginstall Package Manager Scoop Di Windows 10"
date: 2021-01-21T23:23:46+07:00
description: "Tutorial menginstall package manager scoop di Windows 10 dan 11"
categories: ["Tutorial", "Windows 10"]
tags: ["Tutorial", "Windows 10"]
description: 'Apa itu scoop? Scoop adalah command-line package manager untuk memudahkan kalian menginstall aplikasi. Scoop menginstal program ke home direktori (C:/Users/Username) secara default. Jadi, kalian tidak memerlukan izin admin untuk menginstal program, dan kalian tidak akan melihat pop-up UAC setiap kali kalian menginstall atau menghapus program.'
summary: 'Apa itu scoop? Scoop adalah command-line package manager untuk memudahkan kalian menginstall aplikasi.'
image: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgutOMuyXgIb_F63h8SY4FgScmkPOTAydQJ7CkkOB_GmxRRJ35a1ZFthJuBpjflSb8in2HjFF2ns03lLo_neOlAECBQ7bDsaIaigvyKObUHArfBstn0681j3F9cBsPsdo3b9LdT-bY9dO6p4J0lsS9bqLg6WXdRMIPYo9JvN64ySDFNM64dzay7r_2OnjLx/s80-rw/scoop.jpg
ThumbSchema: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgutOMuyXgIb_F63h8SY4FgScmkPOTAydQJ7CkkOB_GmxRRJ35a1ZFthJuBpjflSb8in2HjFF2ns03lLo_neOlAECBQ7bDsaIaigvyKObUHArfBstn0681j3F9cBsPsdo3b9LdT-bY9dO6p4J0lsS9bqLg6WXdRMIPYo9JvN64ySDFNM64dzay7r_2OnjLx/s0/scoop.jpg
---

{{% adsense %}}

Apa itu scoop ? Scoop adalah *command-line package manager* untuk memudahkan kalian menginstall aplikasi. Scoop menginstal program ke home direktori (C:/Users/Username) secara default. Jadi, kalian tidak memerlukan izin admin untuk menginstal program, dan kalian tidak akan melihat pop-up UAC setiap kali kalian menginstall atau menghapus program.

#### Menginstall Scoop
Cara menginstall scoop, pastikan di windows kalian
1. Powershell versi 5 atau lebih baru (di windows 10 sudah terinstall secara default)
2. .NET Framework 5 atau lebih baru (di windows 10 sudah terinstall secara default)

Jika sudah memenuhi syarat diatas, kalian bisa jalankan perintah ini terlebih dahulu untuk menginstall scoop

```powershell
Set-ExecutionPolicy RemoteSigned -scope CurrentUser
```

![Set-ExecutionPolicy RemoteSigned -scope CurrentUser](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEikPXDfvs1Py7-njhDwwnkzZp5ZtoRFYfeb12PgOw0fIsnT8RVHwnuoj-DuDtTBWtc6pvR-OiB8fSOPO4QWWGQTNTkud7T1CxJHXCeSKpFJ2exdCqMGGfwGk2VKNvS7CdP2dg7VPMPgMG2rur0n3zko1dLPGO1eMVEwkKqTuFs30FyCqBiDz_f8Yr7ExCmf/s0/2.jpg)

Setelah itu kalian ketik `Y` dan `Enter`, lalu copy & paste perintah dibawah ini untuk menginstall scoop

```powershell
Invoke-Expression (New-Object System.Net.WebClient).DownloadString('https://get.scoop.sh')
```

Atau yang lebih pendek

```powershell
iwr -useb get.scoop.sh | iex
```

{{% adsense %}}

![Install Scoop](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhevbYpy0qMfbKznSt5R3_Q9dQ51g4ReuNq4PNkJLD7X17Xys2HYwc6bdZaPjkH4CreaQ1XLNM3qvrW7NJi65Jf_XhHzQ-EPEV7CS9HXDyzEXaXVDB83GiVahwWFiusVybCJvAqtPsNX-7QvvIcUYwFl-GJOaxhmiG9Y3JnURrIonBY7fU9AdfnCSlJ5RY5/s0/3.jpg)
#### Menginstall Aplikasi
Sebelum menginstall aplikasi, kalian wajib menginstall `git` terlebih dahulu, dengan perintah
```powershell
scoop install git
```
Note: Jika kalian butuh `openSSH` kalian bisa install
```powershell
scoop install git-with-openssh
```

![Install Git OpenSSH](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEj6o3wDfg2NXhamtj_ClaxD2kbW2_WAmBkrG6mio9R5PmRdS1D99QsMUv3jDAyahjZSEuWxAtNCt-JxO3kFWpec97XN4tn4wEt1ekjnzlwG7DlUDGd3idOdiaz91gOJ43xOWzhCh_jGM4sEjwh_sgVNg-cYbTzZZLCpQzR8ySHG7M1Rps-gfiCmeW9iUs1w/s0/4.jpg)

![Install Git OpenSSH](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjEj6YATD1H0zkJ5VWXlH0IWgS4wW0eSjOJmAP49vmUp7iamZ8bvBRm8u93Z3ZQDToIqAfVg4cjmvX61Wv_NEetyOF9X8Dt7uEaOx7-GYjU_mM5INVB-LP2fTwi1Izu32_y175vMsU8gdd-5HIyXXeBjyAH_vHOtmQLP_6cNs73nxaWWJCPraxjVl6BuzC9/s0/5.jpg)

Setelah git nya terinstall kalian **add extras bucket**, agar banyak aplikasi yang bisa di kalian install via scoop, caranya

```powershell
scoop bucket add extras
```

{{% adsense %}}

![Add Bucket](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEixpWZQWvxdgXLLDW4_0W7igvjPBWiO8Qz6dCJ3P5u-5mQXV6Q8TcGH9wdCWUYLcSf2Z6Yzvm0A7bFy_XaNR0jiteaWSwZeQEuBShnWGMvqAg4JSB8Ig1aKxTyM0y9V_JDrA4LFhCyMiYX44PxTOQX3snQqgOTIwSi_L1wEarDCM96lWBWS7bHINiZpyaIy/s0/6.jpg)

Untuk menginstall aplikasi dengan scoop sangat mudah caranya
1. Kalian buka powershell kalian
2. Jalankan perintah

```powershell
scoop install nama-aplikasi
```
Contohnya, disini saya akan menginstall **FFMPEG** & **HUGO-EXTENDED**, kalian tinggal jalankan perintah
```powershell
scoop install ffmpeg
```
```powershell
scoop install hugo-extended
```
Atau bisa juga disatukan perintahnya
```powershell
scoop install ffmpeg hugo-extended
```
![Install Hugo Extended](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgJCPwJHm7SgTTsTKXGwCPxq2zeQ96yIflqDMwQ4qpAX3snmhZkwXxaXfR_qOpW1EbM9ygE-jfdpOidK5Gk60A981lIBl1sG2wGcxM7TRKO52-KikShhcF1GZHY5zz1oGyt2E4GZTeY0FkWMyvD8YvBM9SMf_GQ02Dsg3sMmnh4mg1qXiC-eTdMjRwz6EQ5/s0/7.jpg)
#### Update Aplikasi
Untuk update aplikasi perintahnya
```powershell
scoop update nama-aplikasi
```
Atau jika kalian ingin mengupdate semua aplikasi bisa dengan perintah
```powershell
scoop update *
```
Setelah kalian mengupdate aplikasi via scoop, pastikan kalian menjalankan perintah dibawah ini untuk menghapus aplikasi versi sebelumnya
```powershell
scoop cleanup *
```

Untuk lebih lengkapnya tentang scoop ini kalian bisa langsung kunjungi [documentation nya di github](https://github.com/lukesampson/(wiki))

{{% adsense %}}
