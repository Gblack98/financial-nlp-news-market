# 📰 Financial NLP — News Sentiment & Market Movement Prediction

![Python](https://img.shields.io/badge/Python-3.10+-blue) ![HuggingFace](https://img.shields.io/badge/🤗-FinBERT-yellow) ![PyTorch](https://img.shields.io/badge/PyTorch-2.0-orange) ![License](https://img.shields.io/badge/License-MIT-green)

> Combining financial news sentiment (FinBERT) with technical indicators (RSI, MACD) to predict stock market direction.

## Problem Statement

Markets are driven by **information asymmetry**. This project explores whether NLP-extracted sentiment from financial headlines can improve short-term market direction prediction beyond pure technical analysis.

## Architecture

```
Financial News Headlines (DJIA) ──► FinBERT ──► Sentiment Score (positive/negative/neutral)
                                                        │
Historical Price Data ──► RSI, MACD, Bollinger ─────────┤
                                                        ▼
                                          Multivariate LSTM
                                                        │
                                                        ▼
                                       Direction Prediction (Up/Down J+1)
```

## Models

- **FinBERT** (`ProsusAI/finbert`) — BERT pre-trained on financial texts (earnings calls, Bloomberg, Reuters)
- **Multivariate LSTM** — sequence model fusing sentiment + price + technical features
- **Baseline** — logistic regression on technical features only

## Kaggle Notebook

[![Open in Kaggle](https://kaggle.com/static/images/open-in-kaggle.svg)](https://www.kaggle.com/code/ibrahimagabardiop/financial-nlp-news-market)

## Datasets

- [`aaron7sun/stocknews`](https://www.kaggle.com/datasets/aaron7sun/stocknews) — Daily DJIA news (1,600+ votes)
- [`marianadeem755/stock-market-data`](https://www.kaggle.com/datasets/marianadeem755/stock-market-data) — NVDA, AAPL, MSFT, GOOGL, AMZN

## Tech Stack

```
Python · PyTorch · HuggingFace Transformers · FinBERT · scikit-learn · TA-Lib
```

## Author

**Ibrahima Gabar Diop** — [Kaggle](https://www.kaggle.com/ibrahimagabardiop) · [GitHub](https://github.com/Gblack98)
