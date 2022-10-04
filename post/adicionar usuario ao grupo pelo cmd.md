+++
author = "Igor Nascimento"
title = "Adicionar usuario ao grupo pelo CMD"
date = "2022-10-04"
description = "Um guia de como adicionar usuario ao grupo pelo cmd"
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

- Adiciona usuário no grupo
```
net localgroup “Nome_do_grupo” Nome_do_usuario /add
```

- Deleta o usuário do grupo
```
net localgroup “Nome_do_grupo” Nome_do_usuario /delete
```

- Lista os usuário do grupo
```
net localgroup Nome_do_grupo
```
