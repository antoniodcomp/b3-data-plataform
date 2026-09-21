#B3 Data Platform

Plataforma de dados financeira que automatiza a coleta, validação, cálculo de indicadores e disponibilização de informações do mercado brasileiro (B3) e indicadores macroeconômicos.

## Arquitetura

Pipeline baseado na **Medallion Architecture** (Bronze → Silver → Gold):

O pipeline é orquestrado diariamente pelo **Airflow**, com retries e alertas de falha.

## Tecnologias

Python · Pandas · Polars · PySpark · PostgreSQL · SQL · FastAPI · Apache Airflow · Power BI · Docker Compose · scikit-learn · statsmodels

## Fontes de Dados

| Fonte | Dados |
|---|---|
| B3 (via `yfinance`) | Preços OHLCV de ~50-100 ações |
| Banco Central (API SGS) | Selic, CDI, IPCA, câmbio |
| CVM (Dados Abertos) | Cadastro de fundos, informe diário |
| Ibovespa (`^BVSP`) | Série histórica do índice |

