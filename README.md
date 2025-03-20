
# 📈 Previsão do IBOVESPA com Séries Temporais e Random Forest

Projeto de modelagem preditiva para prever o fechamento diário do índice **IBOVESPA**, utilizando técnicas de **Séries Temporais**, **Feature Engineering** e algoritmos de **Machine Learning (Random Forest, Arimna, Prophet, XGBoost)**.

---

## 💡 Objetivo

Construir um pipeline preditivo capaz de:
- Extrair dados diários de fechamento da IBOVESTA: https://br.investing.com/indices/bovespa-historical-data
- Prever o valor de fechamento do IBOVESPA para os próximos 3 dias;
- Calcular **intervalos de confiança** para as previsões;
- Analisar desempenho comparativo com diferentes abordagens.

---

## ⚙️ Tecnologias Utilizadas

- **Python 3.10+**
- `pandas`, `numpy`, `matplotlib`,
- `scikit-learn`, `statsmodels`, `prophet`, `XGBoost`, `Random Forest` 

---

## 📊 Features Criadas

- Lags (`lag_1` a `lag_365`)
- Médias móveis:
  - Simples (`rolling_mean`)
  - Exponencial (`EMA`)
- Desvios padrão
- Fourier (sazonalidade cíclica)
- Tendência linear histórica

---

## 🔍 Metodologia

1. **Coleta dos dados históricos do IBOVESPA** via `Investing.com`;
2. **Criação de variáveis derivadas** (lags, rolling, ema, etc.);
3. **Treinamento de modelos diversos para Benchmarking**;
4. **Análise do modelo Random Forest Regressor**;
5. **Validação e previsão para múltiplos dias futuros (3 dias)**;
6. **Cálculo do intervalo de confiança com base na dispersão das árvores individuais**;
7. **Visualização de previsão, com linha de tendência, faixa de incerteza, naive (baseline)**.

---

## 📈 Exemplo de Visualização

![plot](assets/exemplo_previsao_ibov.png)

---

## 📁 Estrutura do Projeto

```
📂 previsao_ibovespa/
├── Base de Dados/                      # Arquivo .csv com dados históricos da IBOVESPA
│   └── ibov_historico.csv
├── Histórico de Pred/                 # Plotagem gráfica das predições por dia
│   └── grafico_predicoes.ipynb
├── Subcodigos/                        # Códigos auxiliares (benchmark de modelos e scraping)
│   ├── benchmarking_models.ipynb
│   └── scraping_ibov_data.ipynb
├── App. Random Forest Predct.ipynb    # Código com foco apenas no modelo Random Forest (melhor performance)
├── Machine Code.ipynb                 # Pipeline completo com todo o código de pré-processamento, modelagem e previsão
├── README.md                          # Documentação do projeto

```

---



## 🔜 Próximas Etapas

- Adição de novos modelos: **SARIMA, LSTM**
- Avaliação por métricas: **MAPE, RMSE, MAE**
- Automatização via pipeline modular
- Otimização de hiperparâmetros
- Scraping por intervalo de última data da base de dados até a data de hoje

---

## 👨‍💻 Autor

**Luis Rufino — Analista de Dados**  
📬 [LinkedIn]([https://www.linkedin.com/](https://www.linkedin.com/in/luis-henrique-rufino-2341901b2/))

---

## 📃 Licença

Este projeto está licenciado sob a **MIT License**.
