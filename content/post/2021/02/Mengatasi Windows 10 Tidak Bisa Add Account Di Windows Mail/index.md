---
title: "Mengatasi Windows 10 Tidak Add Bisa Account Di Windows Mail"
date: 2021-01-31T00:42:03+07:00
categories: ["Tutorial", "Windows 10"]
tags: ["Tutorial", "Windows 10"]
description: 'Biasanya ini terjadi ketika kalian sudah menghapus `bloatware` di windows 10 kalian, Jadinya ada software core yang terhapus.'
summary: 'Biasanya ini terjadi ketika kalian sudah menghapus `bloatware` di windows 10 kalian, Jadinya ada software core yang terhapus.'
image: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhUxPqPM3kQtbb5tb_uNtuNE6A1Zo0MqYsGQuqRZ-8nvISnGigbdMuUqqJiTnCdQUJ71TELdWiw8kXTUm3AZzDhjHSI0-MjgXv2_taOraoM-hSoscrVQRgWqTy38DFOzxIq0qrakQOr5e1bJhIwWxMnYVNYBjyEViGens9BisHYNoG1n9V13ky49I_x3yx9/s80-rw/mail-logo.jpeg
ThumbSchema: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhUxPqPM3kQtbb5tb_uNtuNE6A1Zo0MqYsGQuqRZ-8nvISnGigbdMuUqqJiTnCdQUJ71TELdWiw8kXTUm3AZzDhjHSI0-MjgXv2_taOraoM-hSoscrVQRgWqTy38DFOzxIq0qrakQOr5e1bJhIwWxMnYVNYBjyEViGens9BisHYNoG1n9V13ky49I_x3yx9/s0-rw/mail-logo.jpeg
---

{{% adsense %}}

Biasanya ini terjadi ketika kalian sudah menghapus `bloatware` di windows 10 kalian, Jadinya ada software core yang terhapus.

Untuk mengatasi tidak bisa menambahkan akun di aplikasi Mail Windows 10 caranya cukup mudah

1. Kalian buka `Windows Powershell (Admin)`

![Mengatasi Windows 10 Tidak Bisa Add Account di Windows Mail](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgeV9MsYu9X6l5lRKx6lS-3Sg6xHnd58KL1L370TfXLiSgDn6fj3D1-cU3ZFHPO0MKobIeZ73hzNUF39AIGMXgc6nwEKpv28-QMLU9k2RdCuREHmtLVf79ugleo-XIyPtmXy5hQPPLET9e5yCiZs7Lgnk2unxojha_K55dcfL3hgCDS9DV1YHLKUYKuoGx6/s0-rw/1.jpg)

2. Masukan perintah berikut
```powershell
dism /online /add-capability /capabilityname:OneCoreUAP.OneSync~~~~0.0.1.0
```

![Mengatasi Windows 10 Tidak Bisa Add Account di Windows Mail](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhEi9lTC5rV8pgqIioyJ8x7RxqUUrbrt_vMpPm1QNtMEp2Tx3f2gjogAnI6VWf5baMWurN5io_00HK-3SEytZB45BoPcvnO59w-gdAg3N6WbueI8FwBLPstbrKR3sjSfAHxGo5F8nzdMxLJOXTd37z8MIbbpAIv7bYS6pjnK5YmXBzPySalCV3GYCu4CrP8/s0-rw/2.jpg)

{{% adsense %}}

3. Tunggu sampai selesai (_This operation completed successfully_), biasanya tidak sampai 5 menit

![Mengatasi Windows 10 Tidak Bisa Add Account di Windows Mail](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEg4h7_eS73j3spNSJoPyhV_7e97WXff-PXr1Femtnw-JtONzou2g3YDUfk_Mqn6EQx0heEWXLP90RXWavfAcprKKNaKapfaeOnWxNd_zxo0tGkgt_5rdU0Yb53boZVJX5ovl4jw3ZQAbndsHYiS3hOMRpNl2PPp18k0T8hyaD6xK6KG-Nvub5Ow97ws4FMV/s0-rw/3.jpg)

4. Setelah selesai kalian coba add akun di Windows Mail tanpa perlu restart windows kalian

{{% adsense %}}
