---
title: Git: Motivação e Instalação
description: 
published: true
date: 2022-03-05T05:44:35.930Z
tags: git instalação
editor: markdown
dateCreated: 2022-03-05T03:53:28.372Z
---

## Motivação
Git é um **Sistema de Controle de Versão**, provavelmente sendo o mais usado no mundo hoje. Sendo principalmente utilizado no dia a dia das pessoas que desenvolvem software por um "simples motivos": **ter uma forma fácil de gerenciar o código fonte**.

Pode ser que algumas pessoas ainda tentem gerenciar esses arquivos de maneiras ultrapassadas, tipo: compartilhar diretórios na rede, utilizar ferramentas como Google Drive, ou até manter tudo em um servidor de FTP. **Algo que não encorajamos!**

Não só manter o código fonte, também precisamos manter o **histórico** de todas nossas mudanças nos arquivos e das inúmeras possíveis **versões/ramificações** feitas em grupo. Possibilitando **voltar no tempo** e **recuperar** o sistema em um momento que não estava quebrando, por exemplo.

E o **Github**? Você me pergunta, github é uma **plataforma na nuvem** que utiliza o **git** como sistema de controle, permitindo gerenciar e criar ambientes de colaboração entre desenvolvedores.

## Linux
- Simplesmente rode no terminal
  ```
  apt install git
  ```
- Confirme que está instalado
  ```
  git --version
  ```

## MacOS
> ### Caso ainda não tenha o Homebrew instalado
> - A forma mais prática de instalar no MacOS é utilizando o Homebrew
> 	- Para instalar o Homebrew cole a seguinte linha de comando no terminar
>   ```
>   /bin/bash -c "$(curl -fsSL > https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
>   ```
{.is-info}

- Rode no terminal 
  ```
  brew install git
  ```
- Confirme que está instalado 
  ```
  git --version
  ```

## Windows
- Baixe a última versão e instale [clicando aqui](https://git-scm.com/download/win).
- Confirme que está instalado `git --version`