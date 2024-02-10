---
title: "Mount Google Drive di Linux dengan Google Drive Ocamlfuse"
date: 2021-03-13T16:33:19+07:00
description: "Google Drive OCamlFUSE memungkinkan kalian memasang Google Drive di Linux, tanpa ketergantungan pada desktop envir mana pun."
categories: ["Google Drive", "Tutorial"]
tags: ["Google Drive", "Tutorial"]
description: 'Menurut deskripsi resminya, google-drive-ocamlfuse adalah sistem file FUSE (Filesystem in Userspace) untuk Google Drive yang ditulis menggunakan bahasa pemrograman Ocaml.'
summary: 'Menurut deskripsi resminya, google-drive-ocamlfuse adalah sistem file FUSE (Filesystem in Userspace) untuk Google Drive yang ditulis menggunakan bahasa pemrograman Ocaml.'
image: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhwt-aIrDfkicVex80qrbDItqFfgyBTs2wC8x83xh6zK4tHZo1DNzL78bDUJpSn3HvlHnhbzQ01IsYCqkqYqiv_BSsdZvTqYWmKPJpbC8cwPreQ7ryVzxBU1LJev9XvWudfSxA_2GFvDAmuyF-JX9jKJJ0XBCLNJ4XqZFMi2WrfBmWjJHXepFRghbbM2eF4/s80-rw/Google_Drive_logo.png
ThumbSchema: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhwt-aIrDfkicVex80qrbDItqFfgyBTs2wC8x83xh6zK4tHZo1DNzL78bDUJpSn3HvlHnhbzQ01IsYCqkqYqiv_BSsdZvTqYWmKPJpbC8cwPreQ7ryVzxBU1LJev9XvWudfSxA_2GFvDAmuyF-JX9jKJJ0XBCLNJ4XqZFMi2WrfBmWjJHXepFRghbbM2eF4/s0-rw/Google_Drive_logo.png
---

{{% adsense %}}

Menurut deskripsi resminya, google-drive-ocamlfuse adalah sistem file FUSE (Filesystem in Userspace) untuk Google Drive yang ditulis menggunakan bahasa pemrograman Ocaml. Dengan menggunakan *software* ini, Kalian dapat memasang Google Drive pada sistem linux kalian dan mengaksesnya seperti direktori biasa. Setiap perubahan yang dibuat akan disinkronkan secara otomatis.

Fitur Google Drive Ocamlfuse:
* Full read/write access to ordinary files and folders
* Read-only access to Google Docs, Sheets, and Slides (exported to configurable formats)
* Multiple account support
* Duplicate file handling
* Access to trash (.Trash directory)
* Unix permissions and ownership
* Symbolic links
* Read-ahead buffers when streaming
* Accessing content shared with you (requires configuration)
* Team Drive Support
* Service Account Support
* OAuth2 for Devices Support

Disini saya menggunakan Ubuntu 18.04, tapi untuk sistem operasi berbasis Linux lainnya sama saja.

{{% adsense %}}

1. Installasi di Sistem Operasi
   * Ubuntu kalian harus add ppa terlebih dahulu
```bash
sudo add-apt-repository ppa:alessandro-strada/ppa -y && sudo apt install google-drive-ocamlfuse
```
   * Arch Linux kalian bisa menggunakan yay
```bash
yay -S google-drive-ocamlfuse
```

![Install google-drive-ocamlfuse](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEh-xoRgk4BcZ01HMyCOS8lsBv0zrjKvRWVA8jh1U_sOzsgQoO6NbmSHDwk14wyWJBFSN5WGDD9krHHxAfTKP3v012wkRdhvT7C6UULJ-5QmXHoZ3_HoLVYqe03LBQP1xz6dMSmZ_AwltMxnN_dlmLIl4dxNq0UFs4WIFpWbdYUnSX1fs6PZOsWOVzzkme8F/s0-rw/google-drive-ocamlfuse-0.jpeg)

2. Setelah berhasil terinstall kalian jalankan perintah berikut ini terlebih dahulu (wajib)
```bash
google-drive-ocamlfuse
```

![Perintah google-drive-ocamlfuse](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhgG1v6snxFnqbeTPk_UQdW8LbpDu3tMpryVZ1TqmjdchNkrn4IeAlBwSVqfL8Aec5Yn7a91HDiHaL86w9iTqxm1VcNaANfkXu8E3DWdCDSwvy9KZL6wrck15nFrOzKQbXBrJKptNoGtrM0KNuG-CWgbP6VJ3B63cpN58tmc8MuOcRbJmfjAMWIRWZNi06W/s0-rw/google-drive-ocamlfuse-1.jpeg)

3. Maka akan otomatis membuka browser, kalian log in menggunakan akun Google kalian

![Login dengan akun google kalian](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhdnS-IjNChx5sBsbO7AOz2QrCb1TabvguYoquvSa3HpjDFY8ssNj5f5NQwVa4thMtB23Io88ACTLlx552LlauhHkqK-ci_cMiPNcPyOkvw0KWtXGsN3Oo2l-0zGFw9KXeJiFnIYTJbM6ZRpNTPhn5NARbHhd0PbkhF6hHBXhW-PiHSjHI93V7L8oolCzic/s0-rw/google-drive-ocamlfuse-2.jpeg)

{{% adsense %}}

4. Tunggu beberapa saat sampai di terminal tertulis `Access token retrieved correctly.`

![Mendapatkan Akses Token (otomatis)](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjou011IybR1aOXoDgJeL4PueJlQiXKDj9HTf9v4HjYdDy5AOabSz-VlD3cNQipgXDB8u0F8UQjAqY4jU8DGv82FL3wcB1OctpvrAHILujsHA0VkMcltVVr42dv2u6yNYieMXilQooWTHz4e8GpxZimjEHsLYNJFLBM6qx36N9d3WvJcw1PQPX9G2Kfr696/s0-rw/google-drive-ocamlfuse-3.jpeg) | ![Access token retrieved correctly.](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhrpoAFzcrieWHv-kIP5aofcfN2HxDF1u_37ufXNj0coiCiAYWK8cE5QXcBvWXolKcUojfRsaFt0pW97p-4_l2eMPVqe6hJBovPoONqqkLM5xbi4UW4OPmgoHfTWNeqcLfk2Ka-Qx4u730FakIWMdKw46N-ZL7KiPo6-B3kP7uLdoBXyZCEyj9WK0xdw3XK/s0-rw/google-drive-ocamlfuse-4.jpeg)

5. Buat folder di *home directory* untuk *mount* Google Drive nya, bebas dengan nama apapun, disini saya menggunakan nama **GoogleDrive**
```bash
mkdir $HOME/GoogleDrive
```
6. Kita beri tahu google-drive-ocamlfuse untuk memasang Google Drive di Folder yang telah kita buat tadi di langkah 5
```bash
google-drive-ocamlfuse $HOME/GoogleDrive
```

![mount google-drive-ocamlfuse](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhBPAvgBzLIRLfusjFXqq2VzOkBXsmOwUypNgAkUJKCf7h5N9IiHD9e-Hg_Uo4zOdQcV9otNpaqEe6DS4UMYVHQm5DwT55yRekYhrA4kMV6vs0uCVoS-pkIgOptB9MOLCCBtH4Prnm9v2tjND9zI2IadoybkKD7bXFfdNOnJYZGm92aW7X6vVytlwJRnMb1/s0-rw/google-drive-ocamlfuse-5.jpeg)

7. Cek jika *mount* sudah berhasil
```bash
df -h
```

![mount google-drive-ocamlfuse](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEik4DSsNCqdiEcTFR8YXpe-Dd4IuEoCsEvuZ9D1oPbHIS5tu9gJkPv1lyx5XwNkbeTh8n56TKhnrNyss4r9pw42NtQRng2DFC7FyteUkCafvX5Sq8yz4hUcKrfed-LUnp4WliPjE-lwa8ERU97TBNVvJuIAWRiLdTGoC3NDL9tmEKfpFXT3rvtY4j4WUwQk/s0-rw/google-drive-ocamlfuse-9.jpeg) | ![mount google-drive-ocamlfuse](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjogcdWhmZty_Y5yaIicmxLnPOlUy0Ht1wyQEGuWz7iGbUkK6maWx0M1X1l7aIoR27cupGS2zFFIci4bB_wrKbJmIySg0QnDhd7LBjdsVjOeZFMHyd9IbLr2tQZJoamKadvHFYfk-tNIkpR7tpocSqkp8-J5bNxyMBvTulsAzmcVtZ4k9Dzst9o6lpyJ7OX/s0-rw/google-drive-ocamlfuse-6.jpeg)

8. Jika kalian ingin upload file ke Google Drive, kalian tinggal copy-paste saja file nya ke folder GoogleDrive nya, maka akan otomatis **sync**, disini saya copy-paste **apps.deb**

![Upload ke Google Drive](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgeLcAqq4-PkJZjG9HIYkGsqY6fIfoMnNbfzkSKAl7cWfff7sdrCKq1umTI0GnvFfv3gWdr5sU4XXId_d2ur-8EtcPMd1rTnZGH9kgKX_F9aGN2b1EnTBK68jqzspamifmf4ly-n4D3SFCNPLRzvLcJHeAz_VoSrqAwl8yJprme71qBj87dYY3vbauGx8-o/s0-rw/google-drive-ocamlfuse-7.jpeg) | ![Sync Google Drive](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEg20rRLv6Kuqrjl8ob_FIyRt2vDRMVnqK9WNWouPXlNxsMZSoVJBJhHIgXmnl7mFuPLxz1Tt5IjqJzZ9NRmgRVjdQERHYMnMNkwTjcN4ALGGzXaIsDbhWhHmPlxCWtMts6sB_FEGX0jqI5j3mWlKtVLv37VLpRCA0Y0SSMSJOBDHwL_5hXU-XVLhbfjGOsG/s0-rw/google-drive-ocamlfuse-8.jpeg)

Untuk lebih lengkapnya tentang google-drive-ocamlfuse ini kalian bisa langsung lihat di [documentation](https://github.com/astrada/google-drive-ocamlfuse/wiki) nya yang ada di github\
google-drive-ocamlfuse juga bisa dipakai untuk Team Drive, jika kalian ingin *mount* Shared drives kalian.

{{% adsense %}}
