---
title: Métodos
description: 
published: true
date: 2022-09-02T12:14:24.233Z
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

No exemplo acima, as palavras chave `self.a` e `self.b` ajudam a acessar as variáveis presentes no método `__init__()` da mesma classe.

### Métodos de classe
Métodos de classe são métodos que são chamados na própria classe, não em uma instância de objeto específica. Portanto, ele pertence a um nível de classe e todas as instâncias de classe compartilham um método de classe.

- Um método de classe está vinculado à classe e não ao objeto da classe. 
- Ele pode acessar apenas variáveis de classe e alem disso, modificar o estado da classe alterando o valor de uma variável de classe que se aplicaria a todos os objetos de classe.
- Para definir um método de classe, deve-se especificar que é um método de classe com a ajuda do decorador `@classmethod`.
- Os métodos de classe também recebem um parâmetro padrão - `cls`, que aponta para a classe. Ele não é obrigatorio, mas o melhor é seguir a convenção.

Abaixo é apresentado um exemplo de como criar um método de classe:

```python
class Minha_classe:

  @classmethod
  def metodo_classe(cls):
    return "Este é um método de classe."
```
Abaixo será criada a instância da Minha_classe() e o método de classe será chamado:
```python
obj = Minha_classe()
obj.metodo_classe()
```
Os métodos de classe podem ser acessados diretamente sem criar uma instância ou objeto da classe. Como por exemplo:
```python
Minha_class.metodo_classe()
```

Classe detalhada utilizando o metodo de classe:

![metodo_classe.png](/metodo_classe.png){.align-center}

### Métodos Estáticos
Esses métodos não conseguem acessar os dados da classe, ou seja, não precisam acessar tais dados.Eles são autosuficientes e trabalham por conta própria. Um método estático está vinculado a uma classe em vez dos objetos dessa classe. Isso significa que um método estático pode ser chamado sem um objeto para essa classe. Isso também significa que os métodos estáticos não podem modificar o estado de um objeto, pois não estão vinculados a ele.

O decorator `@staticmethod` é usado para definir um método estático. Diferente dos métodos de instância e métodos de classe, não é preciso passar nenhum parâmetro especial ou padrão.

Ex:
```python
class Minha_classe:

  @staticmethod
  def metodo_estatico():
    return "Este é um método estático."
```
Os métodos estaticos podem ser chamados usando um objeto/instância da classe:

```
obj = Minha_classe()
obj.metodo_estatico()
```

Além disso, podem ser chamados diretamente, sem criar um objeto/instância da classe:

```
Minha_classe.metodo_estatico()
```

Os métodos podem ser resumidos em tres pontos:

- Um método de instância conhece sua instância (e a partir disso, sua classe)
- Um método de classe conhece sua classe
- Um método estático não conhece sua classe ou instância
 





