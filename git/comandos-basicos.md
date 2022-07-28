---
title: Principais Comandos
description: 
published: true
date: 2022-03-07T18:48:56.780Z
tags: git comandos
editor: markdown
dateCreated: 2022-03-05T05:12:19.501Z
---

## Iniciando um novo repositório Local
```sh
git init
```

## Obtendo um repositório remoto
- Forma genérica HTTP: `git clone https://url-git-remoto/repositório`
- Forma genérica SSH: `git clone git@url-git-remoto/repositório`
- Ex.:
```
https://github.com/Pubnic/todo-challenge.git
```
```
git clone git@github.com:Pubnic/todo-challenge.git
```
  
## Olhar situação atual
```
git status
```

## Adicionando arquivos para serem commitados (Commit == Salvar e criar uma nova versão)
- `git add <pasta e/ou arquivo>`
- Adicionar tudo que é novo ou modificado `git add .`

## Associando um repositório remoto ao local
- Situação: Iniciei um repositório local com `git init` e agora quero subir para o git na nuvem (github)
```
git remote add origin git@url-git-remoto/repositório
```

## Criando uma nova versão/commit em cima do que foi selecionado
```
git commit -m "Uma mensagem contextualizando"
git commit -m "de preferência em inglês e curta"
```
> Nesse momento o commit somente existe na sua máquina!
{.is-warning}

## Subindo as novas versões/commits para a nuvem
- Forma genérica `git push apelido_do_remoto branch`
- Ex.: `git push origin master`
> Se a branch for nova e ainda não existir no repositório remoto, será necessário rodar o comando com `-u`. Ex.: `git push -u origin minha_nova_branch`
{.is-warning}

## Pegar/trazer novas modificações
- `git pull` irá trazer de todas as branchs
- `git pull origin branch` irá trazer somente da branch específicada

## Descobrir novas branchs remotas que ainda não existe na local
- `git fetch`

## Criar uma nova branch
- `git checkout -b nome_da_nova_branch`

## Trocar de branch que já existe
- `git checkout nome_da_branch`

## Atualizar minha branch atual com outra (Ex.: `master`)
- `git merge master` irá juntar os commits da **master local** com a sua **branch local**
- `git merge origin/master` irá juntar os commits da **master remota** com a sua **branch local**

## Visualizar o que foi modificado
- `git diff` Irá mostrar tudo que foi *criado/modificado*
- `git diff pasta/arquivo` Irá mostrar tudo que foi **criado/modificado** de uma pasta ou arquivo
- `git diff branch1 branch2` Irá mostrar tudo que foi **criado/modificado** na **branch2** em relação à **branch1**
> Para sair da visualização aperta a letra **Q** do teclado
{.is-info}


## Visualizar todos as versões/commits já criados
- `git log`
> Para sair da visualização aperta a letra **Q** do teclado
{.is-info}

## Resetar/Apagar uma modificação de um arquivo
- `git checkout -- arquivo`
> Essa operação não deleta arquivos novos
{.is-info}

> Está operação é irreversível! Cuidado pois se usada sem cautela poderá perder um trabalho feito importante.
{.is-warning}


## Resetar/Apagar todas as novas modificações
- `git reset --hard HEAD`
- `git checkout .`
> Essa operação não deleta pastas/arquivos novos
{.is-info}

> Está operação é irreversível! Cuidado pois se usada sem cautela poderá perder um trabalho feito importante.
{.is-warning}

## Jogar novas modificações para a lixeira
- `git stash`

## Recuperar os últimos arquivos jogados na lixeira
- `git stash pop`

## Visualizar as últimas lixeiras criadas
- `git stash list`
  
## Recuperar uma lixeira específica
- `git stash apply stash@{index}` Index podendo ser 0, 1, 2, etc...
  
## Configurar nome e email
- `git config --global user.name "Maria Silva"`
- `git config --global user.email maria.silva@gmail.com`

## Configurar o editor para VSCode
- `git config --global core.editor 'code --wait'`

## Visualizar arquivo de configurações
- `git config --global -e`