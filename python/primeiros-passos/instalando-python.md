---
title: Instalando o Python
description: Instalando o python no Linux, MacOS e Windows
published: true
date: 2022-03-30T20:14:55.675Z
tags: python, primeiro passos, ambiente
editor: markdown
dateCreated: 2022-03-01T20:06:18.952Z
---

# Instalar o python
Em sistemas operacionais Linux e MacOS o python normalmente já vem instalado mas vamos conferir a versão.

## Linux (Ubuntu/Derivados Debian)
- Abra o terminal, normalmente com o atalho `ctrl + alt + t` e verifique a versão do python instalado 
  ```
  python3 --version
  ```
- Caso seja menor que `3.8` ou tenha aparecido um erro como `NameError: name 'python' is not defined` vamos instalar uma versão mais atualizada.
	- A versão mais estável no momento em que escrevo esse artigo é a `3.8`
	- Primeiro vamos atualizar os pacotes
    ```
    sudo apt update
    ```
	- Agora vamos instalar o python na versão que desejamos 
    ```
    sudo apt install python3.8
    ```
	- Vamos confirmar que o python foi instalado 
    ```
    python3 --version
    ```
  mostrará algo como `Python 3.8.x`
	- Verifique a versão do instalador de pacotes python
    ```
    pip3 --version
    ```
	- Caso não esteja instalado, rode no terminal 
    ```
    python3 -m pip install -U pip
    ```
  
## MacOS
- Abra o terminal, utilize a barra de pesquisa `cmd + space` e digite `terminal`
- Verifique a versão do python instalado 
  ```
  python3 --version
  ```
- Se for menor que `3.8` vamos instalar uma versão mais atualizada

> ### Caso ainda não tenha o Homebrew instalado
> - A forma mais prática de instalar no MacOS é utilizando o Homebrew
> 	- Para instalar o Homebrew cole a seguinte linha de comando no terminar
> 	```
> 	/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
> 	```
{.is-info}

- Agora podemos instalar o python 
  ```
  brew install python@3.8
  ```
- Verifique a versão do python instalado 
  ```
  python3 --version
  ```
- Verifique a versão do instalador de pacotes python 
  ```
  pip3 --version
  ```
- Verifique a versão do instalador de pacotes python 
  ```
  pip3 --version
  ```
- Caso não esteja instalado, rode no terminal 
  ```
  python3 -m pip install -U pip
  ```
  
## Windows
- Abra o terminal, aperte o botão `Windows` do teclado e pesquise por `Powershell`, clique com o direito do mouse e selecione `Executar como administrador`
- Verique a versão do python digitando 
  ```
  python3 --version
  ```
- Caso seja menor que `3.8` ou tenha apresentado um erro, vamos instalar uma versão mais atualizada.
	- No Windows temos o `Chocolatey` que é similar ao `Homebrew` do MacOS.
		- No terminal cole 
      ```
      Set-ExecutionPolicy AllSigned
      ```
- Agora, cole para instalar: 
  ```
  Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
  ```
- Se não ocorrer nenhum erro, foi instalado com sucesso.
- Para instalar o python, cole: 
  ```
  choco install python --version=3.8.0
  ```
- Verifique a versão do python 
  ```
  python --version
  ```
- Verifique a versão do instalador de pacotes python 
  ```
  pip --version
  ```
- Caso não esteja instalado, rode no terminal 
	```
  python -m pip install -U pip
  ```
