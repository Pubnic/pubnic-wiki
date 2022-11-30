---
title: Herança
description: 
published: true
date: 2022-11-30T16:01:50.048Z
tags: 
editor: markdown
dateCreated: 2022-11-30T16:01:50.048Z
---

# Herança
Herança é uma definição extremamente relacionada com programação orientada a objetos, e é um mecanismo na qual uma classe estende seus atributos e métodos para outras classes. 

Por exemplo, suponha que em um programa fosse necessária a representação de alguns veículos em classes. Existem algumas informações que estão presentes em todos os veículos, e um veículo porde ser uma motocicleta, um caminhão, um carro, etc. Essa seria uma situação em que a herança é uma boa resolução do problema, pois minimizaria reescrita de código. 

### Classe base
Para a situação citada anteriormente, seria possível a criação de uma classe pai chamada de veículo que possuiria a seguinte estrutura e atributos: 

```python
class Veiculo: 
	def __init__(self, chassi, marca, modelo, placa, ano): 
  	self.chassi = chassi
    self.marca = marca
    self.modelo = modelo
    self.placa = placa 
    self.ano = ano
```
Dessa forma, a função init seria um construtor para a classe Veiculo, ou seja, serve para criar os atributos da classe. 

### Classe filha
Para a criação de um motocicleta poderíamos adicionar características que existem somente para motos, além de herdar o estado e comportamento da classe Veiculo: 

```python 
class Motocicleta(Veiculo): 
	def __init__(self, chassi, marca, modelo, placa, ano, cilindrada):
  	super().__init__(chassi, marca, modelo, placa, ano)
    self.cilindrada = cilindrada
  	
```

O método super chama o método init da super classe, no caso, do veículo. 
