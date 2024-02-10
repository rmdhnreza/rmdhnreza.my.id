---
title: "Cara Membuat Icon Website Light Dan Dark Mode"
date: 2021-03-05T17:16:23+07:00
description: "Tutorial Membuat Icon Website Support Light dan Dark Mode"
categories: ["Tutorial"]
tags: ["Tutorial"]
description: 'Kali ini saya akan memberikan tutorial cara membuat icon website menjadi Light Mode dan Dark Mode.'
summary: 'Kali ini saya akan memberikan tutorial cara membuat icon website menjadi Light Mode dan Dark Mode.'
image: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiV_S2fojJ5OaRgHeJ9j60H2LPAH1CJxla3VLptqcPT9H5deRhxKoarSftCILqpctjIlSwi8gzBxtDFQOdqI9cID4TGOEWqtYxEVbjeN9zHVC4OLFkk-YfOTzukKGyeZH95aVo235mIRb6eYU58LuSAYLaxREJxsqouX1LjHmuwNZ5uCTW2d7P0h0BpjyiJ/s80-rw/switch-logo.jpg
ThumbSchema: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiV_S2fojJ5OaRgHeJ9j60H2LPAH1CJxla3VLptqcPT9H5deRhxKoarSftCILqpctjIlSwi8gzBxtDFQOdqI9cID4TGOEWqtYxEVbjeN9zHVC4OLFkk-YfOTzukKGyeZH95aVo235mIRb6eYU58LuSAYLaxREJxsqouX1LjHmuwNZ5uCTW2d7P0h0BpjyiJ/s0-rw/switch-logo.jpg
---

{{% adsense %}}

Kali ini saya akan memberikan tutorial cara membuat icon website menjadi Light Mode dan Dark Mode, seperti ini contohnya:

![rmdhnreza.my.id](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgBoU2BLuC52s4vjC_Tu5Zm1awN5qCI0aeZJozvmOhsCZ5PhISILdyMyvRs1TpAH3VPchhHbr8GGba04lbSYQwI8gBiH0p9JZHJmnChtOfOXpfASkEa3ti-bEYMR7Fto058Z0X4jJR83IKmpuHgx6gQf5-ucbVvAJ1syOs19BegJpFdoo-zjnO7Q5HJUhNd/s0-rw/2.jpeg)

Disini saya akan memberikan untuk penggunakan icon berekstensi **SVG**, jadi tidak menggunakan **Javascript** atau **2 file icon**.
Jika website kalian belum menggunakan **SVG**, pastikan favicon kalian convert terlebih dahulu ke **SVG**, jika sudah kita langsung ke langkah selanjutnya.

1. Buka file **SVG** menggunakan text editor kesukaan kalian (disini saya menggunakan VScode)
2. Tambahkan baris CSS berikut sebelum **`<path>`**
```css
<style>
path {
  fill: black; // light mode, icon berwarna hitam
}

@media(prefers-color-scheme:dark) {
  path {
    fill: white; // dark mode, icon berwarna putih
  }

}
</style>
```
Jika sudah kalian **Save**

![Edit SVG Icon (Klik Pada Gambar Untuk Memperjelas)](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjfIXSwnVg4wL2nA2PkKQ94QDMxVU-yhzzj2mGTNHlLVPf4mxcoaY2-fKps3357BeLzPkrxvVFdWjKUYn6dwAbCCBNpunJuPgByFXiQh5US99qY2CLAXu24o1D3LuoRSpyHmYIlYth4Yh7DkgiIP2qNy4TsaAQTZnItlSKRm1cQd5ZSmioo4Ff9YrzcNRg_/s0-rw/3.jpeg)

{{% adsense %}}

3. Edit bagian **head** pada website kalian, hapus baris favicon sebelumnya dan gantikan dengan baris berikut
```html
<link rel="icon" href="/favicon.svg" type="image/svg+xml">
```
4. Kalian Save lalu test menggunakan browser kesukaan kalian (disini saya menggunakan Microsoft Edge Chromium)

![rmdhnreza.my.id](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgBoU2BLuC52s4vjC_Tu5Zm1awN5qCI0aeZJozvmOhsCZ5PhISILdyMyvRs1TpAH3VPchhHbr8GGba04lbSYQwI8gBiH0p9JZHJmnChtOfOXpfASkEa3ti-bEYMR7Fto058Z0X4jJR83IKmpuHgx6gQf5-ucbVvAJ1syOs19BegJpFdoo-zjnO7Q5HJUhNd/s0-rw/2.jpeg)

{{% adsense %}}
