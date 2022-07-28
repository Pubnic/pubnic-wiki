---
title: Funções
description: 
published: true
date: 2022-05-20T17:54:57.230Z
tags: 
editor: markdown
dateCreated: 2022-05-20T17:19:04.355Z
---

# Funções 
## O que são
As funções, quando inseridas no contexto da programação, tem similaridade com as funções matemáticas. Estas são pedaços de códigos agrupados e com um nome, onde são feitos cálculos ou tarefas que podem retornar (ou não) algum valor.

### Parâmetros

Os parâmetros são os valores que a função necessita para executar suas tarefas, a função recebe dentro de parênteses. A depender da tarefa da função, pode receber nenhum ou vários parâmetros. Quando a função recebe mais de um parâmetro, estes são separados por vírgula.

## Motivação

As funções são muito importantes para a programação, principalmente para códigos mais complexos, já que agrupam o código em diferentes blocos independentes. Dessa forma, a utilização de funções possui vantagens como:

- Facilita a manutenção do código;
- Melhora a organização;
- Reaproveitamento de linhas de código, facilitando o desenvolvimento;


Por exemplo, se durante o código for preciso calcular a média entre números mais de uma vez, faz mais sentido criar uma função que faça esse cálculo e chamá-la toda vez que for preciso do que repetir o mesmo trecho de código várias vezes.

## Declarando uma função em python

Para a criação de uma função, é importante que esta possua um nome significativo e que sugira uma ação, representando a tarefa desta função, os parâmetros e variáveis utilizados também devem ter nomes significativos. 

Os nomes de funções, variáveis e parâmetros normalmente são escritos em letras minúsculas e com palavras separadas por underscores, para melhor legibilidade do código.

> É importante ter bastante atenção à indentação das funções, em python, as linhas de código de uma função tem um espaçamento padrão de 4 espaços ou um TAB da declaração da função. Se um programa não apresenta indentação correta, pode se comportar de forma inesperada.
{.is-warning}

Em python podemos declarar as funções com :

```python
def nome_da_funcao(parâmetro_1, parâmetro_2):
    comandos
    return 
```
> Atenção aos dois pontos, sempre após a declaração da função deve ter dois pontos.
{.is-warning}

Se uma função tem parâmetros em sua declaração, quando for chamada, deve-se colocar os valores que correspondem a esses parâmetros. Exemplo de chamada de função:

```python
nome_da_funcao(variavel_1, variavel_2)
```

Por exemplo, se precisamos calcular a soma entre duas variáveis (a, b):

- Função com parâmetros e retorno:

```python
def soma(a, b):
		resultado = a + b
		return resultado

print("o resultado da soma é", soma(1, 2))
```

A função, ao ser chamada com as variáveis a = 1, b = 2, apresentará o seguinte resultado:

> Saída:
o resultado da soma é 3
{.is-success}

- Função sem parâmetros e sem retorno, nessa função, o a e o b são fixados em 1 e 2, respetivamente, já que esta não possui parâmetros.

```python
def soma():
		a = 1
		b = 2
		print("O resultado da soma entre 1 e 2 é", a+b)

soma()
```


> Saída:
o resultado da soma entre 1 e 2 é 3
{.is-success}


- Função com parâmetros e sem retorno:

```python
def soma(a, b):
		print("o resultado da soma é", a + b)

soma(1, 2)
```

> Saída:
o resultado da soma é 3
{.is-success}



De acordo com os exemplos acima, as funções podem apresentar o mesmo comportamento dependendo da forma que são chamadas, mesmo que tenham estruturas diferentes.