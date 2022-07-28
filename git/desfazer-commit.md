---
title: Desfazer Commit
description: 
published: true
date: 2022-03-08T01:25:23.420Z
tags: 
editor: markdown
dateCreated: 2022-03-08T01:25:20.510Z
---

No dia a dia, é normalm iniciarmos uma nova task e acabar esquecendo de criar uma nova branch antes de fazer o primeiro commit, então vamos abordar como podemos desfazer o commit, criar a nova branch e aí sim criar o commit na branch correta.

- Estamos na branch `master` e criamos um commit que não deveria estar ali, basta voltarmos o commit com: `git reset HEAD~1`, sendo o `1` a quantidade de commits que queremos voltar. 
- Todas suas modificações ainda estarão lá, agora vamos criar a branch correta: `git checkout -b task2`
- Refazer o commit: `git commit -m "Commiting in correct branch"`
- E subir a nova branch para a nuvem: `git push -u origin task2`