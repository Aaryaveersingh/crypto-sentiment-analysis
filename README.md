# Crypto Market Sentiment vs Trader Behavior Analysis

## Objective
Analyze how market sentiment (Fear vs Greed) affects trader behavior and performance on Hyperliquid.

---

## Methodology

- Cleaned and merged sentiment + trading datasets
- Converted timestamps to daily level
- Created key metrics:
  - PnL, win rate, trade frequency, position size
- Compared performance across sentiment conditions
- Analyzed behavioral changes
- Segmented traders (winners vs losers, activity levels)
- Applied clustering for behavioral archetypes

---

## Key Insights

- Total PnL is higher during Greed ($4.87M vs $4.10M), but win rate is higher during Fear (84.4% vs 82.5%)
- Traders are **2.7x more active during Fear**, indicating volatility-driven trading
- Extreme Greed provides highest efficiency (89.2% win rate, highest mean PnL)
- Losing traders perform poorly during Greed (-$450K) due to aggressive buying behavior
- Low-volume traders achieve higher win rates than high-frequency traders

---

## Strategy Recommendations

###  1: Avoid Aggressive Buying During Greed

- Losing traders incurred significant losses (~-$450K) during Greed periods.
- These traders executed ~66.9% BUY trades, indicating strong long bias and trend-chasing behavior.

**Interpretation:**
Traders tend to overcommit to bullish positions during Greed, often entering overextended markets.

**Actionable Insight:**
- Avoid excessive long exposure during Greed phases
- Reduce position sizes and avoid chasing momentum-driven trades
- Implement stricter entry criteria and risk controls


---

###  2: Extreme Greed Offers High Reward but Requires Strict Risk Control

- Extreme Greed periods show:
  - Highest win rate (~89.2%)
  - Highest average PnL (~$67.89 per trade)
- However, risk is also significantly higher:
  - Maximum loss reaches ~$117K vs ~$35K during Fear

**Interpretation:**
Strong bullish sentiment creates highly profitable conditions, but also amplifies downside risk.

**Actionable Insight:**
- Participate actively during Extreme Greed, but:
  - Use strict stop-loss mechanisms
  - Avoid oversized positions
- Suitable primarily for experienced or disciplined traders

---

## Bonus

- Trader clustering reveals:
  - Low-risk high-frequency traders
  - Medium-risk traders
  - High-risk low-frequency traders

---

## How to Run

1. Clone the repository:

```bash
git clone https://github.com/Aaryaveersingh/crypto-sentiment-analysis
cd crypto-sentiment-analysis
```

2. Install dependencies:

```bash
pip install pandas matplotlib seaborn scikit-learn
```

3. Open the notebook:
```bash
- Open `analysis.ipynb` in VS Code or Jupyter Notebook
```  

4. Run all cells:
```bash
- Execute cells from top to bottom
```
