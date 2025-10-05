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

##📊 Etapa 2 — Visualização e Análise (Power BI)

A etapa de visualização foi realizada no Power BI, conectando diretamente o dataset limpo do Python.
Os gráficos e KPIs foram organizados em um dashboard interativo com filtros por ano ,mes e produto
---

##🥇 Vendas por Tipo de Café

Cappuccino e Latte lideram as vendas, representando 38% do faturamento total.
➡️ Reforçar o estoque desses produtos e oferecer combos promocionais.
---

##⏰ Vendas por Hora do Dia

Os horários de maior movimento são 8h–10h (café da manhã) e 16h–18h (fim da tarde).
➡️ Reforçar a equipe e preparar o estoque nesses períodos.
---

##🌅 Vendas por Período do Dia
---

##📆 Vendas por Dia da Semana
---

##💰 Ticket Médio

R$ 19,80 por cliente, subindo para R$ 22,00 nos finais de semana.
➡️ Clientes gastam mais em momentos de lazer, reforçando o potencial de vendas sazonais.
---

##🧠 Conclusões e Recomendações

|#| tema | recomendação |
|:-:|-----------|-----------|
| 1 | Atendimento |Reforçar equipe nos horários de pico (8h–10h / 16h–18h)|
| 2 | Marketing | Criar promoções noturnas e combos para aumentar fluxo |
| 3 |Estoque | Ajustar pedidos conforme os dias e horários de maior movimento |
| 4 | Gestão Financeira |Monitorar mensalmente o ticket médio e volume de vendas |
---

| # | Indicador|	Valor | 	Insight
|:-:|-----------|-----------|
| 1 | Receita Total |R$ 48.500| Volume total do período analisado|
| 2 | Ticket Médio |R$ 19,80|Gasto médio por cliente|
| 3 | Produto Mais Vendido | Cappuccino |Alta margem e popularidade|
| 4 | Horário de Pico |8h–10h / 16h–18h|Alta demanda matinal e vespertina|
| 5 |Dia Mais Lucrativo |Sábado|Maior movimento e faturamento|
| 6 | Qual é o ticket médio por cliente? | Avaliar a rentabilidade das vendas |


