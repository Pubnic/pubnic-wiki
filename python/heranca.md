---
title: Herança
description: 
published: true
date: 2023-01-24T11:46:31.762Z
tags: 
editor: markdown
dateCreated: 2022-11-30T16:01:50.048Z
---

# Herança
Herança é uma definição extremamente relacionada com programação orientada a objetos, e é um mecanismo na qual uma classe estende seus atributos e métodos para outras classes. 

Por exemplo, suponha que em um programa fosse necessária a representação de alguns alunos e professores de uma universidade. Existem algumas informações que estão presentes em todos, que seriam informações que toda pessoa possui, e uma pessoa pode ser um funcionário, professor e aluno em uma universidade. Essa seria uma situação em que a herança é uma boa resolução do problema, pois minimizaria reescrita de código. 

### Classe mãe
Para a situação citada anteriormente, seria possível a criação de uma classe pai chamada de pessoa que possuiria a seguinte estrutura e atributos: 
> Para a representação de classes é interessante que inicie com letra maiúsula. 
{.is-info}

```python
class Pessoa: 
	def __init__(self, nome, cpf, endereco, telefone, data_nascimento): 
  	self.nome = nome
    self.cpf = cpf
    self.endereco = endereco
    self.telefone = telefone
    self.data_nascimento = data_nascimento
```
Dessa forma, a função init seria um construtor para a classe Veiculo, ou seja, serve para criar os atributos da classe. 

### Classe filha
Para a criação de um Aluno poderíamos adicionar características que existem somente para motos, além de herdar o estado e comportamento da classe Pessoa: 

```python 
class Aluno(Pessoa): 
	def __init__(self, nome, cpf, endereco, telefone, data_nascimento, matricula, periodo):
  	super().__init__(nome, cpf, endereco, telefone, data_nascimento)
    self.matricula = matricula
    self.periodo = periodo
  	
```



Já a classe Professor, poderia ter os seguintes atributos: 

```python 
class Professor(Pessoa): 
	def __init__(self, nome, cpf, endereco, telefone, data_nascimento,  formacao):
  	super().__init__(nome, cpf, endereco, telefone, data_nascimento)
    self.formacao = formacao
  	
```

> Para justificar a criação da classe filha, é necessário que pelo menos um atributo da classe a ser criada não esteja na classe base.  
> 
{.is-warning}

O método super chama o método init da super classe, no caso, da pessoa. É necessário passar a classe base como parâmetro para indicar a herança. 
Dessa forma, temos um comportamento interessante, pois o Aluno, por ser uma pessoa, vai herdar todos os comportamentos de uma pessoa, isso inclui atributos e métodos, além de possuir alguns outros comportamentos únicos, esse é um conceito extremamente importante na programação orientada a objetos. 

### Métodos
Além de herdar os atributos da classe da classe mãe, ou também chamada de superclasse, a classe filha, ou subclasse também herda todos os métodos privados da superclasse. Sendo assim, considerando que houvesse um método que calcula a idade de uma pessoa a partir de uma data de nascimento, a superclasse teria a seguinte estrutura: 


```python
from datetime import datetime

class Pessoa: 
	def __init__(self, nome, cpf, endereco, telefone, data_nascimento): 
  	self.nome = nome
    self.cpf = cpf
    self.endereco = endereco
    self.telefone = telefone
    self.data_nascimento = data_nascimento
    
  def calcula_idade(self):
  	dia, mes, ano: (self.data_nascimento).split("/")
    idade = datetime.today().year - ano
  	return idade
```

Caso fosse necessário descobrir a idade de um aluno, pela herança, esse método poderia ser facilmente acessado pela classe aluno: 
```
aluno = aluno.Aluno('João', '07893837786', 'Avenida das Mangueiras', 61992255422, '2022-10-04')
```


Para obter uma maior conhecimento sobre herança em python, é recomendado visitar os seguintes materiais: 
https://algoritmosempython.com.br/cursos/programacao-python/heranca/
