# Arthur Alves

**Data Science @ FIAP** — Machine Learning aplicado à decisão de negócio, com o pipeline inteiro: do
EDA e da engenharia de atributos até o serviço em produção, o orquestrador e o dashboard.

O que me interessa é a pergunta depois do modelo: *vale a pena agir sobre essa previsão, para
este cliente?*

---

## Projetos em destaque

### [churn-prediction-credit-card](https://github.com/artvezz/churn-prediction-credit-card) `MIT`

Sistema que **prioriza a ação de retenção por lucro esperado**, não por threshold de probabilidade.

| | |
|---|---|
| Modelo | XGBoost vs Regressão Logística, CV estratificada, desbalanceamento por `scale_pos_weight` |
| PR-AUC | **0,969** (logística: 0,77) — classe rara de 16%, então acurácia seria enganosa |
| Explicabilidade | SHAP global e **local por cliente**, com código único entre treino e serviço |
| Decisão | CLV (margem, juros, anuidade) → política `lift · p · CLV > custo` por cliente |
| Resultado | EV ≈ **$20,7k** por cliente vs **$19,0k** do melhor corte global — e "reter todo mundo" é o pior caso |
| Stack | FastAPI · Supabase · n8n · Docker · Streamlit · pytest (**67 testes**) |

Dois detalhes de engenharia que a maioria dos projetos ignora: a mesma função de features roda no
treino e no servidor (elimina *train/serve skew*), e o laudo SHAP é gravado por rodada do lote, então
nunca fica defasado do modelo que gerou o score.

### [weather-Agent](https://github.com/artvezz/weather-Agent)

Pipeline de dados end-to-end com coleta contínua e relatório automatizado:

```
OpenWeather API → Apache Airflow (Docker) → Supabase/PostgreSQL
                                        → Streamlit + Plotly  →  Flask/ngrok  →  n8n (e-mail diário)
```

### [deteccao-tumor-cerebral](https://github.com/artvezz/deteccao-tumor-cerebral)

Segmentação de glioma em ressonância magnética (**BraTS 2021**) com **U-Net 3D**: treino, avaliação,
visualização dos volumes estimados e app web local para upload de exame.

> Ferramenta de estudo e pesquisa. **Não é um dispositivo médico** e não substitui avaliação clínica.

---

## Também no repositório

| Repositório | O que é |
|---|---|
| [Analise-de-Marketing-VW](https://github.com/artvezz/Analise-de-Marketing-VW) | Marketing analytics em **BigQuery + Power BI**: CTR, CPC, CPM, ROAS, ROI, LTV e comparação de funis A/B |
| [olist-ecommerce-analytics](https://github.com/artvezz/olist-ecommerce-analytics) | Análise de vendas e customer experience do e-commerce brasileiro (SQL + Power BI) |
| [crm-sales-eda](https://github.com/artvezz/crm-sales-eda) | EDA e diagnóstico de saúde do pipeline de vendas (Jupyter) |
| [SAC-DASHBOARD-PBI](https://github.com/artvezz/SAC-DASHBOARD-PBI) | Dashboard de Customer Service Analytics (Power BI) |
| [teste_ab_projeto](https://github.com/artvezz/teste_ab_projeto) | Teste A/B de campanhas — **WIP**, a análise comparativa não está concluída |

---

## Stack

**Machine Learning** XGBoost · SHAP · scikit-learn · Statsmodels · PyTorch (U-Net 3D) · pandas · NumPy
**Engenharia** FastAPI · Flask · Apache Airflow · Docker · PostgreSQL · Supabase · n8n
**Dados e BI** SQL · BigQuery · Power BI · Tableau · Streamlit · Plotly
**Prática** pytest · Git · Linux

---

## No que estou trabalhando agora

- Análise de sobrevivência (Kaplan–Meier / Cox) para estimar **quando** o cliente sai, não só se sai.
- Calibração de probabilidades e auditoria de **fairness** por gênero, idade e renda.
- Contextualização Brasil do domínio: concorrência de bancos digitais, portabilidade, cartão sem anuidade,
  com os valores em R$.

---

## Contato

<!-- Preencha antes de publicar: troque o e-mail abaixo e adicione seu LinkedIn. -->
<!-- Email: seu-email@exemplo.com -->
<!-- LinkedIn: https://www.linkedin.com/in/seu-perfil/ -->

**LinkedIn:** [em breve](https://github.com/artvezz)
