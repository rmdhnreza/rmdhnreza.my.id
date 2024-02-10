---
title: 'Tutorial how to bulk rename Google Drive files'
date: 2022-05-11T11:30:13+07:00
description: 'Tutorial how to bulk rename Google Drive files'
categories: ['Linux', 'Tutorial']
tags: ['Linux', 'Tutorial']
keywords:
  [
    'Tutorial how to bulk rename Google Drive files',
    'How to bulk rename Google Drive files',
    'Tutorial rename banyak file Google Drive',
  ]
description: "Google Drive is a file storage and synchronization service developed by Google. Launched on April 24, 2012, Google Drive allows users to store files in the cloud (on Google's servers), synchronize files across devices, and share files"
summary: "Google Drive is a file storage and synchronization service developed by Google. Launched on April 24, 2012, Google Drive allows users to store files in the cloud (on Google's servers), synchronize files across devices, and share files"
image: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhwt-aIrDfkicVex80qrbDItqFfgyBTs2wC8x83xh6zK4tHZo1DNzL78bDUJpSn3HvlHnhbzQ01IsYCqkqYqiv_BSsdZvTqYWmKPJpbC8cwPreQ7ryVzxBU1LJev9XvWudfSxA_2GFvDAmuyF-JX9jKJJ0XBCLNJ4XqZFMi2WrfBmWjJHXepFRghbbM2eF4/s80-rw/Google_Drive_logo.png
ThumbSchema: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhwt-aIrDfkicVex80qrbDItqFfgyBTs2wC8x83xh6zK4tHZo1DNzL78bDUJpSn3HvlHnhbzQ01IsYCqkqYqiv_BSsdZvTqYWmKPJpbC8cwPreQ7ryVzxBU1LJev9XvWudfSxA_2GFvDAmuyF-JX9jKJJ0XBCLNJ4XqZFMi2WrfBmWjJHXepFRghbbM2eF4/s0-rw/Google_Drive_logo.png
---

## Google Drive
Google Drive is a file storage and synchronization service developed by Google. Launched on April 24, 2012, Google Drive allows users to store files in the cloud (on Google's servers), synchronize files across devices, and share files. In addition to a web interface, Google Drive offers apps with offline capabilities for Windows and macOS computers, and Android and iOS smartphones and tablets. Google Drive encompasses Google Docs, Google Sheets, and Google Slides, which are a part of the Google Docs Editors office suite that permits collaborative editing of documents, spreadsheets, presentations, drawings, forms, and more. Files created and edited through the Google Docs suite are saved in Google Drive.

## Install Dependencies
First, I'm using Linux Ubuntu, but I think this tutorial will work with other distribution too. This tutorial using Google Drive Ocamlfuse and renameutils, so we install that dependencies first.

{{% adsense %}}

```bash
add-apt-repository ppa:alessandro-strada/ppa -y
apt-get install google-drive-ocamlfuse renameutils
```

## Setting Google Drive Ocamlfuse
After installing Google Drive Ocamlfuse, The first time, you can run `google-drive-ocamlfuse` without parameters:
```bash
google-drive-ocamlfuse
```

This command will create the default application directory `($HOME/.gdfuse/default)`, containing the configuration file config (see the [wiki page](https://github.com/astrada/google-drive-ocamlfuse/wiki/Configuration) for more details about configuration). And it will start a web browser to obtain authorization to access your Google Drive. This will let you modify default configuration before mounting the filesystem.

Then you can choose a local directory to mount your Google Drive `(e.g.: "$HOME/Google Drive")`.

Create the mount point, if it doesn't exists:

```bash
mkdir "$HOME/Google Drive"
```

Then you can mount the filesystem
```bash
google-drive-ocamlfuse "$HOME/Google Drive"
```

If success, you can access your Google Drive files from file manager.

![Google Drive](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhOANOXW-GET-j3epR-6V2h4ukgrIMBlpixh0_unUpsf8E3Dqm31yxK3HUzdmKYcrKcmrQqFhNXlgIIPdXBSjqgWrU4558fZ5z5JUk-XwTVOuYvyGx7LNbI_VzkRtjdGfm_gml0UIhYn80v8eskQPHrmcreUjLkj8ofrDDpZlOcMsqmJe5Y0hKPMIpPqjfo/s0-rw/rmdhnreza.my.id.bulk.rename.2.jpg)

## Bulk Rename
For this example, I will bulk rename inside `rmdhnrezamyid` folder and inside that folder I have file name like this.\
I will change `example001.jpg` to `rmdhnreza.my.id.n.jpg`

{{% adsense %}}

![Default name](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhfpRbb22hCU3eg30pxQSeS2KszQe7Nsh4rAOcLUMxKb9V7krEJRECWyMG0pVJRjYtxPJMugppgE9apx9fQdFUejRAi3Ry1ihyphenhyphenX2LsJUB142H3H_rhrklmcARLa0jDrGbWIqju9CXj0rurDDvOGfrErLpsHihRa-3AWKOBmzxkAUT-SMm5cv_6Of-Yjbkz1/s0-rw/rmdhnreza.my.id.bulk.rename.1.jpg)

1. Open terminal and execute qmv command `qmv mountpoint/folder`
```bash
qmv "Google Drive/rmdhnrezamyid"
```
![qmv](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhdGUWXO2q3Iowdpeyh1271T9_KH6rFoxyTi8U-n8e5gmn6dmTtp7CQFpK-MzApAaBTd4atzhXN1QIi7acy8K5ZjEGyWAz4ISlFMjFLbVGRrKho5UTpxJfEfmEc2fExPk4XmL-rIVU45zHj92q1AR_gjCtBuGWFbwVZagM-9LZTQLfr_p-lc9_0tFLmCtge/s0-rw/rmdhnreza.my.id.bulk.rename.3.jpg)

2. Output will be like this if you use EDITOR nano

![qmv nano editor](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEi6tH4shUxA93bt00fDF-s7PdkWFQJAQsEfka9BHmvDVQC2-dzYQ-gxmaPXEUQfX-cyiXwzQdNkQQ_0yRjpIJbvpA24u3mpaOTj3kFykFnWF-KQsTBrUNLRnEFdzJgWLnYNuCbMgxTrbfjtmzO4wfB46CT6EGOvuArFocgwsYwzx0qXu6YiQXcYMnxL3CSE/s0-rw/rmdhnreza.my.id.bulk.rename.4.jpg)
3. Copy & Paste output from qmv to text editor (I'm using Sublime Text)

![Copy paste to text editor for easy editing](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEj3oFfH04XPFyUSNIpOOCS569SDzy0sD8CIVLZX5CMUrtj9TTBFTQkYGvzyMwTPmuGUzQV8fKrFTGKAgQeMawgEVNKJsxyvN6oJH03o2WFZQUGgFPQdro0P2mqlTxN58ywmf6B_vplbrXi1XBc3-LqmZdWAwMz1ZdSxFvqJ3auG0fYodeW_3ySWImc9OXS9/s0-rw/rmdhnreza.my.id.bulk.rename.5.jpg)
4. **Change only on the right side, not left side**

![Change only on the right side](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEixMwCKwPq-IcxPea91lyeB2F_DsAMHAvgAa5Nej6-ge3dU1vopmMh-el0t8izhBNf9ZEiXjPQP_dK4fthC-tHkPkUKg_j9LbKjGZnOMpmiyDLw1rZ5zxYSn8ikOCtm9FEaPywyl-6UnnyTGZf0LtrCqxWK-dSca7ofgDr-D0grPcRfqUO6klNI-HAdKDV8/s0-rw/rmdhnreza.my.id.bulk.rename.6.jpg)
5. After that, replace all output on qmv with your new file name

![Save new file name](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjCZEvpo4hcE-swzXo4w1vAFxSCrnkbNavQqUdlY4TJBb4qxVs9ly5OuedDhb6L9-d10AORJExiTaTZenhRfPCgscnMLhP2-OEZ-MV7IRUlhUPqjluarGxyYdMkYqWVHfLj8Y-J-aePs-MKy8rBdoAmoJZ8sTX4eM8akrKpQkyFmHSACatheMi_pkB8HDpn/s0-rw/rmdhnreza.my.id.bulk.rename.7.jpg)
6. Save (`CTRL+O` `Enter` `CTRL+X` if you're using nano)\
7. Wait until qmv finished rename

![qmv renaming files](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEijPe1GVrDWKyaj0LLxfSi-oycH5sN-ahiMymH8qSsExOJELXW-B4fxF-fM4C9CUBDE5Kbf_0lWdUpFAlPqRudPazcH2e2hyphenhyphenruAebPAJvtr2VGF2gE0UvmCWkdTFYaaGKChgl731aXEab2-pu_Jq6yCbnu26B_NlEC2f2BLI4es4B5RiNg-UC-h4giefYQ0/s0-rw/rmdhnreza.my.id.bulk.rename.8.jpg)
8. Done!

![Bulk rename success](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjWwhrSH0wZrHlQUnthfQJF5eUmLW8YzntP8ERO8Kd_ujIVfh0Zd3MMxmbCA0Vf7x3nBH779jPuyDBil5pzwNQd-KwjhZNh0aXU-LQVA_0CjIv7u88erHgLhM2K65okbcRGz_-UWgFCUhRmR-cEcTp-VnBDhIkSW0M9qJqNEJbE6UKB1syus3cJt_AmFx5o/s0-rw/rmdhnreza.my.id.bulk.rename.9.jpg)

{{% adsense %}}
