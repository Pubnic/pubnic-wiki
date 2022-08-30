---
title: Exceções
description: 
published: true
date: 2022-08-30T00:48:36.999Z
tags: 
editor: markdown
dateCreated: 2022-08-30T00:48:36.999Z
---

# Exceções
Em python, um programa acaba assim que encontra um erro. Desse modo, a exceção ocorre quando um evento interrompe o fluxo normal das instruções do programa. Em geral, quando um script Python encontra uma situação com a qual não pode lidar, ele gera um erro que pode ser de sintaxe ou uma exceção.

## Exceções versus Erros de sintaxe
Os erros de sintaxe acontecem ao se detectar uma instrução incorreta. Como por exemplo:

```python
>>> print( 0 / 0 ))
  File "<stdin>", line 1
    print( 0 / 0 ))
                  ^
SyntaxError: invalid syntax
```

No bloco de código acima existe um erro de sintaxe que esta indicado pela seta. Ao retirar o colchete o erro desaparece. Então, ao ser executado novamente:

```python
>>> print( 0 / 0)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ZeroDivisionError: integer division or modulo by zero
```

Encontrou-se uma exceção com o bloco acima. Esse erro acontece sempre  que o código Python sintaticamente correto resulta em um erro. A última linha da mensagem mostra o tipo de erro de exceção encontrado. Em vez de mostrar a mensagem *exception error*, o Python detalha que tipo de erro de exceção foi encontrado. Neste caso, foi um ZeroDivisionError. 

> Python vem com várias [exceções  incorporadas](https://docs.python.org/3/library/exceptions.html) , bem como a possibilidade de criar exceções autodefinidas.
{.is-info}

## Hierarquia das exceções

As exceções em python são objetos das classes de exceção. Todas as classes de exceção são subclasses da classe `BaseException`.
Porém, quase todas as classes de *exceção incorporadas* herdam da `Exceptionclasse`, que é uma subclasse da BaseExceptionclasse. Abaixo é apresentado um diagrama dessa hierarquia:

![excecoes.png](/excecoes.png)

> Esta página mostra uma [hierarquia de classes completa para exceções internas em Python ](https://docs.python.org/3/library/exceptions.html#exception-hierarchy).
{.is-info}



