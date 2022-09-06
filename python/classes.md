---
title: Classes em Python
description: 
published: true
date: 2022-09-06T11:02:48.068Z
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

