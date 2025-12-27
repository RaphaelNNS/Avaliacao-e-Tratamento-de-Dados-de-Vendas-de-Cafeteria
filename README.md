
# Cafe Sales – Data Quality Analysis

## Descrição do projeto
Este projeto analisa a **qualidade de um dataset de vendas propositalmente sujo**, simulando um cenário real onde os dados apresentam valores ausentes, inválidos ou inconsistentes.

O foco está em **avaliar, tratar e comunicar a qualidade dos dados**, garantindo transparência sobre o impacto das estimações e sobre o nível de confiança das análises geradas.

---

## Objetivos
- Identificar problemas de qualidade nos dados
- Separar dados brutos (RAW) de dados tratados (FINAL)
- Estimar apenas campos críticos quando necessário
- Criar flags para identificar valores estimados
- Avaliar o impacto das estimações no dataset

---

## Estrutura dos dados
- **CafeSales_RAW**: dados originais, sem estimativas, mantidos para auditoria
- **CafeSales_FINAL**: dados tratados e, quando aplicável, estimados
- **StandartPrice**: tabela auxiliar para padronização de preços por item

---

## Regras de tratamento e estimação
- Apenas colunas críticas foram estimadas:
  - Quantity
  - Price Per Unit
  - Total Spent
- Valores estimados não foram utilizados para estimar outros valores
- Valores em branco, erros e “Unknown” foram tratados como nulos
- Colunas não críticas (ex: Location, Payment Method, Transaction Date) não foram estimadas

---

## Métricas de qualidade
- Total de entradas
- Percentual de linhas com valores estimados
- Percentual de linhas sem valores estimados
- Quantidade de valores estimados por coluna
- Distribuição das estimações por item

---

## Dashboards
O relatório está organizado em duas principais visões:

### 1. Qualidade dos dados (Antes do tratamento)
Apresenta a condição original do dataset, destacando:
- Volume total de entradas
- Percentual de valores críticos ausentes
- Qualidade dos dados por coluna e por item

### 2. Qualidade dos dados (Visão geral – dados críticos)
Mostra o impacto do tratamento:
- Redução de entradas inválidas
- Proporção de linhas com e sem valores estimados
- Distribuição das estimações por item e por coluna

---

## Principais aprendizados
- A qualidade dos dados influencia diretamente a confiabilidade das análises
- Estimações precisam ser controladas e claramente sinalizadas
- Transparência é essencial para decisões baseadas em dados
- Separar dados brutos e tratados facilita auditoria e interpretação

---

## Ferramentas utilizadas
- Power BI
- Power Query (M)
- DAX
