---
title: 'Mempercepat Startup Windows PowerShell'
date: 2022-11-02T15:30:13+07:00
description: 'Tutorial Mempercepat Startup Windows PowerShell'
categories: ['Tutorial', 'Windows']
tags: ['Tutorial', 'Windows']
keywords:
  [
    'Mempercepat Startup Windows PowerShell',
    'Tutorial Mempercepat Startup Windows PowerShell',
    'Cara Mempercepat Startup Windows PowerShell',
    'Cara Mempercepat Startup Windows PowerShell Windows',
    'Cara Mempercepat Startup Windows PowerShell Windows 11',
  ]
description: 'Mempercepat Startup Windows PowerShell'
summary: 'Mempercepat Startup Windows PowerShell'
image: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgcrR2cY-xKSbSBhCWJ3GeoPVsJYKl7jy-nTBki4RE3tj7mKxXY428yVKoFcsSCkve4RIKl2RwzehPmcV759RJwmO5BAnz2309N-znOF_s3dfAR8engrbfZG35dhaBMhZY6oC3rZqSGuI26GmfZgTrRRuGiPEh96ZnK8QnQ8ixaam1CKj8NUXV71xvklXhQ/s80-rw/powershell-logo.png
ThumbSchema: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgcrR2cY-xKSbSBhCWJ3GeoPVsJYKl7jy-nTBki4RE3tj7mKxXY428yVKoFcsSCkve4RIKl2RwzehPmcV759RJwmO5BAnz2309N-znOF_s3dfAR8engrbfZG35dhaBMhZY6oC3rZqSGuI26GmfZgTrRRuGiPEh96ZnK8QnQ8ixaam1CKj8NUXV71xvklXhQ/s0-rw/powershell-logo.png
---

## PowerShell

{{% adsense %}}

Penyebab **PowerShell** lambat pada saat _start-up_ kemungkinan besar diakibatkan oleh aplikasi **.NET** entah itu ada update atau kalian baru saja menginstall ulang Windows, untuk mempercepat kinerja **PowerShell** kita harus compile code yang digunakan **PowerShell** menggunakan aplikasi **ngen.exe**.

Pada saat pertama kali menggunakan **PowerShell** mungkin kalian akan _notice_ jika pada saat _start-up_ terasa sangat lambat seperti ini

## Video sebelum fix

{{% iframe "AD6v5dzx5stqgPyYqH16Q8az_Da8ilAq_iqt28GSfWtsMF435-wjb0YSXTjOIPCTxDESaFzPeWIehhkECpKxbCvs_srikRVJwjTzBv5SMbTF2uqNYKuj_jgzgEEqpKhDtl7dnS4GY7-y" %}}

## Fix PowerShell slow startup

1. Buka **PowerShell** sebagai **Admin**, Untuk Windows 11 cukup buka aplikasi **Terminal** sebagai **Admin**

![Figure 1](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjJ9rp-3uvqkdffjvWd5N-vNVm0awLqawXuI4uV7G_ABRurilarpYpEFNIWzK_FQBE0ynB2XNDfpN3_ligUuOkkOXEbwVNxCIPPdrWqexxqUnwUzRovSrkD_NoPF3rqmifwhhdU_E2pX8EwTSKmhj1OsVlAimN-MapyY2owggV0LQcaDNkJaOErF48cF8er/s0-rw/rmdhnreza.my.id.mempercepat.startup.powershell.1.jpg)

2. Masuk ke Direktori
    + `"C:\Windows\Microsoft.NET\Framework\v4.0.30319\"` untuk 32-Bit
    + `"C:\Windows\Microsoft.NET\Framework64\v4.0.30319\"` untuk 64-Bit

![Figure 2](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiNiupcltqYtsZKah4oQtCToxfflZQLWnBXqxdfGbkOc5jz8Ah8dJCmpK5Xli3qK2hSdjL25hEmI15J0ZR_e81gI7K5viULp_8KNZAsZZccUz1NiishA6heZvFAWcYv5kjiV5DRmdEYN7Z4l9eyK4_Cs1WMVSXIiXVcfVtHiLoiRbjprM7FBZeIuEIcgejm/s0-rw/rmdhnreza.my.id.mempercepat.startup.powershell.2.jpg)

3. Copy & Paste perintah dibawah ini

```Powershell
$env:PATH = [Runtime.InteropServices.RuntimeEnvironment]::GetRuntimeDirectory()
[AppDomain]::CurrentDomain.GetAssemblies() | ForEach-Object {
    $path = $_.Location
    if ($path) {
        $name = Split-Path $path -Leaf
        Write-Host -ForegroundColor Yellow "`r`nRunning ngen.exe on '$name'"
        ./ngen.exe install $path /nologo
    }
}
```

{{% note %}} Jika menggunakan Windows Terminal, pasti akan muncul peringatan seperti ini, klik "Paste anyway" {{% /note %}}

1             |  2
:-------------------------:|:-------------------------:
![Figure 3](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEi6FpwP2SPY7xHy_QSiLAqVYnBRoDYWNUqZkaC18gJr-E7s1hqa33tgZoZ7cp9wLDqZC-MCfzqNXqWX7kvMRC0M_30Aa0Q_IRlbKGdZHol2DzDOm59q6yoKGZTjGEfJWsCq2ezUpr1GlvEtH2mLSRYADb7ReRQYhumY2iBFFDp5j7lGl3u01q-rRGTjDP2C/s0-rw/rmdhnreza.my.id.mempercepat.startup.powershell.3.jpg) | ![Figure 4](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjKeNmMtzxdy0J8l4nTxbv-s54zQ57a1tLvFq505MvA9bNWvJH0dy5AllrbQXVhicerhEyupcY3i4s9bMpuTN7LXrATjCgTL3qyRhIjkIV7V5WgQAYKSALKBrvmJMfkds7bb1qff4Xu6-207eoeI4cZ6zobJUMFXemGoqWQTQkp7jahTHNKOx8vazSRdczK/s0-rw/rmdhnreza.my.id.mempercepat.startup.powershell.4.jpg)

{{% adsense %}}

4. Tunggu sampai _compile_ code nya selesai

1             |  2
:-------------------------:|:-------------------------:
![Figure 5](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiGgd-17ghrlX8J6pAeyaoJmrfkX8EYtNXAAhPkk3s54aG0yiKO5VW42P-ULSu8pVgkWdNdmGqEZ6IqiT4lv138Yqabk50MJj2kpJhSQi489NKgwfAotTqkdRHLHb8CTVx3oOMiFkAzH-ty7YlyYH6eTCDdEBd9QkpjAxEluUzO9hgqG5V6l3ZxX55PThgT/s0-rw/rmdhnreza.my.id.mempercepat.startup.powershell.5.jpg) | ![Figure 6](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiao45puX1shCCr7HbQlIhb2iODwYEipqVcNppKBsQqu5Qu-OduANqwqhqYPixzfwGDXGIxBu-A4npMtM9a3myj8HfD5IMawPYS0LEL2A5VKBYtftONZSn6p22dNmedg816EDfROz5E0YTho3VytrXyuV51bS5ooM8z7GRfFx4d5ieqjzCfNNspY9uZ9dKC/s0-rw/rmdhnreza.my.id.mempercepat.startup.powershell.6.jpg)

5. Setelah selesai jalankan lagi perintah diatas (Cukup tekan tombol panah atas pada keyboard), Lalu `Enter`

![Figure 7](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiQMLFmjajTmy4MY8m46qz920nL3onL1BMZRGCl2-OPGIrvJE1b8Ay7UBQ3E_PKm6-_N7A98AUNcv9pA3WexFx-nMaHCC9QcVOQCXkl2bNTuKsyQElFTOnuptBg_gO2rq6dNOR8V2yBoz-esZEX30tjJIEK37-_OUppsvi0yZ1nUu3c12ve-hJC2Gj4pOyC/s0-rw/rmdhnreza.my.id.mempercepat.startup.powershell.7.jpg)

6. Tunggu lagi sampai _compile_ code nya selesai

1             |  2
:-------------------------:|:-------------------------:
![Figure 8](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiwf8TxhefMI8bTwafY-r1b_IjV5-VQVS0ADcBCr8xpVeyYZu5OdC6iXZkHiOhsYz82N22OjyOunH2cZ2LAJ7Tf-GfOgzC2ZewJgN3SackfSgmfi_cLdpTPAhW-8bvCJsNVZWGGq7Rznvq2GL5XlVGrE2BAsMpoFyBJH9fPLBKkddshTuwt9V-zQ8aedjuT/s0-rw/rmdhnreza.my.id.mempercepat.startup.powershell.8.jpg) | ![Figure 9](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEheZIq1zwfUSO9pWmpOoZa14sEEkN55gXa2hiZejvF0m6TNAxRuF6OVAP4cMsMRGaFnA7sLCCltRDTbmO4u6KUSkX_dZmSqf3PItrW-5j28YLZ0RFkjVwcWZ32PsWahOHveJYpDOMMVPZsI2B83VYIEmKrRZD7H7ETUzoIzGIDqIullbQM2uCtUGFggL3Cx/s0-rw/rmdhnreza.my.id.mempercepat.startup.powershell.9.jpg)

7. _Close_ **PowerShell Admin** nya, lalu jalankan **PowerShell** atau **Terminal** nya sebagai user biasa.

8. Seharusnya kalian _notice_ akan ada perubahan pada saat start-up nya, menjadi lebih cepat seperti ini

## Video setelah fix

{{% iframe "AD6v5dy92yVXFC6SRfxdPSK_xT8VV7oAYiOmvnt09VuJmiNi3WWvTxDPkyA19JzoijY5xBMdq_wKq9VhXvd3Z_6cIdMAPVGdM-vlctcusTL6vHr7TGjph9RS4zGwSX6LGoMA9-XTaTg" %}}

{{% adsense %}}

## Source

1. https://stackoverflow.com/questions/59341482/powershell-steps-to-fix-slow-startup
2. https://stackoverflow.com/a/59343705
