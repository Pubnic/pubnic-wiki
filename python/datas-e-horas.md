---
title: Manipulando Datas e Horários
description: 
published: true
date: 2022-06-03T19:54:25.255Z
tags: 
editor: markdown
dateCreated: 2022-05-29T18:18:32.105Z
---

# Manipulando Datas e Horários
Na programação o uso de datas e horários é um grande desafio, uma vez que se precisa lidar com os diferentes formatos de data escrita, horário de verão e fusos horários. Tornando-se uma tarefa complicada acompanhar os dias e horários referenciados.

### Datas Padrão

Os computadores contam o tempo através do número de segundos, conhecido como tempo Unix. Todavia, é altamente ineficiente determinar o tempo calculando o número de segundos a partir de uma data arbitrária. Em vez disso, trabalha-se com anos, meses, dias e etc. Apesar disso, outro problema ao manipular datas decorre do fato de que distintos idiomas e culturas tem distintas maneiras de escrever datas e horários.
Dessa forma, para impedir os erros de comunicação entre culturas, a International Organization for Standardization (ISO) desenvolveu a ISO 8601. Esse padrão especifica que todas as datas devem ser escritas do valor mais significativo para o menos significativo. Assim o formato é ano, mês, dia, hora, minuto e segundo:

~~~python
YYYY-MM-DD HH:MM:SS
~~~

No bloco acima, `YYYY` representa o ano que contém quatro dígitos, `MM` e `DD` são mês e dia respectivamente, ambos com dois dígitos. Em seguida, `HH`, `MM` e `SS` representam horas, minutos e segundos, com dois dígitos.

## Módulos Python

Utilizar as datas e horas na programação pode se mostrar uma tarefa complicada, no entanto não é necessário implementar os recurso do zero, já que existem muitas bibliotecas disponiveis hoje em dia. No python, existem módulos separados na biblioteca padrão para se trabalhar com as datas e horários.

## Módulo Datetime

Na linguagem python, usa-se o módulo `datetime` para tornar mais simples o armazenamneto e representação das datas e horas. Esse módulos possui as seguintes classes:

- `datetime.date` - utilizada na representação de datas simples, sem informação de fuso horário, apenas ano, mês e dia.
- `datetime.time` - representa um tempo idealizado, no qual existem 86.400 segundos por dia sem segundos bissextos. Este objeto segue o formato hora, minuto, segundo, microssegundos e tzinfo(informações de fuso horário).
- `datetime.datetime` - combina as classes `date` e `time` em apenas um objeto. Essa classe possui o mesmo nome do módulo datetime.
- `datetime.timedelta` - classe usada em cálculos, para apresentar a diferença em dias entre dois objetos `date`, `datetime` ou `time`, possuindo uma precisão de microssegundos.
- `datetime.tzinfo` - Uma classe base abstrata para objetos de informação de fuso horário. Eles são usados pelas classes `datetime` e `time` para fornecer uma noção personalizável de ajuste de horário.
- `datetime.timezone` - Uma classe que implementa o `datetime.tzinfo` como um deslocamento fixo do UTC *(Coordinated Universal Time)*.

> UTC significa Tempo Universal Coordenado e refere-se ao tempo a uma longitude de 0°. UTC é muitas vezes também chamado de *Greenwich Mean Time* , ou GMT. O UTC não é ajustado para o horário de verão, portanto mantém consistentemente vinte e quatro horas todos os dias.


## Date
Date é um objeto que manipula as datas no python. Ele se refere a dias, meses e anos.

```python
from datetime import date

#uma data específica
objeto_data = date(day=7, month=7, year=2007)
print(objeto_data)

#data de hoje
hoje = date.today()
print(hoje)
```

Ao executar o programa a saída será:

```
2007-07-07
datetime.date(2022, 5, 31)
```
No exemplo acima, `date()` é um construtor da classe `date `. O construtor recebe três argumentos: ano, mês e dia. A variável objeto_data é um objeto de `date`. Além disso, a classe `date`, só pode ser importada do módulo `datetime`. Para criar um objeto date contendo a data atual, usa-se um método de classe chamado `today()` como apresentado acima.

Também é possível verificar individualmente os atributos de data, mês e ano:

```python
from datetime import date
hoje = date.today()

print(hoje.day)
print(hoje.month)
print(hoje.year)
```

### Aritmética das Datas
As datas são comparadas entre si, procurando saber qual data é maior, menor, igual ou diferente.

```python
from datetime import date
data_sete = date(day=7, month=7, year=2007)
hoje = date.today()

hoje > data_sete #True
hoje >= data_sete #True
hoje < data_sete #False
hoje <= data_sete #False
hoje == data_sete #False
hoje != data_sete #True
```

No bloco acima, duas datas são comparadas utilizando os operadores, de modo que para uma data ser maior que outra, ela deve está no futuro, por exemplo, 2022 está depois que 2020, logo ele é maior. 

> passado < presente < futuro

## Time

O objeto `time`, instanciado da classe `time` representa a hora local.

```python

from datetime import time

# time(hora = 0, minuto = 0, segundo = 0)
a = time()
print("a =", a)

# time(hora, minuto e segundo)
b = time(9, 15, 20)
print("b =", b)

# time(hora, minuto e segundo)
c = time(hour = 9, minute = 15, second = 20)
print("c =", c)

# time(hora, minuto, segundo e microsegundo)
d = time(9, 15, 20, 254577)
print("d =", d)
```

Saída após a execução:

```
a = 00:00:00
b = 09:15:20
c = 09:15:20
d = 09:15:20.254577
```

No bloco de código acima, foram apresentadas diferentes maneiras de usar horas, minutos e segundos.

### Formatação

| Caractere  | O que significa  | Exemplo  |
| :------------: | :------------: | :------------: |
|  %H | Hora  |  00 - 23 |
| %I  | Hora do relógio de ponteiro  |  00-12 |
| %p  | DEquivalente de localidade  | AM/PM  |
| %M | Minutos| 00-59|
| %S |  Segundos|  00-59|   
|  %f|  Microssegundos | 000000 - 999999 |


## Timedelta

O objeto timedelta representa uma duração, é usado para manipular datas usando o tempo/espaço.

```python
from datetime import date, timedelta
hoje = date.today()
 
ontem = hoje - timedelta(days=1)
print(ontem)
 
amanha = hoje + timedelta(days=1)
print(amanha)
 
semana_que_vem = hoje + timedelta(days=7)
print(semana_que_vem)
 
semana_passada = hoje - timedelta(weeks=1)
print(semana_passada)
```
Saída:

```
2022-06-02
2022-06-04
2022-06-10
2022-05-27
```
Argumentos que podem ser passados no timedelta: timedelta(days=0, seconds=0, microseconds=0, milliseconds=0, minutes=0, hours=0, weeks=0). Não existem meses ou anos como argumentos, devido a existencia dos anos bissextos e meses com mais ou menos de 30 dias.

Além disso, apenas dias, segundos e microssegundos são armazenados internamente. Os argumentos são convertidos para essas unidades:

- Um milissegundo é convertido em 1000 microssegundos.
- Um minuto é convertido em 60 segundos.
- Uma hora é convertida em 3600 segundos.
- Uma semana é convertida para 7 dias.

Os dias, segundos e microssegundos são normalizados para que a representação seja única, com:

- 0 <= microsegundos < 1000000
- 0 <= seconds < 3600*24 (o número de segundos em um dia)
- -999999999 <= dias <= 999999999

### Diferença entre dois objetos timedelta

No bloco de código abaixo é apresentada a diferença entre dois objetos timedelta `t1` e `t2`.

```python
from datetime import timedelta

t1 = timedelta(weeks = 3, days = 6, hours = 9, seconds = 33)
t2 = timedelta(days = 5, hours = 13, minutes = 3, seconds = 54)
t3 = t1 - t2

print("t3 =", t3)
```

Saída:

```
t3 = 21 days, 19:56:39
```
## Conversões para Strings
Para converter datas para strings, seja para enviar para internet, salvar em um arquivo e etc, existe a seguinte tabela:

| Caractere  | O que significa  | Exemplo  |
| :------------: | :------------: | :------------: |
|  %d | Dia  |  01 |
| %a  | Dia da semana abreviado  |  Seg |
| %A  | Dia da semana completo  | Segunda  |
|  %m | Mês  |  01 |
| %b  | Mês abreviado  |  Jan |
| %B  |  Mês completo |  Janeiro |
|  %Y |  Ano  |  2022 |

Na conversão de strings em `datetime` com o python, utiliza-se o método `datetime.strptime(string, formato)`, no qual cria um objeto do tipo datetime ao se passar uma string como parâmetro, que é interpretada de acordo com o formato especificado. O método `datetime.fromisoformat(string)`
é usado em casos onde a string está no formato ISO 8601. Os métodos `date()` e `time()` são inseridos após o método `datetime.strptime(string, formato) `para se que seja retornado o tipo desejado sendo ele date ou time.

```python
from datetime import datetime

data = datetime.strptime('02/12/2022 20:00', '%d/%m/%Y %H:%M')
print(data)

data = datetime.fromisoformat('2022-12-02T20:00')
print(data)

data_normal = datetime.strptime('21-12-2022', '%d-%m-%Y').date()
print(data_normal)

hora_normal = datetime.strptime('10:33:50', '%H:%M:%S').time()
print(hora_normal)
```
Saída:

```
2022-12-02 20:00:00
2022-12-02 20:00:00
2022-12-21
10:33:50
```

> Existe o método strftime(), que é diferente do strptime(). O primeiro significa *string format time*, ou seja, formatar a string a partir de um objeto `datetime`, já o segundo é  *string parse time*, que seria avaliar uma string que deve ser convertida em um objeto *datetime*.

```python
from datetime import datetime

# data e hora atuais
now = datetime.now()

t = now.strftime("%H:%M:%S")
print("hora:", t)

d1 = now.strftime("%m/%d/%Y, %H:%M:%S")
# mm/dd/YY H:M:S formato
print("d1:", d1)

d2 = now.strftime("%d/%m/%Y, %H:%M:%S")
# dd/mm/YY H:M:S formato
print("d2:", d2)
```

Saída:

```
hora: 18:49:03
d1: 06/02/2022, 18:49:03
d2: 02/06/2022, 18:49:03
```

> Para saber mais sobre `strftime()`e formatar códigos, visite: [Comportamento de strftime() e strptime()](https://docs.python.org/pt-br/3.6/library/datetime.html#strftime-and-strptime-behavior).
{.is-info}


## Timezone

A classe timezone é uma subclasse de tzinfo, cada instância da qual representa um fuso horário definido por um deslocamento fixo do UTC (tempo universal coordenado). Ajuda a obter o fuso horário de um local específico.
Ao se falar sobre horários uma derivação importante é que eles podem ser Ingênuos e conscientes. 

- Ingênuo é um horário qualquer, que não carrega informações sobre `timezone`.
- Consciente é um horário que contém o timezone.

> O brasil conta com quatro fusos: Fernando de Noronha: UTC-2,
Brasília: UTC-3, Amazonas: UTC-4, Acre: UTC-5
{.is-info}

O timezone se refere basicamente a esta em alguma zona do tempo do UTC. Dessa forma, fala-se que se está em determinado timezone.

```python
from datetime import time, timedelta, timezone

tz_fnt = timezone(timedelta(hours=-2))
tz_brt = timezone(timedelta(hours=-3))
tz_amt = timezone (timedelta(hours=-4))
tz_act = timezone (timedelta(hours=-5))

horario_exemplo = time(22, 0, tzinfo=tz_fnt)
print(horario_exemplo)
```
Saída:

```
22:00:00-02:00
```
O bloco de código acima exemplifica o uso do timezone, nele o timezone recebe um timedelta com a diferença de onde determinada coisa está do UTC. Desse modo, o timezone é um delta negativo ou positivo dependendo do tempo onde se quer representar. Em Fernando de Noronha a variação no tempo é -2, então em `tz_fnt` o timezone é um tempo delta que por padrão é UTC, ou seja, o tempo zero menos dois e assim por diante nos demais fusos.

### Campos adicionais de strftime

| Caractere  | O que significa  | Exemplo  |
| :------------: | :------------: | :------------: |
|  %z | Diferença do UTC  |  -0300 |
| %Z  | Nome do fuso  |  Atributo do fuso |

```python
from datetime import time, timedelta, timezone

tz_fnt = timezone(timedelta(hours=-2))


tempo = time(22, 0, tzinfo=tz_fnt)
tempo_formatado = tempo.strftime('%I:%M:%S %p - UTC:%z - %Z')
print(tempo_formatado)
```
Saída:

```
10:00:00 PM - UTC:-0200 - UTC-02:00
```

 
## Juntando tudo

### datetime

A `dateclass` é uma casse do módulo `datetime` que contém informações dos objetos `date` e `time`.

```python
from datetime import datetime, timedelta, timezone

horario = datetime(
    year=2022,
    month=5,
    day=23,
    hour=22,
    minute=0,
    second=0,
    tzinfo=timezone(timedelta(hours=-3))
    )

print(horario)
```
Saída:

```
2022-05-23 22:00:00-03:00
```

## Informações Adicionais

### dateparser

A dateparser é uma biblioteca externa que ajuda a transformar os valores (parsear) sem que precise escrever os formatadores.

```python
from dateparser import parse

parse('1/1/2022') # datetime(2022, 1, 1, 0, 0)

parse('1 de maio de 2022') # datetime(2022, 5, 1, 0, 0)

parse('1 de maio de 2022 23:38') # datetime(2022, 5, 1, 23, 38)

parse('1 minuto atrás') # datetime(2022, 6, 3, 15, 11, 10, 402234) - retorna a data de um minuto atrás
```

### Pendulum

Pendulum é uma biblioteca de datetime externa para casos onde o datetime nativo não atende todas as expectativas.

- Casos complexos de parse
- Por padrão os tipos já vem com timezone
- timezones descritivos
- Tem operações complexas
- Formatadores mais simples

```python

#pip install pendulum

pendulum.now() 
# DateTime(2022, 6, 3, 15, 21, 0, 755780, tzinfo=Timezone('America/Sao_Paulo'))

pendulum.today()
# DateTime(2022, 6, 3, 0, 0, 0, tzinfo=Timezone('America/Sao_Paulo'))

pendulum.yesterday()
# DateTime(2022, 6, 2, 0, 0, 0, tzinfo=Timezone('America/Sao_Paulo'))

```





























