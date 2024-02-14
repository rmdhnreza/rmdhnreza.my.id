---
title: "Cara Install Oh My Zsh di Windows 10"
date: 2021-03-28T00:33:19+07:00
description: "Cara Install Oh My Zsh di Windows 10"
categories: ["Windows", "Tutorial"]
tags: ["Windows", "Tutorial"]
keywords:
  [
    "Oh My Zsh",
    "Oh My Zsh Windows",
    "Git",
    "Bash",
    "Tutorial Install Oh My Zsh di Windows",
  ]
description: 'Pada tutorial kali ini saya akan share cara menginstall Framework Oh My Zsh, untuk Sistem Operasi Windows berbeda dengan Linux & Mac OS karena lumayan banyak tahapan yang harus dilakukan'
summary: 'Pada tutorial kali ini saya akan share cara menginstall Framework Oh My Zsh, untuk Sistem Operasi Windows berbeda dengan Linux & Mac OS karena lumayan banyak tahapan yang harus dilakukan'
image: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgDnhusi233Xo9wYnD3pqaNXXmbN_xDOXnVcWhyXxtVpA1wdsQhIxH5dOxfhiX3lBjtqK1SSxRWrjQCQnF6EuKSjXPIkmxSVfX7RCeR1SDPdN40R8RijL6wxsWB7BS_dbJzFPaQv7E2jdkf8ROiAU9DOg-tGG3uI88yYgurjKwvnDvi2KJy5ImqjSCE1-R8/s80-rw/zsh-logo.jpg
thumbschema: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgDnhusi233Xo9wYnD3pqaNXXmbN_xDOXnVcWhyXxtVpA1wdsQhIxH5dOxfhiX3lBjtqK1SSxRWrjQCQnF6EuKSjXPIkmxSVfX7RCeR1SDPdN40R8RijL6wxsWB7BS_dbJzFPaQv7E2jdkf8ROiAU9DOg-tGG3uI88yYgurjKwvnDvi2KJy5ImqjSCE1-R8/s0/zsh-logo.jpg
---

{{% adsense %}}

Pada tutorial kali ini saya akan share cara menginstall Framework Oh My Zsh, untuk Sistem Operasi Windows berbeda dengan Linux & Mac OS karena lumayan banyak tahapan yang harus dilakukan. Tutorial ini kita akan menggunakan **Git Bash**, jadi langsung saja ke tutorialnya.

1. Install [Git for Windows](https://git-scm.com/download/win) sesuai dengan sistem operasi kalian apakah 32/64 Bit, jika kalian menggunakan [scoop](/cara-menginstall-package-manager-scoop-di-windows-10/), kalian bisa lewati langkah ini.
2. Kalian install Zsh terlebih dahulu, kalian bisa download package nya di [packages.msys2.org/package/zsh?repo=msys&variant=x86_64](https://packages.msys2.org/package/zsh?repo=msys&variant=x86_64), dan kalian download yang filenya yang memiliki _extension_ `zst`

![Zsh](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgNSHNIxmvb8g2CN0ALAqbcPZnmRtP86OhaEbVRitMO3vKc7ckw9el1vcaCesMD6k4opqM3k2EK46oivY8YV7fURI7bayUCmfanq-8J_G0TSzOQkwsvMLAbUsGSFvXBpn43Bd6vMkrQKtFSLjYw8rCnLVQpck-JKI5oYCQnenO9LnUDOyxFdwvvWXCB13EM/s0/1.jpeg)

{{% adsense %}}

3. Kalian Extract file `zst` nya, untuk kalian yang tidak bisa extract file nya, coba kalian install [7-zip-zstd](https://github.com/mcmilk/7-Zip-zstd/releases), untuk kalian yang menggunakan [scoop](/cara-menginstall-package-manager-scoop-di-windows-10/) bisa mengikuti [langkah-langkah ini](https://github.com/lukesampson/scoop/issues/3990#issuecomment-631059255)
4. Extract lagi file **.tar** menggunakan **7-zip**

![Extract Zst File](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEg8Hxfd1LZr8iMNCYns4jFgEXg95PZcGAZVs8TZJOZZrp_jcA3fNXpP7bslU9qbNpp2MKGWYGdOpsXt9clraTiq3Dk59srSiA3eDal9FWVOV_86lSU3a3_kHHx75tVzejZpN6RXoutSO9zrM4jE7oUo0aXGsQW1bI1fS7fU3Y1iiyIzFFtTVDMu1LW1sFeq/s0/2.jpeg) | ![Extract Tar File](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjr-4jfzkGfCjC5rSEDaei3rCuFcN2QxnN37A88wJemizLW2brE_x0w3xDzmpFvEJSgGStH17QkYGzI-N_fCskbEbI16P5RtmApglz5Q426PVCcg1agPtyU2iDEV_ZnrUFArtE_PQc2_gv1toIgUHUPugCF3v1NJaPjSyk78-qHDCbGMO8DS4Uhtb-F5ia6/s0/3.jpeg)

5. Kalian Copy-Paste folder **etc** dan **usr** ke folder Git (C:\Program Files\Git) untuk yang menggunakan scoop (C:\Users\%username%\scoop\apps\git\current)

![Tinggal Copy-Paste Saja ](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhUCYf3htrpHFjt_zuUFyUrsliMJMRaA7X890uecAiVc3JuymISfYnekO3N54hc9SeitfAR-qrnub7fMaFwHHDSvXnJuVZL0GIOooAR0A3X2aeFrmscKmwLxi2m2xSxnnA5tZplb1RTk1AiK4rJ3f1p4_chulFpLPB2SnFnKsOKlDV0gU8793mwl9DNdUhC/s0/4.jpeg)

6. Kalian buka **git-bash.exe** dan jalankan perintah `zsh` Enter

![Git Bash](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhPT5GQXNqnfRGMQSMOBQgFwldfLZn3dSh9rh3B33lXolhJDAiTw23FqTC0CA35WaqInOoQ7gDEQKxvTSDh3qfFJeaRq40uNHaNYMNXe2u7vwE12RwpIGskPCfLAsKuIt6qQGQ-M_I_tPGEOo0tWweGZL1oewhp6lOra5UfQtS6ZdPltPyGCwoTvbxmLijz/s0/0.jpeg) | ![Zsh](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgTOXtJ4E0p2z6reYD0Ye9-KfRnFM7mWW6MeL8y-BrS6lQ8AtHIj5GKVVPV5Xmg17vr8a4QpGvebKmS-bJwNLRrxHQzqSDVmKoSSKfDGNgT5YBa9a6u-o4ePkEGRz_oFWsqLJSiKg5gZhenkdkmHbbYDt1m2ftC_-h_cu8LLK-E56J1gzzLIb8wo9AiKoBM/s0/5.jpeg)

{{% adsense %}}

7. Selanjutnya kita install oh-my-zsh dengan perintah

![Install oh-my-zsh](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiZk71ODiScjEBQoHXjXc0v2LXg_R45kg8L0E-CjXtg69dFG0n_aGoUA4pvPiuDEeQANVtxQQS56wotnhk29EPrnupioqtT7NTu-EwCEyeMD2Po7u0gMbMIoBbpxIB7qbKPu557TGF95lWwd5YHPjOaxLXX2TEa5sPDCrThZPyU-pEAg9UK58bhL_79eAez/s0/6.jpeg)

```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

8. Jika muncul **ERROR: this script obsolete: please see git-completion.zsh** abaikan saja, Kalian buat file `.bashrc` di home directory windows kalian (C:\Users\\%username%\\.bashrc)
9. Isikan baris berikut

```bash
# Launch Zsh
if [ -t 1 ]; then
exec zsh
fi
```

![Zsh](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgnoZQVfsrBq5Ca0Ox6B-T4IyJfavhnCins8MkncRXoYIL7PIC4KY-MRdlGCP2E2HQrboQ_rn7v4XbmRH1EJ6GkGfs9rIhQjmhN7960eJfgFzKQgeC6qjEMN_J1E8ybHEYw3mATtgWi78Lfs0lK20CL3IiTefIIhzf-77pOjEV7vblMggkBJSP6X5lSrsOH/s0/7.jpeg)

10. Jalan git-bash nya sekarang sudah load zsh otomatis.

{{% adsense %}}
