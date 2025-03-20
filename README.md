
# 📈 Previsão do IBOVESPA com Séries Temporais e Random Forest

Projeto de modelagem preditiva para prever o fechamento diário do índice **IBOVESPA**, utilizando técnicas de **Séries Temporais**, **Feature Engineering** e algoritmos de **Machine Learning (Random Forest)**.

---

## 💡 Objetivo

Construir um pipeline preditivo capaz de:
- Prever o valor de fechamento do IBOVESPA para os próximos dias;
- Calcular **intervalos de confiança** para as previsões;
- Analisar desempenho comparativo com diferentes abordagens.

---

## ⚙️ Tecnologias Utilizadas

- **Python 3.10+**
- `pandas`, `numpy`, `matplotlib`, `seaborn`
- `scikit-learn`
- `statsmodels` *(opcional para baseline ARIMA/SARIMA)*
- `Prophet` *(em desenvolvimento)*
- `XGBoost`, `LSTM` *(próximas etapas)*

---

## 📊 Features Criadas

- Lags (`lag_1` a `lag_40`)
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
3. **Treinamento do modelo Random Forest Regressor**;
4. **Validação e previsão para múltiplos dias futuros**;
5. **Cálculo do intervalo de confiança com base na dispersão das árvores individuais**;
6. **Visualização com linha de tendência e faixa de incerteza**.

---

## 📈 Exemplo de Visualização

![plot](assets/exemplo_previsao_ibov.png)

---

## 📁 Estrutura do Projeto

```
📂 previsao_ibovespa/
├── data/
│   └── ibov_historico.csv
├── notebooks/
│   └── modelo_rf.ipynb
├── src/
│   ├── feature_engineering.py
│   ├── train_model.py
│   └── forecast_pipeline.py
├── assets/
│   └── exemplo_previsao_ibov.png
├── README.md
└── requirements.txt
```

---

## 📦 Como Executar

```bash
# Clone o repositório
git clone https://github.com/seu-usuario/previsao-ibovespa.git
cd previsao-ibovespa

# Instale as dependências
pip install -r requirements.txt

# Execute o notebook principal
jupyter notebook notebooks/modelo_rf.ipynb
```

---

## 🔜 Próximas Etapas

- Adição de novos modelos: **ARIMA, SARIMA, Prophet, XGBoost, LSTM**
- Avaliação por métricas: **MAPE, RMSE, MAE**
- Automatização via pipeline modular
- Otimização de hiperparâmetros

---

## 👨‍💻 Autor

**Luis — Analista de Dados**  
📬 [LinkedIn](https://www.linkedin.com/)

---

## 📃 Licença

Este projeto está licenciado sob a **MIT License**.
