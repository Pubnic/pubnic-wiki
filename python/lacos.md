---
title: Laços de Repetição
description: 
published: true
date: 2022-06-17T17:21:12.563Z
tags: 
editor: markdown
dateCreated: 2022-05-17T03:28:21.982Z
---

# Laços de Repetição

## O que é e como funciona

Uma estrutura de repetição é uma estrutura de controle usada para executar um bloo de código repetitivamente em um loop contínuo até uma determinada condição ser satisfeita. O loop faz com que se chame essa condição de iteração,uma repetição que analisa alguma estrutura.

> OBS: É importante configurar corretamente essa codição a fim de não cair em erros fatais no programa.
{.is-warning}

A estrutura de repetição em python funciona como uma bloco de código ideal para executar uma única operação em todos os dados. POde-se, depedendo da necessidade, estabelecer-se subcondições (com diferentes IFs) para realizar verificações específicas.

Em python, os loops são codificados por meio dos comandos `for` e `while`.

## Para-cada | For (`for`)

O comando `for` permite pecorrer os itens de uma coleção e, para cada um deles, executar um bloco de código. ESse comando pe utilizado geralemente para percorrer sequências previamente  conhecidas. Já as sequências são coleções embutidas: strings, listas, tuplas e buffers, por exemplo. 

Assim sendo, a cada ("para-cada") "volta" do laço `for`, a variável definida na chamada assumo o valor de um dos elementos da coleção; a execução do comando é finalizada quando chega ao fim da coleção ou por meio de um comando de interrupções.

Em python, o `for` é executado sobre uma coleção de ojetos; o que significa que é possível iterar sobre diversos tipos de objetos e não apenas númeors inteiros, sendo que a única restrição é que essa coleção de objetos precisa ser ***iterável***. Um iterável (***iterable***) é um tipo de objeto que, ao passar para a função embutida `inter()`, retorna um ***iterator*** - um objeto que representa um fluxo de dados e é responsável por dividir o iterável e retornar cada um dos seus elementos

A sintaxe básica da estrutura de repetição for em Python é a seguinte:

> `for` < item > `in` < conjunto_de_itens >:
` ` ` ` ` ` ` ` < bloco_de_codigo>

aonde **item** corresponde a cada elemento presente na variável que permite a interação e **conjunto_de_itens** pode ser uma string,uma lista, uma tupla,um dicionário ou um objeto que permita interações (iteráveis).


> Exemplo 01:
{.is-info}

 ```python
nomes = ['Suzane', 'Débora', 'Wander']
for n in nomes:
	 print (n)
```

> Saída:
{.is-success}
```python
Suzane
Débora
Wander
```

> Exemplo 02:
Caso seja necessário um índice numérico, utiliza-se a função interna `enumarate`
{.is-info}

 ```python
for num, nomes in enumarate(['Suzane', 'Débora', 'Wander']):
	 print num, nomes
```

> Saída:
{.is-success}
```python
0 Suzane
1 Débora
2 Wander
```

> Exemplo 03:
Neste exemplo, a variável é x; no início do laço temos x = 1, porém dentro do for temos a adição com o 1, fazendo com que a contagem do print comece em 2 como vê-se na saída.
{.is-info}

 ```python
lista = [1, 2, 3]
for x in lista:
     x += 1
     print(x)
print(lista)
```

> Saída:
{.is-success}
```python
2
3
4
[1, 2, 3]
```

### Cláusula BREAK

O `break` é uma cláusula utilizada para alterar o fluxo de execução de um laço, interrompendo o loop , encerrando sua execução ao encontrar uma condição específica. o `break` é utilizado em conjunto com uma estrutura condicional (ver:[condicionais](/python/condicionais)) ou até mesmo com outro laço de repetição `for`. A sintaxe dessa estrutura é a seguinte:

> `for` < item > `in` < conjunto_de_itens >:
` ` ` ` ` ` ` ` < bloco_de_codigo>
` ` ` ` ` ` ` ` `if` < condicao_verdadeira >:
` ` ` ` ` ` ` ` ` `< outras_instrucoes >
` ` ` ` ` ` ` ` ` ` `break`

> Exemplo:
{.is-info}

 ```python
pessoas = [({'Nome': 'Suzane', 'cidade-natal': 'Goiânia - GO'}),
                     ({'Nome': 'Débora', 'cidade-natal': 'Brasília - DF'}),
                     ({'Nome': 'Wander', 'cidade-natal': 'Bujaru - PA'})]
contador = 0
for pessoa in pessoas:
    contador += 1
    print(contador)
    if pessoa['Nome'] == 'Débora':
        print(pessoa['Nome'], "nasceu em", pessoa['cidade-natal'])
        break
```

> Saída:
{.is-success}
```python
1
2
Débora nasceu em Brasília - DF
```

No código acima, utilizou-se dicionário (ver: [variaveis](/python/variaveis)); onde o primeiro elemento corresponde à chave e o segundo ao valor. Nota-se que foi criado uma dicionário de pessoas e utilizado o comando `for` para pecorrer cada item do dicionário e o `if` para avveriguar em cada pessoa do dict a que tem o nome *Débora* que ao encontrar dá um `break` na execuçãoe  imprime a frase. A variável `contador` foi colocada para imprimir o número de vezes que o loop foi executado, feito somente para demonstrar o funcionamento do `break`, pois sem ele o loop seria executado três vezes.

### Cláusula CONTINUE

Assim como o `break`, a cláusula `continue` altera o fluxo de execução de um laço, mas, ao invés de interromper, ela pula para o próximo item; isso é feito em conjunto com uma validação, a qual pode ser realizada com uma estrutura condicional ou outro laço de repetição.

> Exemplo:
{.is-info}

 ```python
pessoas = [({'Nome': 'Suzane', 'cidade-natal': 'Goiânia - GO'}),
                     ({'Nome': 'Débora', 'cidade-natal': 'Brasília - DF'}),
                     ({'Nome': 'Wander', 'cidade-natal': 'Bujaru - PA'})]
contador = 0
for pessoa in pessoas:
    contador += 1
    if pessoa['Nome'] == 'Débora':
        continue
    print(contador)
    print(pessoa['Nome'], "nasceu em", pessoa['cidade-natal'])
```

> Saída:
{.is-success}
```python
1
Suzane nasceu em Goiânia - GO
3
Wander nasceu em BUjaru - PA
```
Esse exemplo é uma alteração do código anterior feito para, agora, pular para o pŕoximo item ao encontrar com o nome na condição `if`; como foi utilizado `continue`, a aexibição do contador e a frase não foram exibidas para o segundo elemento.

### Função RANGE em `FOR`

A função `range()` produz uma sequência de números com início e fim determinados e *default* de inicialização da contagem em "0" e é incrementada adicionando "1". Sua sintaxe é:

> `range(início, parada, incremento)`

Aonde **início** é um valor opcional e corresponde a partir de qual número o range será iniciado, **parada** é um valor obrigatório e indica o número de parada do `range` e **incremento** é opcional e indica o valor que se quer adicionar ntre um item e outro.

Essa função é usada no `for` a fim de executar um determinado conjunto de instruções pea quantidade de vezes indicadas na função. Veja os exemplos:

> Exemplo 01:
{.is-info}

 ```python
for n in range(5):
	 print (n)
```

> Saída:
{.is-success}
```python
0
1
2
3
4
```

Observe que nesse exemplo foi seguido o *default*, onde tem-se somente o valor da parada,que é obrigatóro.
> Exemplo 02 - Decrementando
{.is-info}

```python
for numero in range(10, 0, -1):
    print (numero)
```

> Saída:
{.is-success}
```python
10
9
8
7
6
5
4
3
2
1
```

> Exemplo 03:
{.is-info}

 ```python
for n in range(10):
	 if n % 2 != 0:
   		print("O número", n, "é ímpar"
```

> Saída:
{.is-success}
```python
O número 1 é ímpar
O número 3 é ímpar
O número 5 é ímpar
O número 7 é ímpar
O número 9 é ímpar
```

> Exemplo 03:
{.is-info}

 ```python
for numero in range(10, 21,4):
    if numero % 2 == 0:
        print("O número", numero, "é par")
```

> Saída:
{.is-success}
```python
O número 10 é par
O número 14 é par
O número 18 é par
```

Note que os núemros "12" e "16" foram pulados entre os pares devido ao passo de "4"

### `ELSE` em `FOR`

O `for` também pode ser usado junto com o condicional `else`. Ele funciona quando o loop é encerrado sem nenhuma interrupção, como se utilizasse o `break`. O `else` é opcional na estrutura `for` .

> `for` < item > `in` < conjunto_de_itens >:
` ` ` ` ` ` ` ` < bloco_de_codigo > 
`else`:
` ` ` ` ` ` ` ` <novo_bloco_de_codigo>

> Exemplo:
{.is-info}

 ```python
nomes = ['Suzane', 'Débora', 'Wander']
for n in nomes:
	 print (n)
else:
	 print("Laço de repetição finalizado")
```

> Saída:
{.is-success}
```python
Suzane
Débora
Wander
Laço de repetição finalizado
```

### Laços aninhados

Quando ocorre uma situação em que é necessário pecorrer outra variável iterável dentro de uma estrutura de repetição; para tal é usado um loop dentro de outro. Contudo, deve-se tomar cautela com essa estrutura,pois ao se azer muitos laços aninhados, torna-se o código confuso e de difícil manutenção.

> Exemplo
{.is-info}

```python
for numero_coluna1 in range(3, 6, 2):
    print("Tabuada do ", numero_coluna1)
    for numero_coluna2 in range(11):
        print(numero_coluna1, "x", numero_coluna2, " = ", numero_coluna1 * numero_coluna2)
```

> Saída
{.is-success}

```python
Tabuada do  3
3 x 0  =  0
3 x 1  =  3
3 x 2  =  6
3 x 3  =  9
3 x 4  =  12
3 x 5  =  15
3 x 6  =  18
3 x 7  =  21
3 x 8  =  24
3 x 9  =  27
3 x 10  =  30
Tabuada do  5
5 x 0  =  0
5 x 1  =  5
5 x 2  =  10
5 x 3  =  15
5 x 4  =  20
5 x 5  =  25
5 x 6  =  30
5 x 7  =  35
5 x 8  =  40
5 x 9  =  45
5 x 10  =  50
``` 

> A estrutura `for` em python não pode ficar em branco, ou seja, sem execução de instrução. Dssa forma, quando é necessário "ignorar"/"deixar passar" o laço em algum momento do desenvolvmento do software, mas que pode vir a ser usado poseriormente, utiliza-se a instrução `pass`:
	>> `for` n `in` range(5):
  		 ` ` ` ` ` ` ` ` `pass`
{.is-warning}



## Enquanto | while

O comando `while` executa um conjunto de instruções várias vezes enquanto uma condição é atendida; quando o resultado desta determinada condição passa a ser falso,a execução é interrompida, siando do loop.

