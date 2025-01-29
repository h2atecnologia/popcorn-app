# Blackbird Report

| Created/Modified | Version | Author | Email |
|:------------:|:--------------:|:-----------:|---|
| Jan, 2025 | 1.0.0  | Henrique Dias | henrique@3stamina.com |

<img src="./report.png"/>

Este tutorial tem como objetivo, transmitir conhecimento sobre o uso de MongoDB aggregate query diretamente no Blackbird Report (**Report aggregate**)

O **Report aggregate**, como chamaremos de agora em diante, é uma alternativa ao **Report convencional**, e que para que ele possa apresentar filtros através de interface para o usuário, semelhante ao do modelo convencional, requer a definição do dicionário para o mesmo, através do [**Schema**](#Schema).

As partes básicas envolvidas a serem abordatas inicialmente e brevemente neste tutorial, para se executar uma *aggregate query*, são:

- [Schema](#schema)
- [Filtro](#diltro)
- [Dicionário](#dicionário)
- [Aggregate](#aggregate)

E após esta abordagem, veremos como:

- [Criar Schema](#criar-schema)
- [Gerar Dicionário](#gerar-dicionário)
- 
> Nota 1 - **Report convencional** e **Report aggregate** não podem ser misturados e não possuem intercâmbio de design.

> Nota 2 - Este tutorial não tem como objetivos: ensinar o uso prático do **Report**, assim como ensinar **MongoDB**.

## Abordagem básica

### Schema

<img src="./schema.png"/>

**Schema** é o bloco de código javascript que permite a construção de um schema json, inferindo desta maneira, no comportamento visual e funcional dos filtros visuais em um **Report aggregate**.

A parte funcional dos filtros em si, ou seja, filtros e valores dos mesmos, são injetados no bloco [**Aggregate**](#Aggregate), através da variável $F que conterá as propriedades e valores configuradas e informadas no bloco [**Filtro**](#Filtro).

### Filtro

<img src="./filtro.png"/>

**Filtro** é o bloco visual que permite montar o filtro funcional/visual para iteração com o usuário. O mesmo carrega valores defaults para suprir o [**Aggregate**](#Aggregate).

Diferente do modelo **Report convencional**, as operações em sua maioria, não interferem na aggregate query e servem mais como uma maneira de extrair o valor informado e como informação.

### Dicionário

<img src="./dicionario.png"/>

**Dicionário** é o bloco visual montado pelo Report, a partir  do [**Schema**](#Schema) e que dá suporte ao [**Filtro**](#Filtro).

### Aggregate

<img src="./aggregate.png"/>

**Aggregate** é o bloco de código javascript que permite a construção de um pseudo-código de aggregate.

A padrão de construção deste código se assemelha ao do **Blackbird Datasource**.

## Na prática

### Criar Schema

### Gerar Dicionário
