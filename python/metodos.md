---
title: Métodos
description: 
published: true
date: 2022-09-01T13:14:25.640Z
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

 O Python faz a substituição do argumento self pelo objeto de instância, `obj`, quando o método de instancia é chamado.
 Desse forma, precisa-se adicionar um parametro padrão ao definir os métodos de instancia.
