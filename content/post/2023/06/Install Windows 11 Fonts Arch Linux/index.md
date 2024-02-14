---
title: 'Install Windows 11 Fonts Arch Linux'
url: "install-windows-11-fonts-arch-linux"
date: 2023-06-28T00:00:00+07:00
description: "Do you miss using your favorite Windows fonts in Linux? Don't worry, it's easy to install them! In this blog post, I'll show you how to install Windows fonts in Arch Linux."
categories: ['Tutorial', 'Linux']
tags: ['Tutorial', 'Linux']
keywords:
  [
    'install windows 11 fonts arch linux',
    'windows 11 fonts arch linux',
    'how to install windows 11 fonts arch linux',
    'arch linux windows 11 fonts',
    'microsoft fonts arch linux',
    'ttf-ms-win11-autoAUR',
    'install windows fonts linux',
    'install microsoft fonts linux'
  ]
description: 'Install Windows 11 Fonts Arch Linux'
summary: 'Install Windows 11 Fonts Arch Linux'
image: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiB9KmwxElIwG9jVUuI6TGA1yRNWiN5IwL8uNIF3NXhqd--bU-Tetg-f6mDgJ4BOvP7QwzuFUx6TU5shatoDTkS5IlK7jynk7KL96rn0NNNFUikxZwFmreDv1G8J4itLVyXudDHKKPH4VpzA093OOy7v84fkoIX8Le-NnDbi-a-Hh-usyBxuxqvE_RkkfjN/s80-rw/Arch-linux-logo.png
ThumbSchema: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiB9KmwxElIwG9jVUuI6TGA1yRNWiN5IwL8uNIF3NXhqd--bU-Tetg-f6mDgJ4BOvP7QwzuFUx6TU5shatoDTkS5IlK7jynk7KL96rn0NNNFUikxZwFmreDv1G8J4itLVyXudDHKKPH4VpzA093OOy7v84fkoIX8Le-NnDbi-a-Hh-usyBxuxqvE_RkkfjN/s0/Arch-linux-logo.png
---

{{% adsense %}}

In this blog post, I'll show you how to install Windows fonts in Arch Linux using PKGBUILD

## Download Windows 11 Fonts

1. First, you need to download the Windows 11 fonts.
    + https://pomf2.lain.la/f/ozr86mc8.zst
2. After downloading the fonts, extract the files. The format is a `zst` file, which you can extract with `zstd`.

```fish
~ ❱ zstd -d Windows\ 10\ Fonts.tar.zst
~ ❱ tar -xvf Windows\ 10\ Fonts.tar
```

3. Navigate to the font's directory you just extracted and run this command.
```fish
~ ❱ makepkg -si PKGBUILD
```
4. Wait until installation completed.

## Issue
Some Microsoft TTF fonts such as Calibri and Cambria contain embedded bitmap fonts for specific font sizes, which are not anti-aliased. If embedded bitmaps are enabled, the fonts are not anti-aliased at those specific sizes. Embedded bitmap fonts can be disabled in the [Font configuration](https://wiki.archlinux.org/title/Font_configuration):

1. The configuration of the font is located at:
    + `$XDG_CONFIG_HOME/fontconfig/fonts.conf`
    + `/etc/fonts/fonts.conf`
2. You should edit the `fonts.conf` and add this line.

```xml
<?xml version="1.0"?>
<!DOCTYPE fontconfig SYSTEM "fonts.dtd">
<fontconfig>
  <match target="font">
    <edit name="embeddedbitmap" mode="assign">
      <bool>false</bool>
    </edit>
  </match>
</fontconfig>
```
3. Finally, please execute this command `sudo fc-cache -f` after editing `fonts.conf`

## Source

1. ArchWiki: [wiki.archlinux.org/title/Microsoft_fonts](https://wiki.archlinux.org/title/Microsoft_fonts#Disable_embedded_bitmap_fonts)
2. Original PKGBUILD are from AUR: [aur.archlinux.org/packages/ttf-ms-win11](https://aur.archlinux.org/packages/ttf-ms-win11)
