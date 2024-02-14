---
title: "Cara Hapus Semua Log Workflows Hasil Github Actions"
date: 2021-03-14T00:33:19+07:00
description: "Cara Hapus Semua Log Workflows Hasil Github Actions"
categories: ["Github", "Tutorial"]
tags: ["Github", "Tutorial"]
keywords: ["Delete Github Actions","Hapus Semua Github Actions", "Delete Old Workflows Run"]
description: 'Pada kesempatan kali ini saya akan share Cara Hapus Semua Log Workflows Hasil Github Actions'
summary: 'Pada kesempatan kali ini saya akan share Cara Hapus Semua Log Workflows Hasil Github Actions'
image: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjICTyl0qQlb4JHbR_VCnvHIPxC9P0Y_f0wuHQeTae_A7QoAzrjORIgC_k7tLutRQFVsGiT2Af-HQYbKL7VTcdW06tjxNCPoIAfEIOgG8bZpUlTY6UEUHL-MA4PUYfMbeTkxQNIHO0jK6UP-eMPa4ZB2quoBGyEmci4DkOGc6Pb04Evbzdnp3gSdKIJEcdT/s80-rw/github-logo.png
ThumbSchema: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjICTyl0qQlb4JHbR_VCnvHIPxC9P0Y_f0wuHQeTae_A7QoAzrjORIgC_k7tLutRQFVsGiT2Af-HQYbKL7VTcdW06tjxNCPoIAfEIOgG8bZpUlTY6UEUHL-MA4PUYfMbeTkxQNIHO0jK6UP-eMPa4ZB2quoBGyEmci4DkOGc6Pb04Evbzdnp3gSdKIJEcdT/s0/github-logo.png
---

{{% adsense %}}

Pada kesempatan kali ini saya akan share Cara Hapus Semua Log Workflows Hasil Github Actions, seperti ini
![Github Workflows](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgFx7UzlnlGtlgANHMSk_YbXAdNGGoXaUrhkbaciGCwH4g0vL20e-wNyW5Nm5UBGfAnkY7J_7KQ7vjYq2zimxjNVzFYee4y4CHkcADk-YIUW_a1x2tHjheQZ_tAfq7zTWAGSLCAiZMMksA65yQ2fjZdeRK9Bu2_hsVYASyUy9M0MX4wvToOS0iACABm8oVR/s0/gh-actions-1.jpeg)

Disini saya menggunakan Linux Ubuntu, tapi untuk sistem operasi lain sama saja perintahnya, yang berbeda hanya penginstallan gh-cli nya saja, Oke langsung ke tutorialnya.
1. Install **gh-cli jq** dan **findutils** untuk Sistem Operasi
   * Ubuntu gunakan perintah
```bash
sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-key C99B11DEB97541F0
sudo apt-add-repository https://cli.github.com/packages
sudo apt update
sudo apt install gh jq findutils
```
   * Arch Linux gunakan perintah
```bash
sudo pacman -S github-cli jq findutils
```
   * Windows, Untuk sistem operasi Windows gunakan scoop, jika sistem operasi kalian belum terinstall scoop, kalian bisa lihat tutorial nya di [Cara Menginstall Package Manager Scoop Di Windows 10](/cara-menginstall-package-manager-scoop-di-windows-10/). Setelah terinstall scoop gunakan perintah
```powershell
scoop install gh jq findutils
```
![Install github-cli](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhZqfDjEIh3klnr5ws9QRpqV0ogskBz94oM7fEwO3dENMciweWHScFefHoS7DNUEnBhxwJbEZPCUI89oIkfHFolCQ7W2n_oFbXOqdkc0GEzdckPgU1cZEWr3noyyLE3eZvEF8y5dNKF7r88wvi170EZ0t7iq1Pmj04gwcLGJQRaWx5NHbwCDm-oX2KRcuHK/s0/gh-actions-2.jpeg)

{{% adsense %}}

2. Cek github cli nya apakah sudah sukses terintall dengan perintah
```bash
gh --version
```
![Cek gh cli apakah sudah terinstall](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgqtyzCg_jIgXR_7uyGCgUpwTIdIFVrFlAYBqzyZadr8YUppKDpc8QxW1KIgS3j6z0e02OVoiIQSjbIP-ixlv-8R4M5LjDTBu7Wf-m0FBedKhaYA8SAwG4mCnljYx0_zEwNxZgKF2Im7T8Fm_2202V7kOtObnNuhY-F7i8tqOK2d51-i5tTTzt8ZtNXC5w0/s0/gh-actions-3.jpeg)

3. Masukan perintah berikut ini untuk login ke akun github kalian yang akan dihapus log workflows nya
```bash
gh auth login
```
```
   ? What account do you want to log into? -> GitHub.com
   ? What is your preferred protocol for Git operations? -> HTTPS
   ? How would you like to authenticate GitHub CLI? -> Login with a web browser (sangat mudah)
   ? Masukan one-time code nya
   ? Authorize Github
   ? Tekan Enter di terminal
```
![Login akun github menggunakan gh-cli](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgn2sDYQKGxqQhLOTPbabZ_Z2DCY3X0u7fiTaZ_jBySWI-Jn-kFAmjuRiKoXtR_QzUbXx_637BZwNiiWm2tJspPC9Q6bay0sVJvB0J8gngpX7tVmebNuhXk-Tw-VNCLflVYdIJjLf0q90bbiFUsN5hLXvOCQ6MzuwDU4ISANy5ZeDcjP9rIW23mDbpiseYS/s0/gh-actions-4.jpeg)

4. Setelah kalian sukses login, kalian gunakan perintah ini untuk menghapus semua log workflows hasil github actions
```bash
gh api repos/username/namarepo/actions/runs \
| jq -r '.workflow_runs[] | select(.head_branch != "master") | "\(.id)"' \
| xargs -n1 -I % gh api repos/username/namarepo/actions/runs/% -X DELETE --silent
```
**Note:**
   - **username** ganti dengan **username** github kalian !
   - **namarepo** ganti dengan **nama repository** yang akan di hapus log workflows nya !
   - Jika kalian tidak ingin menghapus log workflows di branch `main` ganti `master` dengan `main`, begitupun sebaliknya! Perintah diatas **tidak menghapus** log workflows di branch `master`
![Hapus semua log workflows hasil github actions](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiqFBqY_9iT6qupFRZAKaZe34FrHzYgrFh0xNnsdkJFQdj0VX8h8YOUBlzMHE7l-JDzMdNHkeKVLq9wNitaHPb7-GlP9UhUvg0ct7lG5xWuWoj9QCt5jaFN9QAE6AVniSnRrYmDfINsZ-9r7dYIC84RcJGsqlyF4Wt76aUgVroqq5YykzbLzh8HYyACmhes/s0/gh-actions-5.jpeg)

5. Setelah kalian menjalankan perintahnya cek log workflows nya apakah sudah terhapus atau belum. Jika belum terhapus semua kalian jalankan lagi saja perintahnya sampai semuanya terhapus
![Install github-cli](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhndjyUm67YSIJt9K7EeJ3FmFnzgCqqWrSqGjyT3-b1PyK8K_JG4b3tyGuuJ5HhFtnP3KFiv-MXWP-46c-5Kwxcn_Se93EQGUHx6qLCwaKr3SJl1m_VUJfFj-_Vr3AGlr19YbGlBDr0OjP5_rKQoeaxfuqysqXGtGL2G8EgFwnbgKDHXiw1YL_4e2Z1Upnp/s0/gh-actions-6.jpeg)

{{% adsense %}}
