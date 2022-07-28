---
title: Dicionários
description: 
published: true
date: 2022-05-24T22:16:09.916Z
tags: 
editor: markdown
dateCreated: 2022-05-22T23:47:11.878Z
---

# Dicionários
Os dicionários, também conhecidos como dicts (em inglês), são estruturas de dados compostas que servem para armazenar informações em python. Os dicionários são muito importantes e muito utilizados, pois facilitam diversas aplicações e operações.

Diferentemente das listas e tuplas, os dicionários apresentam dois elementos principais, a chave e o valor, a chave é um index literal e personalizado cuja função é posicionar o elemento dentro do dicionário. Já o valor, é realmente o valor que a chave recebe, esses podem ser de vários tipos (inteiro, float, lista, outro dicionário, string, etc.)

## Sintaxe
Um dicionário em python é delimitado por chaves `{}`, sendo assim, a estrutura de um dicionário é:
```python
{ 'chave': 'valor' }
```
> Atenção aos dois pontos, os dois elementos de um dicionário (chave e valor) devem estar separados por dois pontos.
{.is-warning}

Quando houver mais de uma informação em um dicionário, essas informações são separadas por vírgula.

## Como criar um dicionário em python
Os dicionários são usados quando desejamos indexar os valores de acordo com as suas características, por exempo, se em um código pretendo armazenar os dados pessoais de alguém, como nome e idade, e acessar facilmente as informações, basta criar um dicionário.

Podemos criar um dicionário em python de várias formas, sendo as mais usuais:

```python
dados_pessoais = {'nome': 'João Lucas', 'idade': 15}
```
ou utilizando a função dict que o próprio python possui, recebendo as informações como parâmetro e transformando em um dict da seguinte forma:

```python 
dados_pessoais = dict(nome='João Lucas', idade=15)[
```

Também é possível criar um dict através de uma tupla com duas listas:

```python
dados_pessoas = dict((['nome','idade'], ['João Lucas', 15]))
```
Ao testar as saídas com um print, as duas formas de criar um dicionário apresentam o mesmo resultado:

```python
print(dados_pessoais)
```
> Saída:
`{ 'nome': 'João Lucas', 'idade': 15}`
{.is-success}

> Os dicionários possuem várias funções e operações que tornam possível a sua manipulação. Nos tópicos abaixo serão exemplificadas algumas dessas manipulações.
## Manipulação de dicionários
### Adicionar e alterar elemento
Também é possível adicionar elementos depois do dict já criado, No exemplo acima, podemos adicionar informações de endereço com:

```python
dados_pessoais['endereco'] = 'Rua Paraná'
```
Isso resultará no seguinte dicionário:

> `{ 'nome': 'João Lucas', 'idade': 15, 'endereco':'Rua Paraná'}`
{.is-info}

Da mesma forma que adicionamos um elemento, podemos também alterá-lo. Se a idade da pessoa, que anteriormente era 15, passa a ser 16, podemos alterar:

```python
dados_pessoais['idade'] = 16
```
O resultado será:
> `{ 'nome': 'João Lucas', 'idade': 16, 'endereco':'Rua Paraná'}`
{.is-info}
### Acessar um valor de um dicionário
Quando queremos acessar o valor de uma chave dentro de um dicionário criado, colocamos o nome do dicionário, e dentro de colchetes a chave que se deseja acessar, tendo como base o dicionário criado acima, podemos acessar o nome da pessoa da seguinte forma:
```python
print(dados_pessoais['nome'])
```
> Saída:
João Lucas
{.is-success}

Os dicionários também possuem uma função get(), que recebe a chave como parâmetro para acessar seu valor:
```python
print(dados_pessoais.get('idade'))
```
> Saída:
16
{.is-success}
### Acessar todas as chaves de um dicionário
Em python, podemos acessar todas as chaves usando um laço de repetição (for):
> Nas seguintes linhas de código é fundamental o entendimento do conteúdo de laços de repetição
{.is-warning}

```python
for chave in dados_pessoais:
		print(chave)
```
> Saída :
nome
idade
endereco
{.is-success}

Também podemos acessar utilizando a função `keys()`, já existente em python. Essa retorna uma lista das chaves.:
```python
print(dados_pessoais.keys())
```
> Saída 
dict_keys(['nome', 'idade', 'endereco'])
{.is-success}


### Acessar todos os valores do dicionário
O acesso de todos os valores de um dicionário é bem semelhante ao de todas as chaves, este pode ser feito por meio de um laço de repetição:
```python
for chave in dados_pessoais:
		print(dados_pessoais[chave])
```
> Saída :
João Lucas
16
Rua Paraná
{.is-success}

Também podemos acessar coma a função `values()`, que retorna uma lista de valores:
```python 
print(dados_pessoais.values())
```
> Saída :
dict_values(['João Lucas', 16, 'Rua Paraná'])
{.is-success}

### Método pop
O método pop é utilizado para retirar determinadas informações de dentro de um dicionário. O método recebe como parâmetro a chave que se deseja retirar e retorna o valor dessa chave, que também será retirado. 

Assim, executando as seguintes linhas de código;
```python
print(dados_pessoais.pop('endereco'))
```
Obtemos a seguinte saída:
> Rua Paraná
{.is-success}

Já quando executamos da seguite maneira:
```python
dados_pessoais.pop('endereco')
print(dados_pessoais)
```
> Saída:
`{ 'nome': 'João Lucas', 'idade': 16}`
{.is-success}

Observa-se que a chave 'endereco' e o valor associado a ela, que antes estavam no dicionário, foram retirados.
### Transformando duas listas em dicionário

Quando temos duas listas de informações e queremos relacionar essas informações em um dict, podemos transformá-las em um dict com as funções `zip()` e `dict()`, porém, as duas listas devem ter o mesmo número de elementos.

```python
chaves = ['nome', 'idade']
valores = ['Joao Lucas', 16]
dados_pessoais = dict(zip(chaves, valores))
print(dados_pessoais)
```

> Saída:
`{ 'nome': 'João Lucas', 'idade': 16}`
{.is-success}

### Verificar se existe chave
Para verificar se existe determinada chave dentro de um dicionário, podemos fazer um condicional da seguinte forma:
```python
if 'nome' in dados_pessoais:
	print('sim')
```
Caso o dicionário tenha alguma chave 'nome', a saída será:
> sim
{.is-success}

O conteúdo de dicts é extenso por possuir diversas possibilidades, sendo assim, a prática é fundamental para o entendimento e fixação.