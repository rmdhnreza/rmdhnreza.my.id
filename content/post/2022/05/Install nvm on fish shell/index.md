---
title: 'Install NVM on Fish Shell'
date: 2022-05-10T15:30:13+07:00
description: 'Tutorial how to install NVM on fish shell Linux, MacOS'
categories: ['Tutorial']
tags: ['Tutorial']
keywords:
  [
    'Cara install NVM on fish shell',
    'install NVM on fish shell',
    'Tutorial cara install NVM di fish shell',
    'Tutorial install NVM on fish shell',
  ]
description: 'Fish is a smart and user-friendly command line shell for macOS, Linux, and the rest of the family. Fish includes features like syntax highlighting, autosuggest-as-you-type, and fancy tab completions that just work, with no configuration required.'
summary: 'Fish is a smart and user-friendly command line shell for macOS, Linux, and the rest of the family. Fish includes features like syntax highlighting, autosuggest-as-you-type, and fancy tab completions that just work, with no configuration required.'
image: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEisicyW-w1Bv23AhvpAG2W55KaQ7GAAPFZVVxQedvViaQH4h22oCvx6mXIBp3SjVc_ovqKrKD-swXYrRokbt_A0MwxGwjDkLhpaBHt_EyD4p2nbMS2qJjLT54Yv7xkQeXnmTiL7mBrGflRSHQwLBKufrsRFmEg_KTkumd-03DGjYcIIE-3dqd-lTduJjKU5/s80-rw/fish-shell-logo.png
ThumbSchema: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEisicyW-w1Bv23AhvpAG2W55KaQ7GAAPFZVVxQedvViaQH4h22oCvx6mXIBp3SjVc_ovqKrKD-swXYrRokbt_A0MwxGwjDkLhpaBHt_EyD4p2nbMS2qJjLT54Yv7xkQeXnmTiL7mBrGflRSHQwLBKufrsRFmEg_KTkumd-03DGjYcIIE-3dqd-lTduJjKU5/s0-rw/fish-shell-logo.png
---

![Fish Shell](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEj85qJDXuwx57n5TGE-S3knMhdvlO3XMBYd9hMdR3kZnxjj99GP9Ayo0UtZYr0deKhe6tbX_BLofGmaqMiJ7fUORpd8VqafijUlWcmvvRzM6bGWJ052H2F6zEdvxOmqNNFcTshVavpK0Vrwmiigmxq1pcdVwsGnSNLdMjmmhVohzD-EvMoyf1qrZLgjOb4X/s1600/rmdhnreza.my.id.fish.shell.nvm.1.jpg)

## Fish Shell

Fish is a smart and user-friendly command line shell for macOS, Linux, and the rest of the family. Fish includes features like syntax highlighting, autosuggest-as-you-type, and fancy tab completions that just work, with no configuration required.

Fish has "search as you type" automatic suggestions based on history and current directory. This is essentially like Bash's `Ctrl+R` history search, but because it is always on instead of being a separate mode, the user gets continuous feedback while writing the command line, and can select suggestions with the arrow keys, or as in Bash, press `Tab ↹` for a tab completion instead.

Tab-completion is feature-rich, expanding file paths (with wildcards and brace expansion), variables, and many command specific completions. Command-specific completions, including options with descriptions, can to some extent be generated from the commands' manpages.

## Plugin Manager
Fish shell has many plugin managers
  * chips
  * **fisher**
  * fisherman
  * fundle
  * oh-my-fish

But for now, We will use **[Fisher](https://github.com/jorgebucaran/fisher)**, a plugin manager for Fish—the friendly interactive shell. Here some advantage Fisher

{{% adsense %}}

* Manage functions, completions, bindings, and snippets from the command line. Extend your shell capabilities, change the look of your prompt and create repeatable configurations across different systems effortlessly.
* 100% pure-Fish—easy to contribute to or modify.
* Blazing fast concurrent plugin downloads.
* Zero configuration out of the box.
* Oh My Fish! plugin support.

## Install Fisher and NVM
For install NVM on Fish, first we need execute this command
```fish
curl -sL https://raw.githubusercontent.com/jorgebucaran/fisher/main/functions/fisher.fish | source && fisher install jorgebucaran/fisher
```

After that install NVM with this command
```fish
fisher install jorgebucaran/nvm.fish
```
That's it. Fisher and NVM has successfully installed to Fish shell.

![Install Fisher](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEijbFXY4d9XLhhnw5d7mJIC8t-axw3OBx0juFfSj2c1DPdIJdjy9wvgKXDTGc8MuE31XFWvl6pdoXOtqj228yFfpasya_0GoCKeUpVlNvF5oRPjhBiJZuwygovCYV1BhiJ8u5kV5KPYIiTyhdWBbj0FMcSHjI951ARHe6vUY6l0cq9xkCJuAoPrpSyFt5M7/s1600/rmdhnreza.my.id.fish.shell.nvm.2.jpg) | ![Install NVM](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgfsAD1-5QgIVANs1JUkutBnmQJHhv742Fi3XGx1Mzc7CE_Ofp9vqod7eSkt4KtGv6mEmD9o5GuRw38QTAEVcVieTIJeBolbiCGM9i6rSZ0NsbHTW3x6hGxN6nwDf2-2W8XlT8CFHAMPIlTMD5DLrlL5ebhhZ-xg7WUSNKi4C-Ilx-VVVJ0UZPfP4YvHyJ1/s1600/rmdhnreza.my.id.fish.shell.nvm.3.jpg)

Thereafter, We can install node via NVM, for example I install node LTS version.

## Install Node

* Install the latest Node release and activate it.
```fish
nvm install latest
```
* Install the latest LTS (long-term support) Node release.
```fish
nvm install lts
```
![Install node LTS](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjEodQEKoS1yeBzg-pknhyphenhyphen0k4LQLzHRZnDgr0qMCtBrVe-6M2vE48-sOFLdHuDsTl6b_2-BS0sCDDkMwtKgYiJytGgmEwdWIvsSNZ3-sUCEP8QVdRZnPbdxky7Gg2r8C2kVmM1tByhWHCdbcNvGgwrU_EuoiyWdrd-VGLxi7x0GpQCeiiTKXr2OQ8ARtJ4I/s1600/rmdhnreza.my.id.fish.shell.nvm.4.jpg)

{{% adsense %}}

* Install an older LTS release by codename.
```fish
nvm install carbon
```
The `nvm install` command activates the specified Node version only in the current environment. If you want to set the default version for new shells use:
```fish
set --universal nvm_default_version v16.15.0
```
![Make default node version](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEj-Lzi1LfHq6vhsrEgiG2iZU45Y8yJnmsRSuRS67-fdutYDF37kIVFn1BAfgAfwFNFQ72rfx416zKvjA2zUeJnvUaRk0LqLnHZ2q1d7ducknaEY1VZgz2ihRGB2n6xGBa1CqkJJJIP2P5HYAegL1XT8mrgXoREFKTRee8O1KfnsBAYuMgOTiRl3pN87fg5g/s1600/rmdhnreza.my.id.fish.shell.nvm.5.jpg)

## Install NPM Package
```fish
npm install -g npm@latest
```
![Update npm](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhG94j_kJqw1oJ6owh6JFeAIovJkDD59o54fg9tnu_mK6caWJbsYukjIxH6mlW-jY4e6_S2gqbqT39cQ3sxMrfXoiMfwZZE8veMhbc4yJBF2tbqMMw3XOrv2Q4jvP8fKbDj93hiyNnjPUSffcaXkIdxMyz_SKg0OGnNYSnG8-w4PQo-2f18NkgpzJ7Yy1vN/s1600/rmdhnreza.my.id.fish.shell.nvm.6.jpg)

* Example install firebase-tools
```fish
npm install -g firebase-tools
```
![Install firebase-tools](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgukSPHtMLEQgkFI1zOcwDbz-xC5k2quwIbTriLiSWDwDjGsbQb9NuenLt7UvHLPZoojYbWy0qSelSAJkT8ey8ouu9xfDc9T2yg3nvAZzG8enL0UdE1tpaR3Ca53bYbVRYQw51zhU6O2FC_rE_DRTThMHETQ2j_pJPku03cufdBsLwLXqIJwfu1AvGpOr7a/s1600/rmdhnreza.my.id.fish.shell.nvm.8.jpg)

![Version](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgmw5VTMw8McLsJqqGHpwwufkrqVwWPR8aWg16IhidYbK8lVGOVQnRjdadgllhQg4SSiWRTcOm__IzC0xj43K1riRANHTwSKE_SQISffs0EXShG38W-P9hnoqPm9ELEy972NfH-JHc3H0MckGGbSZ-9wIrmqexyuRGeFtV2HAIgySsIg05m-s0-xOkZNqAh/s1600/rmdhnreza.my.id.fish.shell.nvm.7.jpg)
## Removing Plugin
```fish
fisher remove jorgebucaran/nvm.fish
```

