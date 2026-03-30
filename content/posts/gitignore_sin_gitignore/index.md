---
title: "Gitignore sin .gitignore"
date: 2026-03-30
draft: false
description: "Ignorar cosas del track de git sin usar .gitignore"
tags: ["git"]
categories: ["blog"]
---

Hay veces que necesito mantener files en mi repo, sin que se trackeen y sin que se incluya en el archivo .gitignore.
Para eso existe `$GIT_DIR/info/exclude` y `core.excludeFile` 

<!--more-->


La exclusión de trakeo en git funciona en tres niveles:

- **`.gitignore`** :: es anivel repo local y remote, lo que se incluye aquí no se trackea y es compartido con el equipo.
- **`$GIT_DIR/info/exclude`** :: es a nivel repo local solamente, lo que se incluye aquí no se trackea y no se comparten estas reglas con el equipo ni el git remoto
- **`core.excludeFile`** :: es a nivel config, las reglas que se incluyen acá corren para todos los repositorios locales en tu máquina.

Source: https://git-scm.com/docs/gitignore
