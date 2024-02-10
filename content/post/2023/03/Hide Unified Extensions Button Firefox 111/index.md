---
title: 'Hide Unified Extensions Button Firefox 111'
date: 2023-03-22T10:00:00+07:00
description: 'Tutorial Hide Unified Extensions Button Firefox 111'
categories: ['Tutorial']
tags: ['Tutorial']
keywords:
  [
    'Remove Unified Extensions Button Firefox 109',
    'Tutorial Hide Unified Extensions Button Firefox 109',
    'Remove Unified Extensions Button Firefox 111',
    'Tutorial Hide Unified Extensions Button Firefox 111',
  ]
description: 'Remove Firefox View & Tab Manager Firefox 106'
summary: 'Remove Firefox View & Tab Manager Firefox 106'
image: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgLLrmW9XsjhLNq729L3Pq6-JMtposi_hJatBpaSkdpXJDmjT8hvEV_eOodM-LGtXfpgj3MrynwLJmiwU0AXx7eWP-GDYR-Qa8abHbRzEnoAa_c2MwOQnv0bkqAgjLNdQPVMZt04PJ32zoXXUjaA3iAZgJRmBS0S14Rdr_cizBKa5VOSVuYdJTlmP9JLvp1/s80-rw/firefox-logo.png
ThumbSchema: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgLLrmW9XsjhLNq729L3Pq6-JMtposi_hJatBpaSkdpXJDmjT8hvEV_eOodM-LGtXfpgj3MrynwLJmiwU0AXx7eWP-GDYR-Qa8abHbRzEnoAa_c2MwOQnv0bkqAgjLNdQPVMZt04PJ32zoXXUjaA3iAZgJRmBS0S14Rdr_cizBKa5VOSVuYdJTlmP9JLvp1/s0-rw/firefox-logo.png
---

{{% adsense %}}

![Figure 1](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEg94oSpjt5v_adK7mNeEh5ixesA0YRV6dOyL-SCva7SuCv606lH4i_tpweeNSCmeMyzDm-THNktFiOQRWtBswzSsCpHyR0i37Ewt2gs7wGfQ8xMmiMlERQB5b16jQRWq_01axALg0XRiwgI7IBJ5IO2kaMqE_fJCVMMgV_zMZSxXYLmf3yuy61dLIVu-cH4/s1600/hide.unified.extensions.button.firefox.109.1.jpg)

[Firefox 109.0](https://www.mozilla.org/en-US/firefox/109.0/releasenotes/) releases on **January 17, 2023**, the biggest change in this version is [Manifest Version 3 (MV3)](https://blog.mozilla.org/addons/2022/11/17/manifest-v3-signing-available-november-21-on-firefox-nightly/) extension support is now enabled by default ([MV2 remains enabled/supported](https://blog.mozilla.org/addons/2022/05/18/manifest-v3-in-firefox-recap-next-steps/)). This major update also ushers an exciting user interface change in the form of the [new extensions button](https://support.mozilla.org/kb/unified-extensions).

![Figure 2](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgNmx7SaSuwIDOMPNj4sswS_l-epHbjCNdI7E5gLM8Ub5sAUWX4dkqnqfL-IrjF1oe3xpMGaoEPKouR11DnvTG7Afm_rlRRbxWzAaIAWL_zMDcZIu8qVZ4MKVx9H2ZeAZSKnuZdkWHNWvjkva50PmetKZ8MN-SN9nFfiGS_wJUPkyI-oKRfrY20C0fNNPs9/s1600/hide.unified.extensions.button.firefox.111.1.jpg)

## Hide Unified Extensions Button (Firefox >111)

The `about:config` flag was removed in Firefox version 111, so extensions.unifiedExtensions.enabled flags will not work. However, you can still hide it with `userChrome.css`. We can change the **unified extension button** to `opacity: 0` with `userChrome.css`, so the button is **invisible** but still works.

1. You need to set `toolkit.legacyUserProfileCustomizations.stylesheets` to `true` from `about:config` so `userChrome.css` will work.

![Figure 3](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgzLLKSsrvEeLRwBK-R-q20Wec65SCvuWo3eeSQ1CigGOUZiK9BcK5NDtqih5a1n7iSaLhIa16sbGt-TZQMNJy_YHh8UGQgoe3kVLqTeZX3d8vt2SSxc4he0mgCcohhpncyJrMKfpIDRxe45Utdhsq68aQa-Lf8yc459cbQQreHnkeS3Q8w8uOFblMIXDf7/s1600/hide.unified.extensions.button.firefox.111.7.jpg)

2. Open `about:support` find **Profile Directory** and click the **Open Directory** button.

![Figure 4](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjKNWT405cAR7OB2Ui_5kCDyQEpO1hebyuHU51n0IKMyteI5s0cD-WX58p8dVHFqS8C86gCrjFaL-LcpXXr3aQ3Z8TVTISvaUAgWES0EEItmdgYnpLQY0r2e8OQ5iOSnnQNzUoKdCa8RSsnoRIPMadhnAk15fIo1HBEHrX6yNJP-FA-FaQRenKWjG-N_Z1-/s1600/hide.unified.extensions.button.firefox.111.2.jpg)

3. After File Explorer opens, **create a folder** named `chrome` under your Firefox profile directory.

![Figure 5](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjkHyt5TUGZHKdYi0CyjxdiQ82fiAXPnGPdIJYmNKlwpIbVgGQprnzZIf3QnZqK06V8vp30Gac7OCQfBhH0iCKxyOSJCky_jqLLg9skV4nqFUJNjahM3xSTgRimJq0jPEtGax4j1rEXzNYm8NRBBXHiPcN9NcZGUTwECHmvdChMKhNn_VwPIWFY4v3D8Ry_/s1600/hide.unified.extensions.button.firefox.111.4.jpg)

5. Open the `chrome` folder and create a file with the name `userChrome.css` (for Linux, this is case-sensitive).

![Figure 6](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEifK466BKmXzO2d7NU7Hf6YF0BV_X-q9BeKkVqwgL9-G1bOkeie0uEMj7hzY8K8R63WeLl3Xg69q989BQ3upC9ED4-9rnoj7hMkiN-NDcdyek7bzRwBFOqCTVkTNmp6AiOMNUuv18sViWXNkTWUyx4TmNE1v_KRvoKQzB_UynTFrc5FBczrgOsqTeqAZGFn/s1600/hide.unified.extensions.button.firefox.111.3.jpg)

6. Open `userChrome.css` with a text editor and paste this CSS code & Save.

```css
#unified-extensions-button {
  opacity: 0 !important;
}
```

![Figure 7](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhEqsag4begw8rPeZDL_PalDgy7ErShRsqgrtL12rFiHV1jJU3LMBofLEmmLUMfrl3kghWBzuMTgS77EWb28mmKrJ1lkTtvVWL_DavpWMEeTqHj9bO_0M8j86oST__E3ap6UdM1LGayMlDWBvNLBGJPov4oRrxPm434V5GBRkqtvBwrhJRu3NHkIEDLhH-t/s1600/hide.unified.extensions.button.firefox.111.5.jpg)

7. Open `about:restartrequired` and Restart Firefox, so your tab will not be gone.

![Figure 8](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjrQPVde9x3p9RUm5opNPb5Y_NvgkmM4AskHigiNszjCFSWErvN2g-x6_2BAnfSgyejX9BvOXCxw8VjUBkJPMP2lDvYTNv5dflxYhTdQ5KwZCMq31A_qxHL-HBy896gxVcyH_XwuXbWTavGpVUrY3QWhQIUhT1yI-DSmfOXMi3k747mhLZMeklcqndokd3V/s1600/hide.unified.extensions.button.firefox.111.8.jpg)

## Hide Unified Extensions Button (Firefox <110)

1. Open `about:config` & **Accept the Risk and Continue**

![Figure 9](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEirollUyGnndGYFy3IanFbl5dTYlcHZpww6xnZ2aTnArQH8UESs8ZBMTea5l6xUycXdUwHjdwx6ZAeG-aknfFPS0PnTUzhwrRpMlSv7N2asDgI0Eprc64JdhyphenhyphenBKaZPFVcdbxa0n5au30-MMhn2Ys1eERVcKxoGMmn-2EZqC_D0Gg3SPNup7JYS6rm8wBfb3/s1600/hide.unified.extensions.button.firefox.109.3.jpg)

2. Search `extensions.unifiedExtensions.enabled` set to `false`

![Figure 10](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhJo9dJmcogqVG34W7pRm9H5u80SLMhjO7uFXV7pGJt8cqhaMDakK0AYfVAkZ8ToYWQL9cv6FXOxYuvGsbh0-wkX649TpZ-7Er3kHO67_gcYd3kKtwnfE3v6Wvc25QPx2UVvepKP50A5qKv8XVMIXXDBZ1tHHbmiQJs1jRBqArjNa473Juhf5Dz2GWRXb2Z/s1600/hide.unified.extensions.button.firefox.109.4.jpg) ![Figure 11](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhEgsq0YGCAlcJ9MGQd6WQtsKiiIVZSOxa7z8QqYDeFn6ICrWJuQaGvhsch25ByfJC-cDRTCtW1RosQ3Lru96DxrOn-BGNUs0wRsk6KPOEaXYuoUbx7uOFsZVAyb93OrkLqZD0MnyyE-pasTtJ0bp8UMz1Rge2LJuk6926U4GLv4eIlmJDPVBKcmbKxv4_x/s1600/hide.unified.extensions.button.firefox.109.5.jpg)

3. Open `about:restartrequired` and **Restart Firefox**

![Figure 12](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEh_fFGpOEfYszwJSeuvyL9TsIylcueLm0Mrh-Y-573fftZoa5pKnL1qBrWlpQH74kGv4gpXo5lhyphenhyphenBCpoRXIYh8Wa88SB_eYWqRbapt4LuxI_ttfOodpgP8vARaD25WiZUPHdpNK8uXCmTrjRSVDqSCgZaUFHqKj7HhGz2xhYNqRHuEug_iCtcWYqtke7pSD/s1600/hide.unified.extensions.button.firefox.109.6.jpg)

4. After restart extension button will be reverted to overflow menu like Firefox version 108 and older

![Figure 13](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiGV-zrUfrTVFDb_TpYjc8uIJEQhekFir1oPhgzPSzNcdCqgzWQRyQepWwq4DnsuEP-ePt5Jr-69cQDB_bx08v4BXzrlp4RgW8eBfUPQ3soH5JXMCTNZFkibYZFXiS-CwcbnmJ8d-aSZOXHPj4LM_vxKttquCw6-12etvCEz0QjjZbu0-SbKskDlmvB2WHy/s1600/hide.unified.extensions.button.firefox.109.7.jpg)

## Disable Firefox View & Tab Manager

You can read article here [Remove Firefox View & Tab Manager Firefox 106](https://rmdhnreza.my.id/remove-firefox-view-tab-manager-firefox-106/)
