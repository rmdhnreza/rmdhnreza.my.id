---
title: "Langkah Mudah Membuat Website Upload Sederhana dengan Firebase"
url: "langkah-mudah-membuat-website-upload-sederhana-dengan-firebase"
date: 2024-02-03T00:00:00+07:00
description: "Langkah Mudah Membuat Website Upload Sederhana dengan Firebase"
categories: ["Tutorial", "Web"]
tags: ["Tutorial", "Web"]
keywords:
  [
    "Membuat website Firebase",
    "Langkah mudah upload Firebase",
    "Panduan website sederhana Firebase",
    "Tutorial upload file Firebase",
    "Cara buat situs upload dengan Firebase",
    "Website sederhana menggunakan Firebase",
    "Langkah-langkah upload file dengan Firebase",
    "Panduan membuat situs Firebase",
    "Cara mudah upload file Firebase",
    "Tutorial lengkap Firebase"
  ]
description: "Temukan langkah mudah membuat website upload sederhana dengan Firebase. Ikuti tutorial lengkap ini untuk panduan langkah demi langkah dalam memanfaatkan Firebase untuk membangun situs pengunggahan file yang efisien dan handal."
summary: "Pelajari langkah mudah membuat website upload sederhana menggunakan Firebase. Tutorial ini membahas secara terperinci cara memanfaatkan Firebase untuk mengembangkan situs pengunggahan file yang simpel dan efisien. Dengan petunjuk langkah demi langkah, Anda akan dapat membuat website fungsional dengan kemampuan unggah file yang handal dan dapat diandalkan."
image: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEh9k0x8HPWaXtoM3QhaDyWxLdgFz7CF0Chq717tQHdHQ5qQarKpidJL2Q6QYEU7YMIrv_cVR0qpfd7Wv7ZJhPz48Kg9uMI9LdLCFWE_oB8xks83DwSk3eaxMTI2UMuGm2P2ihGT3qV125cbm4D9-j7PW9HMnnkQLO42sleFGXiGjMx5pD1aWk0Gzr55tPAE/s80-rw/firebase-logo.png
ThumbSchema: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEh9k0x8HPWaXtoM3QhaDyWxLdgFz7CF0Chq717tQHdHQ5qQarKpidJL2Q6QYEU7YMIrv_cVR0qpfd7Wv7ZJhPz48Kg9uMI9LdLCFWE_oB8xks83DwSk3eaxMTI2UMuGm2P2ihGT3qV125cbm4D9-j7PW9HMnnkQLO42sleFGXiGjMx5pD1aWk0Gzr55tPAE/s0/firebase-logo.png
---

## Apa itu Firebase

Firebase adalah platform pengembangan aplikasi mobile dan web yang dimiliki oleh Google. Firebase menyediakan berbagai layanan dan alat untuk membantu pengembang dalam membuat, mengelola, dan mengoptimalkan aplikasi. Berikut adalah beberapa fitur utama Firebase:
  1. Authentication (Autentikasi): Firebase menyediakan layanan otentikasi pengguna yang mudah digunakan. Pengembang dapat mengimplementasikan otentikasi email/password, otentikasi pihak ketiga (Google, Facebook, Twitter, dll.), dan metode otentikasi lainnya.
  2. Realtime Database: Database Firebase adalah database NoSQL yang dapat diakses secara real-time. Ini memungkinkan aplikasi untuk menyinkronkan data secara instan antara pengguna dan perangkat.
  3. Cloud Firestore: Firestore adalah database Firebase yang memungkinkan penyimpanan dan pengambilan data dalam waktu nyata. Firestore memiliki fleksibilitas yang tinggi dan mendukung struktur data yang kaya.
  4. Storage: Firebase Storage menyediakan penyimpanan awan yang dapat digunakan untuk menyimpan dan mengambil file seperti gambar, video, dan dokumen.
  5. Hosting: Firebase Hosting memungkinkan pengembang untuk dengan mudah meng-host situs web statis mereka. Ini menyediakan HTTPS gratis, caching cepat, dan integrasi yang mulus dengan alat Firebase lainnya.
  6. Cloud Functions: Firebase Cloud Functions memungkinkan pengembang menulis dan menyematkan potongan kode ke dalam aplikasi mereka yang dijalankan secara otomatis sebagai respons terhadap peristiwa tertentu.
  7. Cloud Messaging (FCM): Firebase Cloud Messaging menyediakan layanan pemberitahuan push untuk aplikasi Android, iOS, dan web.
  8. Machine Learning: Firebase menyertakan fungsi pembelajaran mesin dengan ML Kit, yang memungkinkan integrasi mudah fitur pembelajaran mesin seperti pengenalan gambar, deteksi teks, dan lainnya.

{{% adsense %}}

Yang akan kita gunakan disini yaitu:
  1. **Firebase Authentication:** Hanya user ter-autentikasi yang bisa *upload* dan *delete* file
  2. **Firebase Realtime Database:** Untuk menyimpan data file yang sudah kita *upload*
  3. **Firebase Storage:** Untuk menyimpan file yang akan kita *upload*. (*Sparks plan* atau *Free Plan* hanya diberi 1GB storage)
  4. Firebase Hosting: Jika kamu ingin host website sederhana ini di Firebase.

{{% note %}} Disini kita akan menggunakan local file saja tidak di upload ke hosting {{% /note %}}

## Membuat Project dan Mendapatkan API Key
Sebelum kita membuat website *upload* nya kita perlu membuat project di Firebase terlebih dahulu.

1. Kunjungi [console.firebase.google.com](https://console.firebase.google.com) dan *Login* menggunakan akun Google kamu dan buat project baru

![Figure 1](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgZ9zTYABtUPQVRWZtLWrDmUqUaVxIJ3qxwIvcAbQnaQhg82jX4Tg5CZDNxHo5BX642WmV57Aq9M3qyF_WIM1CJpROXb6cNmRwKiA5LkagWY6bkkp1E431e7JNIqh0pYkm5Z4NTtpSN_MP6IRIkmhZyMlla9iNz1ja6nytPHhJv2ZiDvC1bLVLye-XcI3oj/s0/rmdhnreza.my.id.firebase.create.project.1.png)

1. Isi nama project, bebas. Setelah itu klik *Continue*

![Figure 2](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhB8hJYl1oplCPpohK_vgj3nJGyPyRbCP0Ywek4mF28GANR1lXG881E9BYFyURp0Xvb5ktArMApuVigogcUdhGjKeb6WX8NpQAppimSyj3O2z8K1ja7c96rzBLXVxAro28ie-rPINZnp2m2ndno_goCiRQ8X_W27Hi-ZjIIGgpGtU1nwtRWFhH6ngL7lTp_/s0/rmdhnreza.my.id.firebase.create.project.2.png)

3. Disable saja Google Analytics nya karena kita tidak akan memakai fitur ini, setelah itu *Create Project*

![Figure 3](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEj1SQS-RJmUuQo3aP4MNFv0TgOVdTPe7olmueWeG3MXsPcUQrNgtplppCTyOk5uia3AOAtCYh5Gp758FBOgzE4_xhgd7u_RtbU_1ReBHS4kw8sbCj3Nt_PdATrjoFofX5f3BEFcvNXmgbjbpFbRyqHqYbZqTn8DbYNn8FukPd2Sy8vTeOSK_D4xGwVpUE_u/s0/rmdhnreza.my.id.firebase.create.project.3.png)

4. Tunggu beberapa saat sampai project nya berhasil dibuat dan akan otomatis masuk ke *dashboard* project yang sudah dibuat.

![Figure 4](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhz7rCXO2u9nOwOAeXQCyJAKnGnJCFMi1liJgWBDkZPUICgBZLssy78HJo3VoaDJk2cYY6FzNdrmbfjRZTjcBMj3mzmuJJUPZKM5NK6ZAsg4LBg2IjjQyGStcgGsKHdWhepeOTUh7Yc8yFsD6szA2iKJ34fscdjPXjiXsgQ4K-kJGx8-vseAYxtJpIMoMTL/s0/rmdhnreza.my.id.firebase.create.project.4.png) ![Figure 5](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgTncM7J9F4NKJNO7snOEU7Tn-hJxswUxht8qaxMUTldEFiTstY1mmiVBwhDaJO6ymehN2fm5AVBvbT4ARZ9iB9ugvsnUCIQVHNElrslMurg1n3_vh9M_1QUe9M90hTWlgVAs1eV4_nXJM_fOayX8tAzzMQfcnTJJvUztVCuhw8LLNnrXlyKKe6sgCBQqt4/s0/rmdhnreza.my.id.firebase.create.project.5.png) 

5. Pada *Project Overview* klik *icon gear* dan pilih *Project settings*

![Figure 6](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiY4sPYLFYmAGoMt_sdWaKttT7pufEkACqs0C4aZ1qOwvr7q1agt3v4rBCYc5bsbJZpfW-LLOAheX96vt31eYbwtAhfWoFieO7l1Ra9lkZBSNl8V38mG_PP53ANe71T2ncaRhu3l0rRcIT8qcKwLctgczW8ObX9G6HOSGy5l6vLNpX1YFRocbe_NnWSR5uz/s0/rmdhnreza.my.id.firebase.create.project.6.png)

6. Klik icon pensil pada ***Default GCP resource location*** dan pilih ***asia-southeast2*** dan klik *Done*.

![Figure 7](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgqkAdkHULx0IKE22jNVflMPHDUEn0WDJf_b5WWKF4OmM6vKK45tdEfEn5luQh1muylPbEJQPpDdYA9YEM2jelB2il9u7PcF2pHNIeeHQfUHyv_FZvXnitFLZ_JJdOJCEFX5x9NNAgmsCNK2QOUfkazt4ur5C26oEgkALwgeSBHiMQvtwZQb4dZcrEKTg7o/s0/rmdhnreza.my.id.firebase.create.project.7.png) ![Figure 8](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgi8o6q5Zcm7XcWCRoJyWVPzK0Meg5JW9LYzeBk6UnmNM2twCZUqoLgGdwAfk_SwH8WnRVY9kZM6URuVJZj75im_3JlaS_-JK0S5zj0IGenIErRs0OoEzAx6urN_UX7k_4XAwXeif5pLmzu4jsEWc3QnKwSWkRgYitR55qcZjO9M1diNfW_ws15uk26k5do/s0/rmdhnreza.my.id.firebase.create.project.8.png)

{{% note %}} asia-southeast2 adalah server negara Indonesia, tepatnya di Jakarta. {{% /note %}}

7. Scroll kebawah dan klik pada icon code `</>`, untuk register web app

![Figure 9](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiPBpvEXd_IxjVGhWbir3Gu-K2TMI7VbrDbyRy2HtrJJ-UQrei8AB28lNtxKq-wcej7g10HSJBKmOLzOzNX4TXaI-n3EuUkTI-mAx1ogMxd3uLDuGCCFVuYjthTKvQm1y4WJcH2mxtes_cOiCJyNo8-5RxHOQsynfD6P9wXBlmL0PbW5QY2L72y09vpdDsY/s0/rmdhnreza.my.id.firebase.create.project.9.png)

8. App nickname bisa kamu isi apa saja, untuk yang lainnya bisa ditinggalkan *default*
   * Add Firebase SDK -> *Continue*
   * Install Firebase CLI -> *Continue*
   * Deploy to Firebase Hosting -> *Continue to console*

![Figure 10](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEh-hyH7m2YD4v2bIfJNf-J_X6wbcu6AfpAZ0PPoZHzYBSo6tHZVCaEDTqQI6ro4_KSbW5wqG7xsxbfCdewNXGKgwR4yD29KY61M4LusW91DqHNecNfGVdbHRI31Vh564swmNuIHErVeSa8t9eULnBqhh44E6bVWgcvdl_jz_j2qh76DCiCj26sV38hJUkGY/s0/rmdhnreza.my.id.firebase.create.project.10.png) ![Figure 11](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgOKv5Xro7JBHuJqrDvCIs-lb8HIwG-WdfCOv3s-44Oml84hiZX0lnptTBAI_wvdyCWtJc-y25N3pZpP3xPdiUTcuJABsJ6IMU2Ou9joLYnFtzKa86IjVfHBL5sJZ3-CT4qYXnNpb8aB-DKF3SoRFsH2Orwi-Cmf7oGVemueRiMUuOi6d_jCqcN56MBMN1u/s0/rmdhnreza.my.id.firebase.create.project.11.png)

9. Sekarang kita dapat config firebase nya.

![Figure 12](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgPf6G8uYESGUskd8AvW4pKX_Rc_ywn8FW41MR9wPU4f_OewIJgpPADDdLzGn5eYkHJo2yluVMo_hGUCKJ1V89wVbAzPO-M7BsHQaMf3kHygw9rcRGHtmsfRnSQpbRImZBcMSMjhfqItRkfuH0Ytj7nYSBKsKSCWi1st2uah-bF0KVWUbBzZH6d0fyFeMgk/s0/rmdhnreza.my.id.firebase.create.project.12.png)

### Membuat User
Supaya yang bisa upload adalah user yang terdaftar maka kita harus membuat User terlebih dahulu

1. Klik pada menu **Build** dan pilih **Authentication**
2. Klik pada **Get started**

![Figure 13](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhGTGeOShA1UFoWXKhYa0IUhvET3N1kkAmt5yJH6Rs1TFl4Pvjn_yBa5b1L8_xINrxt_Caxqc5nO14DAfVfg1MzLZg0qL5uLJNwdWWrXnw1GoM-YMThiqzFH_nXEJBMBB5bSP29UO2DnY4jY5yhvu_ZS_wFFI8Fm6shYCeqP9IvYYbT4xdNLMLvPVyQft_R/s0/rmdhnreza.my.id.firebase.create.authentication.13.png)

3. Pilih **Email/Password**

![Figure 14](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEg2D_MjwFK-souDQ4t54NP5ecc9vp7JcTywDjahrGQxOwfzNh1ZE-zkYLwHsGuQzXLyOYnMfdA_k3KIDEklX1mPPQMZYodqIiJpyigiATeb8UVP4V1k3Bypl61juzLTz7ZB4pTxJhxsl5QfKxOT22Beke0kfsReJF54gZqlvRCXgFo0sU08BjDwF9UKTj4i/s0/rmdhnreza.my.id.firebase.create.authentication.14.png)

4. Enabe **Email/Password** dan Save

![Figure 15](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjjDgge8tFFFuJB5JkxKD-5zUJzQTGjg3odBUY0S8jbooJPdFpLIVZztudUqjH51S5Hl-5prH0owP8NafeilSv_msN-gPmYedjGn5IswcQh1GiosvLkYKn4dcZ5F89ydFixFTYEZpsRvH0DUa99cShRwHJX-VHHPFEEHAPtDj3T2-k7z6HWihzhonJpAJVc/s0/rmdhnreza.my.id.firebase.create.authentication.15.png) ![Figure 16](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgwyXyrnfVhUSM0L0MfGC7JZOplfVixLVqzOeawXre1Aw77vUMJrKu4qiv7Cvs89c_r18t2G_bVFV_DK7xgERWNKhQsz5htyCIe9tuSsBGdmKA-MvmilZ5nquSsVGDATcGX_PcXoPYwphaYx5bTI2EiFmUPmqepSOrGr6suzRsxU-9yvihoWVEvTVDB0v-o/s0/rmdhnreza.my.id.firebase.create.authentication.16.png)

5. Pilih tab **Users** dan Klik pada **Add user**

![Figure 17](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjk3AZ_b8cs9rpCqkEX9gW04TNsgx_rSrohxo6Y2B6CkdFfcJyDtxkjdtRX8xD-7y-JJHDx_ZEJx3wvadcwSxAkxysmmIFGxKmj7XoBediCB4zDBy_FOPIKs8F_qCTj0w8KdS0Q-7_fvHu-U_JfcfE_HuK8f95xLW-c_xICXnr1jJ8eG_CEhAJgQSzu9TMX/s0/rmdhnreza.my.id.firebase.create.authentication.17.png)

6. Masukan **Email** dan **Password** untuk Login nanti dan Pilih **Add user**

![Figure 18](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhuk_yOziwncsXuVm78vWENZYhlMFCoa9eyrs01-IfoSaHXeC1XwyuRpJsJ4fqoC8qLAx7lg_enGsPv-HQJGDQxmU7VgqeIvvX6wVcYHvziZU_Fgq6nK3ZGmpqvjEjaDMgceZAGmQgWQYL4y4Cs7VDgIkOAmhfqSDSOVCJypvnnsWlvbj6Wt_bLanKIzuVx/s0/rmdhnreza.my.id.firebase.create.authentication.18.png)

7. Copy **User UID** nya untuk settings *Rules* pada **Firebase Storage** dan **Realtime Database**

![Figure 19](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhnh_LhqKAbJLRa_R3jeibiRgs1vME6gVib1uMdzg1qVPHWYI3ZKXhsuJxqhSk_hh4F-VgIRnrWyML0wX1VXjZyNRC8wqXEFrTnUsT4praFXAuW0-3Fk4URfrGbDX9mhnigOJ5Y8EYLMm-vusSaDEY24g7xnz-o9uSMRlqTmTrClwqHdBTGzbqz4-xErQhK/s0/rmdhnreza.my.id.firebase.create.authentication.19.png)


### Buat Firebase Storage
1. Klik pada menu **Build** dan pilih **Storage**
2. Klik pada **Get started**

![Figure 20](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiO-B0LIQ8EbSp5XSlD9NjSIYRG35QmFI5UPGMI43Bn0RAFced2CEKUuhv_ez0-5-eRMNnxQj-vEsjERZRJBDscvFUjZWg3DxxlNcIqjK-G4VLiAE_gUe_1CeptUMvToDFsBzw9gyfDbHMxhjwo3t9MptrH0tx2Cs6wkUSbDUMyqRh9aqHtvjnkgiQovmTN/s0/rmdhnreza.my.id.firebase.create.storage.26.png)

3. Pilih **Start in production mode** dan Next dan pilih Next

![Figure 21](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEh5X-rE3MJ4HVBCK37uIgPJ2BjkoS5rYAmqJLg1MHES2XjpnvK9BpwRvqLEkSvykurJT88wVFQZoy60n9xQgCY9V67JpIIa-rF3q0pWGnJXxAvF9q97QEG7FD9-bv_GhNYK_bqIGleUUHQ0b29Lnas1axkPlN7W0yAJfYRudPeVxEIZ_a0WBHxIU9jGvPf1/s0/rmdhnreza.my.id.firebase.create.storage.27.png) ![Figure 22](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgRHqUJciZVXEAMtqRlnpFDgq7n74q3Y8Y4mJL90JwinfeghlhvHDtdZja0W23DyliJgid4amfjJHB5dOshfKKtT7usmLToEF4CVvAO_JX6k8DwHGcuSOi_P8-cHJ7F2nhuSKZU4ijL5qjnsty4o674I_RATdgCX0tOvIC2LdZJQ-TZ_-bUUxiLShVgsfoT/s0/rmdhnreza.my.id.firebase.create.storage.28.png)


4. Buat folder dengan nama **images** dan **videos**

![Figure 23](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhGxFu00IGNK5zH7mQ3692zNf9QAeAeMPj3Bxign_PBR0aRpAl7-E95vdcYNIKTGVesQ0znJQHnlxxgOw1HnQN7ej78ADCvrCVmZcxeRAbrsSPvhemFRNDDpZgK2LPDBy-AjAsZH4jea_1PCOJ0nuM-yz5lXTDRfPvX-9_JD0W5kQiXEcNJJd9EOzjleScy/s0/rmdhnreza.my.id.firebase.create.storage.29.png)

5. Masuk ke tab Rules dan ganti dengan kode berikut lalu klik pada button **Publish**

```yaml
rules_version = '2';
service firebase.storage {
  match /b/{bucket}/o {
    match /images/{allPaths=**} {
      allow read: if true; // Allow read for everyone
      allow write: if request.auth != null &&
                      request.auth.uid == 'UID' && // Ganti dengan UID USER YANG SUDAH DIBUAT
                      request.resource.size < 5 * 1024 * 1024 &&
                      request.resource.contentType.matches('image/.*');
      allow delete: if request.auth != null && request.auth.uid == '123456'; // Ganti dengan UID USER YANG SUDAH DIBUAT
    }

    match /videos/{allPaths=**} {
      allow read: if true; // Allow read for everyone
      allow write: if request.auth != null &&
                      request.auth.uid == '123456' && // Ganti dengan UID USER YANG SUDAH DIBUAT
                      request.resource.size < 5 * 1024 * 1024 &&
                      request.resource.contentType.matches('video/mp4');
       allow delete: if request.auth != null && request.auth.uid == '123456'; // Ganti dengan UID USER YANG SUDAH DIBUAT
    }

    // Add rules for other folders or paths if needed

    // Default rule (if no other rule matches)
    match /{allPaths=**} {
      allow read: if true; // Allow read for everyone
      allow write, delete: if false;
    }
  }
}
```

Pada rules diatas, hanya UID `123456` yang bisa upload dan delete (*write*) files sedangkan yang lainnya hanya bisa *read* saja, hanya bisa upload format image dan video hanya bisa format mp4

![Figure 24](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEganbaOasQzH90zvUXUDo9Tf4VSRWPjbATAztWeTenfo0pS4GaJPVFWMy4tBtPk6tYSbg_PMC_Is2nuDbRkC4aUid1lflkZp3J5fSDP0_kXlMvTSMugIo7_9NgcfeUlLeumpVUEtNS4t3zmgXncGtNXoa4YHcLe-EKuKJ09WU4X6ot_L79dqdX8VVhNgBJT/s0/rmdhnreza.my.id.firebase.create.storage.30.png)

### Membuat Realtime Database

1. Klik pada menu **Build** dan pilih **Realtime Database**
2. Klik **Create Database**

![Figure 25](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiVEBTDKZ228flgUZxbRALlKygF_wtzGwZ5KvfOMI6NbF5rZMQwjusYOP-CJN_Bjak9obXIeqRHDYHVEP5FOt6w1VYhW3K1ciaqvlExqLax6fl7lpyyVd99WqxmEA5ZkLLuLv2Lpr4ZGBNVndjlsW2Xd3nmr07edtNdKgM0TaRqH87Qpxpyx8bNQyHo05Iu/s0/rmdhnreza.my.id.firebase.create.realtime.database.21.png)

3. Pada **Realtime Database location**, Pilih negara **Singapore** lalu Next

![Figure 26](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgjpN6ewHGjQPAg2a3qlXOaARWe3EZerbpbUfe0DeNTvtvaZMHETKZp5Zi5sZJxYwCYWCannJSbU9yhWdlpfDU39Mox31JAbTfCSc6mc-rR2y9sVtxmoG1KbOEad0TjgSuNuSx3jErIM-Rc6htl63SRDFQ9E8SlLuw3760UsJaNgVuTfDtvhzB3KG_dda-n/s0/rmdhnreza.my.id.firebase.create.realtime.database.22.png)

4. Pilih saja **Start in locked mode** lalu **Enable**

![Figure 27](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEi2BqYxAguUWXu5TGFpU2UGa8o1sgBqk8bWuCJONa-Yp62VdCWZ19fdptVXtwX2tXIZZksXHQPC_287LESCjk4nmYzaNAu2wnpm-0a9obGEbmrQTtan_2PQxsXRmc8W8t3willaG0GT-P5Utp-iWZQ4p0kpDsbVyImTVNAv3G7kZ1zR8UnTZVD94tvn7YOM/s0/rmdhnreza.my.id.firebase.create.realtime.database.23.png)

5. kamu copy dan simpan **Realtime Database URL** nya

![Figure 28](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgB5jRG6jNnE7QuHLq4_Cqy6khcyUOvlwlK2toKCFf4krumMAJO-1qzKLeSTrUCplk5542ogYE_Sh5kfLP7Msy1VQicBm16tpU1X4P7CvYy_Cg7iueJlDelVh4AiB5qK12fLA47bua9d_fW0CkefiNwx-W_rKox7KG6reXTIyHVoTfG2pwjNxiy5wGMLFAe/s0/rmdhnreza.my.id.firebase.create.realtime.database.24.png)

6. Masuk ke tab Rules dan masukan kode berikut lalu klik pada button **Publish**

```yaml
{
  "rules": {
    ".read": "auth.uid === '123456'",
    ".write": "auth.uid === '123456'"
  }
}
```

Pada rules diatas, hanya UID `123456` yang bisa *read* dan *write* ke database yang lainnya tidak bisa.

![Figure 29](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjMSGOtswlBqYPSCK8aIiysf73fwNz7U0CRiNCsrszPQEFcx8GiJ9wY7YnT9G4qMh8KR9sRFRPBxXyZ412scA1kvNWVh_RELbGjOiVXoCFfcTYEwWhrlsjjC33y6Oy47_1V8nLA5mcyc8w4oH97CWjRSmWDuVEchK3vfevSlOU0Q7MSDCSOV3sIhDmZQjTH/s0/rmdhnreza.my.id.firebase.create.realtime.database.25.png)

{{% adsense %}}

## Setup Folder dan File
Buat folder baru dengan nama **firebase** dan buat folder dan file ini di dalamnya

 * firebase/index.html
 * firebase/css/style.css
 * firebase/js/config.js
 * firebase/js/copyToClipboard.js
 * firebase/js/deleteFile.js
 * firebase/js/listAll.js
 * firebase/js/listUploadedFiles.js
 * firebase/js/login.js
 * firebase/js/updateProgressBar.js
 * firebase/js/uploadFile.js

Jadinya struktur folder nya seperti ini:

    firebase/
    ├── index.html
    ├── css
    │   └── style.css
    └── js
        ├── config.js
        ├── copyToClipboard.js
        ├── deleteFile.js
        ├── listAll.js
        ├── listUploadedFiles.js
        ├── login.js
        ├── updateProgressBar.js
        └── uploadFile.js

## Setup Code HTML/CSS/JS

1. Copy dan pastekan kode berikut ke `index.html`

{{% spoiler text="index.html" %}}
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Firebase File Upload</title>
    <link href="css/style.css" rel="stylesheet">
    <!-- Bootstrap CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.0/dist/css/bootstrap.min.css" rel="stylesheet">
  </head>
  <body>
    <div class="container mt-5">
      <div id="login" style="display: block;">
        <h2 class="mb-3">Login</h2>
        <div class="mb-3">
          <input type="email" class="form-control" id="emailInput" placeholder="Email" onkeypress="handleKeyPress(event, 'login')" />
        </div>
        <div class="mb-3">
          <input type="password" class="form-control" id="passwordInput" placeholder="Password" onkeypress="handleKeyPress(event, 'login')" />
        </div>
        <button class="btn btn-primary" onclick="login()">Login</button>
      </div>
      <div id="upload" style="display: none;">
        <div class="mb-3">
          <input type="file" class="form-control" id="fileInput" />
        </div>
        <button class="btn btn-success" onclick="uploadFile()">Upload File</button>
        <div class="progress mt-3" style="display: none;" id="uploadProgressBarContainer">
          <div class="progress-bar" role="progressbar" style="width: 0%;" aria-valuenow="0" aria-valuemin="0" aria-valuemax="100" id="uploadProgressBar"></div>
        </div>
        <div id="uploadStatus" class="mt-2"></div>
        <button class="btn btn-danger mt-3" onclick="logout()">Logout</button>
        <div id="fileLink" style="display: none;">
          <h4 class="mt-3">Direct Link:</h4>
          <a id="downloadLink" target="_blank"></a>
        </div>
      </div>
      <button class="btn btn-info mt-3" id="copyToClipboardBtn" data-clipboard-target="#downloadLink" style="display: none;">Copy to Clipboard</button>
      <img id="uploadedImage" class="img-fluid mt-3" style="max-height: 200px; display: none;" />
      <div id="fileList" style="display: none;">
        <h2 class="mt-3">Uploaded Files</h2>
        <ul id="filesList" class="list-group">
          <li class="list-group-item">
            <div class="d-flex justify-content-between align-items-center">
              <div class="me-3">
                <img id="thumbnailImage" class="img-fluid" style="max-height: 100px; display: none;" />
                <a href="#" class="me-3" target="_blank"></a>
              </div>
            </div>
          </li>
        </ul>
      </div>
    </div>
    <!-- Bootstrap JS -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.2.0/dist/js/bootstrap.bundle.min.js"></script>
    <!-- Firebase SDK -->
    <script src="https://www.gstatic.com/firebasejs/8.0.0/firebase-app.js"></script>
    <script src="https://www.gstatic.com/firebasejs/8.0.0/firebase-auth.js"></script>
    <script src="https://www.gstatic.com/firebasejs/8.0.0/firebase-storage.js"></script>
    <script src="https://www.gstatic.com/firebasejs/8.0.0/firebase-database.js"></script>
    <!-- Copy To Clipboard JS -->
    <script src="https://cdn.jsdelivr.net/npm/clipboard@2.0.8/dist/clipboard.min.js"></script>
    <!-- CUSTOM SCRIPT & JANGAN DIGANTI URUTAN INI !!! -->
    <script src="js/config.js"></script>
    <script src="js/copyToClipboard.js"></script>
    <script src="js/login.js"></script>
    <script src="js/uploadFile.js"></script>
    <script src="js/updateProgressBar.js"></script>
    <script src="js/listUploadedFiles.js"></script>
    <script src="js/deleteFile.js"></script>
  </body>
</html>
```
{{% /spoiler %}}

2. Copy dan pastekan kode berikut ke `style.css`

{{% spoiler text="style.css" %}}
```css
#progressBar {
  width: 100%;
  height: 20px;
  background-color: #ddd;
  margin-top: 10px;
}

#uploadStatus {
  margin-top: 10px;
}
```
{{% /spoiler %}}

3. Copy dan pastekan kode berikut ke `config.js`. Pada `firebaseConfig` ganti dengan config yang kamu dapatkan di `langkah 9` pada `Membuat Project dan Mendapatkan API Key`

{{% spoiler text="config.js" %}}
```js
// Ganti value nya dengan config kamu masing-masing
const firebaseConfig = {
  apiKey: "AIzaSyBhW6y8EfqKYUyP7Di4NZ8TmbhTxQnS5eg",
  authDomain: "fir-upload-86d92.firebaseapp.com",
  databaseURL: "https://fir-upload-86d92-default-rtdb.asia-southeast1.firebasedatabase.app",
  projectId: "fir-upload-86d92",
  storageBucket: "fir-upload-86d92.appspot.com",
  messagingSenderId: "531276002779",
  appId: "1:531276002779:web:b14a763ec93a1569b1a3fe"
};

// Inisialisasi Firebase
firebase.initializeApp(firebaseConfig);

// Memanggil layanan firebase yang akan kita gunakan
const auth = firebase.auth();
const storage = firebase.storage();
const database = firebase.database();
```
{{% /spoiler %}}

4. Copy dan pastekan code berikut ke `copyToClipboard.js`

{{% spoiler text="copyToClipboard.js" %}}
```js
// Setelah menginisialisasi Firebase
const clipboard = new ClipboardJS('#copyToClipboardBtn');

// Tambahkan event listener untuk melihat success atau error saat menyalin
clipboard.on('success', function (e) {
  console.log('Teks berhasil disalin ke clipboard:', e.text);
  e.clearSelection();
});

clipboard.on('error', function (e) {
  console.error('Kesalahan menyalin teks ke clipboard:', e.trigger);
});

// Fungsi untuk menyalin tautan ke clipboard
function copyToClipboard(element) {
  const fullLink = element.href;
  
  // Buat element input sementara
  const tempInput = document.createElement('input');
  tempInput.value = fullLink;
  document.body.appendChild(tempInput);
  
  // Pilih dan salin teks
  tempInput.select();
  document.execCommand('copy');
  
  // Hapus element input sementara
  document.body.removeChild(tempInput);
  
  // Tampilkan pesan di console (opsional) 
  console.log('Tautan disalin ke clipboard:', fullLink);
}
```
{{% /spoiler %}}

5. Copy dan pastekan kode berikut ke `uploadFile.js`

{{% spoiler text="uploadFile.js" %}}
```js
let fileUploadProgress = 0;

function uploadFile() {
  const fileInput = document.getElementById('fileInput');
  const file = fileInput.files[0];

  if (file) {
    let customFolder = '';

    // Periksa jenis file dan atur folder khusus sesuai dengan file yang di upload
    // Gambar akan diupload ke folder *images* sedangkan mp4 di folder *videos*
    if (file.type.startsWith('image/')) {
      customFolder = 'images';
    } else if (file.type === 'video/mp4') {
      customFolder = 'videos';
    } else {
      console.error('Jenis file tidak didukung!');
      return;
    }

    const storageRef = storage.ref();
    const fileRef = storageRef.child(`${customFolder}/${file.name}`);

    // Unggah file ke Firebase Storage
    const uploadTask = fileRef.put(file);

    // Perbarui progressbar
    uploadTask.on(
      'state_changed',
      (snapshot) => {
        const progress = (snapshot.bytesTransferred / snapshot.totalBytes) * 100;
        updateProgressBar(progress);
      },
      (error) => {
        console.error('Error mengunggah file:', error);
      },
      () => {
        // Unggah berhasil
        fileRef.getDownloadURL().then((downloadURL) => {
          console.log('File berhasil diunggah!');

          // Tambahkan informasi file ke Realtime Database
          const database = firebase.database();
          const filesRef = database.ref('uploadedFiles');

          // Buat unique key untuk file
          const fileKey = filesRef.push().key;

          // data file yang disimpan di database
          const fileData = {
            name: file.name,
            type: file.type,
            downloadURL: downloadURL,
            timestamp: firebase.database.ServerValue.TIMESTAMP,
          };

          // Tambahkan data file ke database
          filesRef.child(fileKey).set(fileData);

          // Tampilkan gambar atau video yang diunggah
          if (file.type.startsWith('image/')) {
            const uploadedImage = document.getElementById('uploadedImage');
            uploadedImage.src = downloadURL;
            uploadedImage.style.display = 'block';
          } else if (file.type === 'video/mp4') {
            // Tangani tampilan video jika diperlukan
          }

          // Menampilkan direct link pada file yang di upload
          document.getElementById('downloadLink').href = downloadURL;
          document.getElementById('downloadLink').innerText = downloadURL;
          document.getElementById('fileLink').style.display = 'block';

          // Reset proggress bar
          updateProgressBar(0);

          // Tampilkan tombol "Salin ke Clipboard"
          const copyToClipboardBtn = document.getElementById('copyToClipboardBtn');
          copyToClipboardBtn.style.display = 'block';
        });
      }
    );
  } else {
    console.error('Tidak ada file yang dipilih!');
  }
}
```
{{% /spoiler %}}

6. Copy dan pastekan kode berikut ke `updateProgressBar.js`

{{% spoiler text="updateProgressBar.js" %}}
```js
function updateProgressBar(progress) {
  const progressBar = document.getElementById('uploadProgressBar');
  progressBar.style.width = progress + '%';
  progressBar.setAttribute('aria-valuenow', progress);
  progressBar.innerText = `${progress.toFixed(2)}%`;
  document.getElementById('uploadProgressBarContainer').style.display = 'block';
  document.getElementById('uploadStatus').innerText = `Upload Progress: ${progress.toFixed(2)}%`;
}
```
{{% /spoiler %}}

7. Copy dan pastekan kode berikut ke `listUploadedFiles.js`

{{% spoiler text="listUploadedFiles.js" %}}
```js
function listUploadedFiles() {
  const filesList = document.getElementById('filesList');

  // Dapatkan data dari folder 'images' dan 'videos' di firebase storage
  const imagesFolder = 'images';
  const videosFolder = 'videos';
  const imagesRef = storage.ref(imagesFolder);
  const videosRef = storage.ref(videosFolder);

  // Fungsi untuk list file yang sudah kita upload
  const addFileToList = async (fileRef, folder) => {
    // daftar grup untuk setiap file
    const listItem = document.createElement('li');
    listItem.className = 'list-group-item';

    // Tampilkan nama file dan buat thumbnail untuk gambar
    if (fileRef.name.match(/\.(jpg|jpeg|png|gif)$/i)) {
      try {
        const thumbnailUrl = await fileRef.getDownloadURL();
        const thumbnailImage = document.createElement('img');
        thumbnailImage.src = thumbnailUrl;
        thumbnailImage.className = 'img-fluid';
        thumbnailImage.style.maxHeight = '80px';
        thumbnailImage.style.marginRight = '10px';
        thumbnailImage.style.borderRadius = '8px';
        listItem.appendChild(thumbnailImage);
      } catch (error) {
        console.error('Error mendapatkan Thumbnail URL:', error);
      }
    }

    // Buat direct link untuk file
    const fileLink = document.createElement('a');
    fileLink.href = await fileRef.getDownloadURL();
    fileLink.target = '_blank';
    fileLink.innerText = fileRef.name; // Tampilkan nama file sebagai konten teks
    
    // Buat atribut khusus ke tautan untuk mengidentifikasinya nanti
    fileLink.setAttribute('data-filepath', fileRef.fullPath);

    // Buat tombol "Copy to Clipboard"
    const copyButton = document.createElement('button');
    copyButton.className = 'btn btn-info ms-3';
    copyButton.innerText = 'Copy to Clipboard';
    copyButton.addEventListener('click', () => copyToClipboard(fileLink));

    // Buat tombol hapus
    const deleteButton = document.createElement('button');
    deleteButton.className = 'btn btn-danger ms-3';
    deleteButton.innerText = 'Delete';
    deleteButton.addEventListener('click', () => deleteFile(fileLink));

    // Buat link, copy code, dan delete button
    listItem.appendChild(fileLink);
    listItem.appendChild(copyButton);
    listItem.appendChild(deleteButton);

    // List files
    filesList.appendChild(listItem);
  };

  // Daftar semua item di folder 'images'
  imagesRef.listAll().then((imagesResult) => {
    imagesResult.items.forEach(async (imageRef) => {
      await addFileToList(imageRef, imagesFolder);
    });
  }).catch((error) => {
    console.error(`Error listing files in folder ${imagesFolder}:`, error);
  });

  // Daftar semua item di folder 'videos'
  videosRef.listAll().then((videosResult) => {
    videosResult.items.forEach(async (videoRef) => {
      await addFileToList(videoRef, videosFolder);
    });
  }).catch((error) => {
    console.error(`Error listing files in folder ${videosFolder}:`, error);
  });
}
```
{{% /spoiler %}}

8. Copy dan pastekan kode berikut ke `deleteFile.js`

{{% spoiler text="deleteFile.js" %}}
```js
function deleteFile(fileLink) {
  // Dapatkan nilai atribut khusus untuk mengidentifikasi tautan
  const filePath = fileLink.getAttribute('data-filepath');

  // Referensi ke file di penyimpanan
  const fileRef = storage.ref(filePath);

  // Hapus file dari penyimpanan
  fileRef.delete().then(() => {
    console.log('File berhasil dihapus dari penyimpanan!');
    
    // Hapus file dari Realtime Database
    const database = firebase.database();
    const filesRef = database.ref('uploadedFiles');

    // Temukan data file di database berdasarkan path file
    filesRef.orderByChild('downloadURL').equalTo(fileLink.href).once('value', (snapshot) => {
      snapshot.forEach((childSnapshot) => {
        // Hapus data file dari database
        filesRef.child(childSnapshot.key).remove().then(() => {
          console.log('Data file berhasil dihapus dari database!');
        }).catch((error) => {
          console.error('Error menghapus data file dari database:', error);
        });
      });
    });

    // Hapus file dari daftar yang ditampilkan
    const listItem = fileLink.parentElement;

    if (listItem) {
      listItem.remove();
    } else {
      console.error('Elemen daftar tidak ditemukan untuk dihapus.');
    }
  }).catch((error) => {
    console.error('Error menghapus file dari penyimpanan:', error);
  });
}
```
{{% /spoiler %}}

9. Copy dan pastekan kode berikut ke `login.js`

{{% spoiler text="login.js" %}}
```js
auth.onAuthStateChanged(user => {
  if (user) {
      document.getElementById('login').style.display = 'none';
      document.getElementById('upload').style.display = 'block';
      document.getElementById('fileList').style.display = 'block'; // Tampilkan bagian daftar file
      listUploadedFiles(); // Menampilkan daftar file yang diunggah saat sudah ter-authentikasi
  } else {
      document.getElementById('login').style.display = 'block';
      document.getElementById('upload').style.display = 'none';
      document.getElementById('fileList').style.display = 'none'; // Sembunyikan bagian daftar file
  }
});

function handleKeyPress(event, action) {
  if (event.key === 'Enter') {
    event.preventDefault();
    if (action === 'login') {
      login();
    }
  }
}

function login() {
  const emailInput = document.getElementById('emailInput').value;
  const passwordInput = document.getElementById('passwordInput').value;

  // Login menggunakan email dan password
  auth.signInWithEmailAndPassword(emailInput, passwordInput)
      .catch(error => {
          console.error('Error saat login:', error);
      });
  // Code ini bisa dihapus karena menampilkan password di console
  console.log('Email:', emailInput);
  console.log('Password:', passwordInput);
}

function logout() {
  auth.signOut();
  clearDisplay();
}

function clearDisplay() {
  // Hide element ketika logout
  document.getElementById('uploadProgressBarContainer').style.display = 'none';
  document.getElementById('uploadStatus').innerText = '';
  document.getElementById('uploadedImage').style.display = 'none';
  document.getElementById('fileList').style.display = 'none';
  document.getElementById('fileLink').style.display = 'none';
  document.getElementById('copyToClipboardBtn').style.display = 'none';

  // Bersihkan daftar file
  const filesList = document.getElementById('filesList');
  while (filesList.firstChild) {
    filesList.removeChild(filesList.firstChild);
  }
}
```
{{% /spoiler %}}

## Test website secara local
Karena ini static website jadinya kita bisa menjalankannya secara lokal, tidak perlu server hanya memerlukan browser versi terbaru saja.

1. Buka `index.html` pada browser kamu
2. Login dengan Email/Password yang sudah dibuat dilangkah 6 pada [Membuat User](#membuat-user)

![Figure 30](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgkvwGPtkvMksVla5xrPk_I2REddfsuEAITCfkwZgiwAZA3X_2WjpxHv0HHBajywq8Fj384tpUCTykgU0irOkxyP0KQj3TYSqDH_80LWSk8Zc6ayUhu1fdvyneW870-OBMriMUlY65AQb3y_3iPRQCl_K-RIcGJiz2FkOtz0Ha0PP8wLoj_5k6h6lh64frT/s0/rmdhnreza.my.id.firebase.website.32.png)

3. Kamu coba untuk upload file dengan cara klik **Choose File** dan setelah itu klik **Upload File**

![Figure 31](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhhr_dSsWJmbmZlyMY0T_tUOis1dgCFhWT9LFmNQD8sp9swghXfAQA8U0aUszoSdEr4wFJQ6JgOMTQ-AcAbT5dohwiMT5FjIaGrY1XuFvrkjJVp4B4k6oxAUu2Vu1j_mK454j1RhkHigrWh1oq3MhyeTRrahqc_0ktSssQyg9Vs3pB_NZqEgHY4Er3g8-ik/s0/rmdhnreza.my.id.firebase.website.33.png)

4. Jika berhasil maka akan tampil seperti ini

![Figure 32](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEg7M9jIr7Vqv9tz-el6cpra5evc-6Vob3klmOJLbRJwyFyNhfHRN54zSU4BOqEPygUUVI0OLMMtUEbXfxROtH_4R6mpBCIsL-neaMUpRO4UJrFB_zq-2ulMJjeUk8eHskZIkTzu-_H1FeWtCSejznZGlEhU_1IOd4OiAaNQhWEyyw6SyPlkCfW7UYRub92x/s0/rmdhnreza.my.id.firebase.website.34.png) ![Figure 33](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEj9yg-7EFPMNuQ91PvdiraqWS3HWB7SnZZv9g6dCSWlJAULVsWvITPHQDrIBziHgRwaCt-v3fHtMVOEi9RLJknnJFjneg9ByVPpR1MsBOG2xqPK4zxXrtSIAZLJLn0ss5lslKnIwc0Cpp6-OT2SH5oYmlM3Pk98aBKE58kkglvvqhtGMOLrX0P-FxuEopV-/s0/rmdhnreza.my.id.firebase.website.35.png)

5. Cek firebase storage folder images

![Figure 34](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgreD-CHmRKWbese-c2JibmNbbTaUurMaXov7a7sw7nVzktIaMUAGuvlIXgOQU61Baa9-8EIhcxmmUNzcWOr4lYEhVaXy4iSKTFNSXqUjgFA__-9UVow0pG1eAmzoc7ONPrLjLAcsV_PVBTCRDoqlN7Es0mtB6UkDOmjIUve7Sn18xsLZX0Xh_9KPiJtvoj/s0/rmdhnreza.my.id.firebase.website.36.png)

6. Cek juga database nya

![Figure 35](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEi3kOXtCspQalY8ykMY-0SfiaDDE3GIHHFtn1oJwNuDOL74VTCfIjN3UKGs5hRXwgjUIo8GPLL85y2uFhoypHvn5saKKjZJkZY7kQz5rMa_d7CQO2XRlxLB6df4IBs5s9JfKChL6CYvoD-6DffsqXECzgYGKyjlj-6KN18mRPGc8pqQ_zWRxi3MDCpl90Ye/s0/rmdhnreza.my.id.firebase.website.37.png)

7. Coba delete file yang sudah diupload

![Figure 36](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgV95X5nVrgOxgl3TpQ1LsNphosLaXurdamOWdtGsto98-Q5lb6TibvzLVKlzuiaI0pjg47RD5eYHIPl2a8rwKPCXsy3VP2keyTLUPaEVO_BlGjKcIXTfLE1QijdcDW5q_mNgbGAw7DR0h-C4_6x9CKrEgVZYSm_w_MVLN7c9huVkEhnZ6H9uknXTlyslNK/s0/rmdhnreza.my.id.firebase.website.38.png)


Itulah tutorial Langkah Mudah Membuat Website Upload Sederhana dengan Firebase, jika kamu ingin membuat website ini bisa diakses, kamu bisa deploy ke firebase hosting.

{{% adsense %}}