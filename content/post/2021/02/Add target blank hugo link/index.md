---
title: "Add target=`_blank` di Hugo Link"
date: 2021-01-09T17:35:36+07:00
description: "Tutorial Add Target='_blank hugo site'"
categories: ["Hugo", "Tutorial"]
tags: ["Hugo", "Tutorial"]
description: 'Mulai versi 0.60 hugo mengganti Content Format nya dari Blackfriday ke Goldmark. Untuk blackfriday kalian bisa setting di config.toml'
summary: 'Mulai versi 0.60 hugo mengganti Content Format nya dari Blackfriday ke Goldmark. Untuk blackfriday kalian bisa setting di config.toml'
image: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgf1oK8J4S3tNRWW330MlC17FhhksTbIfUXE49C6mbc5OQTrkhr290jKKDMwmYNiVHY-RNXhPurj7DCzzXZpw9XnEO36JnkBWIYMjEk7EEexmYw57w5KDiQVs7rFh71xCvHzMvU0wu-haVqmqgwBxnL-Y7v5lXBGASCMKsNfC-__2j6op-H9eKE6-1aSvds/s80-rw/hugo.png
thumbschema: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgf1oK8J4S3tNRWW330MlC17FhhksTbIfUXE49C6mbc5OQTrkhr290jKKDMwmYNiVHY-RNXhPurj7DCzzXZpw9XnEO36JnkBWIYMjEk7EEexmYw57w5KDiQVs7rFh71xCvHzMvU0wu-haVqmqgwBxnL-Y7v5lXBGASCMKsNfC-__2j6op-H9eKE6-1aSvds/s0-rw/hugo.png
---

{{% adsense %}}

Mulai versi 0.60 hugo mengganti *Content Format* nya dari ***Blackfriday*** ke ***Goldmark***. Untuk `blackfriday` kalian bisa setting di `config.toml`
```toml
[blackfriday]
  hrefTargetBlank = true
```
Tetapi di hugo 0.60 sudah tidak bisa melakukan itu, karena sudah menggunakan `Goldmark`, jadi kalian perlu beberapa langkah tambahan untuk menambahkan `target="_blank"` secara default di setiap link hugo website kalian.
## Render Hooks dengan Goldmark
Goldmark dan [Markdown Render Hooks](https://gohugo.io/getting-started/configuration-markup/#markdown-render-hooks) adalah fitur baru di Hugo v0.62.0 jadi pastikan versi Hugo kalian sama atau lebih baru dari versi ini.

{{% adsense %}}

[Markdown Render Hooks](https://gohugo.io/getting-started/configuration-markup/#markdown-render-hooks) menawarkan beberapa cara untuk mengubah *perilaku* *default markdown* , misalnya mengubah ukuran gambar yang diunggah, menambahkan class *lazy* di setiap gambar yang kalian unggah atau membuka link di tab baru.

Untuk membuka setiap link di tab baru kalian harus membuat `render-link.html` di folder `layout/_default/_markup/`
```go
layouts
└── _default
    └── _markup
        └── render-link.html
```
Jika sudah isikan `content html` berikut ini
```html
<a href="{{ .Destination | safeURL }}"{{ with .Title}} title="{{ . }}"{{ end }}{{ if strings.HasPrefix .Destination "https" }} target="_blank"{{ end }}>{{ .Text }}</a>
```
Kalian juga bisa menambahkan `rel="nofollow"`, `rel="ugc"` atau `rel="nofollow noopener"` jadinya seperti ini
```html
<a href="{{ .Destination | safeURL }}"{{ with .Title}} title="{{ . }}"{{ end }}{{ if strings.HasPrefix .Destination "https" }} target="_blank"{{ end }} rel="nofollow noopener">{{ .Text }}</a>
```
Setelah itu kalian save, dan kalian coba dengan membuat link di post kalian dengan format *markdown*
```markdown
[Contoh Link](https://rmdhnreza.my.id)
```
#### [Contoh Link](https://rmdhnreza.my.id) {class="centertext"}

{{% adsense %}}
