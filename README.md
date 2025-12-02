ARINT - AlphaVantage News + Sentiment Pipeline

What this repo contains
- `ARINT.ipynb`: notebook to fetch news via Alpha Vantage NEWS_SENTIMENT, run VADER sentiment, and save CSV.
- `data_cleaning.ipynb`: notebook to clean raw sentiment CSV into `stock.csv` for analysis.
- `analysis.ipynb`: notebook to aggregate signals and run intraday open->close backtests.

Setup
1. Create a `.env` file or set environment variable `ALPHAVANTAGE_API_KEY` with your Alpha Vantage key.
2. (Optional) create `API.key` (single-line) or `API.rtf` if you prefer legacy format — `.gitignore` prevents committing these.
3. Install dependencies: `pip install -r requirements.txt`

Usage
- Run `ARINT.ipynb` to fetch recent articles (default last 14 days) and produce a `sentiment_stock_news_YYYYMMDD.csv` file.
- Run `data_cleaning.ipynb` to produce `stock.csv` used by `analysis.ipynb`.
- Run `analysis.ipynb` to aggregate majority signals per day and run intraday backtest using `yfinance` or a provided `price.csv`.

