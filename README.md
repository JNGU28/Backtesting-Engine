# Backtesting-Engine
Walk-forward backtester for trading rules on ^SP500TR total-return data (2011–2026).

## Results (test set)
| Strategy | Annualized | Max Drawdown |
|---|---|---|
| Buy-and-hold | 15.28% | −33.79% |
| 60-day trend slope | 9.56% | −27.70% |
| 5-day reversal | 5.36% | — |
| 15-day momentum | 4.51% | — |

## How it works
- 60-day rolling window, no lookahead into future prices
- Validation checks: always-hold must match buy-and-hold; always-cash must return 0.0%

## Run
pip install -r requirements.txt
python backtest.py
