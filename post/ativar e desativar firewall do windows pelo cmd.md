+++
author = "Igor Nascimento"
title = "Ativar e Desativar o Firewall do Windows pelo CMD"
date = "2022-09-28"
description = "Um guia de como ativar e desativar o firewall do windows pelo cmd"
tags = [
    "cmd",
    "Windows",
]
categories = [
    "Microsoft",
]
series = ["Themes Guide"]
aliases = ["migrate-from-jekyl"]
+++

```
netsh Advfirewall set allprofiles state off
```

```
netsh Advfirewall set allprofiles state on
```

```
netsh Advfirewall show allprofiles
```
