# Crypto OHLCV Archive

> **Archival & Educational Purposes Only**

This repository contains historical OHLCV (Open, High, Low, Close, Volume) candlestick data for various cryptocurrency trading pairs, sourced from the **Binance public API** (`api.binance.com`).

## Purpose

This data is collected and maintained strictly for:

- **Archival preservation** of historical market data
- **Educational and research use** (backtesting, data analysis, academic study)
- **Personal reference** and algorithmic trading strategy development in non-production environments

## Data Structure

Databases are organized by year and month:

```
<symbol>/
  <YYYY>/
    <YYYY-MM>.db
```

Example:

```
btc/
  2021/
    2021-01.db
    2021-02.db
  2022/
    2022-01.db
```

Each `.db` file is a SQLite database containing 1-minute interval candles with the following schema:

| Column    | Type    | Description                    |
|-----------|---------|--------------------------------|
| timestamp | INTEGER | Milliseconds since Unix epoch  |
| open      | REAL    | Opening price                  |
| high      | REAL    | Highest price                  |
| low       | REAL    | Lowest price                   |
| close     | REAL    | Closing price                  |
| volume    | REAL    | Trading volume                 |

## Source

All data is sourced from the **Binance public API** and is subject to Binance's terms of service. No private or proprietary data is included.

## Disclaimer

- This data is provided **"as is"** without any guarantees of accuracy or completeness.
- Cryptocurrency trading involves substantial risk. This data is **not financial advice**.
- This repository does not contain any trading algorithms, bots, or execution code.
- Binance is a trademark of its respective owner. This project is not affiliated with or endorsed by Binance.

## License

The data in this repository is made available for personal, educational, and research use only. Redistribution for commercial purposes is not permitted without explicit permission.
