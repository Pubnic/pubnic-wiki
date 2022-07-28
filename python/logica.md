---
title: Lógica booleana
description: 
published: true
date: 2022-05-20T20:00:31.576Z
tags: 
editor: markdown
dateCreated: 2022-05-20T13:25:16.341Z
---

# Lógica Booleana
A lógica booleana é uma forma da álgebra que está inserida em todas as linguagens de programação. No centro da lógica booleana está a ideia de que todos os seus valores são verdadeiros ou falsos. Os booleanos são representados pelas palavras `True` ou `False`, que sempre estarão com `T` e `F` maiúsculos, respectivamente.  Além do mais, os dados booleanos são retorno de algum tipo de operação de comparação.

## Tipo Booleano do Python
Apenas dois valores são atribuidos ao tipo booleano:
- True
- False

Ao se verificar seu tipo, obtém-se:
```python
>>> type(False)
<class 'bool'>
>>> type(True)
<class 'bool'>
```

É possível atribuir um valor booleano a variáveis, todavia ao atribuir um valor a True obtém-se um erro, como apresentado logo abaixo.

```python
>>> valor1 = True
>>> valor1
True
>>> True = 4
File "<stdin>", line 1
SyntaxError: cannot assign to True
```

A mesma regra se aplica a False. Por serem palavras-chave em python, não se pode atibuir um valor a elas. 

Para um maior entendimento do funcionamento dos booleanos em python, serão abordados os conceitos de operadores de comparação, operadores lógicos e tabelas da verdade.

## Operadores Booleanos

Os operadores booleanos são aqueles que ao receberem entradas booleanas, retornam saídas booleanas. Alguns são denotados por símbolos especiais, usados na realização de cálculos lógicos e aritméticos. Uma vez que os valores booleanos possuem apenas as opções, True ou False, consegue-se especificar os operadores em função dos resultados que eles atribuem a cada uma das combinações de entrada. Tais especificações são exibidas nas tabelas da verdade.

### Operadores de comparação

Esses operadores comparam valores, retornando True ou False após uma dada condição.

| Operador | Significado   | Exemplo |
|----------|:-------------:|------:  |
| <p align=center> > </p>| Maior que, ele é verdadeiro <br/> se o valor de `a` for maior que `b`, <br/> como no exemplo. | a > b|
| <p align=center> < </p>| Menor que, ele é verdadeiro <br/> se o valor de `a` for menor que `b`, <br/> como no exemplo. | a < b| </p>
| <p align=center> == </p> | Igual a, ele é verdadeiro <br/> se o valor de `a` for igual ao de `b`, <br/> como no exemplo. | a == b|
| <p align=center> != </p> | Diferente de, ele é verdadeiro <br/> se o valor de `a` for diferente de `b`, <br/> como no exemplo. | a != b|
| <p align=center> >=  </p> | Maior que ou igual a, ele é <br/> verdadeiro  se o valor de `a` <br/> for maior ou igual ao de `b`, <br/> como no exemplo. | a >= b|
| <p align=center> <=  </p> | Menor que ou igual a, ele é <br/> verdadeiro  se o valor de `a` <br/> for menor ou igual ao de `b`, <br/> como no exemplo. | a <= b| </p>
  
Logo abaixo são apresentados os operadores de comparação em um bloco de código.
```python
a = 7
b = 4

print("a == b:", a == b)
print("a != b:", a != b)
print("a < b:", a < b)
print("a > b:", a > b)
print("a <= b:", a <= b)
print("a >= b:", a >= b)
```

Após sua execução, temos a seguinte saída:
```python
a == b: False
a != b: True
a < b: False
a > b: True
a <= b: False
a >= b: True
```
  
### Operadores lógicos

Existem três operadores lógicos utilizados para comparar valores na programação em python, são eles: AND, OR e NOT.

| Operador | Significado   | Exemplo |
|----------|:-------------:|------:  |
| <p align=center> and </p>| É verdadeiro se ambos <br/> os operandos forem verdadeiros, <br/> tanto `a` quanto `b` | a and b|
| <p align=center> or </p>| É verdadeiro se ao menos <br/> um dos operandos for verdadeiro, <br/> `a` ou `b` | a or b| 
| <p align=center> not </p> | É verdadeiro se o operando <br/> for falso <br/> | not a|

Logo abaixo são apresentados os operadores de lógicos em um bloco de código.

```python
print((1 > 3) and (2 < 4))	
print((2 == 2) or (9 != 9))	
print(not(4 <= 1))
```

Ao se executar, obtém-se a seguinte saída:
  
```python
False
True
True
```

No primeiro print, a saída resulta em `False` porque apenas uma das expressões é verdadeira e ao se utilizar o operador and, seu resultado é `True` apenas quando ambas as expressões são verdadeiras. Já o segundo print apresenta uma saída `True` pois só é necessário uma das sentenças ser verdadeira. O terceiro caso, mostra um `True`, pois está negando o valor `False` da expressão o transformando em verdadeiro.

### Tabela da Verdade

Nessa tabela são apresentados os resultados dos operadores lógicos.
#### Tabela AND
Leva dois operandos.

| <p align=center> a </p> | <p align=center> and </p> | <p align=center> b </p> | <p align=center> Retorno </p> |
|----------|:-------------:|------:  |------:  |
| <p align=center> `True` </p>| <p align=center> and </p> | <p align=center> `True` </p>| <p align=center> `True` </p>|
| <p align=center> `True` </p>| <p align=center> and </p> | <p align=center> `False` </p>| <p align=center> `False` </p>|
| <p align=center> `False` </p>| <p align=center> and </p> | <p align=center> `True` </p>| <p align=center> `False` </p>|
| <p align=center> `False` </p>| <p align=center> and </p> | <p align=center> `False` </p>| <p align=center> `False` </p>|

  
#### Tabela OR
Leva dois operandos.
| <p align=center> a </p> | <p align=center> or </p> | <p align=center> b </p> | <p align=center> Retorno </p> |
|----------|:-------------:|------:  |------:  |
| <p align=center> `True` </p>| <p align=center> or </p> | <p align=center> `True` </p>| <p align=center> `True` </p>|
| <p align=center> `True` </p>| <p align=center> or </p> | <p align=center> `False` </p>| <p align=center> `True` </p>|
| <p align=center> `False` </p>| <p align=center> or </p> | <p align=center> `True` </p>| <p align=center> `True` </p>|
| <p align=center> `False` </p>| <p align=center> or </p> | <p align=center> `False` </p>| <p align=center> `False` </p>|

#### Tabela NOT
Leva um operando.
| <p align=center> not </p> | <p align=center> a </p> |<p align=center> Retorno </p> |
|----------|:-------------:|------:  |
| <p align=center> not </p>| <p align=center> `True` </p> | <p align=center> `False` </p>| 
| <p align=center> not </p>| <p align=center> `False` </p> | <p align=center> `True` </p>| 





  


  

  
 







