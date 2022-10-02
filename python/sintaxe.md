---
title: Sintaxe do Python
description: 
published: true
date: 2022-10-02T01:45:13.203Z
tags: 
editor: markdown
dateCreated: 2022-10-02T01:18:52.085Z
---

# Sintaxe da linguagem 
Inicialmente o python foi desenvolvido como uma linguagem de ensino, porém, por ter facilidade de uso e sintaxe limpa, ele foi adotado por iniciantes e especialistas. A limpeza da sintaxe do Python levou alguns a chama-lo de "pseudocódigo executável". Logo abaixo serão discutidos os principais recursos da sintaxe do python.

A sintaxe se refere à estrutura da linguagem (ou seja, o que constitui um programa para ser formado corretamente).

## Espaço em branco e identação
Ao se trabalhar com outras linguagens de programação, como C/C++, C#, Java, usa-se ponto e vírgula para separar as instruçoes. Todavia, no python usa-se espaços em branco e recuo para construir a estrutura do codigo. Considerando o seguinte exemplo de codigo:

```python
# define a função main para imprimir algo
def main():
    i = 1
    max = 10
    while (i < max):
        print(i)
        i = i + 1

# Chama a função main 
main()
```

Analisando a estrutura do código, observa-se que no final de cada linha, não se vê nehum ponto e virgula para encerrar a instrução, além disso, o código usa recuo na sua formatação.

Em linguagens de programação, um bloco de código é um conjunto de instruções que devem ser tratadas como uma unidade. Em C, por exemplo, os blocos de código são indicados por chaves:

```C
// código C 
for ( int  i = 0 ;  i < 100 ;  i ++ ) 
   { 
      // chaves indicam bloco de código 
      total  +=  i ; 
   }
```

Já em python, esses blocos são indicados pela identação:

```C
for  i  in  range ( 100 ): 
		# identação indica o bloco de código 
    += i  
```

Os blocos de código identados são sempre precedidos por dois pontos da linha anterior.

A quantidade de espaço em branco usada na identação depende do usuario, uma vez wue tenha consistencia em todo o script. Nos guias de estilo, é recomendada a identação dos blocos de código em quatro espaços. 

Por fim, organizando o código dessa maneira, tem-se as seguintes vantagens:
- Primeiro, nunca se perderá o código inicial ou final de um bloco como em outras linguagens de programação, como Java ou C#.
- Em segundo lugar, o estilo de codificação é essencialmente uniforme. Caso se precise manter o código de outro desenvolvedor, esse código será igual ao seu.
- Terceiro, o código é mais legível e claro em comparação com outras linguagens de programação.

















