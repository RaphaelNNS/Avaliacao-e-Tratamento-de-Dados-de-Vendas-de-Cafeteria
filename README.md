# Qualidade e Limpeza de Dados – Vendas de Cafeteria

## Objetivo
Analisar a qualidade dos dados de vendas de uma cafeteria e realizar ajustes básicos de limpeza, com o objetivo de deixar o dataset mais organizado e adequado para análises no Power BI.



## Dataset
Dataset sintético de vendas de cafeteria, criado para simular um cenário realista de dados com problemas de qualidade (*dirty data*).

Principais colunas:
- Item  
- Quantity  
- Price Per Unit  
- Total Spent  
- Payment Method  
- Location  
- Transaction Date  

## Problemas Identificados
- Presença de valores ausentes (`null`)
- Valores inválidos como `ERROR` e `UNKNOWN`
- Campos incompletos que precisam de tratamento antes da análise



## Ferramentas Utilizadas
- Power BI (Power Query)
- Git para versionamento do projeto

## Análise Inicial do Dataset
Foi feita uma análise inicial para entender a proporção de valores válidos em cada coluna.


### Qualidade por Coluna
- **Item:** 89% de valores válidos  
- **Quantity:** 94% de valores válidos  
- **Price Per Unit:** 93% de valores válidos  
- **Total Spent:** 95% de valores válidos  
- **Payment Method:** 68% de valores válidos  
- **Location:** 63% de valores válidos  
- **Transaction Date:** 94% de valores válidos  

As colunas `Payment Method` e `Location` apresentam mais valores ausentes ou inválidos quando comparadas às colunas numéricas.

## Decisões Iniciais de Tratamento
- Valores inválidos como `ERROR` e `UNKNOWN` foram considerados dados ausentes e substituídos por `null`.