---
title: "Remapping the Caps lock key to Ctrl"
date: 2022-05-18
showToc: false
TocOpen: false
hidemeta: false
comments: false
disableHLJS: true # to disable highlightjs
disableShare: false
disableHLJS: false
hideSummary: false
searchHidden: true
ShowReadingTime: true
ShowBreadCrumbs: true
ShowPostNavLinks: true
ShowRssButtonInSectionTermList: true
draft: false
tags: [Keys, Tip, Windows]
---

# Introduction

I don't find myself using the _Caps lock_ key that much and would rather have it mapped to _Control_ for convienience. While this is really straight-forward on a Mac, it requires a non-obvious solution on Windows. Luckily, SO came to the rescue.

# The Recipe

We need to run __Powershell__ as an administrator and type the following commands:

```
$hexified = "00,00,00,00,00,00,00,00,02,00,00,00,1d,00,3a,00,00,00,00,00".Split(',') | % { "0x$_"};

$kbLayout = 'HKLM:\System\CurrentControlSet\Control\Keyboard Layout';

New-ItemProperty -Path $kbLayout -Name "Scancode Map" -PropertyType Binary -Value ([byte[]]$hexified);
```

After reboot, the _caps lock_ key will be mapped to _Ctrl_

# Resources

- Original SO post with the recipe: [https://superuser.com/questions/949385/map-capslock-to-control-in-windows-10](https://superuser.com/questions/949385/map-capslock-to-control-in-windows-10)
