---
title: "Cara Bypass Installasi Restrictions Windows 11"
date: 2021-10-21T18:30:13+07:00
description: "Cara Bypass Installasi Restrictions Windows 11"
categories: ["Windows", "Windows 11", "Tutorial"]
tags: ["Windows", "Windows 11", "Tutorial"]
keywords:
  [
    "Bypass Installasi Restrictions Windows 11",
    "Cara Bypass Installasi Restrictions Windows 11",
    "Bypass Installasi Restrictions Windows 11 Rufus",
    "Windows 11",
    "Windows 11 Ghost Spectre",
  ]
description: 'Windows 11 Installasi Restrictions sudah ter-bypass otomatis di versi Ghost Spectre ini, tapi saya tidak terlalu menyarankan versi Ghost Spectre ini karena kita tidak tahu code apa saja yang diubah di Windows versi Ghost Spectre ini.'
summary: 'Windows 11 Installasi Restrictions sudah ter-bypass otomatis di versi Ghost Spectre ini, tapi saya tidak terlalu menyarankan versi Ghost Spectre ini karena kita tidak tahu code apa saja yang diubah di Windows versi Ghost Spectre ini.'
image: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhBHtbalLnHkYsI1w5DDQGDzMKf4vPuwdyj4dKtkGaqQaw9sF9vNffHJOcFGA3lb46CfzsSI9yCDZs4lZVI_s9ZcfF7cf8ee9UxzWtbuxGEV_bZZkH9QkeT4uVCd4_FFo1y80i12pffQ_M_02u5ASx8H_AJcrUWmYrMyK4jYEAuIRDHaUJKrZmYG9K3KWiU/s80-rw/windows11-logo.png
ThumbSchema: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhBHtbalLnHkYsI1w5DDQGDzMKf4vPuwdyj4dKtkGaqQaw9sF9vNffHJOcFGA3lb46CfzsSI9yCDZs4lZVI_s9ZcfF7cf8ee9UxzWtbuxGEV_bZZkH9QkeT4uVCd4_FFo1y80i12pffQ_M_02u5ASx8H_AJcrUWmYrMyK4jYEAuIRDHaUJKrZmYG9K3KWiU/s0-rw/windows11-logo.png
---

{{% adsense %}}

## Cara Bypass Installasi Restrictions Windows 11

## Cara Pertama: MenggunakanAutoUnattend.xml

1. Kalian Download terlebih dahulu Windows 11 nya di
   - https://www.microsoft.com/en-us/software-download/windows11
2. Kalian buat bootable flashdisk menggunakan rufus / yumi / unetbootin / WinNTsetup.
3. Setelah selesai membuat bootable nya kalian buat file bernama **AutoUnattend.xml** dan isikan kode berikut

```xml
<?xml version="1.0" encoding="utf-8"?>
<unattend xmlns="urn:schemas-microsoft-com:unattend">
    <settings pass="windowsPE">
        <component name="Microsoft-Windows-Setup" processorArchitecture="amd64" publicKeyToken="31bf3856ad364e35" language="neutral" versionScope="nonSxS" xmlns:wcm="http://schemas.microsoft.com/WMIConfig/2002/State" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
            <RunSynchronous>
                <RunSynchronousCommand>
                    <Order>1</Order>
                    <Path>cmd /c for %a in (TPM SecureBoot Storage RAM CPU) do reg add HKLM\SYSTEM\Setup\LabConfig /t REG_DWORD /v Bypass%aCheck /d 1 /f</Path>
                </RunSynchronousCommand>
            </RunSynchronous>
            <UserData>
                <ProductKey>
                    <Key></Key>
                </ProductKey>
            </UserData>
        </component>
    </settings>
</unattend>
```

**Catatan**: Code diatas bypass TPM, SecureBoot, Storage, RAM & CPU check, bisa kalian lihat di bagian `<Path>...</Path>`

4. Setelah selesai copy file **AutoUnattend.xml** ke flashdisk yang sudah dibuat bootable sebelumnya

![Copy AutoUnattend.xml](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgIaY99V-P4OvYGkK1S9aiGv6kOGBTr0J5sYVaVm0CKPR7rtSg5VTI5uBlBSdkrUVmW2y-HWODHgfv19bsQZLltb81ZWXrw204qLzSJmNpEeTpvXj861ZhxYvPLC62TqGqeR_MGriY47imZrpPuUJV2YZkAWztL_X4gJbbMKyEPC2FxszNpGr77mhsDk-bo/s0-rw/rmdhnreza.my.id-bypass-tpm-1.jpeg)

5. Selesai! kalian bisa lakukan installasi seperti biasa.

{{% adsense %}}

## Cara Kedua: Menggunakan Rufus versi 3.16 atau yang lebih baru

Developer pembuat aplikasi Rufus yaitu **[pbatard](https://github.com/pbatard)** sudah memperbarui aplikasi-nya untuk bisa mem-*bypass* *restrictions* installasi Windows 11, seperti yang bisa kita lihat di changelog aplikasi rufus versi 3.16 ini disana ada fitur "**Extended**" untuk *bypass restrictions* installasi Windows 11 ini.

- Fix ISO mode support for Red Hat 8.2+ and derivatives [#1777]
- Fix BIOS boot support for Arch derivatives
- Fix removal of some boot entries for Ubuntu derivatives
- Fix log not being saved on exit
- **Add Windows 11 "Extended" installation support (Disables TPM/Secure Boot/RAM requirements)**
- Add UEFI Shell ISO downloads (retroactively applied through FIDO)
- Add support for Intel NUC card readers
- Improve Windows 11 support [#1779]
- Improve Windows version reporting
- Speed up clearing of MBR/GPT

1. Kalian Download terlebih dahulu Windows 11 nya di
   - https://www.microsoft.com/en-us/software-download/windows11
2. Kalian Download **Rufus versi 3.16 atau yang lebih baru**
   - https://rufus.ie/en/ atau
   - https://github.com/pbatard/rufus/releases
3. Buka aplikasi rufus nya
   - Pilih Windows 11 ISO yang sudah kalian download sebelumnya
   - Pada bagian **image option** kalian pilih yang **Extended (Penting!)**
     - **Extended Windows 11 Installation (no TPM/no Secure Boot/8GB- RAM)**
   - Untuk selebihnya sesuaikan dengan system kalian saja, apakah menggunakan BIOS Legacy atau UEFI dan juga apakah menggunakan GPT atau MBR
4. Setelah selesai membuat bootable nya, kalian bisa lakukan cara installasi seperti biasa.

{{% adsense %}}

## Cara ketiga: Menggunakan Windows 11 Ghost Spectre (tidak disarankan)

Windows 11 versi Ghost Spectre ini adalah Windows 11 yang sudah dimodifikasi, yang paling terlihat dari versi ini adalah sudah tidak ada lagi *bloatware* atau aplikasi bawaan Windows 11 pada saat kalian sudah selesai installasi Windows 11, Windows 11 Installasi *Restrictions* sudah ter-*bypass* otomatis di versi Ghost Spectre ini, tapi saya tidak terlalu menyarankan versi Ghost Spectre ini karena kita tidak tahu code apa saja yang diubah di Windows versi Ghost Spectre ini.

1. Windows 11 versi Ghost Spectre bisa di download di web aslinya
   - https://ghostcloud.ml/wp1/windows-11-pro-superlite-compact-x64-version-21h2/
     - **password hxfile: ghostqwERQWE231**
     - **password mediafire: ghostmdot2**
2. Setelah terdownload kalian buat bootable menggunakan rufus / yumi / unetbootin / WinNTsetup.
3. Setelah selesai membuat bootablenya, kalian bisa Install seperti biasa

**Catatan**: Untuk versi Ghost Spectre ini tidak ada **Windows Store** untuk itu kalian bisa install manual **Windows Store** via **Ghost Toolbox** yang sudah otomatis include untuk versi Ghost Spectre ini.

{{% adsense %}}
