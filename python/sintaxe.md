---
title: Sintaxe do Python
description: 
published: true
date: 2022-10-02T01:18:52.085Z
tags: 
editor: markdown
dateCreated: 2022-10-02T01:18:52.085Z
---

# Sintaxe da linguagem 
Inicialmente o python foi desenvolvido como uma linguagem de ensino, porém, por ter facilidade de uso e sintaxe limpa, ele foi adotado por iniciantes e especialistas. A limpeza da sintaxe do Python levou alguns a chama-lo de "pseudocódigo executável". Logo abaixo serão discutidos os principais recursos da sintaxe do python.

A sintaxe se refere à estrutura da linguagem (ou seja, o que constitui um programa para ser formado corretamente).

## Espaço em branco e recuo
Ao se trabalhar com outras linguagens de programação, como C/C++, C#, Java, usa-se ponto e vírgula para separar as instruçoes. Todavia, no python usa-se espaços em branco e recuo para construir a estrutura do codigo. Considerando o seguinte exemplo de codigo:

```python
# define a função main para imprimir algo
def main():
    i = 1
    max = 10
    while (i < max):
        print(i)
        i = i + 1

# Chama a função main 
main()
```

Observando-se a estrutura do código