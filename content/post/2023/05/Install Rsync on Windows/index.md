---
title: 'Install Rsync Windows 10/11'
url: "install-rsync-on-windows-10-11"
date: 2023-05-18T00:00:00+07:00
description: 'Tutorial Install Rsync Windows 10/11'
categories: ['Tutorial', 'Windows']
tags: ['Tutorial', 'Windows']
keywords:
  [
    'Install Rsync Windows 10/11',
    'Tutorial Install Rsync Windows 10/11',
    'Cara Install Rsync Windows 10/11',
    'How to Install Rsync on Windows 10/11',
  ]
description: 'Rsync is a utility for efficiently transferring and synchronizing files between a computer and a storage drive and across networked computers by comparing the modification times and sizes of files'
summary: 'Rsync is a utility for efficiently transferring and synchronizing files between a computer and a storage drive and across networked computers by comparing the modification times and sizes of files'
image: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEga3v9Wyvky-hWIl8pvbG6o3DKmIDuGG4Nm1eIT-QtgPDozU_cdv_2b0XUIhkA3fOVXEPO11k036UKEeuP3m4rSGCTfGhptDOSTVPBQ97WsL74MtlB4VapWDg9b7pJ28Hz7JSyOnFq8qJElZ-_jkySiAfk4ct6wumIUpiVomgRnuJhyAd29_mI-nVexnbWS/s80-rw/rsync-logo.jpg
ThumbSchema: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEga3v9Wyvky-hWIl8pvbG6o3DKmIDuGG4Nm1eIT-QtgPDozU_cdv_2b0XUIhkA3fOVXEPO11k036UKEeuP3m4rSGCTfGhptDOSTVPBQ97WsL74MtlB4VapWDg9b7pJ28Hz7JSyOnFq8qJElZ-_jkySiAfk4ct6wumIUpiVomgRnuJhyAd29_mI-nVexnbWS/s0-rw/rsync-logo.jpg
---

{{% adsense %}}

Rsync is a utility for efficiently transferring and synchronizing files between a computer and a storage drive and across networked computers by comparing the modification times and sizes of files. It is commonly found on Unix-like operating systems and is under the GPL-3.0-or-later license.

Since we're using the Windows operating system, we need another tool called `Git for Windows`. Git GUI using `bash shell` by default, but before that, we need to add a repository first and in this tutorial we can use MSYS2 repository, install pacman (Arch default package manager) and install `rsync` with pacman.

## Install Git for Windows
1. Install [Git for Windows](https://git-scm.com/download/win) according to the operating system you are using whether 32/64 bit, if you are using [scoop](https://rmdhnreza.my.id/cara-menginstall-package-manager-scoop-di-windows-10/), you can use command.
```powershell
scoop install git
```
## Install Pacman
2. Download [pacman](https://packages.msys2.org/package/pacman?repo=msys), [pacman-mirrors](https://packages.msys2.org/package/pacman-mirrors?repo=msys), [msys2-keyring](https://packages.msys2.org/package/msys2-keyring?repo=msys) & [gcc-libs](https://packages.msys2.org/package/gcc-libs?repo=msys&variant=x86_64) from the MSYS2 website.
![Figure 1](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgWCXcmTxr2Fm29J0hLRKsCZcsgjEoV4H-Gq2830HCefcKeo2FG4AFSMW7pIAct0IG14-cAk58oMtjS80QDfAIKl08gmWCHyZZWm4fxYMm-QPVbUr-JD85RCh6o2SrYl42SNH3kT7iat9OMTzfb0ePgeLTex79F4Qrxx8CXAKx85ipXs-8l5bfzh0u2S87r/s1600/rmdhnreza.my.id.rsync.windows.1.jpg)


3. The files are in `zst` format. To *extract* to tar format, you can use [Windows version of zstd](https://github.com/facebook/zstd/releases), for users who use [scoop](https://rmdhnreza.my.id/cara-menginstall-package-manager-scoop-di-windows-10/) You can use the command `scoop install zstd` for installing [zstd](https://github.com/facebook/zstd/releases).
Once the [zstd](https://github.com/facebook/zstd/releases) is installed, run the following command from git GUI/PowerShell `zstd -d *.zst` after successfully *extract* will appear 4 new files with tar format

1             |  2
:-------------------------:|:-------------------------:
![Figure 2](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgYIZsLvOSh8pOaGjnM7clalGL99nyukcn9x3uQ7vdIg0YmbqsQGovtgwmU8BFRCChdesYFLtKVDOrvtUHf_wNTFUaW0hAefQrwVOK6y1uOqghG94PFPewELMhYhhfJ-hK_zOncXc_GTliQz7i-TXtrv5Q6aJo9iqKn7Mgj4_R3YquhwXHWbfr5ZIzca9Nq/s1600/rmdhnreza.my.id.rsync.windows.2.jpg) | ![Figure 3](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgYm7ApPxD6UWZx47yaOjBvEHcjRDwgCkcxGfjloNCvaTMoCv4CRv0q2izZAIzjrGfUC7t8dOjeg3kJL-LKfs9tcqSSHBeekfw_WBQai4ocQorXrGsGhfhpRWZmK38UAcpl_x50Ky7v0K6nBNNaWOezU3TsVodNPdgtFRV7bFw89ET4vaUc-w-PF7HsetZK/s1600/rmdhnreza.my.id.rsync.windows.3.jpg)


![Figure 4](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgIsC5gM_lKDNg2gLgRJQ5UjTsrSLHZaWEenPRjv8J4OHN4wB36DVKEQf1zU2JaQ-NahZDV_EBWnA5-NKU5UORLIzXLLVj6CbeCjwSKO_uKL3mxPRQ1x6qYlemsfWwusX6WR27voDfeRNCpHbbGbVe410GyKgwS5p5JY3ENNbiYGVn82u9mzBRQhoiY8K1G/s1600/rmdhnreza.my.id.rsync.windows.4.jpg)

4. Now, we open the **Git GUI** and run the command below to *extract* the tar file into the **Git GUI root directory**.


```md
cd /
tar -xvf /D/Downloads/msys2-keyring-1~20230316-1-any.pkg.tar
tar -xvf /D/Downloads/pacman-mirrors-20221016-1-any.pkg.tar
tar -xvf /D/Downloads/pacman-6.0.2-4-x86_64.pkg.tar
tar -xvf /D/Downloads/gcc-libs-11.3.0-3-x86_64.pkg.tar
pacman-key --init
pacman-key --populate msys2
pacman -Syu
```

{{% note %}} Make sure the PATH for the tar file is correct! {{% /note %}}

{{% adsense %}}

5. To synchronize metadata files, you need to run the command below. This step may take a few minutes to complete, depending on your internet speed, too.

```bash
URL=https://github.com/git-for-windows/git-sdk-64/raw/main
cat /etc/package-versions.txt | while read p v; do
  d=/var/lib/pacman/local/$p-$v
  mkdir -p $d
  for f in desc files install mtree; do
    echo "$URL$d/$f" ..... $d/$f
    curl -sSL "$URL$d/$f" -o $d/$f
  done
done
```

![Figure 5](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhxLVZhC4lpH-xFiw43qQROVP4dZ5R0Xm5qtmCe_cEZMyTbnHw23rjg3QN672d7Xwg-BWD0AFVoL3A-GP_scnzA5lPj98e_yB0OeLdIFFJqK6ZKbf7duWi4gIQVO1cbqs5-1JmJuNR-abb1mRoLhPaZ91Bv0e7bfMxGOqevM_X9iZIjp2QmQ_32m9UQvkF7/s1600/rmdhnreza.my.id.rsync.windows.5.jpg)

{{% adsense %}}

## Install Rsync

6. Once pacman is installed on **Git Bash**, `rsync` can be installed:

```bash
pacman -S rsync
```

1             |  2
:-------------------------:|:-------------------------:
![Figure 6](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiNi6Hn4EQHg-JtYuduQzcp3TFvFnc0f6WTsTs2B91yMLsPOF1CTxsdvcYwdPDdSJayBqVj3PMSiAJQAevGDozns3SnFhNlyXLLsW7zBtZSHHk3LECMhbQeYEJj89bsW4NBLU1NIFeHfTaYdLmUfnKY0IxhYlBLUJtoSp8XRfr0HSTpXYiQlXR_mLd0VroP/s1600/rmdhnreza.my.id.rsync.windows.7.jpg) | ![Figure 7](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhttkXTiX4AjJQvjRb5lBUCjvTmlDgnZm_pkv4AS22sZ8P86dNuRdOb-3JvOW1_QwNDusdkOzTfsim1z3GD59QOHtc_Govy8MEUzbNzf769Gpg9HofJvumbuytzEdekNlTqWjAA6UkCRrixEACuN_saijIMGjunC4MwT-oITv4AUxs-dKEB6SSY9L46SHMe/s1600/rmdhnreza.my.id.rsync.windows.6.jpg)

7. If everything goes well and works properly, you can use the command `rsync`, The command same as command in the Linux operating system. For example, **if you want to copy a file from drive D to drive Z with progress and stats, you can use these command.**

```bash
rsync -avzh --progress --stats /D/Path/To/File.txt /Z/Path/To/Paste/
```

1             |  2
:-------------------------:|:-------------------------:
![Figure 8](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEigxPKrg5-MA989z4tp9mIWGOzi6CWBYQGJYliAD7zmXHAgrz2dsltm3gvQpazsi7GP75XFvqIaiMoJEyTvkNJpaoLkrXAgn8rQHdIS1Uz2NcP4Zw-FvhY3aFmatZ71IxjI0OWA3Da44hyphenhyphenIw0sJyKfHWwyex0QdKGwB1HaAlRaQfTruRUjP2bAmRGMnzmnD/s1600/rmdhnreza.my.id.rsync.windows.8.jpg) | ![Figure 9](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjDWtsLOsTf1vSNQNy5f2UdRZeTVPJyqJiOcAxx1FfNB9xJGsILB77RzuPgK_jaRALJbt0MeZsagCRztwVeI_WFyjtpbwWyiAwrmCEXKTVhY5u1f3NxM3DQvUenmtmqgAYBbDCzSIqL-I4jC89E7Q6tRImLH1K7n_GJbYs4_Q_0h28K9eeHxacA0vmYcEN8/s1600/rmdhnreza.my.id.rsync.windows.9.jpg)

## Source

1. [https://gist.github.com/rafaelpadovezi/](https://gist.github.com/rafaelpadovezi/1cfc1026f78255458f5a2ea56291ed23)
2. [https://gist.github.com/rafaelpadovezi/#gistcomment-4325219](https://gist.github.com/rafaelpadovezi/1cfc1026f78255458f5a2ea56291ed23?permalink_comment_id=4325219#gistcomment-4325219)
