---
title: "Enable Atau Disable Cortana Di Windows 10"
date: 2021-01-22T16:53:20+07:00
categories: ["Tutorial", "Windows 10"]
tags: ["Tutorial", "Windows 10"]
description: 'Cortana adalah asisten pribadi berbasis cloud yang bekerja di seluruh perangkat Windows dan layanan Microsoft lainnya. Cortana dapat menyediakan berbagai fitur. Cortana di Windows tersedia di negara dan bahasa tertentu. Cortana juga tersedia di platform lain, seperti Android dan iOS.'
summary: 'Cortana adalah asisten pribadi berbasis cloud yang bekerja di seluruh perangkat Windows dan layanan Microsoft lainnya. Cortana dapat menyediakan berbagai fitur. Cortana di Windows tersedia di negara dan bahasa tertentu. Cortana juga tersedia di platform lain, seperti Android dan iOS.'
image: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEg1b05kzmSnLWUrG2u5uokNT3Js6g9uYEMMKfc5wqAdOQ0evNPTlNpFNbF3vizWMbSKYd-m2HKQxY6Hd3jtgWedZEkHho9YlFrh7B_AtOxw0a0HSk_QXGJdJN7oMsZb1Fu1k5fOgTuiNymq3XAgr0IV7lCxwGMFzE_jWkAdM1bLCXVapYr10bSh2wtw_zt5/s80-rw/cortana.jpg
ThumbSchema: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEg1b05kzmSnLWUrG2u5uokNT3Js6g9uYEMMKfc5wqAdOQ0evNPTlNpFNbF3vizWMbSKYd-m2HKQxY6Hd3jtgWedZEkHho9YlFrh7B_AtOxw0a0HSk_QXGJdJN7oMsZb1Fu1k5fOgTuiNymq3XAgr0IV7lCxwGMFzE_jWkAdM1bLCXVapYr10bSh2wtw_zt5/s0-rw/cortana.jpg
---


{{% adsense %}}

Cortana adalah asisten pribadi berbasis cloud yang bekerja di seluruh perangkat Windows dan layanan Microsoft lainnya. Cortana dapat menyediakan berbagai fitur. Cortana di Windows tersedia di negara dan bahasa tertentu. Cortana juga tersedia di platform lain, seperti Android dan iOS.

Cortana bekerja paling baik saat kalian masuk (*sign in*) dan mengizinkannya menggunakan data dari perangkat kalian, layanan Microsoft lainnya, dan layanan pihak ketiga yang kalian pilih untuk disambungkan. Cortana belajar dari data tertentu tentang kalian, seperti pencarian, kalender, kontak, dan lokasi kalian. Kalian dapat mengontrol seberapa banyak data yang Anda bagikan. Jika kalian memilih untuk tidak masuk (*sign in*) ke Cortana di Windows, kalian masih dapat mengobrol dengan Cortana dan menggunakannya untuk membantu kalian mencari di web, dokumen yang disimpan di layanan Microsoft seperti OneDrive, dan perangkat Windows Kalian. Di perangkat iOS dan Android, Cortana hanya berfungsi saat kalian masuk (*sign in*).

Kalian harus log in sebagai **administrator** untuk enable atau disable Cortana

#### Enable atau Disable Cortana menggunakan Group Policy
1. Buka **Local Group Policy Editor**, caranya kalian tekan shorcurt pada keyboard **Win + R**, setelah itu masukan `gpedit.msc` atau Kalian juga bisa menggunakan fitur **Search**
2. Di panel sebelah kiri **Local Group Policy Editor**, Kalian masuk ke

Computer Configuration/Administrative Templates/Windows Components/Search

3. Di Panel sebelah kanan **Search**, double click/tap di **Allow Cortana** Untuk mengedit policy nya

![Local Group Policy Editor](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhrv-nniX8KsXIaoUUFuevBHN4xbMVzhw1-hQ7D4uXJ9z1d94N8zYPHaQO-LSdw_8U6WuWK31aIEQSKldyrQq3L0Cmjc56ZUOazqSMk5omImSVpS9F5LjTtBbbjhSSjXdA5rwdBW5LFVLJUZrhclugEcQ8qkJKp5lU_pE56GN64XRWcUQIN6PtHf-J-Rde4/s0-rw/1.jpg)

{{% adsense %}}

4. Langkah selanjutnya kalian tinggal lihat **langkah 5 untuk enable cortana** atau **langkah 6 untuk disable cortana**
5. Untuk Enable Cortana kalian pilih **Not Configured** atau **Enabled**
6. Untuk Disable Cortana kalian pilih **Disabled**

![Local Group Policy Editor](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEitGTYg5ol76xOnksWFn3BD595_a0dRZm6z4ltejiC29lWlL0XskExjW6TvmRsCnWn9hT772ForMo3m6XQMxnpYZMty6dGYEn2uWgOkeXJ2NsbnBHz91v2IwC7EYXLsB-MDhbB55rlcZ_JFAutgZRSAlkY7nFhnzWGNr1Lmj-mzHGmuAUXPsrJBma3eO9_U/s0-rw/2.jpg)

7. Jika sudah, Close **Local Group Policy Editor**
8. Restart Explorer atau Sign Out & Sign In atau Kalian Restart PC kalian. Untuk menerapkan konfigurasi yang sudah di setting di **Local Group Policy Editor**

{{% adsense %}}

#### Enable atau Disable Cortana menggunakan Regedit

File .reg dibawah ini mengubah value DWORD registry key berikut
HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows\Windows Search
AllowCortana DWORD
0 = Disable
1 atau delete = Enable

1. Download file **langkah 2** untuk Enable Cortana & **langkah 3** untuk Disable Cortana
2. Enable Cortana (Default Settings)
   * [Download Reg File](https://www.tenforums.com/attachments/tutorials/41034d1443973120-cortana-enable-disable-windows-10-a-enable_cortana.reg)
3. Disable Cortana
   * [Download Reg File](https://www.tenforums.com/attachments/tutorials/41033d1443973120-cortana-enable-disable-windows-10-a-disable_cortana.reg)
4. Save file di Desktop atau dimana saja

{{% adsense %}}

5. Double click/tap di file .reg yang kalian download.
6. Ketika muncul UAC kalian klik Yes, dan klik OK lagi untuk menerapkan konfigurasi regedit nya.
7. Restart Explorer atau Sign Out & Sign In atau Kalian Restart PC kalian. Untuk menerapkan konfigurasi yang sudah di setting di **Regedit**

**Note:** Cara pertama (gpedit), biasanya tidak bisa diterapkan di **Windows versi Home**, untuk itu kalian bisa menggunakan cara kedua (regedit)

Source Tutorial: [tenforums](https://www.tenforums.com/tutorials/25118-enable-disable-cortana-windows-10-a.html)

{{% adsense %}}
