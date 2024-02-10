---
title: 'GitHub remove blinking cursor'
url: "github-remove-caret-blinking-cursor"
date: 2024-01-31T00:00:00+07:00
description: "GitHub remove blinking cursor"
categories: ['GitHub', 'Tutorial', 'Linux']
tags: ['GitHub', 'Tutorial', 'Linux']
keywords:
  [
    'GitHub remove blinking cursor',
    'GitHub remove caret cursor',
    'GitHub disable blinking cursor',
    'GitHub disable blinking cursor when viewing code'
  ]
description: 'GitHub remove blinking cursor.'
summary: 'GitHub remove blinking cursor.'
image: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjICTyl0qQlb4JHbR_VCnvHIPxC9P0Y_f0wuHQeTae_A7QoAzrjORIgC_k7tLutRQFVsGiT2Af-HQYbKL7VTcdW06tjxNCPoIAfEIOgG8bZpUlTY6UEUHL-MA4PUYfMbeTkxQNIHO0jK6UP-eMPa4ZB2quoBGyEmci4DkOGc6Pb04Evbzdnp3gSdKIJEcdT/s80-rw/github-logo.png
ThumbSchema: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjICTyl0qQlb4JHbR_VCnvHIPxC9P0Y_f0wuHQeTae_A7QoAzrjORIgC_k7tLutRQFVsGiT2Af-HQYbKL7VTcdW06tjxNCPoIAfEIOgG8bZpUlTY6UEUHL-MA4PUYfMbeTkxQNIHO0jK6UP-eMPa4ZB2quoBGyEmci4DkOGc6Pb04Evbzdnp3gSdKIJEcdT/s0-rw/github-logo.png
---

![Blinking Cursor](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgZwjahguCiik83KKxJ2gSuj1TzIJQr0oiH4UqinuGN1nSQWOl0iQfw5gPxHnqDiWabOjrnTDoiOyqgyofovmt0MrmRrlIz79GDCSsvl1BT90gyIhEr2I1aHZk-oqHNXepluWbfNsZvww3lc0GqgHMItrn2b05uLM_5Ba1Erph_XAxOd6BDIHs80_51glMR/s0-rw/chromium-20240131_003241.png)

(Not) Recently, GitHub updated its UI. Now, when viewing a code file, dragging the mouse to select text, or simply clicking anywhere on the page, a blinking cursor appears, similar to caret browsing in browsers. If you select a code or accidentally click on the code page, you have to find an off-screen area to click before you can use the back/forward buttons. This makes browsing code files quite annoying.

## Disable via GitHub itself

1. Click on the **horizontal dot icon**.
2. Enable `Wrap Lines`, and it's done.

![Enable Wrap Lines](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgqwxOLKVzUdwvX17q7UN1MyDqlxEq3Nk7x8o9J9bbs1ppRcVyropzlqj0gUuvzKAT8rMnnZmSBjPI4mUEyoLBiqxKjPe3m9RWh_rubiQdkqbi6mXdFKyfOoSBaCtmRMg_-lJhwTjfgG0s7-fDsHTijGNwKmmaY7twXKl9boxoSr9DZilS3x1qx0ZmRuOQS/s0-rw/chromium-20240131_004607.png)

3. That useless feature is gone, but you need to enable Wrap Lines every time if you delete cookies from your browsers.


## Using AdBlocker

You can block this useless feature with an AdBlocker such as AdBlock, AdBlock Plus, AdGuard, or uBlock Origin (uBo).
1. Just add this `filter` to your AdBlocker:

```css
github.com##.code-navigation-cursor
```

2. Save it, and it's done.

## Using userstyles

You can disable this useless feature using CSS `userContent.css` in Firefox or Stylus Extensions.

1. Create a new style that only applies to github.com.
2. Paste this line:

```css
.code-navigation-cursor {
  display: none !important;
}
```

3. Save it.