---
title: 'Taming Your Rofi Launcher: How to Hide Desktop Files for a Cleaner and More Efficient Experience'
url: "how-to-hide-desktop-files-for-a-cleaner-and-more-efficient-experience"
date: 2023-12-31T00:00:00+07:00
description: "Rofi is a versatile tool that packs several functionalities into one, making it a popular choice for productivity and customization among Linux users."
categories: ['Tutorial', 'Linux']
tags: ['Tutorial', 'Linux']
keywords:
  [
    'Best ways to manage desktop files in Rofi',
    'Customize Rofi appearance',
    'Customize Rofi application list',
    'Exclude desktop files Rofi',
    'Filter Rofi results',
    'Hide desktop files Rofi',
    'How to hide specific applications in Rofi',
    'Improve Rofi performance',
    'Improve Rofi search results by removing unwanted entries',
    'Keyboard shortcuts for Rofi',
    'Make Rofi launcher cleaner and more organized',
    'Remove applications Rofi',
    'Rofi configuration desktop files',
    'Rofi configuration tips',
    'Rofi themes and plugins',
    'Stop Rofi from showing certain apps'
  ]
description: 'Rofi is a versatile tool that packs several functionalities into one, making it a popular choice for productivity and customization among Linux users. '
summary: 'Rofi is a versatile tool that packs several functionalities into one, making it a popular choice for productivity and customization among Linux users.'
image: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEit2ksmgVibRPiuswMMjmLJckW_l5AAhSEG6h27_t8Uv63TTPypJaf2LeDdOrHDQRaEbnI9e3Gp4Vm8X87whQ7GAygnGuJv8Cv_vRpgGBa54Gthq8COHmTLQRUbq3Rhyphenhyphenl6vSDJaEHDBVgGsd5HgrjGhAuOKX-NESZMDOwY3xue4DBHlTdWxSL0w5VGCFvUx/s80-rw/rofi-logo.png
ThumbSchema: https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEit2ksmgVibRPiuswMMjmLJckW_l5AAhSEG6h27_t8Uv63TTPypJaf2LeDdOrHDQRaEbnI9e3Gp4Vm8X87whQ7GAygnGuJv8Cv_vRpgGBa54Gthq8COHmTLQRUbq3Rhyphenhyphenl6vSDJaEHDBVgGsd5HgrjGhAuOKX-NESZMDOwY3xue4DBHlTdWxSL0w5VGCFvUx/s0-rw/rofi-logo.png
---

![Rofi](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhhgaGIUB0QNS_camoEBHA3fss-RKsdSM1izk51t8gM7QdpYmUfFt6Z-dyTxXLFQWDk6fi13930lPb-GCrfDUJDwRE8xEj7Ci559pPWeXmZyPloW4KPh-Z_DC4tJcHnUDGESPhqLlWOgbNdHM3eWyBsBwqsJpWIVmq9jkFjtHTNkKUthX_8Fy0VFA-1u8B1/s0-rw/rmdhnreza.my.id.rofi.1.png=s0?imgmax=0)

## Rofi: A window switcher, application launcher and dmenu replacement

Rofi is a versatile tool that packs several functionalities into one, making it a popular choice for productivity and customization among Linux users.

Here's a quick breakdown of its key features:
  * Application Launcher: Launch programs effortlessly by typing their names or browsing through a customizable list. Forget digging through menus and folders.
  * dmenu Replacement: Rofi can substitute for dmenu, another popular text-based launcher, offering similar functions with additional enhancements.
  * Beyond the Basics: Rofi's capabilities extend further with the help of themes, scripts, and plugins. You can personalize its appearance, integrate it with your workflow, and unlock even more powerful features.

Rofi is a powerhouse application launcher and window switcher, but sometimes its default behavior can leave your launcher a bit cluttered. Want to streamline your workflow and hide those desktop files you rarely use? Here's a guide to banishing unwanted apps from Rofi's search results and keeping your launcher tidy.

## Modifying Desktop Files

1. Copy desktop file with the same name from `/usr/share/applications` to `$HOME/.local/share/applications/`

![Copy desktop file](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgiVYO4lydVwoxSvsFh2fB3MzaCXjbf_Xebl6QhDWMAK0ah472z8UPOvadqKSV2EvI851DUmVZTBpl1gr4i5nR5s7YjkAZbKRVW42VC_BhOk31eeINjWNh_pwIgTBcCYHh_Pp7KLzLb4XUSf0kLfGjIQLUKrQGUHk3IdRJSuUe9pBzHaMK06TU1W6uTvjoh/s0-rw/rmdhnreza.my.id.rofi.2.png=s0?imgmax=0)

2. Open the desktop file you want to hide in a text editor.

![Open desktop file](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhJJVJ9T8wMtTvDcborQedHs38vvSgL4BWBkdMXparSwKfAjdy9obyI4esn4ghkXeRTN-b71SVpsNQ_Nt3ycfO1dFgWpK0cLn6TY16zSaEYZ0m9g_5T_rDtY_ZD6dEcgQzDu3OwM5lq5t7uYwxMMAURFw7N3bHWk3NT6YpF8Nt9oGmAgYL4HrfkFLFSo8AB/s0-rw/rmdhnreza.my.id.rofi.3.png=s0?imgmax=0)

3. Add a Line: Insert a new line with the text `NoDisplay=true` within the `[Desktop Entry]` section.

![Insert NoDisplay=true](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgbM_CPfsy1t8aliNYsfWOQ41XSjDp4Ssa8AT65I_ORFTgacgtCf8nWGET2lupEY7wj-kJHIEcWTRSdKfCLEfeOXapfS2Zbt1HIzYUrITcI3nzPrNSNOXhbAaa0AAW9IblBzoicAT62ZQAuktMcpOLDENN_HHnX13kiBqkzkNH5RQ3db_wRsdvNMTqG0wXP/s0-rw/rmdhnreza.my.id.rofi.4.png=s0?imgmax=0)

4. Save and Enjoy: Save the file, and Rofi will respect its privacy-seeking desires.

![Desktop file hidden](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjjgQa_VUod6nD1DMZzrUhRmWJajZrvyph2GTg1EAq4_cLDCnVCg72Mt5qW3Nl2d34Nj3RbabbBfDHZpD3QoPNCf82Uzw_nu4JSfPtsBIaLEugEJZFVsi9oEREb_cTKux-7lQbh-M8zyOKvLQL_2Elb0pY0nFJsRH238_WcEpi2KTN3ZPofTAE_eZWAvyvK/s0-rw/rmdhnreza.my.id.rofi.5.png=s0?imgmax=0)

{{% note %}} Also you can use `Hidden=true` instead of `NoDisplay=true` {{% /note %}}

{{% center %}} Different between `NoDisplay=true` vs `Hidden=True` {{% /center %}}

|`NoDisplay=true`|`Hidden=True`|
|---|---|
| NoDisplay means "this application exists, but don't display it in the menus". This can be useful to e.g. associate this application with MIME types, so that it gets launched from a file manager (or other apps), without having a menu entry for it (there are tons of good reasons for this, including e.g. the netscape -remote, or kfmclient openURL kind of stuff). | Hidden should have been called Deleted. It means the user deleted (at their level) something that was present (at an upper level, e.g. in the system dirs). It's strictly equivalent to the .desktop file not existing at all, as far as that user is concerned. This can also be used to "uninstall" existing files (e.g. due to a renaming) - by letting make install install a file with Hidden=true in it.|

| 1 | 2 |
:-------------------------:|:-------------------------:
|![Before](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhhgaGIUB0QNS_camoEBHA3fss-RKsdSM1izk51t8gM7QdpYmUfFt6Z-dyTxXLFQWDk6fi13930lPb-GCrfDUJDwRE8xEj7Ci559pPWeXmZyPloW4KPh-Z_DC4tJcHnUDGESPhqLlWOgbNdHM3eWyBsBwqsJpWIVmq9jkFjtHTNkKUthX_8Fy0VFA-1u8B1/s0-rw/rmdhnreza.my.id.rofi.1.png=s0?imgmax=0) | ![After](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEieJJ2OG_SFukV1opfPCynAwY_KlfB8dwW8itIg_XPxDM3NHGi9rvAbIi0L48cPFNe36fgMxB5TpJbqnfHq-l9S-dZmN5qDSc4NJT_eEHTSLHeL-31bhj3RxnD508br3o6QOAmnnic6Gm98OZ7O3u0TnhXajS2xMmG2S1_dmQCe3KrQWul1E6FNMzssdKRK/s0-rw/rmdhnreza.my.id.rofi.6.png=s0?imgmax=0) |

## With Rofi Configuration

1. Open Rofi's Configuration File: Locate your `config.rasi` file, usually found in `$XDG_CONFIG_HOME/rofi/`
2. Disable Parsing: Add these lines to the configuration section to halt desktop file parsing:

```yaml
drun {
  parse-user: false;
  parse-system: false;
}
```

## Additional Approaches
  1. Moving Desktop Files:
       * Move the desktop files to a different directory that Rofi doesn't scan (e.g., `~/.hidden`).
  2. Symlinking to /dev/null:
       * Create a symlink to `/dev/null` with the same name as the desktop file in its original directory. However, this might not work for all applications.

## Tips

  * Backup Files: Before modifying desktop files, create backups to avoid unintended consequences.
  * Prioritize User-Specific Changes: When possible, make modifications within your user's directories (`$HOME/.local/share/applications`) to avoid affecting system-wide settings.
