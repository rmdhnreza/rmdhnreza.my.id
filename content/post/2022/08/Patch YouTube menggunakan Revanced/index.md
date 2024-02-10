---
title: 'Tutorial Patch YouTube Android dengan ReVanced'
date: 2022-08-09T15:30:13+07:00
description: 'Tutorial Patch YouTube Android dengan ReVanced'
categories: ['Android', 'Tutorial']
tags: ['Android', 'Tutorial']
keywords:
  [
    'Tutorial Patch YouTube Android dengan ReVanced',
    'How to Patch YouTube Android with ReVanced',
  ]
description: 'Tutorial Patch YouTube Android dengan ReVanced'
summary: 'Tutorial Patch YouTube Android dengan ReVanced'
image: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgRG1aqNJ299j2-lxVdxy0A5AQgPkya57k12PBkasFj1rjaG964AAkvRdqkduF5W7IsCbk-J6pdZLtzz282SsOzTE_FbYNkRA_oQzzCTl7IZre891a-n6kS2b5Ljzfsq5QuPTeuNaQ8ocTBEUtsFdt9G_6NpgKm0GW0fvozrl6MGYooetKcam6xWRa8LIdC/s80-rw/revanced-logo.jpg
ThumbSchema: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgRG1aqNJ299j2-lxVdxy0A5AQgPkya57k12PBkasFj1rjaG964AAkvRdqkduF5W7IsCbk-J6pdZLtzz282SsOzTE_FbYNkRA_oQzzCTl7IZre891a-n6kS2b5Ljzfsq5QuPTeuNaQ8ocTBEUtsFdt9G_6NpgKm0GW0fvozrl6MGYooetKcam6xWRa8LIdC/s0-rw/revanced-logo.jpg
---

{{% adsense %}}

Sebelumnya saya sudah buatkan tutorial [Cara Block Iklan di Aplikasi YouTube Android 2021 (root dan tanpa root)](https://rmdhnreza.my.id/cara-block-iklan-di-aplikasi-youtube-android-2021-root-dan-tanpa-root/), sayangnya YouTube Vanced sudah tidak akan di update lagi dan lambat laun YouTube nya tidak akan bisa dibuka karena versi nya yang sudah lawas.

![YouTube Vanced](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgFtPSaHCkLUz7hFL4TFlLLAS95aA-FxeNyvgiUZW709RfoL9T1W2aJlchIjHPHQHSvs7lhUXhR9hHez1ihVtloim9EzTSkGq75f9zZOw7aJIbcoocw5whyphenhyphenDY6bG2kpntNwf_6PRQp1yKiIU-IaqqeG2EslXSde45X7utfuA4KG4BGZ2RPb6BLiiXnv1HDt/s0-rw/rmdhnreza.my.id.revanced.0.jpg)

Untuk itu sekarang kita harus menggunakan ReVanced dan patch sendiri (untuk saat ini) aplikasi YouTube nya.

## Aplikasi yang dibutuhkan

Sebelum mulai tutorial nya pastikan kalian download dan install terlebih dahulu aplikasi yang dibutuhkan:
* [ADB](https://adb.clockworkmod.com/)
* [Zulu OpenJDK versi 17+](https://www.azul.com/downloads/?package=jdk#download-openjdk)
  * Untuk check apakah Java nya sudah terinstall atau belum kita bisa buka `PowerShell` atau `Terminal` lalu ketikan `java --version` jika yang muncul adalah versi java-nya penginstallan berhasil, jika belum, pastikan java-nya sudah ada di `PATH`.

![Java Version](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgT657E4KIy6s5QzpOCXAcEvr1kfcp8LXojyVFjH5c1nX1NRD1XZy-BYhbR3Em7uQdR-awULGzX8e2NiEOofqCwt_MTA3rmT8LNjUBJpKIQGP7kHmG9bqnUTTP_FjdhRpvhlD_JFAJOZLzQMgENFhAo7p0W4pnLHGzF1kC5y-77x5S1keWIPcvMNK_cYJdA/s0-rw/rmdhnreza.my.id.revanced.1.jpg)

* [APK YouTube yang akan kita Patch](https://apkcombo.com/apk-downloader/#package=com.google.android.youtube)\
  (Untuk menghindari error pada saat proses Patch pastikan versi `Architecture` & `Android` nya sesuai dengan smartphone yang kalian pakai dan rename apk file nya menjadi `youtube.apk`)

![YouTube APK](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgcxnDcxnGAnw6edSC_MvtBbz9E4rn50tbJOKrvR7FFggkNjf7OgBgnKBkn1uSIohjgJtQOdXDkF6JKEUBuNZKdfQYTZotV9-1pWU0ZobGj3UCj_ueVmL6pcRycWQdjrqfM0iZs_AuIGnMwNQaV5_O3t7pxfyAbAlrJy3z6QfpRDRk7T03dNcpoLa3vRjVs/s0-rw/rmdhnreza.my.id.revanced.2.jpg)

* Prebuild Packages untuk
  * [ReVanced CLI](https://github.com/revanced/revanced-cli/releases/latest) (setelah di download rename menjadi `revanced-cli-all.jar`)
  * [ReVanced Patches](https://github.com/revanced/revanced-patches/releases/latest) (download yang ber-ekstensi `.jar` setelah itu rename menjadi `revanced-patches.jar`)
  * [ReVanced Integrations](https://github.com/revanced/revanced-integrations/releases/latest)


{{% adsense %}}

## Proses Patch
Jika semua file nya sudah ada di Desktop kita, file `youtube.apk`, `revanced-cli-all.jar`, `revanced-patches.jar` & `app-release-unsigned.apk`, harus berada di folder yang sama (agar perintahnya sama).

![File di tempatkan di folder yang sama](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhwmVtJGsOA0cl3PXq8u1VNBlO1mXRZTd4jQV-0JCWZCHflynNtZKbwClY7rlv3_kN9kSoqxmVQ0_Ui2yVRDO7EN3inpp36w4QGHX-ddC6o4_zRbrfAsjWS4bJccuyf594DkgeRIAFmI9MeEaKKYIp0EWqY3Mkv1wJkeZU35c52_Z9BsQ8JBpTXI5yizNOA/s0-rw/rmdhnreza.my.id.revanced.3.jpg)

1. Pastikan kalian `Uninstall` atau `Uninstall Pembaruan` terlebih dahulu aplikasi YouTube nya (entah itu YouTube Vanced atau Original dari PlayStore)
2. Buka `PowerShell` atau `Terminal` di folder ReVanced nya.
   * Untuk Windows cukup tekan `SHIFT` + `Klik Kanan`  lalu pilih `Open PowerShell Window Here` atau
   * cukup `cd folder/ReVanced`
3. Koneksikan Android kita ke PC dan pastikan Android kita sudah terbaca, lalu ketikan perintah `adb devices`, dikarenakan kita membutuhkan `Device Name` nya.
   `RR8M9XXXXXX` adalah `Device Name` punya saya, pasti ini berbeda-beda setiap Android.

![adb devices](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgdNxuQ9h0YgSpCJzy6nkNWeEczn5_DNsKK7qxWHzY0k9IyflKimueYIBw19QYPndqZKUvWsD1eFmoNw3IY5wYQoJVv0sLooxkJA5-yjh97dZma0VlY-FAuDtkeWKHWpoOtJ1Q0u7Arw6pEyJuJtMGNJ4oFPxheA1HJOrpAxztag_7bIZG4vBGyxh1oa-35/s0-rw/rmdhnreza.my.id.revanced.4.jpg)

4. Terakhir masukan perintah berikut ini

### Non Root
```fish
java -jar revanced-cli-all.jar \
     -a youtube.apk \
     -c \
     -m app-release-unsigned.apk \
     -d device-name \
     -o revanced.apk \
     -b revanced-patches.jar \
     --experimental
```

### Root

```fish
java -jar revanced-cli-all.jar \
     -a youtube.apk \
     -c \
     -d device-name \
     -o revanced.apk \
     -b revanced-patches.jar \
     -e microg-support \
     --experimental \
     --mount
```

![Perintah Patch](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjWKYiWbBVkQsxCYPFqmUXeqgS3FChYpBJuPKIBulxyH_FdVCZgRD0iAM1DXSk8ujyt07mSMaOL7sD1_xpnGH5bWXyVRCdzb5kK9I8AzksAKW7tyWcncVzLJAR9Q3Di10AWGKqa7AlSMw-IZlys3e4SrzEaluvMlIBkw07shEieS6kFpJNxIBfkPol_8OKd/s0-rw/rmdhnreza.my.id.revanced.5.jpg)

5. Kurang lebih output nya seperti ini jika berhasil, dan langsung otomatis terinstall ke Android kita.\
   Catatan: Cukup abaikan `WARNING` karena kita hanya fokus ke aplikasi `com.google.android.youtube` saja.

{{< spoiler text="Patch Berhasil" >}}

```fish
INFO: Decoding resources
INFO: Reading dex files
INFO: Merging app-release-unsigned.apk
WARNING: Skipping timeline-ads: Incompatible with com.google.android.youtube. This patch is only compatible with com.twitter.android
WARNING: Skipping general-reddit-ads: Incompatible with com.google.android.youtube. This patch is only compatible with com.reddit.frontpage
WARNING: Skipping minimized-playback-music: Incompatible with com.google.android.youtube. This patch is only compatible with com.google.android.apps.youtube.music
WARNING: Skipping tasteBuilder-remover: Incompatible with com.google.android.youtube. This patch is only compatible with com.google.android.apps.youtube.music
WARNING: Skipping hide-get-premium: Incompatible with com.google.android.youtube. This patch is only compatible with com.google.android.apps.youtube.music
INFO: Skipping compact-header: Not explicitly included
WARNING: Skipping upgrade-button-remover: Incompatible with com.google.android.youtube. This patch is only compatible with com.google.android.apps.youtube.music
WARNING: Skipping background-play: Incompatible with com.google.android.youtube. This patch is only compatible with com.google.android.apps.youtube.music
WARNING: Skipping music-microg-support: Incompatible with com.google.android.youtube. This patch is only compatible with com.google.android.apps.youtube.music
WARNING: Skipping music-video-ads: Incompatible with com.google.android.youtube. This patch is only compatible with com.google.android.apps.youtube.music
WARNING: Skipping codecs-unlock: Incompatible with com.google.android.youtube. This patch is only compatible with com.google.android.apps.youtube.music
WARNING: Skipping exclusive-audio-playback: Incompatible with com.google.android.youtube. This patch is only compatible with com.google.android.apps.youtube.music
WARNING: Skipping promo-code-unlock: Incompatible with com.google.android.youtube. This patch is only compatible with de.dwd.warnapp
INFO: Skipping enable-debugging: Not explicitly included
INFO: swipe-controls succeeded
INFO: seekbar-tapping succeeded
INFO: minimized-playback succeeded
INFO: amoled succeeded
INFO: disable-create-button succeeded
INFO: hide-cast-button succeeded
INFO: return-youtube-dislike succeeded
INFO: hide-autoplay-button succeeded
INFO: premium-heading succeeded
INFO: custom-branding succeeded
INFO: disable-fullscreen-panels succeeded
INFO: old-quality-layout succeeded
INFO: hide-shorts-button succeeded
INFO: hide-watermark succeeded
INFO: sponsorblock succeeded
INFO: enable-wide-searchbar succeeded
INFO: custom-video-buffer succeeded
INFO: always-autorepeat succeeded
INFO: microg-support succeeded
INFO: settings succeeded
INFO: custom-playback-speed succeeded
INFO: hdr-auto-brightness succeeded
INFO: remember-video-quality succeeded
INFO: video-ads succeeded
INFO: general-ads succeeded
INFO: hide-infocard-suggestions succeeded
INFO: Compiling resources
INFO: Writing modified dex files
INFO: Writing dex file classes4.dex
INFO: Writing dex file classes.dex
INFO: Writing dex file classes3.dex
INFO: Writing dex file classes2.dex
INFO: Writing dex file classes5.dex
INFO: Writing dex file classes8.dex
INFO: Writing dex file classes7.dex
INFO: Writing dex file classes6.dex
INFO: Writing resources...
INFO: Aligning revanced_raw.apk to revanced_aligned.apk
INFO: Signing revanced_aligned.apk to revanced_signed.apk
INFO: Copying revanced_signed.apk to revanced.apk
INFO: Cleaned up cache directory
INFO: Installing without mounting
INFO: Finished
```

![Patch Berhasil](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgJ0F9Hf8L4gbogu2ghQfL_1w2UHNhhIqgVm1e4AYGJwTz8-ZnlOgGu4Iei_qpmxChRtEd0CCXde9Fe86jBWqmFad9ULWDIRAdXJYoGJ_0e6xbQaMikcvEsG9I2n5UAGKemTNj5nyLhG2n4RACCCdW6cc14sNEYBX52Qk2ljPXgvubqb9iL2bnMiz7UlRae/s0-rw/rmdhnreza.my.id.revanced.6.jpg)

{{< /spoiler >}}

{{% adsense %}}

6. `YouTube ReVanced` berhasil terinstall dan untuk `Micro-G` nya bisa menggunakan `Vanced Micro-G`

1             |  2
:-------------------------:|:-------------------------:
![YouTube ReVanced](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgW2tDE5qMimxgHJtCT-WMkBBKNZp-Pw3q2c-DYOmQF_hIfm5WEKOLCOX9JS_LXvwuYATDtQCsdfzR71SGs-kaPbEVdKS0YUWVKHwkz4PdwpuUhoXmN9X2N2GnHsxNBFlQNOY9WIUsLq-aVckrCB4SPlj8vqTnayo5lDVTBBD7myFkzZ5ceCBXk6vN-PqZ0/s0-rw/rmdhnreza.my.id.revanced.7.jpg) | ![YouTube ReVanced](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhdgICnrYGLHRL1a-Fpardk7tCWAbcyLQ73JnWg8bZW6avI7WwWEmKlchkxYsi9R-emm3xviTQ1qioBY3VqDfflI_83kmjb0axcWO-bY9muP_kZuYD9X_73rwT4ZRWVsJIBjqb6lNzUCxUftt6kEe1ArUAevj6W5dI7jF8uhIoUMGCUiv61FL_gOsZMIw6V/s0-rw/rmdhnreza.my.id.revanced.8.jpg)
