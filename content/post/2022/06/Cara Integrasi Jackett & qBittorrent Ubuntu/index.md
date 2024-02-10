---
title: 'Tutorial Pasang Search Indexer Jackett & qBittorrent Ubuntu'
date: 2022-06-18T11:30:13+07:00
description: 'Tutorial Pasang Search Indexer Jackett & qBittorrent Ubuntu'
categories: ['Linux', 'Tutorial']
tags: ['Linux', 'Tutorial']
keywords:
  [
    'Tutorial Pasang Search Indexer Jackett & qBittorrent Ubuntu',
    'Install Indexer Jackett & qBittorrent Ubuntu',
    'Cara Install Indexer Jackett & qBittorrent Ubuntu',
    'Cara Memasang Indexer Jackett & qBittorrent Ubuntu',
  ]
description: '*Jackket adalah plugin search index untuk mencari file torrent yang support banyak tracker mulai dari private, semi-private dan public tracker.'
summary: 'Jackket adalah plugin search index untuk mencari file torrent yang support banyak tracker mulai dari private, semi-private dan public tracker.'
image: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhQdnh9S46i3M4Z9Rw5uJA58ey9da_-UXswcmNknr7laOhQysVC-yGf7lSsSOpkWET2F1kGBWNkGq3jWZnTFWQ3FHWb4PHZY-eBOX46c5i4djFoaZemZSi8wR6-zROc_MwdgntOo7CZtRs5JqLlmunKkntrvAS4T1shqynIGs_ApnrfI9X5yAqHEuHG5zmM/s80-rw/jackett-logo.png
ThumbSchema: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhQdnh9S46i3M4Z9Rw5uJA58ey9da_-UXswcmNknr7laOhQysVC-yGf7lSsSOpkWET2F1kGBWNkGq3jWZnTFWQ3FHWb4PHZY-eBOX46c5i4djFoaZemZSi8wR6-zROc_MwdgntOo7CZtRs5JqLlmunKkntrvAS4T1shqynIGs_ApnrfI9X5yAqHEuHG5zmM/s0-rw/jackett-logo.png
---

## Jackett
**Jackket** adalah plugin *search index* untuk mencari file torrent yang support banyak tracker mulai dari private, semi-private dan public tracker.

Jika kita memakai plugin **Jackett**, kita tidak perlu repot-repot membuka situs torrent untuk mencari file nya, kita cukup search saja di torrent client nya, dalam hal ini qBitorrent.

## Install Runtime .NET
Untuk menginstall Jackett di sistem operasi berbasis Linux, kita perlu menginstall **runtime .NET**
1. Download **runtime .NET** nya terlebih dahulu di situs resminya [docs.microsoft.com/en-us/dotnet/core/install/linux](https://docs.microsoft.com/en-us/dotnet/core/install/linux)
2. Pilih Distro kalian (disini saya memakai Ubuntu 18.04, jadi saya pilih Ubuntu)
3. Install **runtime .NET** nya sesuai dengan operasi yang kalian pakai

![Install Runtime .NET](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjvUcijTcIjqSJpSBpOtnHCrK_p1XrYJi-az4FsGLmiSAeCtZ9KFIM_M9Jr3YVa9Fz9XtRnOGLxkT63GnvpJ2FX-m5lhYVciJAKxHgKP-MK4tceuUP7p0zat5uUk6DIfRQIxCRfHqASbUi98-vjbt3iLQ-LxW_u1A0whl5GDv02xgfJKZ1IexwISHn6LTQw/s1600/rmdhnreza.my.id.install.jackett.qbitorrent.1.jpg)

## Install Jackett
1. Download Jackett terbaru di github release nya [Jackett/Jackett/releases](https://github.com/Jackett/Jackett/releases/)
2. Untuk Linux download **Jackett.Binaries.LinuxAMDx64.tar.gz**

![Jackett.Binaries.LinuxAMDx64.tar.gz](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEi8OcPMaiR7MeWqtM_CHcHjlTkiArkqzvZFhTEo13e2e6_zet0GC0C_ojggWMXKlO3P-UnQ9CtlgvyACeausJpGTbb5iVbwJ1ZMiKqMStYVhtmPWz4g_wKgy-ZUYZjJHsVzmqkoc6vlAetK-GcmQ7KVsbrXRQVkC9WjDKFvfU9u11RxprsFDH1WR1EKK4Z3/s1600/rmdhnreza.my.id.install.jackett.qbitorrent.2.jpg)

3. Extract file **Jackett** nya dengan perintah

```fish
tar xf Jackett.Binaries.LinuxAMDx64.tar.gz
```

![Extract Jackett](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiNc56gDaOyq0sNYNKVZ0kP2qdn6RrQoNrXEyc9BKCaoCDSK3jF9NiULFhyZkpv9alf5PYy3UF8GXwH6zJGAC6LRtDt-EuswDOXbrh2ZRny9hBcQzqFQGEBdQguJbA99TQE63qGXGUXKBVS5u66MnHtWJWEoFDMu97jQAt25kEPQBTc1bRyJeuARx7lJnwK/s1600/rmdhnreza.my.id.install.jackett.qbitorrent.3.jpg)

4. Masuk ke directory **Jackett** nya

```fish
cd Jackett
```

5. Jalankan **Jackett** nya

```fish
./Jackett
```

1             |  2
:-------------------------:|:-------------------------:
![Jackett Directory](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjQxGcdUP-Ov6rtAvPZtxfzZ4fIc9anxPPvor1MwDFjGSS2CURzJ6pox7FKjz4Yz3dOZ6uIU_K-g7LlSaBtiF0KV87CGWZU3XN3BySEWSYRro_hwjj8tNlOeeMNw4Fc9M0J5JH5jaQ7lAJaPrOU_lsVZmptb_oHjcvfbOGoYdLsSS9YfjMNlI5mu-9_OL3t/s1600/rmdhnreza.my.id.install.jackett.qbitorrent.4.jpg) | ![Jalankan Jackett](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEin3Kikvf_Nfa0BW-h9wRyHlyGCAuMS0qwiVot5yHxWESAed_Tlt0kaBB0K_MCR4YFiNPyo1UQyCAZ_M62vsYNo0HTiCFsYRm_Ji11D8hyphenhypheniUJoju_W2SzLacxMfq7noSJVtBXz8p9kkXUXTBvI-_1x6K-dWzMcc0uj7Hwy5f9mt-kiWZUJKXRekaTw9xzEy/s1600/rmdhnreza.my.id.install.jackett.qbitorrent.5.jpg)

6. Jika berhasil kita bisa mengunjungi halaman **127.0.0.1:9117** atau **localhost:9117**

![Tampilan Jackett](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEi0EsEXCAhySeNwVrOCHJgeGtsSJdTq17dfiiNQHbR3VNwWd1YlPVAerqxB3_LBU3kr2NgpOX4KKmWt8cwS0jBjE44foAXZXGCgNoEEYzpeL3xgNQGhmpTkDYyRdq46MRztcVIZouhKtIQjixxdPCb6xMO7eGRHhAysRqNYo8riZdeQMiMqYr1UeEEe1bYH/s1600/rmdhnreza.my.id.install.jackett.qbitorrent.6.jpg)

7. Tambahkan public tracker dengan mengklik **Add Indexer**, disini saya menambahkan situs **1337x** & **rarbg**, kalian juga bisa menambahkan private tracker jika kalian punya akunnya.

1             |  2
:-------------------------:|:-------------------------:
![Tambahkan Indexer](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjbgG8nGG8SVCX_6FiPBI3Ne2zRj727S5NiLSkmwkmeNzNVqv0laz07JSApFHg0rvi0c4yoYpWV1ir0xOE-aJXE16xdmv6TK84igZebJE9iJZ5lv9PBQ9eo8ix_xygwGEtI7WHMMszBtX18Qu9imE27pEz5n4K0Bp8rlNY24vi_DGd9HeIWskkt07vFdgbM/s1600/rmdhnreza.my.id.install.jackett.qbitorrent.7.jpg) | ![1337x & rarbg](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjYakFmQNiOQ9M4f6vgj_rJi_Ryt4XfEBN-k0kcryWIdl1lx9DL1kZPqJlTAGJbQxHfPOF0vCwo5FwZz1gjO24RhMHKcLNkImEalWwcPIXuZtEugjAfDObGmGWsasEcqxZiSxkxfJDAwQ0lVPpMfAwLcnWPSbwoW5t6h-qOuptWtFc9Ii41shVnMTBUOR2-/s1600/rmdhnreza.my.id.install.jackett.qbitorrent.8.jpg)

## Setting qBittorrent
1. Jalankan aplikasi qBittorrent nya
2. **View** dan **ceklis** pada **Enable Search Engine**

![Enable Search Engine](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjQbLQA7BB8OcGxBEl8zHdaDZBA_r-WkvPXe1wV5y5CHhzm29-AcN-mTwPnI3E6V92qXt-YaIY7nLbgI9F-Xgf9nxKPk1wfmaWle444uDuUbkYtuunwhIQcklAPk_Ob-k46vOtagyGTPpt4zNeJ25hRdbD7hAEQP8K1ZOI3ktGVGe5C1Pb7-CEq-fxpOYLQ/s1600/rmdhnreza.my.id.install.jackett.qbitorrent.9.jpg)

3. Masuk ke ***tab Search*** klik pada ***Search Plugin*** dan klik **Check for updates**
4. Disable plugin yang lainnya dengan cara `klik kanan -> Hilangkan ceklis pada Enable` dan hanya sisakan plugin **Jackett** saja yang **Enable**

![Enable Search Engine](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhhG8sXQczvjnJyycnrmqGFHrbVP1otCCiVHoWET6zkmrIEnkI0EOkBzNVnruLW3sylYHKjwCd1yF3e5qTJG1XR_hu-tnaMZVnEW-pn9ZBN77wCGdVEFEH-dZgLoxvptxWBTsDSTcrW-PauW6C9kRKY9xYnKrMkSiQQ_Adn5JPZt6iS3tEjO1wlA6swZP32/s1600/rmdhnreza.my.id.install.jackett.qbitorrent.12.jpg)

5. Masuk ke directory `$HOME/.local/data/qBittorrent/nova3/engines`

![Setting Jackett Plugin](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgpFQl7Yv34Hwr0EcPdnyhdDQ33lrPscwXnUWbF4sC6xQkCXruFODmaw59AEJW1NGj1Q3TU-5azTvBzuK4CLQ-sOYMMxdOVe-sqaCk0iuq-cZsm2n4kRbCIjUvipAlW284cezvX2ZJV6GC7B1fBw1Vb_INE-qu4MEUda7pV55Hhkv5WmfnLL9wrZQ_y24nq/s1600/rmdhnreza.my.id.install.jackett.qbitorrent.10.jpg)

6. Buat file dengan nama `jackett.json` dan isi dengan baris berikut\
   Catatan: **API_KEY** bisa kalian dapatkan di dashboard **Jackett** nya

```json
{
    "api_key": "API_KEY",
    "tracker_first": false,
    "url": "http://127.0.0.1:9117"
}
```

![Setting Jackett Plugin](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhG8q9I1RcbuS_NvyUKB8_Y0PnZxanG5K5oG6VCZ1d-nQnSmh_uSu0j8Tds9VhU3zjAmapP9tLQhGvPGKZ-L5aJFeVUkEMWj9qONq6Rxz0fy9L84SPNXlPekKYLqCUGvwNXqhj81RoBT-PPzXoAhqNIyH6bhN9sip6ObMIfc7WmU83GG5ZpugQyt1B6zpHu/s1600/rmdhnreza.my.id.install.jackett.qbitorrent.11.jpg)

## Search File Torrent
1. Kalian cukup cari torrent yang akan kalian download, disini saya contoh nya akan men-download film **Spiderman**
2. Untuk mendownload cukup klik 2x pada file yang akan di download, maka nanti akan otomatis masuk ke tab transfer dan men-download nya.

1             |  2
:-------------------------:|:-------------------------:
![Download Torrent](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgMPSJYjFs8eQPYmxHEP_Jv0_dCc5rQ_C0lqQ-aRR_ioOOaC9BnuH31wNmYOVuSNvYxL2DifX4LGvLk5l3kcD4llViWo-bacf2E5z-GnTs3_-8yC3KWGXQYQFubysF7IPhML9UWBkONxw6NtsUjnPCW72o_BMVBZoD5E3dJTtN4TnR7uA8FJA_PHY45jZzK/s1600/rmdhnreza.my.id.install.jackett.qbitorrent.13.jpg) | ![Download Torrent](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiJU8dVfAbGOtxoRL1OB9clghXGClC77OB8iEX_bpAsCAJFOAuFnB2yiKIBbu4YSco3tsjZvBhOBLoRj7r1rmw10Cw3-QIpBx-LS2UUHhFqbXK_WPlX4zqNOLUgFTWZAsUE1giQlSrN7ztHHLq46277L5KZGwUXu3UnWay6yen0Zh7a2huIAQ8aLuVkIwEH/s1600/rmdhnreza.my.id.install.jackett.qbitorrent.14.jpg)

## Install Jackett sebagai Service

Untuk menginstall Jackett sebagai service
1. Masuk ke directory Jackett nya
2. Jalankan

```fish
sudo ./install_service_systemd.sh
```

3. Jackett akan otomatis aktif saat booting, untuk stop Jackett kita bisa menggunakan perintah

```fish
sudo systemctl stop jackett
```

{{% adsense %}}
