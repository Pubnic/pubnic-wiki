---
title: De iniciando uma nova task até o Pull Request
description: 
published: true
date: 2022-03-08T01:20:12.385Z
tags: git, github, processo de desenvolvimento
editor: markdown
dateCreated: 2022-03-08T01:20:09.315Z
---

Vamos lá, o processo de desenvolvimento com git normalmente se resume nos seguintes passos:

- Ir para a branch principal. Normalmente será `master` ou `main`.
```
git checkout master
```
> Pode ser que sua branch esteja com modificações não commitadas, caso isso aconteça será necessário commitar ou limpar a branch antes. Para limpar, basta jogar todas as modificações na lixeira: `git stash`
{.is-warning}
- Atualizar a branch principal Local com a Remota.
```
git pull origin master
```
- Criar a nova branch
```
git checkout -b task2
```
- Trabalhar na nova task, realizar commits periódicos e sempre que possível, deixar o remoto atualizado com o local
```
git add .
git commit -m "Finished the function xpto"
git push
```
- Finalizando a task, vamos no github abrir um novo Pull Request
	- Vá no repositório do projeto no github
	- Logo abaixo fica disponível o botão de `Pull Requests`
  ![pull_request_pages.png](/pull_request_pages.png)
	- Clicando no botão, seremos direcionado para a página de `Pull Requests`
	- Agora, vamos clicar em `New pull request` mais a direita da tela
  ![new_pull_request_button.png](/new_pull_request_button.png)
	- Agora, estamos na tela de criação de Pull Requests, vamos modificar a branch do `compare:` para a nossa branch da task
  ![pr_create_page.png](/pr_create_page.png)
  ![pr_selected_branch.png](/pr_selected_branch.png)
	- Agora clicamos em `Create pull request`
	![pr_create_button.png](/pr_create_button.png)
	- Vamos adicionar uma descrição e como testar
  ![pr_description.png](/pr_description.png)
	- Criar o Pull Request, o resultado será algo como:
  ![pr_created.png](/pr_created.png)
	- Agora é esperar para alguém revisar seu código e caso esteja tudo certo, aprova-lo através do botão
  ![pr_approve_button.png](/pr_approve_button.png)
- PR Criado e estamos prontos para voltar ao primeiro passo para iniciar uma nova demanda :D