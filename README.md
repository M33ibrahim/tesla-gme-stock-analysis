# Tesla & GameStop | Stock and Revenue Analysis

A Python learning project retrieving historical TSLA and GME prices, extracting quarterly revenue tables, and plotting closing-price histories.

## Project contents

- Historical stock requests from 2010-01-01 to 2025-08-01 (exclusive end date).
- Quarterly revenue tables cleaned into numeric values and dates.
- Separate closing-price charts for Tesla and GameStop.

Revenue is printed for inspection; it is not plotted alongside stock prices.

## Run locally

Install Python 3.10 or later and Google Chrome, then create and activate a virtual environment.

```bash
python -m pip install -r requirements.txt
python -m jupyter lab
```

Open [the analysis notebook](<1 Analyzing Tesla and GameStop Historical Stock Trends, Revenue Insights & Visual Dashboard (2010–2025).ipynb>) and run its cells. Selenium may need network access to download a compatible Chrome driver.

## Reliability improvements

The notebook waits for table elements, validates missing tables and empty price data, converts revenue fields to numeric/date types, and closes Chrome in a finally block. Saved outputs have been cleared to avoid presenting stale results as a fresh run.

## Interpretation and limitations

Stock queries use a fixed historical window; revenue tables are fetched live and may cover another period. Align their dates before comparing them. The charts use closing prices with `auto_adjust=False`; account for corporate actions before interpreting returns.

Yahoo Finance and Macrotrends access restrictions, rate limits, or page changes can prevent execution. This peer-graded educational project demonstrates collection and visualization and does not establish causation or implement a trading strategy.

## License and author

[MIT License](LICENSE) applies to the code. External data remains subject to provider terms.

[Muhammad Ibrahim](https://www.linkedin.com/in/m135ibrahim/) · [GitHub portfolio](https://github.com/M33ibrahim)
