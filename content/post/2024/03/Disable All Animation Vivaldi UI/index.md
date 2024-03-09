---
title: 'Disable all animation Vivaldi UI'
date: 2024-03-8T11:30:13+07:00
description: 'Tutorial how to disable all animation Vivaldi UI'
categories: ['Tutorial']
tags: ['Tutorial']
keywords:
  [
    'Cara disable all animation Vivaldi UI',
    'Disable all animation Vivaldi UI',
    'Tutorial Cara all animation Vivaldi UI',
    'Tutorial how to disable all animation Vivaldi UI',
  ]

description: 'Animation of Vivaldi UI make browser look slow for me, so I just want browser with no UI animations.'
summary: 'Animation of Vivaldi UI make browser look slow for me, so I just want browser with no UI animations.'
image: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEj2JK3oWUZ-t-40Nhqt4jhOeYlp9HSiM3ZpOINd88fpwyireJ1fYy_yxdU7gWGfQBYfuEWsmzblIbk41YJzIRiI_hM4hTL9StW6bSnxXhMzJZ90whU0uAyzJ6odNXTvfGY4n37XH6pQ8Hgj0tfw02YTM0c-ps4HA1cDWo-nl4OFtORr2mhrLyeCwVao_ukn/s80-rw/vivaldi-logo.png
ThumbSchema: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEj2JK3oWUZ-t-40Nhqt4jhOeYlp9HSiM3ZpOINd88fpwyireJ1fYy_yxdU7gWGfQBYfuEWsmzblIbk41YJzIRiI_hM4hTL9StW6bSnxXhMzJZ90whU0uAyzJ6odNXTvfGY4n37XH6pQ8Hgj0tfw02YTM0c-ps4HA1cDWo-nl4OFtORr2mhrLyeCwVao_ukn/s0/vivaldi-logo.png
---

## Vivaldi Animations
Animation of Vivaldi UI make browser look slow for me, so I just want browser with no UI animations.\
Vivaldi had internal setting for disable UI Animation, but some animations still there.\

![Vivaldi setting animation](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEim9h3DFHl83KSTk9RJtYo1HDy7rA3M71BVENVwdaBryTOPtD0paJdy-ttrdnZlW0h1XsH2kFgm7OACPwGu8ItiNgTxSLu5NF5sq40n48l8BFVI7JeHzq5eBpguAlWxU0roNOd80BQFhSY-phRKcZV4CE8qdrvm-Zl5-q5M3dVzIINcfhrYkvIMU7ZaDQWB/s0/rmdhnreza.my.id.disable.vivaldi.animation.1.jpg)

For example if you click on `+` new tab, extensions icon there still transform animation.

{{< spoiler text=" Example Video" >}}
{{% iframe "AD6v5dw0NaSVm7wssS4my2lGkQan1DfBaDHbJjDjZ9laKyxOUn62-2DaG9BZ5fHAK-UFI1WxfGRwGGaSV6BXWN2zYsliN5qomN7SYmVlnO_1yD1aDFylwCTP-ruFS1g2R3ijmqE88qav" %}}
{{< /spoiler >}}

{{% adsense %}}

## Add Custom CSS
For disable Vivaldi UI animations, we need custom CSS to override default Vivaldi CSS.
Here step-by-step for enabling `custom.css`
1. Open `vivaldi://experiments`
2. Check [x] `Allow for using CSS modifications.`
3. Open `vivaldi://settings/appearance/`
4. New setting will be appeared `Custom UI Modifications`
5. Choose the folder you want to use, for example:
   * `$HOME/.config/vivaldi/CustomCSS`
   * `Documents/Vivaldi/CustomCSS`
6. Place CSS files inside it, for example:
   * `$HOME/.config/vivaldi/CustomCSS/custom.css`
   * `Documents/Vivaldi/CustomCSS/custom.css`

![Vivaldi custom css](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgW92tKdMgt53F_H13gAgsUyL8zTHsAIhBpDw7DhGuhHQIj8qRDQosdvZF4mCJthvZshP0wh7m4Ril3Enxqd01IDfUxsiV3vgYVQpxVCtw8vS9xQNI6nsoIC0OpJj3R6vx0xbJWSqdfAEFoSIprP8bGrpPH59qq5NR7xjZga6BdbyE8gWe-2l9TwctaKrU9/s0/rmdhnreza.my.id.disable.vivaldi.animation.2.jpg)

{{% adsense %}}

## Disable UI Animations
After you enabling, `Allow for using CSS modifications` next step is add CSS to override default Vivaldi CSS.
Just copy this line to `custom.css` and save, after that restart your Vivaldi browser.
```css
/* 
  Disable UI Animations 
*/

*:not(.favicon):not(.jstest-favicon-image):not(.tab-audio):not(.audioicon):not(.tab-position):not(#modal-bg):not(input[type=checkbox]) {
  animation-delay: 0s !important;
  animation-duration: 0s !important;
  animation: none !important;
  transform: none !important;
  transition-delay: 0s !important;
  transition-duration: 0s !important;
  transition: none !important;
}
```

If working, it looks like this.

{{< spoiler text=" Example Video" >}}
{{% iframe "AD6v5dwRq1xxG1Idl_FHk44_Bc8gbl-3NWkBHx-yD9wy4wyO392oI6Im1zqRiPoVAQzxbt_EslR9vesQL3OhvOLNitWRgn6EbJFlL5TwEMqKbYmoosOCgAw1oRtResstDZhRqrBMLvTs" %}}
{{< /spoiler >}}
