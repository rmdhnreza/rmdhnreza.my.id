---
title: "Membuka Situs Terblokir Menggunakan DNS Over HTTPS"
date: 2021-01-08T15:33:28+07:00
Description: "Membuka Situs Terblokir Menggunakan DNS Over HTTPS"
categories: ["Android", "Linux", "Windows", "Tutorial"]
tags: ["Android", "Linux", "Windows", "Tutorial"]
description: 'Kali ini saya akan share cara Membuka Situs Terblokir Menggunakan DNS Over HTTPS atau biasa disingkat DoH, cara ini tidak menggunakan aplikasi pihak ketiga, seperti VPN atau yang lainnya, cara ini hanya membutuhkan Browser Up-to-Date.'
summary: 'Kali ini saya akan share cara Membuka Situs Terblokir Menggunakan DNS Over HTTPS atau biasa disingkat DoH, cara ini tidak menggunakan aplikasi pihak ketiga, seperti VPN atau yang lainnya, cara ini hanya membutuhkan Browser Up-to-Date.'
image: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEg7G_GN-v6Qr48XUggyNQRzf84f12_b0IXt5IK3SnJ7cKPmoE-kADN9PiYDcPu7d9orm2XdnWaDsgFAdO2Tem_gUMIYKz2LTv76kOeVJUc1TYWdRKSk23xYreRFxjkHv_yRelm_xz3WsGOXujYCS-crK9lWS2CEw6G7Qew-aEkiLm9wotoBLLJ8SapdASCV/s80-rw/dns-logo.jpeg
ThumbSchema: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEg7G_GN-v6Qr48XUggyNQRzf84f12_b0IXt5IK3SnJ7cKPmoE-kADN9PiYDcPu7d9orm2XdnWaDsgFAdO2Tem_gUMIYKz2LTv76kOeVJUc1TYWdRKSk23xYreRFxjkHv_yRelm_xz3WsGOXujYCS-crK9lWS2CEw6G7Qew-aEkiLm9wotoBLLJ8SapdASCV/s0/dns-logo.jpeg
---

{{% adsense %}}

Kali ini saya akan share cara **Membuka Situs Terblokir Menggunakan DNS Over HTTPS** atau biasa disingkat **DoH**, cara ini tidak menggunakan aplikasi pihak ketiga, seperti VPN atau yang lainnya, cara ini hanya membutuhkan **Browser Up-to-Date**. Kelebihan menggunakan **DoH** ini tidak terlalu berpengaruh pada kecepatan internet kalian, tetapi kekurangan **DoH** ini hanya bisa membuka situs terblokir yang menggunakan protokol **HTTPS**, tapi tenang saja karena tahun 2021 ini hampir semua web sudah menggunakan protokol **HTTPS**.

## Menggunakan DNS Over HTTPS Google Chrome
Untuk Google Chrome sendiri sudah support DNS Over HTTPS di sistem operasi Windows, Android, hanya saja di sistem operasi Linux belum support (teatpi bisa menggunakan policy). Untuk mengaktifkannya kalian bisa
1. Masuk ke bagian **Settings** (Klik titik 3 dibagian atas kanan lalu pilih settings)
2. Pilih **Privacy and Security** (dibagian kiri) dan kalian Klik **Security**
3. On kan **Use Secure DNS** kalian pilih **With:** lalu disana kalian pilih DNS yang kalian pakai
![Dns Over HTTPS Chrome](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhCE5-vZFuVWDLULVJNiXN4YlO8U_MBg3H3jjiu7hf7bFgoGb4faJKn9XGH8AqnvbUrkLQf3R_gfcSXezisx3BEE1BKNd6gu2bP2kE-AhDea4s7cu6cD3sgpvjhZRVn0bfbU2NTHvX09V4BJE0NtklvS3raWr9Zwn2FV4dJbGBmgVEVDf0auYuOFGRItqV5/s0/DoH_Option%201)

{{% adsense %}}

Untuk sistem operasi Linux kalian bisa menggunakan policy
1. Kalian buat file **policies.json** di
   * /etc/opt/chrome/policies/managed/policies.json (Untuk Google Chrome)
   * /etc/opt/chromium/policies/managed/policies.json (Untuk Chromium Based Browser)
2. Lalu isikan
```json
{
	"DnsOverHttpsMode"      : "secure",
	"DnsOverHttpsTemplates" : "https://dns.quad9.net/dns-query",
}
```
3. Save

**Note:** DNS Over HTTPS diatas (Untuk Linux) menggunakan DNS quad9, untuk DNS lain kalian bisa ubah templatenya dengan
   *  https://dns.google/dns-query (DNS Google)
   *  https://cloudflare-dns.com/dns-query (DNS Cloudflare)

{{% adsense %}}

## Menggunakan DNS Over HTTPS Microsoft Edge (Chromium)
Untuk Microsoft Edge sendiri sudah support **DNS Over HTTPS** di sistem operasi Windows, Linux. Untuk mengaktifkannya kalian bisa
1. Masuk ke bagian **settings** (Klik titik 3 dibagian atas kanan lalu pilih settings)
2. Pilih **Privacy, search, and services** (dibagian kiri) dan kalian scroll kebawah sampai bagian **Security**
3. On kan **Use Secure DNS** kalian pilih **Choose a service provider** klik kolomnya lalu disana kalian pilih DNS yang kalian pakai


![Dns Over HTTPS Microsoft Edge](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhven61BUdvXcpvRdW2Qw9-IoJi_iQPvNPXTYgT8glA_KJvMyDPYpaBFJ6GpFDNraLGPHXtJZM6biU9whb42fx-bdnHyArSveV2hu9GstaCiEtBcdPm3oR3BgymE5EdUAxR3-c-yErklxUtgEtPaKpD05z9AS-8NyYJ7OdUUCnUWljt-9PP_Wdl2c2E521z/s0/doh-edge.jpg)

{{% adsense %}}

## Menggunakan DNS Over HTTPS Mozilla Firefox
Untuk Microsoft Edge sendiri sudah support **DNS Over HTTPS** di sistem operasi Windows, Linux. Untuk mengaktifkannya kalian bisa
1. Masuk ke bagian **Preferences** (Klik strip 3 dibagian atas kanan lalu pilih Preferences)
2. Scroll ke paling bawah sampai bagian **Network Settings** dan kalian klik **Settings**
3. Ceklis **Enable DNS over HTTPS** lalu kalian pilih **Cloudflare** atau **NextDNS**
![Dns Over HTTPS Firefox](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhvcLqfhyphenhyphenX8ZTqMqOLPogP8D1MdvOj81KI9HAxm0Z1m-DSuKT_6_zdzAusgr19TOcZ7yeKXS42W8V21izWZnQqyrZM3_nOT9vjfmP91olgeQElQSGrNCFPO2m9cy4rrvSHtO1GkgsBaAu1qqztgDqTjctFD7PMcG1Tz0UhCslAh1GXVAJ9vtuShTbu9BeKJ/s0/doh-firefox.jpg)

## Menggunakan DNS Over HTTPS Andorid 9+
Untuk Android 9 keatas sudah support **DNS Over HTTPS** atau **Private DNS**. Untuk mengaktifkannya kalian bisa
1. Buka **Settings** ⇢ **Connections** ⇢ **Cari Private DNS** atau Jika kalian mau lebih cepat kalian search aja **“Private DNS”** dibagian settings
2. Kalian Klik **Private DNS** nya dan Pilih **Private DNS provider hostname**
3. Kalian isi
   * **dns.google** untuk DNS Google
   * **1dot1dot1dot1.cloudflare-dns.com** untuk DNS Cloudflare
4. Jika sudah klik Save, kalian sudah bisa membuka situs yang terblokir
![Dns Over HTTPS Android](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiV4SiKhHCwroZE7T5DLZRZ8Xgrli99KxvNOffX9HUHTf7g5xjIZQsEq7gPY7GFWCYB1qg369xhGaLaQCFXjkOh3DAVE0DcppNK9d9Umkss6VxKMMFJQ0Z-nM5MLFmvkPByfthZQE38CnTInebH9UZBGRFN-lN9gdLJezjXTNjRyETh8Ly2wKgH5leV-fmB/s0/doh-android.jpg)

{{% adsense %}}
