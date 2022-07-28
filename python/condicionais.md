---
title: Condicionais
description: 
published: true
date: 2022-06-17T14:35:53.266Z
tags: 
editor: markdown
dateCreated: 2022-05-17T03:26:34.447Z
---

# Estruturas condicionais

## O que é e como funciona


Uma estrutura condicional é um artifício das linguagens para analisar uma condição, ou seja, verificar se ela é verdadeira e, com base no resultado desta análise, executar uma certa ação.

> Exemplo:
`SE condição`
`ENTÃO comando`

Para compreender bem as estruturas condicionais é necessário estudar sobre os operadores codicionais: [operadores](/python/operadores)

As estruturas condicionais podem ser basicamente em três:

- Condicionais simples;
- Condicionais compostas;
- Condicionais aninhadas.

## Condicionais simples

Essa estrutura utiliza-se basicamente apenas de `if`, que traduzido significa "se".

**O** `if` **executa uma ação somente se a condição testada for verdadeira, executando tudo o qeu estiver dentro dela, e para isso é importante fazer a identação.**

> Sintaxe:
```python
if condição:
		`execute_esta_ação`
```

Observe que após o comando do `if`, houve a identação do que deveria ser executado; caso contrário, se estivesse alinhado com o if, o comando de ação estaria fora da estutra condicional, não obdecendo a esta.

>Exemplo:
{.is-info}
```python
a = 2
b = 4
soma = a + b

if soma > 0:
		print ('Maior que zero')
```

> Saída:
{.is-success}
```python
Maior que zero
```

## Condicionais compostas

A estura condicional composta faz uso do `if` , já explicado, e do `else`, que traduzido segnifica "senão". 

Esta estrutra analisa uma condição em `True` ou `False`. Caso a condição contida no `if` não seja verdadeira, a estrutura executará o comando contido no `else`.


> Sintaxe:
```python
if condição:
		execute_esta_ação
else:
		execute_esta_ação
```


>Exemplo:
{.is-info}
```python
a = 2
b = 4
soma = a + b

if soma < 0:
		print ('Menor que zero')
else:
		print ('Maior ou igual a zero')
```

> Saída:
{.is-success}
```python
Maior ou igual a zero
```

Observe que a condição presente no comando `if` é `False`, logo não foi executada, passando para o comando `else`, o qual executa a ação contida nele.

## Condicionais aninhadas

As estruturas condicionais aninhadas são usadas a fim de averiguar mais de uma condição.

EStas estruturas nada mais são do que várias condições em cascata, ou seja um `if` dentro de outro `if`. Para isso, esta estrutura, além do `if` e `else`,  faz uso do `elif`, o qual é uma junção **ELSE + IF**


> Sintaxe:
```python
if condição1:
		execute_esta_ação
elif condiçao2:
		execute_esta_ação
else:
		execute_esta_ação
```


>Exemplo:
{.is-info}
```python
a = 2
b = 4
soma = a + b

if soma < 0:
		print ('Menor que zero')
elif soma = 0:
		print ('Igual a zero')
else:
		print ('Maior que zero')
```

> Saída:
{.is-success}
```python
Maior que zero
```

Observe que agora foi adicionada uma condição para testar se era igual a zero, o que nao havia sido feito anteseriormente.

## Condicionais com operadores booleanos e de associação.

As esturas cpndicionais podem ser usadas não somente com os operadores condicionais, mas também com outros operados, como os booleanos. Veja a tabela abaixo e os exemplos.

` ` ` ` ` ` ` ` ![condicional-bool.png](/condicional-bool.png)

>Exemplo 1 (condicional composta):
{.is-info}
```python
a = 4.7
b = 2.2

if b < a and a > 4:
		print ('Ambas condições são verdadeiras')
else:
		print ('Ao menos uma condição é verdadeira ou ambas falsas')
```

> Saída:
{.is-success}
```python
Ambas condições são verdadeiras
```

>Exemplo 2 (condicional aninhada):
{.is-info}
```python
media = 6
if media < 4:
		print ("Aluno(a) foi reprovado(a)")
elif media > 4 and media < 6:
		print ("Aluno(a) fará a recuperação")
else:
		print ("Aluno(a) foi aprovado(a)")
```


> Saída:
{.is-success}
```python
Aluno(a) foi aprovado(a)
```

