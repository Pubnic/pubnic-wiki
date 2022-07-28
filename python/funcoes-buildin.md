---
title: Funções Built-in ou Funções Embutidas
description: 
published: true
date: 2022-07-28T14:56:21.015Z
tags: 
editor: markdown
dateCreated: 2022-06-23T01:35:42.499Z
---

# Funções Built-in (embutidas)

As funções embutidas são funções internas cuja funcionalidade é pré-definida no python. O interpretador python apresenta inúmeras funções que estão sempre prontas para uso. Elas são listadas abaixo:

## Função abs()

A função python `abs()` retorna o valor absoluto de um número, levando apenas um argumento, sendo este o número no qual o valor absoluto deve ser retornado. O argumento pode ser um número inteiro ou ponto flutuante e se for complexo, retornará a magnitude do número.

```python
inteiro = - 10  
print (abs(inteiro))  

flutuante = - 7.83  
print (abs(flutuante)) 

numero_complexo = 3+5j
print (abs(numero_complexo))
```
Saída:

```
10
7.83
5.830951894845301
```

## Função all()

Na função all() é aceito um objeto iterável, como por exemplo, lista, dicionário, set, etc. Retorna verdadeiro caso todos os itens passados sejam verdadeiros, senão retorna falso. Além disso, com o objeto iterável vazio, ela retorna verdadeiro.

```python
# Retorna falso, porque zero é o mesmo que falso.
lista = [0, 1, 1]
x = all(lista)
print(x)

#Retorna falso, porque o primeiro e o terceiro itens são falsos.
tupla = (0, True, False)
x = all(tupla)
print(x)

#Todos os itens são verdadeiros.
meu_set = {2, 1, 6}
x = all(meu_set)
print(x)

#Retorna falso, porque a primeira chave é falsa
dicionario = {0 : "Apple", 1 : "Orange"}
x = all(dicionario)
print(x)
#Para dicionários, a função all() verifica as chaves, não os valores.
```

Saída:

```
False
False
True
False
```

## Função bin()

A função python bin() é usada para retornar a representação binária de um inteiro especificado. Um resultado sempre começa com o prefixo 0b.

```python
a = 9  
b = bin(a)  
print(b) 

```

Saída:

```
0b1001
```

## Função bool()

O método python bool() retorna o valor em booleano (True ou False) usando o procedimento padrão de teste de verdade. Sempre retornará verdade, a menos que:

- O objeto esteja vazio, como [ ], (), {}
- O objeto seja Falso
- O objeto seja 0
- O objeto seja None

```python

teste = []  
print (teste, 'é' ,bool(teste))  
  
teste =  0.0  
print (teste, 'é' ,bool(teste))  
  
teste =  None  
print (teste, 'é' ,bool(teste))  
  
teste =  True  
print (teste, 'é' ,bool(teste))  
  
teste =  'pubnic'  
print (teste, 'é' ,bool(teste))  
```

Saída:

```
[] é False
0.0 é False
None é False
True é True
pubnic é True
```

## Função bytearray()

Essa função retorna um novo vetor de bytes. A classe bytearray é uma sequência mutável de inteiros no intervalo 0 <= x < 256. Ela pode converter objetos em objetos bytearray ou criar um objeto bytearray vazio do tamanho especificado.

### Sintaxe

`bytearray([source[, encoding[, errors]]])`


### Parametros

bytearray()recebe três parâmetros opcionais:

- source (Opcional) - source para inicializar o array de bytes.
- encoding (Opcional) - se a fonte for uma string, a codificação da string.
- errors (opcional) - se source for uma string, a ação a ser tomada quando a conversão de codificação falhar.

O parâmetro source pode ser usado para inicializar a matriz de bytes das seguintes maneiras:

**String**:	Converte a string em bytes usando str.encode(). 
**Integer**:	Cria uma matriz de tamanho fornecido, tudo inicializado como nulo.
**Object**:	Um buffer somente de leitura do objeto será usado para inicializar a matriz de bytes.
**Iterable**:	Cria um array de tamanho igual à contagem iterável e inicializado com os elementos iteráveis.
**Sem source(argumentos)**:	Cria uma matriz de tamanho 0.

### Exemplos
**1. Array de bytes de uma string:**

```python
string = "Python e legal"

# string com encoding 'utf-8'
arr = bytearray(string, 'utf-8')
print(arr)
```

Saída:

```
bytearray(b'Python e legal')
```

**2. Matriz de bytes de um determinado tamanho inteiro:**

```python
tamanho = 5

arr = bytearray(tamanho)
print(arr)
```

Saída:

```
bytearray(b'\x00\x00\x00\x00\x00')
```

**3.Array de bytes de uma lista iterável**

```python
lista = [1, 2, 3, 4, 5]

arr = bytearray(lista)
print(arr)
```

Saída:

```
bytearray(b'\x01\x02\x03\x04\x05')
```

## Função bytes()

A função python bytes() em Python é usada para retornar um objeto bytes . É uma versão imutável da função bytearray().Ela tem os mesmos métodos e o mesmo comportamento de índices e fatiamento, consequentemente,os argumentos do construtor são interpretados como os de bytearray().

### Exemplos

**1.Conversão de string em bytes:** 

```python
string =  "pubnic"  
arr = bytes(string,  'utf-8' )  
print(arr) 
```

Saída:

```
b'pubnic'
```

**2.Cria um byte de um determinado tamanho inteiro:**

```python
tamanho =  5  
arr = bytes(tamanho)  
print(arr)  
```

Saída:

```
b'\x00\x00\x00\x00\x00'
```

## Função callable()

Uma função python callable() em Python é algo que pode ser chamado. Essa função interna verifica e retorna True se o objeto passado parecer ser chamado, caso contrário, False.
Mesmo que `callable() `seja True, a chamada para o objeto ainda pode falhar. Todavia, se `callable()` retornar False, a chamada para o objeto certamente falhará.

### Sintaxe

`callable(object)`

### Exemplo

```python
a = 10
print(callable(a))

def testFunction():
  print("Teste")

b = testFunction
print(callable(b))
```

Saída:

```
False
True
```

## Função chr()

Essa função converte um inteiro em seu caractere unicode. Esse método retorna um caractere unicode do argumento inteiro correspondente ao intervalo de 0 a 1.114.111.

### Sintaxe
`chr(number)`

### Exemplos

```python
print(chr(94))
print(chr(75))
print(chr(1250))
```

Saída:

```
^
K
Ұ
```

Foram convertidos diferentes inteiros em seu caractere unicode correspondente.
- ^ é o caractere unicode de 94
- K é o caractere unicode de 75
- Ұ é o caractere unicode de 1200

## Função complex()

Essa função retorna um número complexo especificando um número real e um número imaginário.

### Sintaxe

`complex(real, imaginary)`

### Exemplo
Converter o número 3 e o número imaginário 5 em um número complexo:

```python
a = complex(3, 5)
print(a)
```
Saída:
```
(3+5j)
```

Converter uma string em um número complexo:

```python
a = complex('2+8j')
print(a)
```

Saída:

```
(2+8j)
```

## Função delattr()

A função delattr() é utilizada quando se quer excluir um atributo de uma classe. Leva dois parâmetros, o primeiro é um objeto da classe, e segundo é um atributo que queremos excluir. Depois de excluir o atributo, ele não está mais disponível na classe e gera um erro ao tentar chamá-lo usando o objeto de classe.


### Sintaxe

`delattr(object, attribute)`

### Exemplo

```python
class Pessoa:
  nome = "Joao"
  idade = 36
  estado = "Ceara"
  
  def getinfo(self):  
        print(self.nome, self.idade, self.estado)  
s = Person()  
s.getinfo()  
delattr(Pessoa,'idade') # removendo atributo 
s.getinfo() 
```

Saída:

```
AttributeError: 'Pessoa' object has no attribute 'idade'
```

## Função dict()

A função dict() cria um dicionário, que é uma  coleção não ordenada, mutável e indexada. O dicionário Python fornece três construtores diferentes para um dicionário de criação.

- Se nenhum argumento for passado, ele cria um dicionário vazio.
- Se um argumento posicional for fornecido, um dicionário será criado com os mesmos pares chave-valor. 
- Se forem fornecidos argumentos de palavra-chave, os argumentos de palavra-chave e seus valores serão adicionados ao dicionário criado a partir do argumento posicional.

### Sintaxe

`dict ([**kwargs])  `
`dict ([mapping, **kwargs]) ` 
`dict ([iterable, **kwargs])  `

- É um argumento de palavra-chave.
- É outro dicionário.
- É um objeto iterável na forma de um(s) par(es) chave-valor.

### Exemplos

Dicionário vazio ou não vazio:
```python
dicionario1 = dict() # retorna um dicionario vazio
dicionario2 = dict(a=8,b=3)  

print(dicionario1)  
print(dicionario2)  
```

Saída:

```
{}
{'a': 8, 'b': 3}
```
Dicionário usando mapping:

```python
dicionario1 = dict({'x': 1, 'y': 6}, z=10) 
dicionario2 = dict({'x': 1, 'y': 6, 'z':10})  

print(dicionario1)  
print(dicionario2)  
```

Saída:

```
{'x': 1, 'y': 6, 'z': 10}
{'x': 1, 'y': 6, 'z': 10}
```

Usando iterable:

```python
dicionario1 = dict([( 1 ,  'um' ), [ 2 ,  'dois' ], [ 3 , 'tres' ]]) 
dicionario2 = dict([[ 'a' , 'A' ],( 'b' , 'B' )])  
 
print(dicionario1)  
print(dicionario2) 
```

Saída:

```
{1: 'um', 2: 'dois', 3: 'tres'}
{'a': 'A', 'b': 'B'}
```

## Função dir()
Essa função retorna todas as propriedades e métodos do objeto especificado, sem os valores, mesmo as propriedades internas que são padrão para todos os objetos.

### Sintaxe
`dir(object)`

### Exemplo
Exibir o conteúdo de um objeto:
```python
class Pessoa:
  nome = "Joao"
  idade = 36
  estado = "Ceara"

print(dir(Pessoa))
```

Saída:

```
['__class__', '__delattr__', '__dict__', '__dir__', '__doc__', '__eq__', '__format__', '__ge__', '__getattribute__', '__gt__', '__hash__', '__init__', '__init_subclass__', '__le__', '__lt__', '__module__',
```

## Função divmod()

Essa função retorna uma tupla contendo o quociente e o resto de uma divisão.

### Sintaxe

`divmod(dividend, divisor)`

### Exemplo

```python
a = divmod(7, 3)
print(a)

```

Saída:

```
(2, 1)
```
## Função enumerate()

Essa função  função recebe uma coleção (por exemplo, uma tupla) e a retorna como um objeto enumerado. Ela leva dois parametros, o primeiro é uma sequencia de elementos, já o segundo é o indice inicial da sequencia. Os elementos da sequencia são obtidos por meio de um metodo loop() ou next().

### Sintaxe
`enumerate (sequence, start=0)  
`

**sequence**: Deve ser uma coleção ou uma sequência. 
**start** : É um índice opcional, usado para definir o início da sequência.

### Exemplos

**Exemplo simples da função:**

```python
resultado = enumerate([1,2,3])  
print(resultado)  
print(list(resultado)) 
```
Saída:

```
<enumerate object at 0x151839ee61c0>
[(0, 1), (1, 2), (2, 3)]
```

**Obter elementos usando um loop:**

```python
resultado = enumerate([1,2,3])  
# Mostrando resultado  
for elemento in resultado:  
    print(elemento) 
```

Saída:

```
(0, 1)
(1, 2)
(2, 3)
```

**Passando o índice inicial como 10, a enumeração começará a partir de 10 até os elementos presentes na sequência.**

```python
resultado = enumerate([1,2,3],10)  
# Mostrando resultado  
for elemento in resultado:  
    print(elemento)  
```
Saída:

```
(10, 1)
(11, 2)
(12, 3)
```

## Função eval()

A função python eval() analisa a expressão passada para ela, se a expressão for uma instrução Python, ela será executada dentro do programa. Ela retorna o resultado avaliado da expressão.

### Sintaxe

`eval(expression, globals, locals)`

**expression**: Uma string que é analisada e avaliada como uma expressão Python.
**globals** (opcional): Um dicionário que especifica os métodos e variáveis globais disponíveis.
**locals** (opcional) - É um outro dicionário que é comumente usado para mapeamento de tipos em Python.

### Exemplos

Avaliar a expressão 'print(55)':

```python
a = 'print(55)'
eval(a)
```

Saída:

```
55
```

**Logo abaixo, a função eval() analisa a expressão com uma variável inteira chamada `a` e retorna o resultado avaliado da expressão.**

```python
a =  5  
print (eval( 'a + 1' ))  
```

Sáida:

```
6
```

## Função filter()

A função filter() é utlizada quando se quer obter elementos filtrados. Ela recebe dois argumentos, o primeiro é uma função e o segundo é o iterável. Seu retorno é uma sequência de elementos do iterável para os quais a função retorna True.

### Sintaxe
`filter (function, iterable)`

**function**: é uma função. Se definida como None, retorna apenas os elementos que são True.
**iterable**: Qualquer sequência iterável como lista, tupla e string.

### Exemplo

**Este exemplo retorna valores superiores a 5 usando a função filter().**

```python
def filtredados(a):  
    if a>5:  
        return a    
resultado = filter(filtredados,(1,2,8,10))  
print(list(resultado)) 
```

Sáida:

```
[8, 10]
```

## Função float()

A função python float() retorna um número de ponto flutuante de um número ou string.

### Sintaxe
`float(value)  `

**value**: um número ou string que é convertido em um número de ponto flutuante.

### Exemplos

```python

# Converter tipo inteiro
print(float(5))  
  
# converter tipo floats  
print(float(8.32))  
  
# converter string do tipo floats  
print(float("-24.17"))  
  
# converter string do tipo floats com espaço em branco
print(float("     -14.10\n"))  
```

Saída:

```
5.0
8.32
-24.17
-14.1
```

## Função format()

A função python format() retorna uma representação formatada do valor fornecido.

### Sintaxe
`format(value, format)  `

**value** : É o valor que precisa ser formatado.
**format** : É a especificação de como o valor deve ser formatado.

### Exemplo

```python
# d, f e b são um tipo
  
# inteiro
print(format(123, "d"))  
  
# argumentos float  
print(format(123.4567898, "f"))  
  
# formato binário
print(format(12, "b"))  
```
Saída:
```
123
123.456790
1100
```

## Função getattr()

Essa função retorna o valor de um atributo nomeado de um objeto. Se não for encontrado, retorna o valor padrão.

### Sintaxe
`getattr(object, attribute, default) ` 

**object**: Um objeto cujo valor de atributo nomeado deve ser retornado.
**attribute**: Nome do atributo do qual se deseja obter o valor.
**default**(opcional): É o valor a ser retornado se o atributo nomeado não for encontrado.

### Exemplo

```python
class Pessoa:
  nome = "Joao"
  idade = 36
  Pais = "Brasil"

x = Pessoa()
print('A idade é:', getattr(x, "idade")) 
```
Saída:

```
A idade é: 36
```

## Função help()

Executa o sistema de ajuda integrado.

## Função input()
Essa função permite a entrada do usuário.

### Sintaxe
`input(prompt)`


**prompt**: Uma String, representando uma mensagem padrão antes da entrada.

### Exemplo

```python
print("Digite seu nome:")
x = input()
print("Olá, " + x)
```
Saída:
```
Digite seu nome: nome digitado
Olá, nome digitado
```

## Função int()
A int()função converte o valor especificado em um número inteiro.

### Sintaxe
`int(value, base)`

**value**: Um número ou uma string que pode ser convertida em um número inteiro.
**base**: Um número que representa o formato do número. Valor padrão: 10.

### Exemplo
**Convertendo string em inteiro:**

```python
x = int("12")
print(x)

```

Saída:
```
12
```

## Função iter()
A função python iter() é usada para retornar um objeto iterador. Ele cria um objeto que pode ser iterado um elemento por vez.

### Sintaxe
`iter(object, sentinel)`

**object**: Um objeto iterável.
**sentinel**: É um valor especial que representa o final de uma sequência.

### Exemplos
No exemplo abaixo, a função iter() converte uma lista iterável em um iterador.
```python
# lista de numeros 
lista = [1,2,3,4,5]  
  
listaIter = iter(lista)  
  
# prints '1'  
print(next(listaIter))  
  
# prints '2'  
print(next(listaIter))  
  
# prints '3'  
print(next(listaIter))  
  
# prints '4'  
print(next(listaIter))  
  
# prints '5'  
print(next(listaIter))
```

Saída:
```
1
2
3
4
5
```

## Função len()
Essa função é usada para retornar o comprimento (o número de itens) de um objeto. Quando o objeto é uma string, a len() retorna o número de caracteres na string.

### Sintaxe
`len(object)`

### Exemplo

Comprimento da lista:

```python
lista = ["maça", "banana", "uva"]
x = len(lista)
print(x)
```

Saída:

```
3
```

Comprimento de uma string:

```python
lista =  'Pubnic'  
print(len(lista))  
```

Saída:

```
6
```

## Função list()
Essa função cria um objeto de lista que é uma coleção ordenada e mutável.

### Sintaxe
`list(iterable)`

**iterable**(opcional): Um objeto que pode ser uma sequência (string, tupla etc.) ou coleção (conjunto, dicionário etc.) ou objeto iterador.

### Exemplos
```python
# lista vazia 
print(list())  
  
# lista a partir de string  
String = 'python'       
print(list(String))  
  
# lista 
Lista = [1,2,3,4,5]  
print(list(Lista))  
```
Saída:

```
[]
['p', 'y', 't', 'h', 'o', 'n']
[1, 2, 3, 4, 5]
```

## Função map()
A função python map() é usada para retornar uma lista de resultados após aplicar uma determinada função a cada item de um iterable(list, tuple etc.)

### Sintaxe
`map(function, iterables)`

**function**: A função a ser executada para cada item
**iterables**: Uma sequência, coleção ou um objeto iterador. Você pode enviar quantos iteráveis quiser, apenas certifique-se de que a função tenha um parâmetro para cada iterável.

### Exemplo
```python
def Frutas(a, b):
  return a + b

x = map(Frutas, ('maça', 'banana', 'uva'), ('laranja', 'limao', 'cereja'))

print(list(x))
```
Saída:

```
<map object at 0x153b354f12b0>
['maçalaranja', 'bananalimao', 'uvacereja']
```

## Função open()

Essa função abre um arquivo e o retorna como um objeto de arquivo.

### Sintaxe
`open(file, mode)`

**file**: O caminho e o nome do arquivo.
**mode**: Uma string, define-se em qual modo você deseja abrir o arquivo, por meio de:
- "r" - Leitura - Valor padrão. Abre um arquivo para leitura, erro se o arquivo não existir.
 
- "a" - Append - Abre um arquivo para anexação, cria o arquivo se não existir.
 
- "w" - Write - Abre um arquivo para escrita, cria o arquivo caso não exista.
 
- "x" - Criar - Cria o arquivo especificado, retorna um erro se o arquivo existir.

Além disso, é possível especificar se o arquivo deve ser tratado como modo binário ou texto:
- "t" - Texto - Valor padrão. Modo de texto.
- 
- "b" - Binário - Modo binário (por exemplo, imagens).

### Exemplo

```python
# arquivo é aberto para leitura 
f = open("path_to_file", mode='r')  
# arquivo é aberto para escrita  
f = open("path_to_file", mode = 'w')  
# arquivo é aberto para gravação até o final  
f = open("path_to_file", mode = 'a')  
```

## Função pow()
Esta é utilizada para o cálculo das potências de um número. Ele retorna x elevado a y módulo z se um terceiro argumento(z) estiver presente, ou seja, (x, y) % z.

### Sintaxe
`pow(x, y, z)`

**x**: Um número, a base
**y**: Um número, o expoente
**z**(Opcional):. Um número, o módulo

### Exemplos
```python
# x positive, y positive (x**y)  
print(pow(8, 2))

# x negativo, y positivo   
print(pow(-8, 2))  
  
# x positivo, y negativo (x**-y)  
print(pow(8, -2))  
  
# x negativo, y negativo   
print(pow(-8, -2))  
```
Saída:

```
64
64
0.015625
0.015625
```

## Função print()
A print()função imprime a mensagem especificada na tela ou em outro dispositivo de saída padrão. A mensagem pode ser uma string, ou qualquer outro objeto, o objeto será convertido em uma string antes de ser escrito na tela.

### Sintaxe
`print(object(s), sep=separator, end=end, file=file, flush=flush)` 

**object(s)**: É um objeto a ser impresso. O símbolo * indica que pode haver mais de um objeto.

**sep='separator'** (opcional): Os objetos são separados por sep. O valor padrão de setembro é ' '.

**end='end'** (opcional): determina qual objeto deve ser impresso por último.

**file** (opcional): - O arquivo deve ser um objeto com o método `write(string)`. Se for omitido, será usado `sys.stdout` que imprime objetos na tela.

**flush** (opcional): Se True, o fluxo é liberado à força. O valor padrão de flush é False.

### Exemplos
```python
print("Pubnic é revolucionaria")  
  
x = 7  
# Dois objetos passados
print("x =", x)  
  
y = x  
# Três objetos passados 
print('x =', x, '= y')
```
Saída:

```
Pubnic é revolucionaria
x = 7
x = 7 = y
```

## Função range()
A função range() retorna uma sequência de números, começando em 0 por padrão e incrementa em 1 (por padrão) e para antes de um número especificado.

### Sintaxe
`range(start, stop, step)`

**start** (opcional): É um número inteiro que especifica a posição inicial. O valor padrão é 0.

**stop** (opcional): É um inteiro que especifica a posição final.

**step** (opcional): É um inteiro que especifica o incremento de um número. O valor padrão é 1.

### Exemplos
Sequência de números de 3 a 7 que imprime cada item na sequência:

```python
x = range(3, 8)

for n in x:
  print(n)
```
Saída:
```
3
4
5
6
7
```

Sequência de números de 3 a 24, mas incrementa em 3 em vez de 1:

```python
x = range(3, 25, 3)
for n in x:
  print(n)
```
Saída:

```
3
6
9
12
15
18
21
24
```

## Função round()
Essa função retorna um número de ponto flutuante que é uma versão arredondada do número especificado, com o número especificado de decimais.

### Sintaxe
`round(number, digits)`

**number** : O número que deve ser arredondado.

**digits** : É o número para o qual o número dado deve ser arredondado, e é um parâmetro opcional.

### Exemplos
```python
#  inteiros 
print(round(20))  
  
# Ponto flutuante
print(round(17.8))  

# Arredondar para duas casas decimais
x = round(5.76543, 2)
print(x)
```

Saída:

```
20
18
5.77
```
