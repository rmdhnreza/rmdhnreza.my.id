---
title: 'Deploy Hugo Website ke Cloudflare Pages'
date: 2022-05-27T11:30:13+07:00
description: 'Tutorial Cara Deploy Hugo Website ke Cloudflare Pages'
categories: ['Hugo', 'Tutorial']
tags: ['Hugo', 'Tutorial']
keywords:
  [
    'Deploy Hugo Website ke Cloudflare Pages',
    'Tutorial Deploy Hugo Website ke Cloudflare Pages',
    'How to Deploy Hugo Website to Cloudflare Pages',
  ]
description: 'Cloudflare Pages adalah platform JAMstack (arsitektur pengembangan web modern berdasarkan JavaScript sisi klien, reusable APIs dan prebuilt Markup) untuk pengembang frontend untuk berkolaborasi dan menyebarkan situs web.'
summary: 'Cloudflare Pages adalah platform JAMstack (arsitektur pengembangan web modern berdasarkan JavaScript sisi klien, reusable APIs dan prebuilt Markup) untuk pengembang frontend untuk berkolaborasi dan menyebarkan situs web.'
image: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhHYeiY6yfe8xAATQ8h2ZHuJRboTeCZXToJOG-dew3Gq3t5TqYwyz1btQxwx8tUJpgNLvkjUM6Vco49OXdxKZfrxgtrFcpy9F1ggatkY4lJ-c_TfCdF3nDvSR-Til-OZV-iITK1Ldcrdk0Up3PGnPaeqxCO5j6Bc0hccerO3V0xrwWB-yx54sK8UXBMUAt0/s80-rw/clouflare-logo.png
ThumbSchema: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhHYeiY6yfe8xAATQ8h2ZHuJRboTeCZXToJOG-dew3Gq3t5TqYwyz1btQxwx8tUJpgNLvkjUM6Vco49OXdxKZfrxgtrFcpy9F1ggatkY4lJ-c_TfCdF3nDvSR-Til-OZV-iITK1Ldcrdk0Up3PGnPaeqxCO5j6Bc0hccerO3V0xrwWB-yx54sK8UXBMUAt0/s0-rw/clouflare-logo.png
---

## Cloudflare Pages

Cloudflare Pages adalah platform JAMstack (arsitektur pengembangan web modern berdasarkan JavaScript sisi klien, reusable APIs dan prebuilt Markup) untuk pengembang frontend untuk berkolaborasi dan menyebarkan situs web.

Beberapa fitur Cloudflare Pages diantaranya:
  - Berfokus pada pengembang dengan integrasi Git yang mudah.
  - Fungsionalitas dinamis melalui integrasi dengan Cloudflare Worker.
  - Performance website yang sangat cepat.
  - Gratis SSL (HTTPS)
  - Dll.

## Settings Domain

Untuk setting domain sebetulnya ini optional, karena *Cloudflare Pages* sendiri sudah memberikan kita subdomain yaitu `pages.dev`.\
Tapi disini saya akan menggunakan domain gratis dari freenom yaitu `rmdhnreza.tk`

1. ***Add site*** di Cloudflare dan pilih saja ***Free Plan***

1             |  2
:-------------------------:|:-------------------------:
![Add Site](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgDEQDDposZhoGGKN7RhBdEdNeDfe4X3BA_Xu6-n9Ju0rO6LkwjOvouR3P0j09W7oacD4FyarxM7K0FitTTCgpKbL6BHb3uij21jf6-cJu4rzpmSDfM8IydCS5P_1Fb2pxQuoPE4LeTJnc6JRzy3d-EB68m5lMV-Pjcm0dNHhcni_f17ok44lkPUenEP3J6/s1600/rmdhnreza.my.id.hugo.cloudflare.pages.2.jpg) | ![Free Plan](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiARd63c3q16X8gSzjWOokrxZBj9Nj1_XKnj991pR62BXN1dEo0fcBq1kopeFiy23Vfx9nXo__kZQcgGsWzXUD-hX9uc9u5j2LOB1oQ8a7eOaUPydeA_pE5PdHj4BB7wUI-Smfo0Ba9NuGSuen_P4Cc12Lw3YBnm-8b6kXh0m5rJROw65GQoDVY8oBNpgtr/s1600/rmdhnreza.my.id.hugo.cloudflare.pages.3.jpg)

2. Untuk DNS, jika kosong seperti ini cukup klik ***Continue*** saja. Nanti akan muncul *pop up* ***Add records later*** kalian klik saja ***Confirm***

1             |  2
:-------------------------:|:-------------------------:
![DNS Record](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhRxNTd3Ew-NN9tSG_IALPDKkddb3LSn8HuqkItzNoVrs2upVovIvJ6T4Y_O7B-QRxh83Hl_Vh2E9iGE0G3Ji4WpymzrNQ90wBeHuYlBmhYOp-OCmGb1yPpYRI6YcH3ZQebouYMDmGpe81fOBS6d-0jo0O4tTiQjoBKta7lPQvVL7GiBZTqNt77sgneOVka/s1600/rmdhnreza.my.id.hugo.cloudflare.pages.4.jpg) | ![Confirm](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEg8O4WIcIJ7z5GH2dYOw8u_xw-mtkNdssvG9xh_NT5jXN08CLdrzowyLjNureRHvQBDydw5qUNhhDTCF4R4stb0ilYGyqUDj5ogOc-UwSkcIOve2pY78kITohosHk_JRaVGjWG9iuHRvunX4Z2cOFwcvz9meJ_PAt-jLB67YyHXLXKqA-6S4IftdcZYMKO_/s1600/rmdhnreza.my.id.hugo.cloudflare.pages.5.jpg)

3. Pointing *nameserver* dari cloudflare ke domain kalian, jika sudah klik ***Done, check nameserver***

1             |  2
:-------------------------:|:-------------------------:
![Nameserver Cloudflare](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEipw5chHc7AffInST4FlcY2imOxQo8rbAWAaIgi-JSdkom5v8FA_S9k3FkbmqLDyy7HC3WZkEbno5jwCGHo7z-ObEtJMunw7yEc9Dyfir8rFUzJWyaCc7xBG5hLJUst_YYJrdOItvVYnscx8zUolppw_H1KcIiIA5b-NNhDPicmvTY2kkzjUblzkwRGtz1h/s1600/rmdhnreza.my.id.hugo.cloudflare.pages.6.jpg) | ![Nameserver Domain](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEipFqj5eDwZWBWCKeMlWYa-ktHZZuA7Cn563x0-fjPKl8x9-mVAark9I9vgZliUDtkD0CAm_sdCLSAyeB4LDlm86mZbchq4cLqBysUXzJwi4_t4swigCAP8g1mT99N5MCOqGliyZpzaWYAEZ5hhOv3Oh8o4katw9PzB7_11y0SoNJRvLobQW78_wu5O7uL2/s1600/rmdhnreza.my.id.hugo.cloudflare.pages.7.jpg)

4. Pada bagian ***Quick Start Guide*** kalian klik ***Finish later***

![Klik Finish later](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiGzjg2zoSHlY5pIFfRjyrcQq-St4HCRPbK9DTNRUVX0hrHuIm-HkADXoPHje0ySItdEJuKje2e5ZPAXeGbcMSxrK4TkLE8U0_BPkKjMQsvmyKmvxndt00zti5waVpdZPFL34XCDYaxezhaI82vjRs_-RTJOAE_GUlJWgXSYeeILHS7lbpNYznVJteG6kpg/s1600/rmdhnreza.my.id.hugo.cloudflare.pages.8.jpg)

5. Tunggu beberapa sampai domain kalian aktif, proses ini tidak membutuhkan waktu lama (kurang dari 10 menit). Pastikan saja langkah nomer 3 sudah benar.

1             |  2 | 3
:-------------------------:|:-------------------------:|:-------------------------:
![Domain Pending](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjkOMqFPB3STMS3CrKmmoUL75lpeiyPM7kObo_EcCfFTwNN0EJCvvoJ6OYZ-QLRIXD3dyDTxdU2I7YVWhSL42HcF1uWe4fNByNbDw6t_yXwyrGbOe22Lnj7lOHjRGJMEkcfsgaG_CJV-RL8h9gZ8kEmAITJ_vCRlmCZHFZiY2i3H0A8LOIFIok63qv5TlJJ/s1600/rmdhnreza.my.id.hugo.cloudflare.pages.9.jpg) | ![Domain Pending](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhZR4PGrx0Jkt-VZ2FtuRzgdggviK2g_ReEelS-WpP4_PjvbjTPgen7OblOmaaHrAr7Z6YZ0BLCn31yvuxWmHRys0v7INAGZhly1JedufYrieUQ93K_axk1WGqkCOwx_OTorWjIrEKUF0Q85lPiU3oWXovr13nHhNHNvqo9i3PLBzc-BTRynxsw89vcDBbi/s1600/rmdhnreza.my.id.hugo.cloudflare.pages.10.jpg) | ![Domain Aktif](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjpuHT82uQ2mXROkCj5sVrqYZtABS5GoLDFlY48t0AAXnB6XYSfQYHNzbgpzDiAXwDAe_n0s62xXYu2r24SJSC1fAnx-xbovJFucwZ1HhKUeRAt8cUjYdC5uQKF_fHOIUJHyOabmZ91ZQ8oUBzr78dIKNS-mf8oEOlxN3Le1mIEBHla_iPOJ2RwaekwoQPd/s1600/rmdhnreza.my.id.hugo.cloudflare.pages.11.jpg)


## Deploy Hugo Website

Pastikan kalian sudah membuat website hugo kalian dan sudah ada di repository [GitHub](https://rmdhnreza.my.id/tutorial-build-hugo-website-ke-github-pages-menggunakan-github-actions/) atau [GitLab](https://rmdhnreza.my.id/cara-hosting-atau-deploy-hugo-di-gitlab/), disini saya menggunakan GitLab.

1. Kunjungi halaman [pages.cloudflare.com](https://pages.cloudflare.com)
2. Pilih ***Create Project*** -> ***Connect to Git***

![Create Project](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEj4VPM_CeefAszkTTTQL2LsMlW9tAbsHtsBFRlIBjvrhS3ZN7zqrPjB6sS3kdFCPK4SlqXvNDom9TpZaxfFoyawhQ0SIxADDcHz99ACvgzI4IUfp-viRdaaR7fNAdvroxdkR3kISXlwY8pbmgjKbCIDBgbkgMmjJUM-aj43jdnKKI8nVpzOkoukUukpMlf4/s1600/rmdhnreza.my.id.hugo.cloudflare.pages.12.jpg)

3. Sambungkan akun kalian ke GitHub atau GitLab (Jika project kalian ada di GitHub, maka kalian pilih GitHub) dan ***Authorize Cloudflare Pages to use your account***.

1             |  2
:-------------------------:|:-------------------------:
![HSTS](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEggZzr4CJHi_C1kIU0LktxgBGAe6s-V2DbBsgSxtri9RAluImgaaCJL0iZVbBhApLyVgLbzZy2DaF7nbTRFiWpn0rbj8KS-VQlXPZ3b5kb_iyiG1LFoAznZuw7B2sE7a-POVVVB1D3GQqBFlKjl9b3O2rHklJH3ygUXZLHz2819MGQGPQBANNf_1f6iDKGZ/s1600/rmdhnreza.my.id.hugo.cloudflare.pages.29.jpg) | ![HSTS](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgK55SVDVL8QWE-t5JbZ_tAESG75dvkahMn2G_0jgY6rQoIHPIvRHSS61pkFdReHEhr69hYn4Mnq5Eh93Pcltj_2joerYIVTYUn6zemDC8NhvafJub0rS8zDLs86ZoeVcIKgxtYkwmZtx9_XPiC_F9cPXzV5aI0b6nlO1dWHIhBh_x7cf_U6OH2nvr2w7rQ/s1600/rmdhnreza.my.id.hugo.cloudflare.pages.30.jpg)

1             |  2
:-------------------------:|:-------------------------:
![Authorize Cloudflare Pages](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgwY6XvhN_2w-nBm2LksIEIQ3IhtWypuKWV2VAzuTg7uSvyjgoprzYa08JveZ5HnGLwXc744K3KgH4BgRWwfCgix5DYd1FLHjcWRgOglEB57hun2wbRLm-fn_UV0GXbuv7FKeKOm-4ovHKrFcQD-Sj55rAHAjZbXY3cdO20wAGNi1iY7cB51va6hY_8R0Eo/s1600/rmdhnreza.my.id.hugo.cloudflare.pages.15.jpg) | ![Authorize Cloudflare Pages](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjYv_t5D-j7YIhNo766OBeRRM4sW3eitQxXcKx0pEIu_cg5qoC0LrgIn_be5sngHb39kqeOWtgE_EtyYTiDXIKBII151Z-OufBQgO7L-mf0tAlR7nFOOQA3OpGWql_Z2Nrq1UHwhIhR_MdIFxSTBhoeQ4id7Zy0pvHryTIawYROKqez6QGmMYg06tuOopLh/s1600/rmdhnreza.my.id.hugo.cloudflare.pages.16.jpg)

4. Jika sudah tersambung maka akan muncul username akun kalian dan juga nama repository, disini nama repository saya *Cloudflare Pages*, pilih repository nya dan Klik ***Begin Setup***

![Setup](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEj9hl8Ef6S6n_vcmVBzxdwKxOzYDfa-p7hgZ9of7l97-VvBrsc5Kpxw-p4foROcHVdGjgNvNTOq-0WmgCNSS950MepHOy_j22bM_f7Z3n50NCJ5rYSpyWhPL9XmRsRquHmk4xnEvVMPlYa72KWVzUfHpFxYgMgqBu00X9jtBBcF_v4JuYR2aGzZ78hZ0acb/s1600/rmdhnreza.my.id.hugo.cloudflare.pages.14.jpg)

5. Nanti akan muncul tampilan seperti ini
   - Project Name: Nama project kalian, ini yang akan menjadi subdomain `pages.dev`
   - Production Branch: Untuk default ini main (atau bisa juga master)
   - Framework presets: Pilih Hugo
   - Build command: `hugo --gc --forceSyncStatic --minify --cleanDestinationDir`
   - Build output directory: `public`
   - Environtment Variables (Advanced)
| Variable Name  |  Value |
|---|---|
|  HUGO_VERSION | 0.99.1 |
    - Catatan: Pada saat artikel ini dibuat, versi hugo paling baru adalah versi 0.99.1, jadi jika nanti ada update, pastikan kalian juga update **HUGO_VERSION** nya
6. Save and Deploy

1             |  2
:-------------------------:|:-------------------------:
![Set up build & deployments](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjiLlaoZQy5o-ybABoHr5-oA4Mo3JO5cFYb2YGI1g43m9L8bXbNMTnwbSB2VDUIvFZgkKlI-LK5lVAxByla-UZto0jAoBHVj_MX8qUoRo1rzP_hS5rn98GUP56ODhyn6Gxr17-BhrlH45yGe7l86ViipXl4NxAINByR5I6KRqNTn7hi5JgTCGSRbkGhrIhu/s1600/rmdhnreza.my.id.hugo.cloudflare.pages.19.jpg) | ![Set up build & deployments](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiCyDWixJFa8KCD-uVoXGQu0RzQUMsNNouMXCaXRZc9Cx719LGiSJCtCl_R-SWYIG7x5bNDdFnAeGmyTT2Ot8HqasDGno0jK66c4mYLfb8TbqVYCvXePgIWL7OJCrC9QxpUuQMxDy2ThRthnQRDbs-My9J0uJxZeMc-hh-N87-DiF5Q-x4LWowCJvx5Ugf4/s1600/rmdhnreza.my.id.hugo.cloudflare.pages.20.jpg)

![Deploy Berhasil](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgWYVogI0tuXVadMWxf7487CZvGOEosGEjpqlAGC_PvXs33FAhBOYofj03xqRjpMjPUQo9yiCrDOM4mp3SaooYdmglKelAIblF98bxr04mmi5wyLZw7a_vf8428drhaon__pJqfcyjmMJjGXf0SmWGDLHXsqwRBn6M7aFd0P3e0TwuS8HZiVtAWaaF1i0wh/s1600/rmdhnreza.my.id.hugo.cloudflare.pages.21.jpg)

## Mengubah Domain

1. Masuk ke tab Custom domains dan Pilih Set up custom domain

![Setup custom domain](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEifhJiO_KFEJwZ9-vfti_m_rPuultr5Q37bQ5HxVMgkDvT4J3ddY4iMFehEHWykgGCaTt-iqdJ9MiSEMKKx7-tb14a9JsjBpxK2hv1t4GLVBUbMTNnrNquttunWrblEFcR_HdG29oEhzNrYdPWswHLpSCPTbOebSZMNl07zEZnGUHRf85GYnUNeaih0f7eQ/s1600/rmdhnreza.my.id.hugo.cloudflare.pages.22.jpg)

2. Tambahkan domain kalian yang sudah di setting tadi di langkah pertama

![Menambahkan domain](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEheIYqGdBdF0PfkP6fvyatmnhT8F8ao2jL6wc0_QB3xWE0qq-e1hKzt24YHyIWamX7GyN1jbIuNL8-aF1vdD1LV2Gd9hBy8tD9KvnQa3lhGnXUhWNvSEyfl0qmlGf4pCL-z6b8W7J4bZ3lpvb3v4uzA_zXqOq_7dpxicjSNtXfT7FdAd2zEHDNsjIXbOQNH/s1600/rmdhnreza.my.id.hugo.cloudflare.pages.23.jpg)

3. Confirm new DNS record -> Activate domain

![Confirm DNS record](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEh055IHAHwrXAcdoGoq0K5EiV4NzwPb3r35C3ZbCsv5f0M-CVkppKID0wkryt1NC87Hz9FKoldTI_2pgN1-qTUxaDcB8yUhXNrW2cbhj_Ayf_wb7EdDsYudT7m4IX7OKvcoexb9Vd6ENiytvqKrDOuqy-tf3MCJ2I_id5V0PZ5iXCTF9zb0_1-qPq5zKWTQ/s1600/rmdhnreza.my.id.hugo.cloudflare.pages.24.jpg)

4. Tunggu beberapa saat hingga domainnya aktif.

![Pending DNS](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiZECZV3N196100ZARnURi8nM1xV-D6z5qlIIdsEE93a0vEXPPyAAxe9gmS6q3YQAh2wx9KDdrtLjAMYGlv02ZoSJD_soqzjZkYmRlT7YmA4khTe7Xfg12AKwE8-TKFv0yCT3cpeGi0cMrhV5pEx1YM87ugdgCPCUTl4Lj6jrARN1CnYTqeqxBVXA7YLxEm/s1600/rmdhnreza.my.id.hugo.cloudflare.pages.25.jpg)

5. Tambahkan new DNS Record
| Type  |  Name (required) | Target (required)
|---|---|---|
|  CNAME | www | @ |
6. Jadinya seperti ini

![Menambahkan CNAME](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhEQco3JAJ9qYbx9M9IVvPl3Z_0FI9WRbH-lhfa-SrkXtfTTCP00-B1bKGl1gv5OW8TUsFfE1VNkO1qFQ8JBC_pGIU_YPfgp8MdbvFae4j9YqzSyt6eW30zSz4lDpKLFyz2p0ixXJ0GH3vf6QUVe1_qbl4ifz_voGCsNORojiRzOLDA4RdBcfwjzOCY2x_u/s1600/rmdhnreza.my.id.hugo.cloudflare.pages.26.jpg)

## Setting HTTPS

1. Masuk ke bagian SSL/TLS dan pilih Full (Strict)

![Setting SSL/TLS encryption](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEj9xcbGAkCpetVz92Ds09NucXVr65I66qQrUP9O0WWzDgwTv0eOcnqTJ_QTrZYyshahpgfr8Rs4r6FchTAi1C4ol7HvxD28KOGzIYeOFo3ZeK2tUSECQFyTy9G1VhBHLRTrN0yu7HYJOL-JkdYvVFP1Me_0QdBQjNXQsMYtba37bu3QS5DgAVSbxcdPpu-a/s1600/rmdhnreza.my.id.hugo.cloudflare.pages.27.jpg)

2. Pilih bagian ***Edge Certificates***
   - Always use HTTPS -> On
   - Automatic HTTPS Rewrites - > On
   - Change Settings HSTS seperti ini

![Always use HTTPS](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhxTJrRERhgQP51K8XIxjQpN53m8vw1Fr8Z_cRy4KlG86pkMZh_xOkoeeD2xQ0_Y5AXx7M4B6SM2HxsN9KkVsFxKyrdK1KUZZUeLjG8sjVjVnDTK4yNyNzAtZ-akcZN9UxLex_8OYDD6aWM5JJY7mJl5SlM_V-ZLN3DqEAYQvmi-m1dMh6Oivf-Y7NivFKb/s1600/rmdhnreza.my.id.hugo.cloudflare.pages.28.jpg)

1             |  2
:-------------------------:|:-------------------------:
![HSTS](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEggZzr4CJHi_C1kIU0LktxgBGAe6s-V2DbBsgSxtri9RAluImgaaCJL0iZVbBhApLyVgLbzZy2DaF7nbTRFiWpn0rbj8KS-VQlXPZ3b5kb_iyiG1LFoAznZuw7B2sE7a-POVVVB1D3GQqBFlKjl9b3O2rHklJH3ygUXZLHz2819MGQGPQBANNf_1f6iDKGZ/s1600/rmdhnreza.my.id.hugo.cloudflare.pages.29.jpg) | ![HSTS](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgK55SVDVL8QWE-t5JbZ_tAESG75dvkahMn2G_0jgY6rQoIHPIvRHSS61pkFdReHEhr69hYn4Mnq5Eh93Pcltj_2joerYIVTYUn6zemDC8NhvafJub0rS8zDLs86ZoeVcIKgxtYkwmZtx9_XPiC_F9cPXzV5aI0b6nlO1dWHIhBh_x7cf_U6OH2nvr2w7rQ/s1600/rmdhnreza.my.id.hugo.cloudflare.pages.30.jpg)

## Website Live

Jika semuanya berhasil, pasti website kita langsung bisa di akses seperti ini

[https://rmdhnreza.tk](https://rmdhnreza.tk)

![rmdhnreza](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgo8qm_bMB9-yjJUAEfw_DKnKpI6zxNaCR1cSOXik2mHgv_slLu2Eew0Mg3LB1P0kkdSV6innDEDa7LtGd_6KSNhSAH2dLr7s8uiRqlR6mgiFepLYRRb7KAQMAwtK5VJ1q86XypLxC2YcGS4rQwIdf14DVarF1v0mSN5l60L-usUVmKD9OLt684jfWYDq4K/s1600/rmdhnreza.my.id.hugo.cloudflare.pages.31.jpg)
