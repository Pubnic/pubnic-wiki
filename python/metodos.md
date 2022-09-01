---
title: Métodos
description: 
published: true
date: 2022-09-01T13:39:55.638Z
tags: 
editor: markdown
dateCreated: 2022-08-31T23:50:56.422Z
---

# Métodos
Na programação orientada a objetos, tem-se os objetos que representam propriedades e comportamentos. Essas propriedades são definidas pelos atributos e o comportamento é definido ao se utilizar os métodos. Esses métodos são uma parte do código reutilizavel que pode ser chamado em qualquer ponto do programa e estão dentro de uma classe.

## Tipos de Métodos em python
Existem três tipos de métodos em python basicamente:
- Método de instancia
- Método de classe
- Método de classe

Abaixo eles serão explicados com mais detalhes.

### Métodos de instância
Métodos de instância são usados para manipular dados de um objeto específico. Eles são conhecidos como métodos de instância porque eles estão vinculados a uma instância específica de uma classe. Esses métodos podem acessar e modificar os dados de uma instância.

Eles possuem um parâmetro padrão chamado `self`, que aponta para uma instancia de classe. Esse parametro não é necessario todas as vezes. Além disso, esse nome pode ser alterado, mas o melhor é seguir a convenção e usar `self`.

Qualquer método que você cria dentro de uma classe é um método de instância, a menos que você diga ao Python o contrário.

Ex:
```python
class Minha_classe:
   def metodo_instancia(self):
     return "Este é um método de instância."
```

Deve-se criar um objeto/instancia da classe para chamar um método de instancia. Com a ajuda desse objeto é possivel acessar qualquer método de classe.

Ex:
```
obj = Minha_classe() 
obj.metodo_instancia()
```

 O Python faz a substituição do argumento self pelo objeto de instância, `obj`, quando o método de instancia é chamado. Desse forma, precisa-se adicionar um parametro padrão ao definir os métodos de instancia. Dessa forma, conforme o exemplo anterior, observa-se que ao chamar o `metodo_instancia()`, não se precisa passar o self.
 
Também pode-se adicionar outros parametros em conjunto com o self:
```python
class Minha_classe: 

  def metodo_instancia(self, a): 
    return f"Este é um método de instância com um parâmetro a = {a}."
```
No bloco de codigo abaixo será criado o objeto de classe e o metodo sera chamado, com o novo parametro `a` adicionado:

```python
obj = Minha_classe() 
obj.metodo_instancia(10)
```

Mais uma vez não foi necessario passar o `self` como arggumento, pois o python ja faz isso. No entanto, os outros argumentos devem ser passados. Assim, o 10 foi passado como valor de `a`.

O `self` pode ser usado dentro do metodo de instancia para acessar os demais atributos e metodos da mesma classe:

```python
class Minha_classe: 

  def __init__(self, a, b): 
    self.a = a 
    self.b = b 

  def instance_method(self): 
    return f"Este é o método de instância e pode acessar as variáveis a = {self.a} e\ 
 b = {self.b} com a ajuda de self."
```

> `__init__()` é um tipo especial de método conhecido como construtor. Este método é chamado quando um objeto é criado a partir da classe e permite que a classe inicialize os atributos de uma classe.
{.is-info}

 
 
