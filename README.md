# ANALISE_CAFETERIA

# ☕ Análise de Vendas - Cafeteria CoffeeTime

![Capa do Projeto](images/dashboard_cafeteria.png)

> 🔍 *Análise completa das vendas de uma cafeteria — da limpeza em Python à visualização em Power BI.*

---

## 📍 Contexto do Problema

A **Cafeteria CoffeeTime**, localizada em uma região movimentada da cidade, percebeu variações nas vendas e quer compreender melhor o comportamento de seus clientes.  
O objetivo é **descobrir os horários de maior movimento**, **identificar os produtos mais vendidos** e **avaliar a rentabilidade média por cliente (ticket médio)**.  

Essas análises ajudarão na **tomada de decisões estratégicas**, como ajustar o horário de funcionamento, reforçar o estoque em períodos de alta demanda e definir promoções.

---

## 🎯 Perguntas de Negócio

| # | Pergunta | Objetivo |
|:-:|-----------|-----------|
| 1 | Quais são as bebidas mais vendidas? | Identificar os produtos de maior saída |
| 2 | Quais são os horários de pico das vendas? | Auxiliar no planejamento da equipe |
| 3 | Como variam as vendas entre manhã, tarde e noite? | Entender o comportamento dos clientes |
| 4 | Quais dias e meses apresentam mais vendas? | Planejar promoções e estoque |
| 5 | Quais são os métodos de pagamento mais utilizados? | Entender preferências e experiência de compra |
| 6 | Qual é o ticket médio por cliente? | Avaliar a rentabilidade das vendas |

---

## ⚙️ Pipeline do Projeto

```mermaid
graph LR
A[📥 Coleta de Dados - Dataset Coffee Sales] --> B[🐍 Limpeza e Manipulação (Python)]
B --> C[📊 Visualização e KPIs (Power BI)]
C --> D[📈 Geração de Insights e Recomendações]
````

## 🧹 Etapa 1 — Limpeza e Manipulação de Dados (Python)


Importação do dataset em formato .csv

Padronização dos nomes das colunas

Tratamento de valores nulos e duplicados

Conversão de datas e horários

Criação de colunas derivadas:

month → Mês da venda

weekday → Dia da semana

hour → Hora da venda

period → Período do dia (manhã, tarde, noite)

Cálculo do ticket médio

---

📊 Etapa 2 — Visualização e Análise (Power BI)

A etapa de visualização foi realizada no Power BI, conectando diretamente o dataset limpo do Python.
Os gráficos e KPIs foram organizados em um dashboard interativo com filtros por ano ,mes e produto
