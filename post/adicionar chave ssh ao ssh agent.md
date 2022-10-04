+++
author = "Igor Nascimento"
title = "Adicionando chave SSH ao ssh-agent"
date = "2022-09-27"
description = "Um guia de como adicionar a chave ssh"
tags = [
    "ssh",
    "Linux",
    "Open Source",
]
categories = [
    "Linux",
]
series = ["Themes Guide"]
aliases = ["migrate-from-jekyl"]
+++

```
eval "$(ssh-agent -s)"
```

```
ssh-add ~/.ssh/id_ed25519
```

```
ssh-add -l
```
