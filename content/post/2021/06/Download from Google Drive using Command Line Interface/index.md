---
title: "Download from Google Drive using Command Line Interface (CLI)"
date: 2021-06-08T17:30:13+07:00
description: "Download from Google Drive using Command Line Interface (CLI), using curl, Linux, MacOS, Windows"
categories: ["Linux", "Windows", "Tutorial"]
tags: ["Linux", "Windows", "Tutorial"]
keywords:
  [
    "Download from Google Drive using Aria2",
    "Download from Google Drive using CLI",
    "Download from Google Drive using Command Line Interface (CLI)",
    "Download from Google Drive using Curl",
    "Download from Google Drive using Wget",
    "Download from Google Drive Without Limitation",
  ]
description: 'In this tutorial, I will share How to Download a File in Google Drive using Command Line Interface, using this script you can download a file without file size limitation'
summary: 'In this tutorial, I will share How to Download a File in Google Drive using Command Line Interface, using this script you can download a file without file size limitation'
image: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhwt-aIrDfkicVex80qrbDItqFfgyBTs2wC8x83xh6zK4tHZo1DNzL78bDUJpSn3HvlHnhbzQ01IsYCqkqYqiv_BSsdZvTqYWmKPJpbC8cwPreQ7ryVzxBU1LJev9XvWudfSxA_2GFvDAmuyF-JX9jKJJ0XBCLNJ4XqZFMi2WrfBmWjJHXepFRghbbM2eF4/s80-rw/Google_Drive_logo.png
ThumbSchema: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhwt-aIrDfkicVex80qrbDItqFfgyBTs2wC8x83xh6zK4tHZo1DNzL78bDUJpSn3HvlHnhbzQ01IsYCqkqYqiv_BSsdZvTqYWmKPJpbC8cwPreQ7ryVzxBU1LJev9XvWudfSxA_2GFvDAmuyF-JX9jKJJ0XBCLNJ4XqZFMi2WrfBmWjJHXepFRghbbM2eF4/s0/Google_Drive_logo.png
---

{{% adsense %}}

<svg xmlns="http://www.w3.org/2000/svg" class="icon icon-tabler icon-tabler-brand-google-drive" width="200" height="200" viewBox="0 0 24 24" stroke-width="1.5" stroke="CurrentColor" fill="none" stroke-linecap="round" stroke-linejoin="round" style="display: block;margin: auto;">
    <path stroke="none" d="M0 0h24v24H0z" fill="none"></path>
    <path d="M12 10l-6 10l-3 -5l6 -10z"></path>
    <path d="M9 15h12l-3 5h-12"></path>
    <path d="M15 15l-6 -10h6l6 10z"></path>
</svg>

In this tutorial, I will share How to Download a File in Google Drive using Command Line Interface, using this script you can download a file without file size limitation, maybe you can use **[gdown](https://github.com/wkentaro/gdown)** but **[gdown](https://github.com/wkentaro/gdown)** sometimes still error if you **[download a big file](https://github.com/wkentaro/gdown/issues/26)** from Google Drive

## Before Download a Big File, Create OAuth Authentication First
This script also same if you don't configure first, can't download a big file from Google Drive, so you must create **OAuth Credentials** first

1. Login to **[Google Developer Console](https://console.developers.google.com/)** and Create Project first 
    * Note: If you don't have project Click on **Select Project** → **New Project**

{{< spoiler text="Click to Show Image" >}}
![Create Project](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgKiiqWLiCdF5eRRE5Lq0DxOW6d7XOul1EVAjPBBo_pWOGoWB8fShP2neYsBNHsA3rMCDZFtKSaEns1SH3uqeXdYN7eI73BxYCbyPRqZzMvUXJHpIixqGwvfhMiQ9TgJe5kjgBquvOtukrF4zcTc_wI40MES70bo40bWzBJI5AA7DG6whZNSKNwsHmLl6J8/s0/rmdhnreza.my.id.google.drive.cli.1.jpeg) | ![Create Project](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEghqFBsVIYg1aK0T06OeLxX0HbZ9LqahgoHHJoRbZQ_WFl5ZRSzuLFNi-dO6b6Fj5zx9dADJQBxN80FR5ym9YanxdDbYZFgsOQCTQyRHHAFRCmsyOuVOvCYFL3IhE2XDJ8iIBx8UAWpGwumlpcmg9h2XCS44ikRHWJROUnpDTb8PhcRq8XrmlcW74H9ICRN/s0/rmdhnreza.my.id.google.drive.cli.2.jpeg)
{{< /spoiler >}}

2. Click Hamburger menu on the left → **Select API & Services** → **Select Library**

{{< spoiler text="Click to Show Image" >}}
![API & Services](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjfYxW0BSR0zGRmYNddYyUfFyNN9dY7jIB8h-aGv81yk_0lN7TbcRMCN7YxJevHZFYRmz3Z35GHpCo3CHXV1SIZ80dNl-mwN5qA8Dd1mTRZuc2nw4e2b5FzczGRgTqu-55O89By6HeseA1BPj7NNtaF4WYVA05952fspspftRotIyf7i0LdiMs2br6LONPo/s0/rmdhnreza.my.id.google.drive.cli.3.jpeg)
{{< /spoiler >}}

{{% adsense %}}

3. Search for **Google Drive API** and **Enable Google Drive API**

{{< spoiler text="Click to Show Image" >}}
![Enable Drive API](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgdYOAPqS0rK75_Wtiit0aXmvZEG0Yvqt0QYHvnuz789RlixBEqFQc30rWKgr4YDghgf7MRP2iPTjxOsw4-dWqKoHRR46L1fTNwuh7cXKfI7zxZkamYlek1gCZ5xJkdCWCtnw3uZOlHEvDHtnbNYEVX8KtFicw_VAaIf8Xi4DBwc2QWzA2XnZvQyYVMjpro/s0/rmdhnreza.my.id.google.drive.cli.4.jpeg) | ![Enable Drive API](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgbW0E9yDsQe5lDAEgqrRW7MZln-oFEUjgXCScUcLMvKu-07Lv-hbx9LjLngykdciUMck1CPUpUtdC-0uCxZVGt3MYm5ZiIGCkunxC3UZRbvSaf9ghQfEBoAE9LgXf4bjgECLK4MmiNHiJ1UrvBZPnn7rgJjxCx-GiNKFR4vGrDdYv6HXSAxGGJQ-ojHXJM/s0/rmdhnreza.my.id.google.drive.cli.5.jpeg) 
{{< /spoiler >}}

4. Click Credentials on left pane and Click **+ CREATE CREDENTIALS** and select **OAuth Client ID**

{{< spoiler text="Click to Show Image" >}}
![Create Credentials](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEimjiQAwVuMCN1tx9xekhEMQBPwPGz4psrY90UgWjXLDhgwv8s1a8r26bFYyjKAaoVDEzXvNQ_Ma8j41MNhBpNkVVJyAGBBeHTZdR_gQ2hUyaahTb4VJouL3BHRBMpNy3_r-9xoVUe1r0HfmvgmbJ7K1RzQ_PMbi8ubd0pBrNwMDGTQCWHBnqFg8s6jcIdY/s0/rmdhnreza.my.id.google.drive.cli.6.jpeg) | ![Create Credentials](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEg6bQwr_Bklh7UNCg1-IFNICdL0sopJlGipt63UF8mivCiY8NmSSxuxVQqQGCZS1hp_sZm5aqDepGkvwjJT96zNxTYhS3IO8z3OrVVeooppFtyQ-LC5a1An3DULpO455ujBZjK3U8oJIFlLpPPJhVFh834Ridq57qEMna5_tHceCqlqV9ro7vV2z05S465u/s0/rmdhnreza.my.id.google.drive.cli.7.jpeg) 
{{< /spoiler >}}

**Note:** If you face this error, click on **CONFIGURE CONSENT SCREEN**

{{< spoiler text="Click to Show Image" >}}
![CONFIGURE CONSENT SCREEN](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgtWR6VYzZEjW7YU23Df9Cs1XRzo4XdrpVBxlYlS9URH1uTqJhm82r6gK_54DuFS40wa5g_r5BHYfhY9Gt59O4r-BmYLNuF9gX7lPvPA96XDIxtZChdQAe5X3w_4M_3pAfGCR4vc5S3hsn9OwOIPDs2q16YW_C_C9b1SgcrXoh4svq3OYOf3pPb7ziYHeeJ/s0/rmdhnreza.my.id.google.drive.cli.8.jpeg) 
{{< /spoiler >}}

  * Select **External** and click **CREATE**

{{< spoiler text="Click to Show Image" >}}
![CONFIGURE CONSENT SCREEN](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEguZQsufEuOMTZxzZN0xccaNqWJNYnMDTC0Dox2BMI5w47K4ngkMUm6v5qu0j4Fe3QfWTM30_sKIwiLS5p9OZwBu1JFcKe6mrJAS_iK-k5fVlFZKYeJRiOZXBiqOrKtKpoiKkXhISrGTs5WNLWJKitQoMGNe_7cP7yS_-9jUb0tIBXLlsi7Dz3Jmkl-5JaE/s0/rmdhnreza.my.id.google.drive.cli.9.jpeg) 
{{< /spoiler >}}

{{% adsense %}}

  * Just fill in the section
    * App name *
    * User support email
    * Email addresses
  * Click **SAVE AND CONTINUE** until **Step 4** and **Click Publish** in the **Production** section
  * Back to Create Credentials
5. After select **OAuth Client ID**
    * Application type select **Desktop app**
    * Name fill whatever you want
    * Click **CREATE**
6. If success, you will get Client ID and Client Secret, **Save it**.

{{< spoiler text="Click to Show Image" >}}
![Client ID and Secret ID](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgb_3xdLORo69juIofRe6r4mPBnz3Jbq6zRTPBbzORmzLGgjEnONqs4dZK4zPAI4zrdKRn9xMFwNH9Ly-K8rnrVsnvG_vbWgdm1Rjkn5pVIs_kihoDvL7Jod0lRLUoghFbQgsMCJy-itZlzM3RaIuQlBebZNQIiPm_47EPVz0VBbA_2ZQzxegF1-kGj8pvj/s0/rmdhnreza.my.id.google.drive.cli.10.jpeg) 
{{< /spoiler >}}

## Download a File From Google Drive
1. This script you can find it in **[Official GitHub Repository](https://github.com/Akianonymus/gdrive-downloader/)**
2. To install this script, just execute command
```ruby
curl -Ls --compressed https://drivedl.cf | sh -s
```
alternatively, you can use the original github url instead of https://drivedl.cf
```ruby
curl -Ls --compressed  https://github.com/Akianonymus/gdrive-downloader/raw/master/install.sh | sh -s
```
3. This script installed at `${HOME}/.gdrive-downloader/`
4. To Download a File from Google Drive (Especially big file) use command
```ruby
gdl -o driveID
```

{{% adsense %}}

{{< spoiler text="Click to Show Image" >}}
![Download File from Google Drive](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEi9M8pOADp_r6AaqhAjn8drBpT5oWC-eztel2BeFJRCV2C2ce82FSC_avZrnWw_WebYU9eeUFWJ0fEHASFcIWil4QJ9ofrYBGlK_w1Lv-EBSUSDR2gb3gyKT6DD-UkVpqZBButNHLO_AKdnCJll8FsKS5UfMNy4_7TAWRLfKBFVRHHCDF5_3F2r1WHUlDq-/s0/rmdhnreza.my.id.google.drive.cli.11.jpeg) 
{{< /spoiler >}}


5. And you will be asked to put (Only one time), and this config file saved in `${HOME}/.gdl.conf`
    * Client ID → Fill in the client ID with the one you created earlier
    * Client Secret → Fill in the client Secret with the one you created earlier
    * Refresh Token → Just blank and hit enter
    * And the link will appear, click on that link to get **authorization code**
{{< spoiler text="Click to Show Image" >}}
![Download File from Google Drive](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiOUKxsPr0Dt_wbZrVk5m5DP2izgUp3njwezfPwfEtb0FKTZmMLUXCu2E7P-S0oKa3pE7TQe5e99iGt1YijIkw4B8wx1dCvm0H8sciyKsrRjbMw0JPVtWtvggnAZmQ008l8GmitYhJ3rWtRKAwc6t51_Lg-QVUXCgplQfKLVJD0CWBcdtOX3mK_YxYfjscX/s0/rmdhnreza.my.id.google.drive.cli.12.jpeg)
{{< /spoiler >}}
      * Login with your Google Account
{{< spoiler text="Click to Show Image" >}}
![Login Google Account](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhyHSOsxbkcCdstjODs8ZikRecDt0r7OrQ6n8qz1Nzua1VKnI6jYsin61S1Kyu8UHL91nSEahw7J0YQOjrV1uisMvuJgvttshyphenhyphenGIxwVXBTTnDbizHQt-S1IMakZLlyPjNwyNxlEsBMMOl6E1EiFLhGH_0bzK9ZsimKybjrnhDYsVIQVv1j5G4mnBOV-ISZQ/s0/rmdhnreza.my.id.google.drive.cli.13.jpeg)
{{< /spoiler >}}
      * **In this case** Warning like this is normal, because app we create earlier is not verified by Google, so just click **show advanced** and click Go to **yourappname (unsafe)**
{{< spoiler text="Click to Show Image" >}}
![Warning](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhkRf-8r3ADPyyipq6tJ0Yw2hJOjXvy7R9hA3VPFOxAfExDe0OBuaWlm2GGeOOYEB_WG7AUzL6qic0MY6xRvotnYVTWPtfROi6EClkk7NrNN-8fXjK-1pWwExMTesnFmkkJJ__s5B_mVQoB2Ritjbk7BMn7MSVqh_FLckBJ4QQA6BWT4k_HW9_c2Jsj80uN/s0/rmdhnreza.my.id.google.drive.cli.14.jpeg)
{{< /spoiler >}}
      * Click Allow
{{< spoiler text="Click to Show Image" >}}
![Allow Apps](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEj-aPYfUypWttENPpuUAu2PZgi2EsZjOneOAT4VYi-LYExYWvgzCT-wP8bnuWzGYOdz5Wpu4ChZHJjIEL25vh8DXsJkRYGhQnl464BArCtkEHJqnVty3PBllo_CiNCPOg57_wrobXUxqKXE3Ja5YNA46WY-392SO24icfdtMTtjWLOLUx94TV8Y43D96lon/s0/rmdhnreza.my.id.google.drive.cli.15.jpeg)
{{< /spoiler >}}
      * Click Allow Again
{{< spoiler text="Click to Show Image" >}}
![Allow Apps](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjTM9WwkkDJ6ApVNsjM19cz650Pm7Bxe_eKA3R0tzWzLhVdEHocyqGcVOJZ5Gk2g-56AUMrx2GvykfDAhKusPbEB5vksuJZQU4E5TYjXyUPKsKEkmBuGEQuvXdn5Q-vcDchifazNwkVGWjwVJepRHBt8uc4Lh52735rbzoQOrEPq0pVGpndB_m-2OoopvFl/s0/rmdhnreza.my.id.google.drive.cli.16.jpeg)
{{< /spoiler >}}
      * And you get **authorization code** copy and paste to terminal console
{{< spoiler text="Click to Show Image" >}}
![Auth code](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEh9khBiCvq__4fuGCYMk7UBQBaz_WjPaPJ_c-q7s6NsWbXB1xXHK03uLxuqjpyivyYDtQ4ZID4Mmy0n2OtT2RuY2FQiAPkuhVK_JT9KUG0vK7En0Ga_epaDiuyUdBjqdwJQQe2kxZQBNAU8BH16Y7upCVg62WmmPyjjPVEZOAYL_bk3na5338sFGoin8T6e/s0/rmdhnreza.my.id.google.drive.cli.17.jpeg)
{{< /spoiler >}}
6. And file will be downloaded immediately

{{< spoiler text="Click to Show Image" >}}
![Download File](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjcL6p4soI5YkyrsdgHVJjv1KsXI0CpibYjFnBxUflqhU49pbTRBxFNhDoWSRa4DG6heD0HWEc5WyXOnPAA5rQ5aOmrGZdORuuHxPQsXfMrzF5lBQejUiy_bBIbZFnEQ4jIf5sSwF0OJs0C6A9e_y-sAcq0DqPP2P5dn9I8aa7sIRwG4TMGrXQ1FBCIl41n/s0/rmdhnreza.my.id.google.drive.cli.19.jpeg)
{{< /spoiler >}}

If you want to download a big file again, just use command `gdl -o driveID`  and will not be asked to enter the auth code.

For Documentation, you can see in [GitHub Repository](https://github.com/Akianonymus/gdrive-downloader/)

Special Thanks to: **[Akianonymus](https://github.com/Akianonymus)** for making a great script!

{{% adsense %}}
