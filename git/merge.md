---
title: A master/main atualizou, e agora?
description: 
published: true
date: 2022-03-08T01:30:33.295Z
tags: 
editor: markdown
dateCreated: 2022-03-08T01:30:30.360Z
---

Em um projeto com muito colaboradores, é natural a sua branch local ficar desatualizada com a remota, mas sem desespero, podemos resolver isso de maneira "fácil"
- Vamos remover qualquer modificação recente que ainda não foi commitda: `git stash`
- Agora vamos puxar tudo que tem no remoto de novo: `git fetch`
- Agora, atualizar a branch local com a remota: `git merge origin/mater`
	- Resolver qualquer conflito que tenha acontecido
		- Se tiver acontecido conflito e você já tiver resolvido, vamos adicionar a correção: `git add .` e continuar o merge: `git merge --continue`
- Pronto, branch local atualizada com a remota
	- Se tivermos jogado modifições na lixeira, podemos recupera-las: `git stash pop` irá remover da lixeira o último `stash` realizado.