---
title: Módulo
description: 
published: true
date: 2022-10-18T14:24:01.697Z
tags: 
editor: markdown
dateCreated: 2022-09-19T23:13:06.790Z
---

# Módulo

Quando fazemos um código no interpretador python e depois saímos do interpretador, todos esses dados são perdidos, por isso, para alguns programas maiores, é interessante a utilização de arquivos de texto que guardem a entrada, o que é conhecido como criar um script. 

Um módulo é nada mais do que um arquivo python `.py` que pode conter definições e instruções de execução, também funções e classes que podem ser utilizadas. 

No python já existem diversos módulos e bibliotecas que podem ser importados para facilitar a codificação e a manipulação de dados, as bibliotecas são um conjunto de módulos disponíveis na biblioteca. Em python temos algumas bibliotecas muito conhecidas e utilizadas, sendo elas: 

- Math: Utilizada para manipulações e operações matemáticas. 
- Numpy: Processamento de grandes vetores e matrizes.
- Datetime: Utilizada para manipulação de data e hora.
- TensorFlow: Utilizada para treinamento de Inteligência Artificial.

Existem muitas outras bibliotecas a serem utilizadas em python. Para incluir módulos no desenvolvimento de códigos utilizamos do comando import. Utilizando a biblioteca math como base, podemos importá-la da seguinte forma: 

```python
import math

resultado = math.pow(4, 2)
print(resultado)
```

Podemos importar um módulo dessa da seguinte forma: 
```python
from math import sqrt

resultado = sqrt(16)
print(resultado)
```
Saída: 
> 4.0
{.is-success}

O módulo importado a cima foi o sqrt, que realiza e devolve a raiz quadrada de um número, foi possível importar com from `biblioteca` import `módulo`. Dessa forma, só importamos essa única funcionalidade, que é o calculo da raiz quadrada. Isso facilita bastante e evita a reescrita de código. 

Também é possível a criação de módulos a serem utilizados exclusivamente pelo projeto em questão, pois muitas vezes são scripts específicos e não existem bibliotecas para isso. Por exemplo, para 

