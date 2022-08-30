---
title: Exceções
description: 
published: true
date: 2022-08-30T11:33:34.105Z
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

## Tipos de exceção incorporados padrão

Existem inumeras exceções, uma para cada situação de erro. Abaixo são apresentadas as mais comuns.

- `NameError` – Gerado quando um nome não existe entre variáveis locais ou globais:

Ex:
```python
print(x)
```

Saída:
```
Traceback (most recent call last):
  File "./prog.py", line 1, in <module>
NameError: name 'x' is not defined
```

- `TypeError` – Gerado quando uma operação é executada em um tipo de dados inaplicável:

Ex:
```python
print(2+'2')
```
Saída:
```
Traceback (most recent call last):
  File "./prog.py", line 1, in <module>
TypeError: unsupported operand type(s) for +: 'int' and 'str'
```

- `ValueError` – Gerado quando uma operação ou função recebe um valor inválido de um argumento:

Ex:
```python
print(int('d'))
```
Saída:
```
Traceback (most recent call last):
  File "./prog.py", line 1, in <module>
ValueError: invalid literal for int() with base 10: 'd'
```

- `IndexError` – Gerado quando um índice não existe em um iterável:

Ex:
```python
print('dog'[3])
```
Saida:
```
Traceback (most recent call last):
  File "./prog.py", line 1, in <module>
IndexError: string index out of range
```
- `IndentationError` – Gerado quando o recuo está incorreto:

Ex:
```python
for i in range(3):
print(i)
```
Saída:
```
Traceback (most recent call last):
  File "/usr/lib/python3.8/py_compile.py", line 144, in compile
    code = loader.source_to_code(source_bytes, dfile or file,
  File "<frozen importlib._bootstrap_external>", line 846, in source_to_code
  File "<frozen importlib._bootstrap>", line 219, in _call_with_frames_removed
  File "./prog.py", line 2
    print(i)
    ^
IndentationError: expected an indented block
```

- `ZeroDivisionError` – Ocorre na tentativa de dividir um número por zero:

Ex:
```python
print(5/0)
```
Saída:
```
Traceback (most recent call last):
  File "./prog.py", line 1, in <module>
ZeroDivisionError: division by zero
```

- `ImportError` – Gerado quando uma instrução de importação está incorreta:

Ex:
```python
from numpy import pandas
```
Saída:
```
Traceback (most recent call last):
  File "./prog.py", line 1, in <module>
ImportError: cannot import name 'pandas' from 'numpy' (/usr/local/lib/python3.8/dist-packages/numpy/__init__.py)
```

- `AttributeError` – Gerado na tentativa de atribuir ou referenciar um atributo inaplicável para um determinado objeto Python:

Ex: 
```python
print('a'.sum())
```
Saída:
```
Traceback (most recent call last):
  File "./prog.py", line 1, in <module>
AttributeError: 'str' object has no attribute 'sum'
```

- `KeyError` – Gerado quando a chave está ausente no dicionário:

Ex:
```python
animals = {'gato': 1, 'cachorro': 2}
print(animals['coelho'])

```
Saída:
```
Traceback (most recent call last):
  File "./prog.py", line 2, in <module>
KeyError: 'coelho'
```
> Para obter uma lista completa de exceções internas do Python, consulte a [Documentação do Python ](https://docs.python.org/3/library/exceptions.html).
{.is-info}




