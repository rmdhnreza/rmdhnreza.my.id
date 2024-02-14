---
title: "Enable Atau Disable Windows Defender Windows 10"
date: 2021-01-26T19:38:52+07:00
categories: ["Tutorial", "Windows 10"]
tags: ["Tutorial", "Windows 10"]
description: 'Mulai Windows 10 versi 2004 Windows Defender diganti namanya menjadi Microsoft Defender Antivirus, Sebetulnya Microsoft Defender Antivirus akan nonaktif sendiri jika kalian menginstall Antivirus pihak ketiga, seperti: ESET, Norton, dll.'
summary: 'Mulai Windows 10 versi 2004 Windows Defender diganti namanya menjadi Microsoft Defender Antivirus, Sebetulnya Microsoft Defender Antivirus akan nonaktif sendiri jika kalian menginstall Antivirus pihak ketiga, seperti: ESET, Norton, dll.'
image: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgNt9DpgKPxflrbnYq1EiEI4P6Y6IvGA3JSS6bPryXjFoZxdu0Ny7qGTe1dn30lbAel_ZChMiMfDrko85txVSjhZF4VDfNqhuHXHOtBWZsXDanh5KLsBbo9wl9J2V-ldSHm3dgE72xbyDwRigQFLue4KEktFF_-XCwiwcMo_UpEm4wkXdM2ksB2AF193Eiv/s80-rw/defender-logo.png
ThumbSchema: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgNt9DpgKPxflrbnYq1EiEI4P6Y6IvGA3JSS6bPryXjFoZxdu0Ny7qGTe1dn30lbAel_ZChMiMfDrko85txVSjhZF4VDfNqhuHXHOtBWZsXDanh5KLsBbo9wl9J2V-ldSHm3dgE72xbyDwRigQFLue4KEktFF_-XCwiwcMo_UpEm4wkXdM2ksB2AF193Eiv/s0/defender-logo.png
---

{{% adsense %}}

Mulai Windows 10 versi 2004 Windows Defender diganti namanya menjadi Microsoft Defender Antivirus, Sebetulnya Microsoft Defender Antivirus akan nonaktif sendiri jika kalian menginstall Antivirus pihak ketiga, seperti: ESET, Norton, dll.

__Note:__ Jika kalian menggunakan Windows 10 Home, kalian gunakan cara ke dua yang menggunakan regedit (registry editor).

Sebelum menonaktifkan Defender Antivirus, pastikan kalian Off kan terlebih dahulu __Microsoft Defender Antivirus Tamper Protection__

Caranya:

{{% adsense %}}

1. Buka __Windows Security__, dan click/tap di __Virus & threat protection__ icon.

![Tamper Protection](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjIiAzB52xTWRqZBw_ToK4tgcvg5Mbvrr2VWSq2ONNA3N8TyXVB53NmpTkCt-Xb3FUd8xwJOZYV56_DBD8ykumJARfVmRieN82QLNtdAIeBxiwy9r1CYmtQtyN7bznw33g0ofw05OCbHmuFZIAqxhB_sjcQ9IR12oEH-K0GCqtl2gs29Qd-iVCca5dtP10k/s0/tamper-protection-1.jpeg)

2. Click/tap on the __Manage settings__ link dibawah __Virus & threat protection settings__

![Tamper Protection](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjiPMaSuohuo2vz9RamauPY953s5JQ4VdPKGLwIrCw9e5kJ18aJ4POVXDUhu1Yo77Ygxzj9mzuNEGlHoH8zaq6O2dYvxj36ZouRqMSrT5ITrTXEjZNFiP8BxMVk3MeM5ZdXrX7o-eioN-fMdgwStpj0mdHf6EPx97qy5zCnWmlejBfGDcBGUpcF7AYe8ZTa/s0/tamper-protection-2.jpeg)

3. Scroll sampai bawah dan Off kan __Tamper Protection__

![Tamper Protection](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEg1ZzdcN4o9BZf5xbhm-9zPKkj4Rr0-K2uOWbs0x-h0pcYqdAYduFl1rNJ5KXkjAQmwG95fZFlwCnZ0Nwrd1xvJf0rMTMDDZArbpQz0WGsQLDZW_rhWQXcT-FrrgDkAQ121z4f8wNTLxrgLxAxEflk2-eO-ImWyQk-URvuscQzya8NOWYsL2d4GyWWgZY09/s0/tamper-protection-3.jpeg)

Jika sudah, ikuti langkah selanjutnya.

{{% adsense %}}

#### Cara 1: Menggunakan Local Group Policy Editor
1. Buka __Local Group Policy Editor__, caranya kalian tekan shorcurt pada keyboard __Win + R__, setelah itu masukan `gpedit.msc` atau Kalian juga bisa menggunakan fitur __Search__
2. Di panel sebelah kiri __Local Group Policy Editor__, Kalian masuk ke

Untuk Windows 10 version 1909 dan sebelumnya
Computer Configuration\Administrative Templates\Windows Components\Windows\Defender Antivirus

Untuk Windows 10 version 2004 dan selanjutnya
Computer Configuration\Administrative Templates\Windows Components\Microsoft Defender Antivirus

![Local Group Policy Editor](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgZIG3BgLZelVtbE3OSI8Zcoar1CuxI8BWDOaN5wqMsbEoD4fq09NWyWIgQszetvfS6xiJlFgpcbHBKlv5dtxCwl6nMoj_ejjUZZ5obwN4EiJ_TFDGU47wUQvmlmZN5G22xc_nU4kbrB9ax7iQu2qS2w1TRc-RFUR3hKjjQVvS5lIH22pP4N2aouKyUQmVk/s0/gpedit-1.jpeg)

3. Di Panel sebelah kanan __Windows Defender Antivirus__ atau __Microsoft Defender Antivirus__, double click/tap di __Turn off Windows Defender Antivirus__ atau __Turn off Microsoft Defender Antivirus__ Untuk mengedit policy nya
4. Untuk Disable Defender Antivirus kalian pilih __Enabled__
5. Sedangkan untuk Enable Defender Antivirus kalian pilih __Not Configured__ atau __Disabled__

![Local Group Policy Editor](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEga4cWvbPZawrHQqMA4B1hPpRbWXr1SC1vL80VoRf642tTU8mMYgXyDqeg7FXPOVgRmHKaciGlQmm5fnouTJxnd_N2Hap-zUmQP60iK7QUyArRRA6OQWkUUTVWRkq6d2IojPLy9IWqbWWDzz5eab-0V30Rl8aFiGH8FKGd72Kfb-tbTNjqnMBSejORxU8Ur/s0/gpedit-2.jpeg)

#### Cara 2: Menggunakan Registry Editor (Regedit)

{{% adsense %}}

File .reg dibawah ini mengubah value DWORD registry key berikut\
HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows Defender\
DisableAntiSpyware DWORD\
0 = Disable\
1 atau delete = Enable

1. Enable Defender Antivirus (Default Settings)
2. Disable Defender Antivirus
   * [Download Reg File](https://www.tenforums.com/attachments/tutorials/130449d1492353257-turn-off-windows-defender-windows-10-a-turn_on_windows_defender_antivirus.reg)
3. Save file di Desktop atau dimana saja
   * [Download Reg File](https://www.tenforums.com/attachments/tutorials/130448d1492353257-turn-off-windows-defender-windows-10-a-turn_off_windows_defender_antivirus.reg)
4. Double click/tap di file .reg yang kalian download.
5. Ketika muncul UAC kalian klik Yes, dan klik OK lagi untuk menerapkan konfigurasi regedit nya.
6. Restart Explorer atau Sign Out & Sign In atau Kalian Restart PC kalian. Untuk menerapkan konfigurasi yang sudah di setting di **Regedit**

Source Tutorial: [tenforums](https://www.tenforums.com/tutorials/5918-how-turn-off-microsoft-defender-antivirus-windows-10-a.html)

{{% adsense %}}
