---
title: Operadores
description: 
published: true
date: 2022-05-26T21:20:04.204Z
tags: 
editor: markdown
dateCreated: 2022-05-17T03:22:39.862Z
---

# Operadores

Os operadores são usados na construção de expressões, que possuem uma quantidade variada de operadnos.

No python existem os seguintes tipode de operadores:

- Operadores aritméticos;
- Operadores de comparação ou relacionais;
- Operadores lógicos;
- Operadores de atribuição;
- Operadores de incremento e decremento;
- Operadores de identidade;
- Operadores de assossiação.

## Operadores Aritméticos

Esses operadores são usados na execução de operações matemáticas. Eles têm como característica a precedência, ou seja, ele obdece a ordem de execução deles e acontece quando mais deum operador está presente em uma expressão.

### Adição (`+`)

- Realiza a soma entre operandos; adiciona o sinal de positivo ao número.

> Exemplo:   (-10 **+** 7)

### Subtração (`-`)

- Realiza a subtração entre operandos; adiciona o sinal de negativo ao número.

> Exemplo:   (-10 **-** 7)

### Multiplicação (`*`)

- Realiza a multiplicação entre operandos.

> Exemplo:   (10 *  2)

### Divisão (`/`)

- Realiza a divisão entre operandos.

> Exemplo:   (10 **/** 2)


### Divisão inteira (`//`)

- Realiza a divisão entre operandos e a parte decimal do resultado.

> Exemplo:   (10 **//** 3)


### Módulo (`%`)

- Retorna o resto da divisão entre operandos.

> Exemplo:   (10 **%** 2)


### Exponenciação (`**`)

- Realiza o cálculo de um número elevado a outro.

> Exemplo:   (10**2)

Abaixo segue um código com exemplos de cada uma das operações:

>Exemplo:
{.is-info}
```python
a = 10
b = 3
soma = a + b
subtracao = a - b
multiplicacao = a * b
divisão = a / b
divisao_inteira = a // b
modulo = a % b
exponenciação = a ** b

print(soma)
print(subtração)
print(multiplicacao)
print(divisao)
print(divisao_inteira)
print(modulo)
print(exponenciacao)
```

> Saída:
{.is-success}
```python
13
7
30
3.3333
3
1
1000
```

### Ordem de precedência

1.  As expressões contidas em parênteses têm a prededência maior no Python; isso permite que a expressão execute antes da outra.

> Ex:
{.is-info}
```python
print((7 + 3) * 2)
```

> Saída:
{.is-success}
```
20
```

2.  Após os parênteses, o próximo operador com maior precedência é o de exponenciação.


> Ex:
{.is-info}
```python
print(7 + 3 ** 2)
```

> Saída:
{.is-success}
```python
16
```

3. A multiplicação e a divisão, assim como na matemática, têm precedência sobre a adição e subtração.


> Ex:
{.is-info}
```python
print(7 * 3 + 2)
```

> Saída:
{.is-success}
```python
23
```

4. Ordem d eorecedência é avaliada da esquerda para a direita; ou seja aapós o analisado acima, a sequência de execução será da esquerda para a direita.

> Ex:
{.is-info}
```python
print(7 + 3 - 2)
```

> Saída:
{.is-success}
```python
8
```

## Operadores de comparação ou relacionais

Os operadores de comparação são utilizados a fim de comparar valores, o que retorna `True` ou `False`, a depender da condição.

### Maior que (`>`)

- Verifica se um valor é maior que o outro.

> Exemplo: a **>** 4 

### Menor que (`<`)

- Verifica se um valor é menor que o outro.

> Exemplo: a **<** 4

### Igual a (`==`)

- Verifica se um valor é igual a outro.

> Exemplo: a **==** 4 

### Diferente de (`!=`)

- Verifica se um valor é diferente de outro.

> Exemplo: a **!=** 4

### Maior ou igual a (`>=`)

- Verifica se um valor é maior ou igual a outro.

> Exemplo: a **>=** 4


### Menor ou igual a (`<=`)

- Verifica se um valor é menor ou igual a outro.

> Exemplo: a **<=** 4

Dessa fora, pode-se criar condições para os códigos.

Pra ver sobre condicional, clique aqui: [condicionais](/python/operadores/condicionais)


>Exemplo:
{.is-info}
```python
a = 10
b = 3
soma = a + b

if soma < 15:
				print ('soma menor que 15')
else:
				print ('soma maior que 15')`
```

> Saída:
{.is-success}
```python
soma menor que 15
```


## Operadores lógicos

Para entender os operadores lógicos e relacionais, leia primeiro sobre lógica boolenana: [logica](/python/logica)

Esses operadores são usados para unir expressões condicionais, por meio de conectivos lógicos: `and`,`or`,`not`.


### AND (`and`)

- Retorna verdadeiro (`True`) se **todas** as condições forem verdadeiras, caso contrário retorna falso (`False`)

> Exemplo: x > 2 **and** x<5



### OR (`ou`)

- Retorna verdadeiro (`True`) se **uma** das condições forem verdadeiras, caso contrário retorna falso (`False`)

> Exemplo: x > 2 **or** x<5


### NOT (`not`)

- Inverte o resultado, se ele forverdadeiro (`True`), o operador retorna falso (`False`) e vice-versa

> Exemplo: **not** (x > 2 **and** x<5)

>Exemplo:
{.is-info}
```python
idade_debora = 24
idade_julia = 13

# usando o and
if idade_debora >=18 and idade_julia>=18:
				print ('As duas são maiores de idade')
else:
				print ('Ao menos uma delas é maior de idade')`

# usando o or
if idade_debora >=18 or idade_julia>=18:
				print ('Ao menos uma delas é maior de idade')
else:
				print ('As duas são menores de idade')`
```

> Saída:
{.is-success}
```python
Ao menos uma delas é maior de idade
Ao menos uma delas é maior de idade
``` 

Observa-se que a primeira condicional retornou `False` e a segunda `True`.


## Operadores de atribuição


Estes operadores, como o próprio nome diz, atribuem valor  a uma variável, sendo sua representação feita pelo sinal de igual "`=`" e sua variantes.

> Exemplo: variavel **=** 15
Lê-se: "variavel recebe 15"

Abaixo esta os variantes do operador de atribuição:
![operadores-atribuicao.png](/operadores-atribuicao.png)

## Operadores de incremento e decremento

Estes operadores incrementam ou decrementam um determinado valor. Entretanto no Python esses operadores não são permitidos.

Não se escreve coisas no python como:
> `para (int i = 0; i < 5; i++)`
{.is-danger}

Ao invés disso é utlizada a seguinte sintaxe usando laços:

> `for nome_da_variavel in intervalo (iniciar em, parar em, a passo de) `
{.is-success}

Nessa sintaxe mostrada tem-se:
- **Iniciar**: opcional; um número inteiro que especifica em qual posição começar e tem como padrão o "0" (zero);
- **Parar**: Um número inteiro que determina em qual posição finalizar;
- **A passo de**: opcional; um número inteiro que especifica a incrementação/decrementação e tem como padrão o "1" (um).


Exemplo:
{.is-info}
```python
print ('Incrementando:')
for i in range(1,5)
				print(i)

print ('Decrementando:')
for i in range(10, -1, -2)
				print(i)
```

> Saída:
{.is-success}
```pytho
Incrementando:
1
2
3
4
Decrementando:
10
8
6
4
2
0
```


` `

> Observa-se que o número onde se coloca ara parar não aparece na contagem, pois ele é um limite aberto.
{.is-warning}


OBS: Para entender sobre laços de repetição, clique aqui: [lacos](/python/lacos)

## Operadores de identidade

Os operadores de identidade são utilizados para a comparação de objetos, na qual é verificado se eles ocupam uma mesma posição na memória; ou seja, eles serão o mesmo objeto

### Operado IS (`is`)

- Retorna `True` caso as variáveis comparadas forem o mesmo objeto

> Exemplo: sobrenome is 'Guedes'

### Operado IS NOT (`is not`)

- Retorna `True` caso as variáveis comparadas não forem o mesmo objeto

> Exemplo: sobrenome is not 'Guedes'

>Exemplo:
{.is-info}
```python
sobrenome_debora = 'Guedes'
sobrenome_julia = 'Vieira'
sobrenome_marcos = 'Guedes'

if sobrenome_debora is sobrenome_julia:
				print ('Sobrenosmes são o mesmo objeto')
else:
				print ('Sobrenosmes são objetos diferente')

if sobrenome_debora is sobrenome_marcos:
				print ('Sobrenosmes são o mesmo objeto')
else:
				print ('Sobrenosmes são objetos diferente')
```

> Saída:
{.is-success}
```python
Sobrenosmes são objetos diferentes
Sobrenomes são mesmo objeto
```

## Operadores de associação

Estes operados servem para averiguar se uma sequência contém um objeto.

### Operador IN (`in`)

- Retorna `True` caso o valor esteja presente na sequência.

> Exemplo: cor1 in cores

### Operador NOT IN (`not in`)

- Retorna `True` caso o valor esteja ausente na sequência.

> Exemplo: cor1 not in cores
{.is-info}
```python
cores = ["amarelo","verde","azul","vermelho"]

cor_1 = "vermelho"
cor_2 = "roxo"

print(cor_1 in cores)
print(cor_2 in cores)
```

> Saída:
{.is-success}
```pyhton
True
False
```



