---
title: Herança
description: 
published: true
date: 2022-12-16T20:20:11.659Z
tags: 
editor: markdown
dateCreated: 2022-11-30T16:01:50.048Z
---

# Herança
Herança é uma definição extremamente relacionada com programação orientada a objetos, e é um mecanismo na qual uma classe estende seus atributos e métodos para outras classes. 

Por exemplo, suponha que em um programa fosse necessária a representação de alguns funcionários alunos e professores de uma universidade. Existem algumas informações que estão presentes em todos, que seriam informações que toda pessoa possui, e uma pessoa pode ser um funcionário, professor e aluno em uma universidade. Essa seria uma situação em que a herança é uma boa resolução do problema, pois minimizaria reescrita de código. 

### Classe base
Para a situação citada anteriormente, seria possível a criação de uma classe pai chamada de pessoa que possuiria a seguinte estrutura e atributos: 
> Para a representação de classes é interessante que inicie com letra maiúsula. 
{.is-info}

```python
class Pessoa: 
	def __init__(self, nome, cpf, endereco, telefone): 
  	self.nome = nome
    self.cpf = cpf
    self.endereco = endereco
    self.telefone = telefone
```
Dessa forma, a função init seria um construtor para a classe Veiculo, ou seja, serve para criar os atributos da classe. 

### Classe filha
Para a criação de um Aluno poderíamos adicionar características que existem somente para motos, além de herdar o estado e comportamento da classe Pessoa: 

```python 
class Motocicleta(Veiculo): 
	def __init__(self, nome, cpf, endereco, telefone, matricula, periodo):
  	super().__init__(nome, cpf, endereco, telefone)
    self.matricula = matricula
   	self.periodo = periodo
  	
```
Para justificar a criação da classe filha, é necessário que pelo menos um atributo da classe a ser criada difere da classe herdada
O método super chama o método init da super classe, no caso, da pessoa. É necessário passar a classe base como parâmetro para indicar a herança. 
Dessa forma, temos um comportamento interessante, pois o Aluno, por ser uma pessoa, vai herdar todos os comportamentos de um veículo e ter alguns outros comportamentos únicos, esse é um conceito extremamente importante na programação orientada a objetos. 


