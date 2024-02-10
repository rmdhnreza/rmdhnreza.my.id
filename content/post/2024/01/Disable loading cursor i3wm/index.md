---
title: 'Getting rid loading cursor i3wm'
url: "getting-rid-loading-cursor-i3wm"
date: 2024-01-20T00:00:00+07:00
description: "Getting rid loading cursor i3wm"
categories: ['Tutorial', 'Linux']
tags: ['Tutorial', 'Linux']
keywords:
  [
    'Getting rid loading cursor i3wm',
    'i3wm cursor',
    'i3wm loading cursor',
    'fix i3wm loading cursor'
  ]
description: 'Getting rid loading cursor i3wm Menggunakan PC.'
summary: 'Getting rid loading cursor i3wm Menggunakan PC.'
image: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiTm2PtNd5Nfo61qHzzv5zm4_nQ17cA-msE8KK9uf1VS1zm8MCIOE4i_h3E1MCcJN8PWlA0Gf2duXwbzSIGukSrjpSXxUwUD6eUEh44LoJzqsG-NVrUNeHhBRyqnT36EoDH4LxJO3ydYRg6sUVmmF06Cm6ZJSU7Wtf4w31jjpyG6KyvwOI4zgFcESaZLAkx/s80-rw/i3wm.png
ThumbSchema: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiTm2PtNd5Nfo61qHzzv5zm4_nQ17cA-msE8KK9uf1VS1zm8MCIOE4i_h3E1MCcJN8PWlA0Gf2duXwbzSIGukSrjpSXxUwUD6eUEh44LoJzqsG-NVrUNeHhBRyqnT36EoDH4LxJO3ydYRg6sUVmmF06Cm6ZJSU7Wtf4w31jjpyG6KyvwOI4zgFcESaZLAkx/s0-rw/i3wm.png
---

![Loading Cursor](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEio1GzP4a1y2Nxb08t5CQInHH4cQoBiG3Xfd4D4b5zWDffBhAWzbCVwqmGeYGzwajJUfLAaDWz_xaTZw3ZBRSSr80-hBt4bCx68QAhiXt6ML36aUFOGXcFakpQOPBwcgn0gRqmudLJh5IqNgnRNa5-rqGLM726HR37nbgwwrZ10duPCMvXLU1JWgbs985UJ/s1600/loading-cursor.jpg)

{{% adsense %}}

## Cursor waiting mode
When starting a script or application which does not support startup notifications, the mouse cursor will remain in busy/watch/clock mode for 60 seconds.

## --no-startup-id
To solve this for a particular application, use the `--no-startup-id` parameter, for example:

```fish
exec --no-startup-id ~/script
bindsym $mod+d exec --no-startup-id dmenu_run
```

{{% adsense %}}

## To disable loading cursor animation globally
If the above does not solve the problem, look in `/usr/share/icons/{CURSOR_NAME}/cursors` or `$HOME/.icons/{CURSOR_NAME}/cursors/` and rename or remove the `watch` cursor

```fish
mv watch watch.bak
mv left_ptr_watch left_ptr_watch.bak
ln -s left_ptr watch
ln -s left_ptr left_ptr_watch
```

{{% adsense %}}