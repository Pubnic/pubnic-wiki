---
title: Listas
description: 
published: true
date: 2022-05-27T13:09:53.513Z
tags: 
editor: markdown
dateCreated: 2022-05-25T18:25:38.769Z
---

# Listas

As listas são utilizados para armazenar diferentes elementos em uma única variável. São representadas pelo tipo `list`, no qual, é uma sequencia de elementos que podem ser do mesmo tipo ou não. As listas são um dos quatro tipos de dados internos do python, que armazenam coleções de dados.

## Criar Listas Python
As listas são construidas colocando os seus itens entre colchetes `[]` que são separados por vírgula. Tais itens podem ser de diferentes tipos, como float, int, string, etc.

```python
# lista de inteiros
lista0 = [1, 2, 3]

# lista vazia
lista1 = []

# lista com diferentes tipos de dados
lista2 = [1, "Ola", 9.5]
```

No python também é possível a criação de listas aninhadas (nested), ou seja, uma lista dentro de outra. As listas mais internas são chamadas de sublista (sublist).

```python
# lista aninhada
lista1 = ["banana", [5, 1, 6], ['c']]
```
## Acessar elementos de uma lista

As listas podem ser acessadas de diferentes maneiras.

### Índice da lista

Um item na lista é acessado por meio do índice `[]`, que começa em zero. Ao se tentar usar um tipo diferente no indice, como float, por exemplo, retornará um `TypeError`.

```python
lista1 = ['p', 'y', 't', 'h', 'o', 'n']

# Primeiro elemento
print(lista1[0])  # p

# Terceiro elemento
print(lista1[2])  # t

# Quinto elemento
print(lista1[4])  # o
```
Saída:

```
p
t
o
```

Para acessar as listas aninhadas usa-se a indexação aninhada, por exemplo:

```python
lista1 = ["amor", [2, 0, 1, 5]]

# Indexação aninhada
print(lista1[0][1])

print(lista1[1][3])

```

Saída:

```
m
5
```

### Indexação negativa

Outra forma de acessar as listas é usando os inteiros negativos. O índice [-1] diz respeito ao último item da lista.

```python
# Indexação negativa em listas
lista1 = ['p','y','t','h','o','n']

# último item
print(lista1[-1])

# primeiro item
print(lista1[-6])
```

Saída:

```
n
p
```
### Representação de uma lista 

Logo abaixo é apresentada uma imagem que mostra por meio de blocos, o funcionamento de uma lista.

```python
lista1 = ["abc", 34, True, 40, "masculino"]
```

![diagrama.png](/diagrama.png)
## Comprimento de uma lista

Para se obter o comprimento da lista, ou seja, o seu número de elementos, utiliza-se afunção `len`. Todavia, como existem as listas aninhadas, é importante salientar que o `len` retorna apenas o comprimento da lista mais externa.

```python
lista1 = ['paz!', 3, ['João', 'Maria'], [1, 2, 3]]
# último item
print(len(lista1))
```
Saída:

```
4
```
## Fatias de Lista

Para se ter o acesso a mais de um item de uma vez da lista, aplica-se a operação de fatiar (slice). O primeiro índice apresenta o ponto inicial da fatia e o segundo é um após o final da fatia (não faz parte da fatia).

```python
lista1 = ['p','r','o','g','r','a','m','a','r']

# elementos do índice 2 ao índice 4
print(lista1[2:5])

# elementos do índice 3 ao final
print(lista[3:])

# elementos do começo ao fim
print(lista1[:])
```

Saída:

```
['o', 'g', 'r']
['g', 'r', 'a', 'm', 'a', 'r']
['p', 'r', 'o', 'g', 'r', 'a', 'm', 'a', 'r']
```

## Adicionar/Alterar elementos da lista

Diferente das tuplas ou strings, as listas são mutáveis, o que significa que podemos alterar ou adicionar elementos. A atualização do item é feita ao se usar o operador e indexação a esquerda de um comando de atribuição.

```python
# Mudança de valores
val = [1, 3, 5, 7]

# Alterando o primeiro item  
val[0] = 2            

print(val)

# Alterando do segundo ao quarto item
val[1:4] = [4, 6, 8]  

print(val) 
```
Saída:

```
[2, 3, 5, 7]
[2, 4, 6, 8]
```
Para adicionar um elemento na lista, usa-se o método `append()`, ou para adicionar vários elementos utiliza-se `extend()`.

```python
itens = ["amor", 3, 9]

itens.append(7.1)

print(itens)

itens.extend([4, "paz", 20])

print(itens)
```

Saída:

```
['amor', 3, 9, 7.1]
['amor', 3, 9, 7.1, 4, 'paz', 20]
```

Um outro método é o `insert()`, que insere elementos em um local desejado da lista. 

```python
valores = [1, 7]
valores.insert(1,5)

print(valores)
```

Saída:

```
[1, 5, 7]
```
Desse modo, o primeiro número refere-se ao índice no qual o elemento será inserido, e o segundo é o valor a ser inserido.

## Excluir elementos da lista

Para deletar os elementos de uma lista, usa-se `del`, que pode até excluir a lista por completo.

```python
# Excluindo itens da lista
lista1 = ['p', 'r', 'o', 'g', 'r', 'a', 'm', 'a', 'r']

# Excluindo um item
del lista1[4]

print(my_list)

# Excluindo vários itens
del lista1[1:6]

print(lista1)

# Excluindo toda a lista
del lista1

# Erro: lista não definida
print(lista1)
```

Saída:

```
['p', 'r', 'o', 'g', 'a', 'm', 'a', 'r']
['p', 'a', 'r']
Traceback (most recent call last):
  File "./prog.py", line 16, in <module>
NameError: name 'lista1' is not defined
```

Existe também o `remove()`, que vai remover o item fornecido, ou `pop()` que remove o item no **índice** fornecido. Ao se utilizar apenas `pop()`, sem forncer um valor de índice, o método remove e retorna o último ínidice.

```python
lista1 = ['p','r','o','g','r','a','m','a']
lista1.remove('p')

# Saída: ['r', 'o', 'g', 'r', 'a', 'm', 'a']
print(lista1)

# Saída: 'g'
print(lista1.pop(2))
# Saída: ['r', 'o', 'r', 'a', 'm', 'a']
print(lista1)

# Saída: 'a'
print(lista1.pop())
# Saída: ['r', 'o', 'r', 'a', 'm']
print(lista1)

lista1.clear()

# Saída: []
print(lista1)

```
Saída:

```
['r', 'o', 'g', 'r', 'a', 'm', 'a']
g
['r', 'o', 'r', 'a', 'm', 'a']
a
['r', 'o', 'r', 'a', 'm']
[]
```

## Operações com Listas

É possível usar alguns operadores em listas. Por exemplo, o operador `+`, faz a combinação de duas listas, isso chama-se concatenação. Já o `*`, faz a repetição de uma lista.

```python
lista1 = [2, 7, 1]

print(lista1 + [4, 9, 5])

print(["py"] * 4)
```
 
Saída:

```
[2, 7, 1, 4, 9, 5]
['py', 'py', 'py', 'py']
```

## Métodos de Lista

Alguns dos principais métodos de python, são apresentados abaixo.

| Métodos      | Descrições |
| ----------- | ----------- |
| append()      | Adiciona elementos no final da lista      |
| extend()   | Adiciona elementos de uma lista em outra lista.|
| insert()   | insere um item no índice definido|
| remove()   | remove um item da lista|
| pop()   | retorna e remove um elemento no índice fornecido.|
| clear()   | remove todos os itens da lista.|
| index()   | retorna o índice do primeiro item correspondente.|
| count()   | retorna a contagem do número de itens passados como argumento.|
| sort()   | classificar itens em uma lista em ordem crescente.|
| reverse()   | inverter a ordem dos itens na lista.|
| copy()   | retorna uma cópia superficial da lista.|










