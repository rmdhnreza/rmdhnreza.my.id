---
title: "Mengatasi White Flash Saat Dark Mode Pada Browser"
date: 2021-03-06T00:15:23+07:00
categories: ["Linux", "Windows", "Tutorial"]
tags: ["Linux", "Windows", "Tutorial"]
description: 'White Flash adalah hal paling menjengkelkan pada saat kita berselancar di dunia maya, White Flash ini biasanya muncul ketika kalian membuka tab bar atau sedang memuat website yang kalian kunjungi.'
summary: 'White Flash adalah hal paling menjengkelkan pada saat kita berselancar di dunia maya, White Flash ini biasanya muncul ketika kalian membuka tab bar atau sedang memuat website yang kalian kunjungi.'
image: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEja_Xr-FGjd3bRVh3IYkF4Cr-RQdRkOvHRucbzgCQ1ZJDa97U0oAoKiyF9djhuTY6QJeZ1KdrIWWcBJI-fKXst9Osa0K_UA9wKfZ7Zc_yG8Toi5mx6wMCGQN8s7ACu_KBSMqHKP1FD5WRpoI6hpwKpu5ipDJUHeAFIRtMwqaBGR2KtTG_5IYCfPzc_ynqn9/s80-rw/browser-logo.png
thumbschema: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEja_Xr-FGjd3bRVh3IYkF4Cr-RQdRkOvHRucbzgCQ1ZJDa97U0oAoKiyF9djhuTY6QJeZ1KdrIWWcBJI-fKXst9Osa0K_UA9wKfZ7Zc_yG8Toi5mx6wMCGQN8s7ACu_KBSMqHKP1FD5WRpoI6hpwKpu5ipDJUHeAFIRtMwqaBGR2KtTG_5IYCfPzc_ynqn9/s0/browser-logo.png
---

{{% adsense %}}

***White Flash*** adalah hal paling menjengkelkan pada saat kita berselancar di dunia maya, ***White Flash*** ini biasanya muncul ketika kalian membuka tab bar atau sedang memuat website yang kalian kunjungi. Disini saya akan membagikan tutorial untuk Web Browser [Firefox](https://www.mozilla.org/en-US/firefox/new/), [Chrome](https://www.google.com/chrome/) & [Microsoft Edge](https://www.microsoft.com/en-us/edge).

Pertama-tama jika kalian menggunakan Windows 10, Fitur ***Dark Mode*** nya kalian aktifkan, ***White Flash*** tidak akan muncul, tetapi jika kalian tetap menggunakan ***Light Mode*** dan ingin menghilangkan ***White Flash*** ikuti tutorial berikut.

{{% adsense %}}

## Firefox
1. Kalian kunjungi **about:config** & **Klik Accept the Risk and Continue**
2. Copy dan Paste baris beriku
```
ui.systemUsesDarkTheme ->> Number ->> 0 itu Light Mode & 1 Dark Mode
browser.in-content.dark-mode ->> boolean ->> Jika Dark Mode pilih **True** sedangkan Light Mode **False**
```
Jadinya Seperti ini
```
ui.systemUsesDarkTheme ->> Number ->> 1
browser.in-content.dark-mode ->> boolean ->> true
```
Jika ingin Light Mode
```
ui.systemUsesDarkTheme ->> Number ->> 0
browser.in-content.dark-mode ->> boolean ->> false
```
![Firefox Force Dark Mode](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEh13oYIkjDXk4DARIrocy2Qho8RVkDAoFRsFYJsrExkk-fpXPYXZn8xvT0YYo_5UZcW0FthQ7yu4ebNSKqLaZAFz6uRYGpN-K0OVDBXSszx7w9l7rHCLmdPoeoOsl0YsLsTS_hjuiyhHSJk1IaRiawO9kEzKo97ylmxBDnRuqEx8mGn3bFOsLEqtrzaYwK-/s0/f-1.jpeg) | ![Firefox Force Dark Mode](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgCmrC-p0xob-VAb_4Ez1SuP3zKMdGjDM_DZVYDkzlJpG1vCZqaYcqm970TrE1ZDDdiEUc2-o7FVJ8oiaTVsYxG79O0moTTtqiUn34fdMMexm2S2cyjoBNQJuSFy2cukD7dODEKinGbPNHr2k7bej5uSnWbNPkJKG8NzNOJPrANyHcPV8QzxzfjHgYjCQg1/s0/f-2.jpeg)

3. Install Add-ons [Dark Reader](https://addons.mozilla.org/en-US/firefox/addon/darkreader/) dan Jika sudah terinstall lanjut ke langkah 4
4. Klik icon Dark Reader nya &#8608; Dev Tools &#8608; Preview new design &#8608; Apply &#8608; Exit

![Settings Dark Reader](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhmpKl-rUwpQQk4BWr3jW7KFkm2IadaEMzsts78OEke3X8P0PolQ_0MO0VDE3Y6UZsWvs8JkWxI_ExGxEFGMiuqD_19RjFaY6oflIUO7KDl35dOlstqT-u3ISg_866BMb6mRSn_rgXgLHJlXFqjgLY_9xmLULbGGcYYklRYlw46LcIBPD4D31BaFHadRtKZ/s0/f-3.jpeg) | ![Settings Dark Reader](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgtNF2IpE7SyImt6fU5l3tqQtvuDKaNreAdPCx9e-nr_OSGFrU3pVECCbYlCS6gUkaa5_WQiEPoqBgOP4wm0AwHCR72vcweVGUsXMoh_-0LoT4leIESwnFtqJt7rwl7hXDHvVSfXFlQ3b-dmxi73PNjmhND9Wp3EV_0_assCbL27QwcyOBUHZus0zfd8oJE/s0/f-4.jpeg)

5. Klik Settings &#8608; Site List &#8608; On kan Enable on restricted pages &#8608; Back &#8608; Manage Settings &#8608; On kan Synchronize site fixes

![Settings Dark Reader](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEh6-YuaxTf6JNvahLYZbl_kmlaLZ06y7wuOFSfxVa_Ro2-trYfYd2-MeF4pkaRL4K6Hkg25Ocf0t_nXpVj3bRlrEmsu1iVMsU72QLO-rq5b2dUWIa_b6Kl9c_Wsbp8YubbJCooUrm3_cEwkLug0JZ3dVhuUHRkM_Gap5NAYK2CHp0BaLCAAfWhDQCF6QiWz/s0/f-5.jpeg) | ![Settings Dark Reader](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgAeG7BW8Z4S5nZ63iqR9tpeJ9o-zojA-wmkHj6Kjjc7_1tUfOBY8ihAPaBjyBjL0Wwm3ZITH7O6pyaH6kDuy4Nl3AvkOOzolPhmDDL9euEiehQS-45nKiD5S1NXDt1WJjOWWhxnHWxYM8lRQGuc1Hr3CAOS-iMM8vWJPclrCnTihPVVsWm6Ee7PWXOSYzC/s0/f-6.jpeg)

6. Selesai, White Flash tidak akan Muncul.

{{% adsense %}}

## Google Chrome
1. Kalian buat shortcut Google Chrome di Desktop kalian dengan cara
```
Klik Start Menu ->> Klik Kanan pada icon Google Chrome ->> More ->> Open file location
->> Klik Kanan pada icon Google Chrome ->> Send to ->> Desktop (create shortcut)
```
![Buat Shortcut Google Chrome](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgTSogeX4hsIV-ayLuRRKeJmYwWOPrQ58k_ente_QHEknb5_Moycd8hQLOegSjZpqjVn9PY3jwwkU0D4uu0kNCkf-bN0ul7wI1UPvdd52ZdXUZM63a6Ri3zjX9ItJVd2wU7SRrBLZG9KCwi506zOVqDSeTj8iqd6lPorKiiQz0BZkpr5NmtXpraOxToeCpQ/s0/s-1.jpeg) | ![Buat Shortcut Google Chrome](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgNIV0Y_KOvOUfb_spnT_1gzLSGO-B_jnCNueNo7z1GNi_bc2smLia4JwN0unNp7PdoQ7gLin2Oux8JZzavczcRU_QVkee11IJ-CKEMqf3HG3PGyMNrMqMWcLc7l7u9lIpk2exL3WQIiq-XS_IpVEHGozF8ir4IxlVEnk8pWlJuEu0rwGUsDAsn_eXE-mHz/s0/s-2.jpeg)

2. Klik kanan pada shortcut Google Chrome yang baru saja dibuat, tambahkan command line **--force-dark-mode** setelah chrome.exe"
```
"C:\Program Files\Google\Chrome\Application\chrome.exe"[spasi]--force-dark-mode
Jadinya seperti ini
"C:\Program Files\Google\Chrome\Application\chrome.exe" --force-dark-mode
```

![Menambahkan --force-dark-mode](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEi2HZvQIpf72Nsr7JbiGR_HyLS6UcUb6cndg2RKkXxU2kfmzDUy_APN3lUyY-sAMANq2g0obEmBJLJAV5E6tJNlxeoWDO5MIom_6AWG16Q930UPf9SIYWO01FQA-kDcRdTjjHHAta3_29SiUs4hiVf9ffveaP1G4hTl2NAclXXU9u0Tz6AOEmFTAIiZh0ZI/s0/c-2.jpeg) | ![Klik Continue jika ada prompt seperti ini](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiO-lVPm6yNICI9K-iY0qrOjC3sJoGlAstW0OoIBvu3lMrPW5MpCqUVSRO6T8i6MoOrm3URcrdUmIQDxffeCGxL74TGwHXI6KJprokv4_VCQ-IVsXG0ux2YeLi-dFl4hMTXmdHkopo-Y8b4NUZ3HEJIv6v0kqJNufED3G5Dnxws1D6JadtYkAU3ksO4wesm/s0/c-3.jpeg)

3. Buka Chrome & Install Extension [Dark Reader](https://chrome.google.com/webstore/detail/dark-reader/eimadpbcbfnmbkopoojfekhnkhdbieeh) dan Jika sudah terinstall lanjut ke langkah 4
4. Klik icon Dark Reader nya &#8608; Dev Tools &#8608; Preview New Design &#8608; Apply &#8608; Exit

![Settings Dark Reader](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEi5dHL27hQysr2fvpdP-kxtfcruy9d5aRe3W26dn9S52ZROgRPPuxGOBUSZx0yAdDpS1wXx48NMv0472XiUjkO7uhQW_q0D_t4YXyHE8U6hB0DbOgxveYL6uQqyKaKWcBwQVlapSO9Hhd92GQ_y_9L5LOM2hYJ7bosKc-JHr-XImjtnAY1L09ZJDFxXFGTN/s0/c-4.jpeg)

5. Klik Settings &#8608; Site List &#8608; On kan Enable on restricted pages &#8608; Back &#8608; Manage Settings &#8608; On kan Synchronize site fixes

![Settings Dark Reader](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjzEPaw7vGnl434miMqfBtIZ301Mjmxus4gnmvzbwlww1UyWTh0tMmzNHa5REu3NdQuKSFU8AivAwDlAazVxA5a_WPmdbivrKNtF4jcZ73r8Y2FbnJVVCz52RO14VxW1Tz11uYr1pfAEylTWRfRLzJ3A_NTgBOxuVRldnJuol7Glz3oGbAeuhl64VZP8USp/s0/c-5.jpeg) | ![Settings Dark Reader](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEj36JjIDzi2RmB_HJHLeXaGjW49T_x-yz-lIyHyKD-QV-Kxgf-M2iG9YqSmN2uM7V3fGWHRWoloqzQjCsr84S6VbJjNvbRmX1jRJDefZiTLsGVjA3h-3-Za2n5FkqnruJqn7mYhyphenhyphen_G_crpp60_cVKkWLn554Qrm2qi8RqvekDeHquGqRUumrjLgnpafGmyn/s0/c-6.jpeg)

6. Selesai, White Flash tidak akan Muncul.

{{% adsense %}}

## Microsoft Edge
1. Kalian kunjungi **edge://settings/appearance** dan ganti **Default Theme** ke **Dark**

![Mengganti Tema](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhMhIiIpIf0APvcXDYxwzUWU9SeELrLnnAa-EzC_z72SZZedVzV6NnhZT6utlO2tZx13cfo9krckVBCBnS4_Cm0yPJ5eW0WenrGxGa3SFBfgvaxJ9Nl2HtwZmEdKVemC9uBj3Nkl9sDPGJd6ZfX5Tu_GaZUys2j_rwOK4LYbyBqg3_TCrhSO3ExF8-lNnyy/s0/e-1.jpeg)

2. Install Extension [Dark Reader](https://microsoftedge.microsoft.com/addons/detail/ifoakfbpdcdoeenechcleahebpibofpc) dan Jika sudah terinstall lanjut ke langkah 3
3. Klik icon Dark Reader nya &#8608; Dev Tools &#8608; Preview New Design &#8608; Apply &#8608; Exit

![Settings Dark Reader](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhux9qLlmOo5ZKa4jyB0jDKRC02FpuRh6wxetcw0gPfm2jio0O4ZeWA9UTFA-hJg9gherBwEPcfsKt4dvyNPtSeynakP3EpHBMW-eSeerie7nFusad48K-abVcWh7wMTnMWcpbWzaEXlsvqyWR44y2yd7XBVrlozudx13DPWZKFYAGukZdHAbVfLK9Ul-_v/s0/e-2.jpeg)

4. Klik Settings &#8608; Site List &#8608; On kan Enable on restricted pages &#8608; Back &#8608; Manage Settings &#8608; On kan Synchronize site fixes

![Settings Dark Reader](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEigXclcAi76MZF3d6yGUv5QHI4bjxOIN4nHBFVgxvmzXfHBvjD3dCOCdgE4ERqvqJ6JiWR3hnffuHLicCFucvttjmQc_szKGMvVX-nVZhvfUNwktlLDqq8FQWM52BYmF77LFsAnC8zgE5W2cV5pvW-DRusveZ8I_V4mUce3sAjb-2n48OjcO1dnzQNeGcw9/s0/e-3.jpeg) | ![Settings Dark Reader](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgVPRiO-lW3ONuatrCMUQGgd4djOEchAUGv-FXWscHYHmM2tfZq1-7mRv6TWo1yjvLJskgmHyZDr_Gy-WebFA3xs3jPiZI22vrE-KCyj8MBGaVms62KQe8ookI1N0SV1yEzy8kxapRZJ_8O1JQaK6hJahSUsrPp5LcEyoqpEXOpdhZ-fu4RqH_MQlv26BZJ/s0/e-4.jpeg)

5. Selesai, White Flash tidak akan Muncul.

{{% adsense %}}
