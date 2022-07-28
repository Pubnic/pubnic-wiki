---
title: Variáveis
description: 
published: true
date: 2022-05-24T17:49:13.909Z
tags: 
editor: markdown
dateCreated: 2022-05-17T03:24:11.298Z
---

# Variáveis

## O que é uma variável

Uma **variável** é uma ferramenta que um programa de computador utiliza para armazenar dados/ informações na memória.

> EX.: `variável = "Olá mundo"`

Neste exemplo, a string (tipo da variável, que você verá logo a mais) `"Olá mundo"` é armazenada na variável denominada `"variável"`; ou seja o programa do computador armazena a string dentro dessa variável e quando essa variável for chamada novamente no código, o valor que ele irá retornar é a string.

## Declaração de variáveis

> `<Nome_da_variavel> = <Valor>`

- `"Nome_da_variavel"` não pode conter caracteres especiais e espaços e nem começar com dígito;
- É sensível, ou seja, há diferença entre lestras maiúsculas e minúsculas. Ex: Nome_da_variavel é diferente de nome_da_variavel;
- Uma sugestão é usar o padrão "Snake Case", onde os espaços são substituidos por "_". EX: `nome_da_variavel`;
- O operador de atribuição é o símbolo de igualdade: `"="`;
- O valor possui um determinado tipo de variável.

Assim, uma variável possui um nome (ou identificador), um tipo, um valor e um endereço de memória.


## Tipos de variáves

O python é uma linguagem dinamicamente tipada, ou seja, não é necessário decalrar o tipo de variável ou fazer *casting* (mudar o tipo de variável), já que o interpretador já realiza esse processo. Dessa forma, o tipo de variável pode variar durante a execução do programa.

Os tipos padrões do Python são:

1. Numéricos:

	- Inteiro (int);
	- Ponto flutuante ou Decimal (float);
	- Booleano (bool);
	- Complexo (complex).
 
2. Não numéricos:

	- String ou Texto (str);
	- Lista (list);
	- Dicionário (dict);
	- Tupla (tuple);
    
      

### Tipo Inteiro (`int`)

O inteiro é um tipo composto por caracteres numéricos inteiros, ou seja, sem um componente decimal; podendo ter ou não sinal, isto é: ser positivo ou negativo.

Ele tem como valor padrão o "0" (zero) e valores possíveis no Python 2 de 2^31^-1 (após isso é considerado long) e no Python 3 não possui limite, podendo o inteiro ter valor tão gande quanto a máquina puder suportar.

> Exemplo:
{.is-info}

 ```python
idade = 25
```

> Saída:
{.is-success}
```python
<class 'int'>
```

### Ponto Flutuante ou Decimal (`float`)

O float é um tipo composto por caracteres numéricos decimais e é usado para números racionais. ALém disso o valor padrão é "0.0"(zero ponto zero).
> 
> Exemplo:
{.is-info}

```python
altura = 1.72
print(type(altura))
```

> Saída:
{.is-success}
```python
<class 'float'>
```

### Booleano (`bool`)

O booleano é um tipo de dado lógico que pode assumir apenas dois valores: `True` ou `False`, sendo seu valor padrão o `False`.
> 
> Exemplo:
{.is-info}

```python
menor_de_idade = True
bebida_alcoolica = False
print(type(menor_de_idade))
print(type(bebida_alcoolica))
```

> Saída:
{.is-success}
```python
<class 'bool'>
<class 'bool' >
```
Para entender melhor sobre lógica booleana: [logica](/python/logica)
### Complexo (`complex`)

Esse tipo é utilizado para representar números complexos e é usado geralemnte em cálculos geométricos e científicos.

O tipo complexo é composto por duas partes: a real e a imaginária, sendo que esta última contém a letra "j" no sufixo.

Existe a função `complex(real[,imag])` do Python, a qual possibilita a criação de números imaginários, passando como argumento: `real`, que é a parte Real do número e o argumento opcional `imag`, que é a parte imaginária do número.

> Exemplo:
{.is-info}

```python
a=4+3j 
print(type(a))
print(complex(7,-4))
```

> Saída:
{.is-success}
```python
<class 'complex'>
(7-4j)
```

### String ou Texto (`str`)

Este tipo é um conjunto de caracteres alfanuméricos, que é usado normalmente para representar palavras, frases ou textos.

> Exemplo:
{.is-info}

```python
forma_geometrica = 'Triângulo'
numero_de_lados = '3 lados'
print(type(forma_geomatrica))
print(type(numero_de_lados))
```

> Saída: 
 {.is-success}
```pyhton
<class 'str'>
<class 'str'>
```


### Lista (`list`)

Este tipo de variável é muito importante e servem para agrupar um conjunto de elementos variados, sendo que estes podem ser inteiros, pontos flutuantes, strings, outras listas e outros tipos também.

Para definir uma lista utiliza-se colchetes para sua delimitação e vírgulas paraa a separação dos elementos.


>Exemplo:
{.is-info}
```python
alunos = ['Ana', 'Carlos', 'Fernanda', 'Joaquim']
notas = [10, 8.0, 7.2, 8.5]
print(type(alunos))
print(type(notas))
```

> Saída:
{.is-success}
```python
<class 'list'>
<class 'list'>
```

### Dicionários (`dict`)

Altamente flexível, o `dict` é usado para agrupar elementos por meio da estrutura de chave e valor, sendo que a chave é o primeiro elemento seguido por dois pontos e o seu respectivo valor.



>Exemplo:
{.is-info}
```python
notas = {'Ana': 10, 'Carlos': 8.0, 'Fernanda': 7.2, 'Joaquim': 8.5}
print(type(notas))
```
> Saída:
{.is-success}
```python
<class 'dict'>
```
---

> Os dicionários possibilitam um tipo de manipulação muito poderosa, chamada de *Dict Comprehensions*. Para mais informações. clique aqui: CRIAR O LINK*
{.is-warning}

### Tuplas (`tuple`)

Da mesma forma que a lista, a tupla é um tipo que agrupa um conjunto de elementos; contudo sua definição é dada de maneira distinta, usa-se parênteses e os elementos também são separados por vírgulas.

Deve-se ter cautela, pois diferentemente das listas, as Tuplas são imutáveis, ou seja, após serem definidas, elas não podme ser modificadas.

>Exemplo:
{.is-info}
```python
`numeros = (33, 25 ,100, 89, 21.3)`
`print(type(numeros))`
```

> Saída:
{.is-success}
```python
<class 'tuple'>
```

---

> Se houver uma tentativa de alterar os itens de uma tupla após sua definição como no código a seguir:
     `tuple = (0,1,2,3)`
		 `tuple[0] = 4`
O seguinte erro do tipo `TypeError` aparecerá no interpretador:
{.is-warning}

> Traceback (most recente call last):
    	File "< stdin>", line 1, in < module> 
   TypeError: 'tuple' object does not support item assignment
{.is-danger}


## Como alterar o tipo de variável

Às vezes é necessário mudar o tipo de uma variável e o Python permite fazer isso de maneira muito simples, veja abaixo os exemplos:

### `float` para `str`
>Exemplo:
{.is-info}
```python
# Antes da conversão
altura = 1.72
print(type(altura))

# Conversão do tipo
altura = str(altura)

# Após a conversão
print(type(altura))
print(altura)
```

> Saída:
{.is-success}
```python
<class 'float'>
<class 'str'>
'1.72'
```
### `int` para `float`
>Exemplo:
{.is-info}
```python
# Antes da conversão
idade = 25
print(type(idade))

# Conversão do tipo
idade = float(idade)

#Após a conversão
print(type(idade))
print(idade)
```

> Saída:
{.is-success}
```python
<class 'int'>
<class 'float'>
25.0
```

### `bool` para `int`
>Exemplo:
{.is-info}
```python
# Antes da conversão
menor_de_idade = True
print(type(menor_de_idade))

# Conversão do tipo
menor_de_idade = int(menor_de_idade)

# Após a conversão
print(type(menor_de_idade))
print(menor_de_idade)
```

> Saída:
{.is-success}

```python
<class 'bool'>
<class 'int'>
1
```

## Erros comuns com os tipos de variáveis

Entreos erros mais comuns ao manejar variáveis no Python estão os **TypeError** o qual está relacionado a tipagem errrada de uma variável ou objeto.

Os **TypeError** podem representar uma operação incompatível, como tentar realizar uma operação matemática com variáveis de tipo incompatíveis, como por exemplo, dividir um float por um "número" dado como string.

Dessa forma, sempre que esse erro aparecer no programa, deve-se ter atenção aos tipos de dados e as operações que estão sendo feitas; se necessário deve-se fazer a conversão de variáveis para se trabalhar com os tipos adequados.


## Escopo de variável

O escopo de uma variável indica a partir de onde, dentro do código, a variável é acessível

Há dois escopos para variáveis em python: escopo global e escopo local.

**1. Escopo local** 

- É uma variavel que existe apenas dentro da função ([funcoes](/python/funcoes)) em que foi criada;
- As variáveis locais são inicializadas a cada nova chamada à função;
- Não é possível acessar os valores dessas variáveis locais fora de onde elas foram criadas;
- Para interegir com variáveis locais, passa-se parâmetros e se retorna valores nas funções.

**2. Escopo global**

- Uma variável global é criada (decalrada) fora das funções e pode ser acessada por todas as funções presentes no módulo em que ela foi definida;
- Uma variável global também pode ser acessada por outros módulos, caso o módulo em que ela foi declarada seja importado.

> Deve-se ter cautela ao mudar o valor de uma global dentro de uma função, pois o que acontece na verdade, é a criação de uma nova variável local com o mesmo nome que a global!
{.is-warning}


>Exemplo:
{.is-info}
```python
variavel_global = 'isso é uma variável que é declarada para todo módulo`

def funcao_escrever_frase():
	variavel_local='isso é uma variável local - dentro da função'
```