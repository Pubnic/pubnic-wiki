---
title: Exceções
description: 
published: true
date: 2022-08-31T13:33:34.976Z
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

## Manipulando Exceções em Python
Para manipular e capturar as exceções, usa-se o bloco `try` e `except`. Nele, o python executa o código seguindo a instrução `try` como parte normal do código. Já a parte que segue a instrução `except`, apresenta a resposta do programa a quaisquer exceções da cláusula `try` anterior.
<center> 
<div class="cat">
    <img src="/try_except.png" width="300" height="300"  />
</div>
</center>

Conforme o diagrama acima, quando o código sintaticamente correto é executado em um erro, o Python lançará um erro de exceção. Este erro de exceção travará o programa se não for tratado. A cláusula except determina como seu programa responde as exceções.

O exemplo a seguir ajuda a entender o bloco try e except:

Ex:
```python
try:
    print(x)
except:
    print('Por favor, declare a variável x primeiro')

print(1)
```
Saída:
```
Por favor, declare a variável x primeiro
1
```

A exceção foi tratada com o bloco except, foi recebida uma mensagem personalizada significativa do que exatamente deu errado e como corrigi-lo. Além disso, desta vez, o programa não parou de funcionar assim que encontrou a exceção e executou o resto do código. 

Anteriormente, antecipou-se e tratou-se apenas um tipo de exceção, mais especificamente, um NameError. A desvantagem dessa abordagem é que a parte do código na cláusula `except` tratará todos os tipos de exceções da mesma maneira e produzirá a mesma mensagem: *"Por favor, declare a variável x primeiro"*. Para evitar isso, é possivel mencionar explicitamente o tipo de exceção que precisa-se capturar e tratar logo após o comando `except`:
Ex:
```python
try:
    print(x)
except NameError:
    print('Por favor, declare a variável x primeiro')
```
Saída:
```
Por favor, declare a variável x primeiro
```

### Lidando com várias exceções
Abaixo é apresentada uma função chamada `divisao`, que retorna o resultado de `a` dividido por `b`.

Ex:
```python
def divisao(a, b):
    return a / b

c = divisao(5, 0)
```
Saída:
```
Traceback (most recent call last):
  File "./prog.py", line 5, in <module>
  File "./prog.py", line 2, in divisao
ZeroDivisionError: division by zero
```

Para esse exemplo, ocorre a exceção `ZeroDivisionError` se b for zero. Logo, para manipular esse erro, usa-se o `try... except` da seguinte forma:

```python
def divisao(a, b):
    try:
        return {
            'sucesso': True,
            'mensagem': 'OK',
            'resultado': a / b
        }
    except ZeroDivisionError as e:
        return {
            'sucesso': False,
            'mensagem': 'b nao pode ser zero',
            'resultado': None
        }


resultado = divisao(5, 0)
print(resultado)
```
Saída:
```
{'sucesso': False, 'mensagem': 'b nao pode ser zero', 'resultado': None}
```

Caso não se pegue a exceção `ZeroDivisionError`, mas se use uma exceção mais geral como a classe `Exception`:

```python
def divisao(a, b):
    try:
        return {
            'sucesso': True,
            'mensagem': 'OK',
            'resultado': a / b
        }
    except Exception as e:
        return {
            'sucesso': False,
            'mensagem': 'b nao pode ser zero',
            'resultado': None
        }


resultado = divisao(5, 0)
print(resultado)
```
Saída:
```
{'sucesso': False, 'mensagem': 'b nao pode ser zero', 'resultado': None}
```
O programa irá funcionar como antes porque `try...except` também captura o tipo de exceção que é a subclasse da classe `Exception`. Porém,caso se use duas strings em vez de dois números para na função divisao(), a mesma mensagem irá ser mostrada como se a exceção `ZeroDivisionError` tivesse ocorrido:
```python
def divisao(a, b):
    try:
        return {
            'sucesso': True,
            'mensagem': 'OK',
            'resultado': a / b
        }
    except Exception as e:
        return {
            'sucesso': False,
            'mensagem': 'b nao pode ser zero',
            'resultado': None
        }


resultado = divisao('1', '2')
print(resultado)
```
Saída:
```
{'sucesso': False, 'mensagem': 'b nao pode ser zero', 'resultado': None}
```
Para este exemplo, a exceção não é, `ZeroDivisionError` mas o `TypeError`. Todavia, o código ainda o trata como a exceção `ZeroDivisionError`. Desse modo, sempre se deve tratar as exceções da mais específica para a menos específica. Por exemplo:
```python
def divisao(a, b):
    try:
        return {
            'sucesso': True,
            'mensagem': 'OK',
            'resultado': a / b
        }
    except TypeError as e:
        return {
            'sucesso': False,
            'mensagem': 'Ambos a e b devem ser números',
            'resultado': None
        }
    except ZeroDivisionError as e:
        return {
            'sucesso': False,
            'mensagem': 'b nao pode ser zero',
            'resultado': None
        }
    except Exception as e:
        return {
            'sucesso': False,
            'mensagem':  str(e),
            'resultado': None
        }


resultado = divisao('1', '2')
print(resultado)
```
Saída:
```
{'sucesso': False, 'mensagem': 'Ambos a e b devem ser números', 'resultado': None}
```
No exemplo acima, foram usadas as exceçoes `TypeError`, `ZeroDivisionError`, e `Exception` na ordem em que aparecem na instrução `try...except`. Cso o código que trata de diferentes exceções seja o mesmo, pode-se agrupar todas as exceções em uma, da seguinte forma:

```python
def divisao(a, b):
    try:
        return {
            'sucesso': True,
            'mensagem': 'OK',
            'resultado': a / b
        }
    except (TypeError, ZeroDivisionError, Exception) as e:
        return {
            'sucesso': False,
            'mensagem':  str(e),
            'resultado': None
        }


resultado = divisao(5, 0)
print(resultado)
```
Saída:
```
{'sucesso': False, 'mensagem': 'division by zero', 'resultado': None}
```
Com isso, conclui-se que as exceções do Python são objetos de classes, que são as subclasses da classe `BaseException`. Além disso, trata-se a exceção do mais específico para o menos específico.

## Declaração else

Além das cláusulas `try` e `except`, pode-se usar um comando `else` opcional. Caso se utilize esse comando, ele deve ser adicionado após todas as cláusulas except e ter sua execução somente se não ocorrer nenhuma exceção na cláusula try. No exemplo abaixo será tratada uma divisão por zero:

```python
try:
    print(5/0)
except ZeroDivisionError:
    print('Você não pode dividir por zero')
else:
    print('A divisão foi realizada com sucesso')
```
Saída:
```
Você não pode dividir por zero
```
A exceção foi capturada e tratada no bloco except e, portanto, a cláusula else foi ignorada. Ao se fornecer um número diferente de zero:
```python
try:
    print(5/2)
except ZeroDivisionError:
    print('Você não pode dividir por zero')
else:
    print('A divisão foi realizada com sucesso')
```
Saída:
```
2.5
A divisão foi realizada com sucesso
```
Uma vez que não ocorreu nenhuma exceção, o bloco `else` foi executado.

## Declaração finally

A finally é uma outra instrução opcional, que deve ser adicionada após todas as cláusulas, incluindo o `else`. Ela é executada em qualquer caso, mesmo que não tenha sido levantada uma exceção na cláusula `try`. Incluindo no exemplo anterior:

```python
try:
    print(5/0)
except ZeroDivisionError:
    print('Você não pode dividir por zero')
else:
    print('A divisão foi realizada com sucesso')
finally:
    print('Esta mensagem é sempre impressa')
```
Saída:
```
Você não pode dividir por zero
Esta mensagem é sempre impressa
```
Sem levantar a exceção:

```python
try:
    print(5/2)
except ZeroDivisionError:
    print('Você não pode dividir por zero')
else:
    print('A divisão foi realizada com sucesso')
finally:
    print('Esta mensagem é sempre impressa')
```
Saída:
```
2.5
A divisão foi realizada com sucesso
Esta mensagem é sempre impressa
```

Assim, em ambos os casos, a cláusula `finally` gera a mesma mensagem.
 
