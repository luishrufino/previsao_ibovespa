# 📈 Previsão do IBOVESPA com Séries Temporais e Random Forest

Projeto de modelagem preditiva para prever o fechamento diário do índice **IBOVESPA**, utilizando técnicas de **Séries Temporais**, **Feature Engineering** e algoritmos de **Machine Learning (Random Forest, ARIMA, Prophet, XGBoost)**.

---

## 💡 Objetivo

Construir um pipeline preditivo capaz de:
- Extrair dados diários de fechamento da IBOVESPA: https://br.investing.com/indices/bovespa-historical-data
- Prever o valor de fechamento do IBOVESPA para os próximos 3 dias;
- Calcular **intervalos de confiança** para as previsões;
- Analisar desempenho comparativo com diferentes abordagens.

---

## ⚙️ Tecnologias Utilizadas 
          
- **Python 3.10+**
- **Análise de Dados:** `pandas`, `numpy`, `matplotlib`, `datetime` 
- **Machine Learning:** `scikit-learn`, `statsmodels`, `prophet`, `xgboost`
- **Web Scraping:** `BeautifulSoup`, `request`

---

## 📊 Features Criadas

- Lags (`lag_1` a `lag_365`)
- Médias móveis:
  - Simples (`rolling_mean`)
  - Exponencial (`EMA`)
- Desvios padrão
- Tendência linear histórica
- Calendário:
  - `.day` 
  - `.weekofyear`
  - `.month`
  - `.year`


---

## 🔍 Metodologia

1. **Coleta dos dados históricos do IBOVESPA** via `Investing.com`;
2. **Criação de variáveis derivadas** (lags, rolling, ema, etc.);
3. **Treinamento de modelos diversos para benchmarking**;
4. **Análise do modelo Random Forest Regressor**;
5. **Validação e previsão para múltiplos dias futuros (3 dias)**;
6. **Cálculo do intervalo de confiança com base na dispersão das árvores individuais**;
7. **Visualização da previsão, com linha de tendência, faixa de incerteza e naive (baseline)**.

---

## 🏁 Benchmarking

![plot](Benchmarking.png)

---


## 📈 Exemplo de Visualização

![plot](Historico%20de%20Pred/2025-03-20.%20-0.84.jpeg)

---

📂 previsao_ibovespa/
```
├── 📂 Base_de_Dados/                   # Arquivo .csv com dados históricos da IBOVESPA
│   └── 📄 Dados Históricos - Ibovespa.csv
├── 📂 Historico_de_Pred/               # Plotagem gráfica das predições por dia
│   └── 📄 grafico_predicoes.jpeg
├── 📂 Subcodigos/                      # Códigos auxiliares (benchmark de modelos e scraping)
│   ├── 📄 benchmarking_models.ipynb
│   └── 📄 scraping_ibov_data.ipynb
├── 📄 App_Random Forest Predct.ipynb   # Código com foco apenas no modelo Random Forest (melhor performance)
├── 📄 Machine_Code.ipynb               # Pipeline completo com todo o código de pré-processamento, modelagem e previsão
└── 📄 README.md                        # Documentação do projeto
```

---

## 🔜 Próximas Etapas

- Adição de novos modelos: **SARIMA, LSTM**
- Avaliação por métricas: **MAPE, RMSE, MAE**
- Automatização via pipeline modular
- Otimização de hiperparâmetros
- Scraping por intervalo de última data da base de dados até a data de hoje

---

## 👨‍💻 Contato: **Luis Rufino — Analista de Dados**  
[<img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/linkedin/linkedin-original.svg" width="50" height="50" />](https://www.linkedin.com/in/luis-henrique-rufino-2341901b2/)


---

## 📃 Licença

Este projeto está licenciado sob a **MIT License**.
