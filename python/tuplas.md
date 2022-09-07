---
title: Tuplas 
description: 
published: true
date: 2022-09-07T03:12:41.006Z
tags: 
editor: markdown
dateCreated: 2022-05-30T14:32:58.137Z
---

# Tuplas 
Tupla é um estrutura de dados composta em python, que se assemelha bastante a uma lista, porém, ao contrário da lista, que podemos adicionar, alterar e remover elementos, uma tupla é imutável.

Porém, uma tupla não é considerada totalmente imutável, pois, se uma tupla for composta de duas listas, as duas listas podem ser modificadas.

## Como declarar uma tupla em python
Uma tupla é declarada entre parênteses e com os seus elementos separados por vírgula, da seguinte forma:

```python
 numeros = (1, 2, 3)
```

Ao imprimir a variável criada, obtemos a seguinte saída:
```
print(numeros)
```
> (1, 2, 3)
{.is-success}

Também é possível declarar uma tupla sem utilizar os parênteses, porém, colocar os parênteses é considerada uma boa prática.

Para criar uma tupla com apenas um elemento, deve ser acrescentada uma vítgula final, da seguinte forma:

```python
 numeros = (1,)
```
## Contar elemento em uma tupla
Em uma tupla, podemos contar quantas vezes um elemento aparece dentro de uma tupla, utilizando a função `count()`, assim, para verificar quantas vezes o número 10 aparece em uma tupla, podemos fazer assim:

```python
numeros = (5, 20, 30, 10, 12, 10)
print(numeros.count(10))
```

> Saída:
2
{.is-success}

A saída esperada é 2, pois o elemento 10 aparece duas vezes na tupla.
## Fatiamento em tuplas
Assim como outras variáveis compostas em python, também é possível acessar os elementos de uma tupla, ou uma parte desses elementos por meio de índices. 

É importante lembrar que em python os índices iniciam com 0, sendo assim, o primeiro elemento de uma tupla tem índice 0. 

Na tupla declarada acima:
```python
numeros = (5, 20, 30, 10, 12, 10)
```
Podemos representar os seus índices da seguinte forma:

Elemento| Índice |
--------| ------ |
5 | 0 |
20| 1 | 
30|2 |
10| 3 |
12| 4 | 
10 |5

Por exemplo, se desejo pegar o primeiro elemento da tupla declarada acima, acessamos com:
```python
numeros = (5, 20, 30, 10, 12, 10)
print(numeros[0])
```
O que terá como saída:
5
### Acessando elementos de trás pra frente
Também é possível acessar os elementos de trás pra frente, através de números negativos. Por exemplo, a seguinte entrada tendo como base a tupla declarada acima:
```python
numeros = (5, 20, 30, 10, 12, 10)
print(numeros[-1])
```
Apresentaria o seguinte resultado: 
> 10
{.is-success}

### Acessando conjunto de elementos
Já para obter um conjunto de elementos de uma tupla:
```python
print(numeros[0:2])
```
Sendo o primeiro dos números o início e o segundo o final do intervalo. É importante observar que o final do intervalo não está incluido no conjunto, então, considerando a tupla declarada como exemplo, essa entrada apresentaria como saída:
>  (5, 20)
{.is-success}

Outra alternativa para pegar um conjunto de elementos de uma tupla é utilizando dos seguintes operadores:

| Operador | Significado | 
| -------- | ----------- | 
| [a::]    | A partir de a, sendo a incluso e até o final da tupla
| [::a]    | Até o a, porém a não incluso

Como exemplo:
```python
numeros = (5, 20, 30, 10, 12, 10)
print(numeros[1::])
```
> Saída:
(20, 30, 10, 12, 10)
{.is-success}

```python
print(numeros[::1])
```
> Saída:
(5)
{.is-success}
### Modificação na tupla
Como a tupla é uma estrutura de dados composta imutável, não é possível trocar o valor de um determinado elemento. Por exemplo, ao tentar modificar um elemento semelhante ao que é feito em [listas](/python/listas):

```python
numeros = (5, 20, 30, 10, 12, 10)
numeros[1] = 3
```

A saída será a seguinte mensagem de erro:

> 'tuple' object does not support item assignment
{.is-danger}




## Verificando elemento em tupla

Para verificar a existência de um determinado elemento em uma tupla, podemos utilizar dos seguintes operadores:
```python
20 in numeros
```
Que apresentaria um valor True, pois o 20 realmente é um elemento da tupla.
Já as seguintes linhas de código tem como objetivo verificar se o número não está na tupla:
```python
20 not in numeros
```
Então, o valor seria False.

## Índice de elemento de uma tupla 
Em python, na manipulação de tuplas, existe o método `index()`, que serve para exibir o índice de um elemento de uma tupla. Por exemplo, se desejo saber em que índice consigo encontrar o elemento 20, basta executar a seguinte linha de código:
```python
numeros = (5, 20, 30, 10, 12, 10)
print(numeros.index(20))
```
E terá como saída o index, que no caso é 1.


As tuplas podem ser compostas por strings, floats, listas, dicionários, etc.

### Tuplas de listas 
É possível declarar uma tupla composta de listas, apesar da tupla ser imutável, é possível alterar os elementos da lista.
Para declarar uma tupla de listas:
```python
t = (['Luana', 'Joana', 'Mateus'],[1, 2, 3])
print(t)
```
Saída:
> (['Luana', 'Joana', 'Mateus'],[1, 2, 3])
{.is-success}

### Tuplas de dicionários
As tuplas também podem ser formadas por dicionários, sendo declaradas da seguinte forma, para entender mais do dicionario clique [aqui](python/dicionarios) .

```python
t = ({"nome":"Luana"}, {"idade":19})
print(t)
```
Saída:
> ({"nome":"Luana"}, {"idade":19})
{.is-success}


Em python, as tuplas são muito importantes, pois são estruturas essenciais para armazenar dados que não devem ser modificados durante a execução do código.

É possível encontrar informações mais detalhadas sobre tuplas [aqui](https://penseallen.github.io/PensePython2e/12-tuplas.html).