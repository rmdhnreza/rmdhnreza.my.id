---
title:  'Fix Inverted Image When Dark Mode on Google Chrome'
date: 2022-05-06T15:30:13+07:00
description:  'How to fix inverted image when dark mode on Google Chrome'
categories:  ['Tutorial']
tags:  ['Tutorial']
keywords:
  [
    'Fix Inverted Image When Dark Mode on Google Chrome',
    'How to fix inverted image when dark mode on Google Chrome',
    'YouTube player shadow dark mode chrome'
  ]
description: 'Fix Inverted Image When Dark Mode on Google Chrome.'
summary: 'Fix Inverted Image When Dark Mode on Google Chrome.'
image: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEh4gS484_RRF5AP20-jeEH9_uybKhpE1g8e_3oDcy6NQIJ6IM2Syvp_hIltipnbQwvpfO9BgZzZa6utCPWPNGTrowES-q8sDUH3GPiShw_sX570qVJEHkEMl-sLHW_nqAgVbWK9ukhEQ4qwJUYWPlDCjCi_jS-nPYUJdm58zB49iOZv0prsPL8UeRaG4C1B/s80-rw/chrome-logo.png
ThumbSchema: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEh4gS484_RRF5AP20-jeEH9_uybKhpE1g8e_3oDcy6NQIJ6IM2Syvp_hIltipnbQwvpfO9BgZzZa6utCPWPNGTrowES-q8sDUH3GPiShw_sX570qVJEHkEMl-sLHW_nqAgVbWK9ukhEQ4qwJUYWPlDCjCi_jS-nPYUJdm58zB49iOZv0prsPL8UeRaG4C1B/s0/chrome-logo.png
---
## Notes
Since Chrome 97 (I think), Chrome dark mode looks broken, not only chrome others browser chromium has this issue too such as
1. Brave
2. Chromium
3. Edge

So, this is for example:

* SVG icon inverted look like this.

1             |  2
:-------------------------:|:-------------------------:
![SVG Icon Inverted](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEghc4jTPTyi36D225epIcE6FEjMP0iRR-r2_VuKnVHJ2wTNNsAeQLcfI1NsSLuJf7tJy1H3rdckv310aO7nl0_oXdrd5Hi2vB_S99k8e91nezXGq3Vl-Cb9on8KRYtZNT9U5wX4jegIvU4om68WCX3fbvlipG7hKD6fgi70IZDDJLaipS5Ar6glJxkqLTaq/s0/rmdhnreza.my.id.chrome.inverted.1.jpg)  ![SVG Icon Not Inverted](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhDL9CFFRConof0e1e779JUxDIGBYfPa4R7i4TZuN31Yh__21v1lZhl6gtjaodOzH7TO167vXLPJyffmBHG96tWHjoppti75MgcanK6AUDxTTbcaHvGq75pOi7TnXbYi2M0M0IXmoo9x2xRuqp9nYMqklMdNPSrFA-KoXek9KMayRML487Hv_iPPaR4f83O/s0/rmdhnreza.my.id.chrome.inverted.2.jpg)

* YouTube has weird shadow

![YouTube weird shadow](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhvLw-_M8vpAd31j976diJV7WhPySKITx2T_CpntE1GKk4LfsT0mNxB5zX0XyU0asnrmafU4Po6rDhW5RyJntNvAcszezmRy4rloEb0Iz4sLT_Cb7dgH4NLWoRVbRLizz-AOLlocW9ZZ3U60hVGh35M-olMDb3yoIi9S3YLr4oX4zFckSvVH41xUR9M6D2I/s0/rmdhnreza.my.id.chrome.inverted.3.jpg)

## Fix inverted images & weird shadow YouTube

For fix this weird issue, you just change `Auto Dark Mode for Web Contents` flags from `Enabled` to `Enabled with selective inversion of non-image elements`

Step-by-step for resolving this issue:

1. Open this URL `chrome://flags/#enable-force-dark`
2. Change from `Enabled` to `Enabled with selective inversion of non-image elements`
3.  **Restart** or **relaunch** your browser.

{{% adsense %}}

### If you want to disable Dark Mode completely

1. Open this URL `chrome://flags/#enable-force-dark`
2. Change to `Default` or `Disabled`
3.  **Restart** or **relaunch** your browser.

**This fix also can use on others Chromium-based browser.**

## Fix Background Image for some pages
Numerous of website has `background-image` CSS, in dark mode these websites look broken.

1             |  2
:-------------------------:|:-------------------------:
![Website with background images,](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhCP7MH53kHrLYmwJhXEIr9n6F_BJFGPuvR5hpBiedPZXw1Ru9QyE-sONWCQKzEFW1ZwodQovSLTRTF0CwdWflQ3AxFXxLdANmj2Xk9mAJChyphenhyphenJbeiN3d8FnaJy_P3vZcEbz1kGM1hId7l5q-TRSei_0ZuSWakuoYgLHwZ9sI_6JeWwBTgxJWB8s17N2xCdU/s0/rmdhnreza.my.id.chrome.inverted.4.jpg)  ![Website without background images](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhCYaFCTNklADBSEETJINb1yAPsP0guvZtYM6I25gHG7kvHdxymo3bdlVUaQE83BFJXt98YL7-5s30yRQUJ5SDIGowhnkTZO81jTiqa-0n7mhyXua78nZCQsmLKGBCN33HNkcUgK47OT6PUEtwAzAMasyygPXMxaUrn0b_M_fpahHexgadSlg6aYzohkPfA/s0/rmdhnreza.my.id.chrome.inverted.5.jpg)

For resolve this issue, we need extensions called [Stylus](https://chrome.google.com/webstore/detail/stylus/clngdbkpkpeebahjckkjfobafhncgmne?hl=en).

[Stylus](https://chrome.google.com/webstore/detail/stylus/clngdbkpkpeebahjckkjfobafhncgmne?hl=en) can change attribute or value CSS for website, so in this case We change an attribute `background-image` to `none`

1. Install extensions [Stylus](https://chrome.google.com/webstore/detail/stylus/clngdbkpkpeebahjckkjfobafhncgmne?hl=en)
2. Click on **Stylus** icon and Click **Manage**
3. Click on **Write new style**

1             |  2
:-------------------------:|:-------------------------:
![Stylus Extensions](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEikHU0a4sXUiYWxyoCO9QoAHNzDxLcM-1ALgT5uY_pXa0t7Y2iMpwr9qaEtcDlD7o5BrtuCEp36-k7QISmK6Qo7GTalG-ncDZ-YHP8OFKDN-aMRAGJY4Jgouu0ATyw8wvt8cqBEYh44G_0GIiX2QTyn_abhBr54zeuRja8XZhyphenhyphenwXtuXrB8U5GMiBqjsfzXP/s0/rmdhnreza.my.id.chrome.inverted.6.jpg)  ![Stylus Extensions](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhBYOmO609jNo31xljfwnX7SSy408FC7Wt-JYkAQYaQXMjXU7ozeo819ZGV4ozTJKHah4GYyALFKuem1zeCtI_9uZM5oA9cdJrjqDhg_yUJbzH8V8gUN_omPr215bI5iXvNg8jWI6r4-Eb_B0ISj53wUlg3tebFYOlwpD3yNCNgL4X6TvGW_4D3DDOMkVEM/s0/rmdhnreza.my.id.chrome.inverted.7.jpg)

4. For example, my style name is, `Remove Background Images` but, you can use other names.
5. Copy and Paste this line to Stylus editor.

```css
body  {
  background-image:  none  !important;
}
```
6. Save.

![Stylus Extensions](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEi7fx2ezQsp8tFZ9mxwQGXd56TdmArxswXKfh6d5Gdrx0irzs8xSz7l878qPFRGbaPBw_k7ax46tqeormqon6ru2M0TYy1Jg7afABqWaTcFAGgewSYTHP9IxtcEd36AgQxLWrimrOG0dwKH0quhgt8BGfC9-YwmUqrz0rndegiKDErb7nWxW-IrAbhWf94c/s0/rmdhnreza.my.id.chrome.inverted.8.jpg)

For comparison, website https://subscene.com with and without Background Images

1             |  2
:-------------------------:|:-------------------------:
![With Background Images](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiKsSQtMiUbsjEinAQoNJrifJOEwgK9dBudttybVqHdJAEwsxBqAZ5fB3jbYt6hyphenhyphenebHsuzo_HKz9uQzEx5XI3QBc7jAyQYr5pI3kE-uQn1B3DcZkcWTa8qEVZhDAWiUhMb3GOXfYGfhEG8isHF5hhB5o20b9TiPPgUfIWk3EX80QMQGuGVOYcTjM1ZsQXMb/s0/rmdhnreza.my.id.chrome.inverted.9.jpg)  ![Without Background Images](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgyYSn2etZeGsfW8mQ30a2WGG3TWnvFrbpZ4d3bLWayk04xWCZ_mjn17V1k_h_3eKg-OI_HKjmgg5CtpGiH_jHm6AZxWXwIc3kr8E2XQchVgsN51CKz4yYz1DNzsILpUzsRISqxJ82CnsGocMNs9J0FdAuphi5pH2k0J6UFC8tD62lnrGyXoHEk4Srkr8ph/s0/rmdhnreza.my.id.chrome.inverted.10.jpg)

{{% adsense %}}
