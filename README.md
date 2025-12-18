# Qualidade e Limpeza de Dados – Vendas de Cafeteria

## Objetivo
Analisar a qualidade dos dados de vendas de uma cafeteria e aplicar ajustes básicos de limpeza, com o objetivo de tornar o dataset mais organizado e adequado para análises no Power BI.

O foco do projeto é identificar problemas comuns em dados brutos (*dirty data*) e documentar, de forma simples, as decisões tomadas durante o processo de limpeza.

---

## Dataset
Dataset sintético de vendas de cafeteria, criado para simular um cenário realista de dados com problemas de qualidade.

Principais colunas:
- Item  
- Quantity  
- Price Per Unit  
- Total Spent  
- Payment Method  
- Location  
- Transaction Date  

---

## Problemas Identificados
- Presença de valores ausentes (`null`)
- Valores inválidos como `ERROR` e `UNKNOWN`
- Campos incompletos que dificultam análises diretas
- Inconsistências causadas por dados faltantes em colunas relacionadas (quantidade, preço e valor total)

---

## Análise Inicial do Dataset
Foi realizada uma análise inicial para entender a proporção de valores válidos em cada coluna antes de qualquer tratamento.

### Qualidade por Coluna (Antes da Limpeza)
- **Item:** 89% de valores válidos  
- **Quantity:** 94% de valores válidos  
- **Price Per Unit:** 93% de valores válidos  
- **Total Spent:** 95% de valores válidos  
- **Payment Method:** 68% de valores válidos  
- **Location:** 63% de valores válidos  
- **Transaction Date:** 94% de valores válidos  

As colunas `Payment Method` e `Location` apresentavam maior volume de dados ausentes ou inválidos em comparação com as colunas numéricas.

---

## Processo de Limpeza e Decisões Tomadas

Durante o tratamento dos dados, foram adotadas as seguintes decisões:

- Valores inválidos (`ERROR`, `UNKNOWN` e campos vazios) foram padronizados como `null`.
- As colunas numéricas foram convertidas para seus tipos corretos (número inteiro, número decimal e data).
- As colunas originais (`Quantity`, `Price Per Unit` e `Total Spent`) foram preservadas como colunas **raw**, garantindo rastreabilidade.
- Foram criadas colunas finais com valores estimados apenas quando havia informação suficiente para o cálculo.
- Nenhum valor foi estimado utilizando outro valor previamente estimado, evitando propagação de erro.
- Foram criadas colunas de **flag** para identificar registros cujo valor foi estimado.
- O tratamento foi realizado integralmente no Power Query, mantendo o processo transparente e reproduzível.

---

## Resultado Após a Limpeza
Após a aplicação das etapas de limpeza e estimativa:

- Mais de **99% das entradas passaram a conter valores válidos** nas principais colunas numéricas.
- O dataset tornou-se adequado para análises exploratórias e criação de relatórios no Power BI.
- Os registros estimados permanecem identificáveis através das flags, permitindo análises com ou sem esses dados.

---

## Ferramentas Utilizadas
- Power BI (Power Query)
- Git para versionamento e documentação do projeto
