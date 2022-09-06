---
title: Classes em Python
description: 
published: true
date: 2022-09-06T12:28:37.731Z
tags: 
editor: markdown
dateCreated: 2022-09-06T01:13:34.602Z
---

# Classes
Python é uma linguagem de programação orientada a objetos. Diferente da programação orientada a procedimentos, onde a ênfase principal está nas funções, a programação orientada a objetos enfatiza os objetos.

Uma classe Python é como um esboço para criar um novo objeto. Um objeto é qualquer coisa que se deseja manipular ou alterar ao trabalhar no código. Sempre que um objeto de classe é instanciado, que é quando uma variavel é declarada, um novo objeto é iniciado do zero. Objetos de classe podem ser usados repetidamente sempre que necessário.

## Definindo uma classe em Python
De modo similar as funções que começam com a palavra-chave `def` em python, as classes começam com `class`.

Abaixo é mostrada uma definiçao simples de classe:
```python
class MinhaClasse:
    '''Esta é uma docstring. Criei uma nova classe'''
    pass
```
A primeira string dentro da classe chama-se docstring e tem uma breve descrição sobre o conteúdo da classe. Embora não seja obrigatório, isso é altamente recomendado.

Ao se definir uma classe, um objeto de classe é criado com o mesmo nome. Ele permite que diferentes atributos sejam acessados, assim como instanciar novos objetos de classe.

### Sintaxe de definição de classe
```
Sintaxe de definição de classe:

class ClassName:
    # Declaração
    
Sintaxe de definição de objeto: 
obj = ClassName()
print(obj.atrr)
```

Pontos importantes:
- As classes são criadas por classe de palavra-chave.
- Atributos são as variáveis que pertencem a uma classe.
- Os atributos são sempre públicos e podem ser acessados usando o operador ponto (.). Ex.: `Minhaclasse.Meuatributo`

## Objeto de Classe
Um objeto consiste em: 

- `Estado`: É representado pelos atributos de um objeto. Também reflete as propriedades de um objeto.
- `Comportamento`: É representado pelos métodos de um objeto. Também reflete a resposta de um objeto a outros objetos.
- `Identidade`: Dá um nome exclusivo a um objeto e permite que um objeto interaja com outros objetos.

O objeto de classe pode ser usado para acessar diferentes atributos. Também pode ser usado para criar novas instâncias de objetos (instanciação) dessa classe. O procedimento para criar um objeto é semelhante a uma chamada de função. Para uma classe pessoa, por exemplo:
Ex:
```python
class Pessoa:
    "Esta é uma classe de pessoa"
    idade = 10

    def saudacao(self):
        print('Olá')
```
A chamada seria:

```
Maria = Pessoa()
```

No bloco acima, é criada uma nova instancia de objeto chamada `Maria`. Os atributos do objeto podem ser acessados usando o prefixo do nome do objeto. Os atributos podem ser dados ou métodos. Os métodos de um objeto são funções correspondentes dessa classe.
Ou seja, como `Pessoa.saudacao` é um objeto de função (atributo de classe), `Pessoa.saudacao` será um objeto de método.

##  Self
No exemplo anterior, existe o parametro `self` na definição da função dentro da classe, todavia o método é chamado como se Maria.saudacao() não tivesse nehum argumento. Isso acontece porque, toda vez que um objeto chama seu método, o pŕoprio objeto é passado como primeiro argumento. Logo, Maria.saudacao() se traduz em `Pessoa.saudacao(Maria)`.

Pontos importantes:
- Os métodos de classe devem ter um primeiro parâmetro extra na definição do método. Não é dado um valor para este parâmetro quando se chama o método, o Python o fornece.
- Se existir um método que não aceita argumentos, ainda precisará ter um argumento.

## Construtores em Python
As funções que iniciam com um sublinhado duplo `__` são chamadas de funções especiais, pois elas tem um significado especial. Elas também são chamadas de construtores em Programação Orientada a Objetos (OOP). Normalmente são utilizadas para inicializar todas as variáveis.

Assim como os métodos, um construtor também contém uma coleção de instruções que são executadas no momento da criação do objeto. Ele é executado assim que um objeto de uma classe é instanciado. O método é útil para fazer qualquer inicialização que se queira fazer com o objeto.

Ex:
```python
# Uma classe de exemplo com o método init
class Pessoa:
 
    # método init ou construtor
    def __init__(self, nome):
        self.nome = nome
 
    # Método simples
    def diga_oi(self):
        print('Olá meu nome é', self.nome)
 
 
p = Pessoa('Maria')
p.diga_oi()
```

Saída:
```
Olá meu nome é Maria
```
No exemplo acima, definiu-se uma nova classe para representar uma Pessoa. Eles tem duas funções, `__init__()` para inicializar as variáveis e  diga_oi() um método simples para mostrar a saudação.

## Variáveis de classe e instância
As variáveis de instância são para dados, exclusivas para cada instância e as variáveis de classe são para atributos e métodos compartilhados por todas as instâncias da classe. Variáveis de instância são variáveis cujo valor é atribuído dentro de um construtor ou método com self, enquanto variáveis de classe são variáveis cujo valor é atribuído na classe. No exemplo abaixo são apresentadas variaveis de instancia usando um construtor:

```python
# Programa Python3 para mostrar que as variáveis com um valor
# atribuído na declaração de classe, são variáveis de classe e
# variáveis dentro de métodos e construtores são instâncias
#variáveis.
 
# Classe for cachorro
 
 
class Cachorro:
 
    # Variável de classe
    animal = 'cachorro'
 
    # O método init ou construtor
    def __init__(self, raca, cor):
 
        # Instance Variable
        self.raca = raca
        self.cor = cor
 
 
# Objetos da classe Cachorro
Rodger = Cachorro("Pug", "marrom")
Buzo = Cachorro("Bulldog", "preto")
 
print('Rodger detalhes:')
print('Rodger é um', Rodger.animal)
print('Raça: ', Rodger.raca)
print('Cor: ', Rodger.cor)
 
print('\nBuzo detalhes:')
print('Buzo é um', Buzo.animal)
print('Raça: ', Buzo.raca)
print('Cor: ', Buzo.cor)
 
# Variáveis de classe podem ser acessadas usando 
# nome da classe também
print("\nAcessando a variável de classe usando o nome da classe")
print(Cachorro.animal)
```

Saída:
```
Rodger detalhes:
Rodger é um cachorro
Raça:  Pug
Cor:  marrom

Buzo detalhes:
Buzo é um cachorro
Raça:  Bulldog
Cor:  preto

Acessando a variável de classe usando o nome da classe
cachorro
```
