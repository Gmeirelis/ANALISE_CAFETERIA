# ANALISE_CAFETERIA

# ☕ Análise de Vendas - Cafeteria CoffeeTime

![Capa do Projeto](graficos/dashboard.png)

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
````
 df = pd.read_csv('Coffe_sales 1.csv')
  ````
renomeando  nomes das colunas
````
df_limpo = df_limpo.rename(columns={
    'hour_of_day': 'Hora do Dia',
    'cash_type': 'Tipo de Pagamento',
    'money':'valor',
    'coffee_name':'nome do produto',
    'Time_of_Day':'turno',
    'Weekday':'nome do dia',
    'Month_name':'nome do mes',
    'Weekdaysort':'numero do dia',
    'Monthsort':'numero do mes',
    'Date':'data',
    'Time':'horas',
    'id':'id'
})

df_limpo.head()
````

Tratamento de valores nulos e duplicados
````
df_limpo = df.dropna()
df_limpo = df.drop_duplicates()
````
renomeando linhas  da coluna 
         
````         
         turno    
df_limpo['turno'] = df_limpo['turno'].replace({
    'Morning': 'Manhã',
    'Afternoon': 'Tarde',
    'Night': 'Noite'
})

       nome do dia

      df_limpo['nome do dia'] = df_limpo['nome do dia'].replace({
    'Mon': 'seg',
    'Tue': 'ter',
    'Wed': 'qua',
    'Thu': 'qui',
    'Fri': 'sex',
    'Sat': 'sab',
    'Sun': 'dom'
})
        nome do mes
df_limpo['nome do mes'] = df_limpo['nome do mes'].replace({
    'Jan': 'jan',
    'Feb': 'fev',
    'Mar': 'mar',
    'Apr': 'abr',
    'May': 'mai',
    'Jun': 'jun',
    'Jul': 'jul',
    'Aug': 'ago',
    'Sep': 'set',
    'Oct': 'out',
    'Nov': 'nov',
    'Dec': 'dez'
})



# traduzindo linhas para pt br
df_limpo['nome do mes'] = df_limpo['nome do mes'].replace({
    'Jan': 'jan',
    'Feb': 'fev',
    'Mar': 'mar',
    'Apr': 'abr',
    'May': 'mai',
    'Jun': 'jun',
    'Jul': 'jul',
    'Aug': 'ago',
    'Sep': 'set',
    'Oct': 'out',
    'Nov': 'nov',
    'Dec': 'dez'
})
````

---

##📊 Etapa 2 — Visualização e Análise (Power BI)
---
A etapa de visualização foi realizada no Power BI, conectando diretamente o dataset limpo do Python.
Os gráficos e KPIs foram organizados em um dashboard interativo com filtros por ano ,mes e produto

---

##🥇 Vendas por Tipo de Café

  americano e Latte lideram as vendas
➡️ Reforçar o estoque desses produtos e oferecer combos promocionais.



 ![graficos](graficos/bebidas_mais_vendidas.png)




---

##⏰ Vendas por Hora do Dia

Os horários de maior movimento são 9h–10h (café da manhã) e 18h-20h (noite).
➡️ Reforçar a equipe e preparar o estoque nesses períodos.


![graficos](graficos/vendas_por_horario.png)

---

##🌅 Vendas por Período do Dia

As vendas estão equilibradas entre os turnos da manhã, tarde e noite, permitindo uma operação uniforme e planejamento de estoque eficiente. Recomenda-se manter a estratégia atual de atendimento e promoções distribuídas ao longo do dia.

![graficos](graficos/vendas_por_turno.png)

---

##📆 Vendas por Dia da Semana

dias movimentados são seg,sex e ter 
➡️ Reforçar equipe e operação nesses dias,aumentar a escala de funcionários ou reforçar o atendimento nesses dias ajuda a evitar gargalos.


![graficos](graficos/vendas_por_dia.png)

---

##💰 Ticket Médio

O ticket médio de R$ 2.920,00 indica clientes com maior poder de compra. Recomenda-se estratégias de upsell, combos premium e campanhas de fidelização para maximizar a margem e manter o faturamento estável

![graficos](graficos/tickt_medio.png)

---

##🧠 Conclusões e Recomendações

|#| tema | recomendação |
|:-:|-----------|-----------|
| 1 | Atendimento |Reforçar equipe nos horários de pico (8h–10h / 16h–18h)|
| 2 | Marketing | Criar promoções noturnas e combos para aumentar fluxo |
| 3 |Estoque | Ajustar pedidos conforme os dias e horários de maior movimento |
| 4 | Gestão Financeira |Monitorar mensalmente o ticket médio e volume de vendas |

---

##📈 KPIs do Projeto
--

| # | Indicador|	Valor | 	Insight
|:-:|-----------|-----------|------------|
| 1 | faturamento |R$ 10,35 mi | faturamento 2024 e 2025 |
| 2 | Ticket Médio |R$ 2.920,00|Gasto médio por cliente|
| 3 | Produto Mais Vendido | latte |Alta margem e popularidade|
| 4 | Horário de Pico |9h–10h / 18h–20h|Alta demanda matinal e vespertina|
| 5 |Dia Mais Lucrativo |Segunda|Maior movimento e faturamento|

##🧰 Ferramentas Utilizadas
--

|#|Etapa|	Ferramenta|	Finalidade|
|:-:|-----------|-----------|------------|
|1|Coleta de Dados	Kaggle| (Coffee Shop Sales Dataset)|	Fonte do dataset|
|2|Limpeza e Manipulação|	Python (Pandas)|	Tratamento e enriquecimento dos dados|
|3|Visualização|	Power BI|	Criação de dashboards e KPIs|

## 👨‍💻 Autor
---

**Guilherme Meireles**  

📧 [gmeirelis8@gmail.com]  
🔗 [www.linkedin.com/in/guimeireleslima]  


