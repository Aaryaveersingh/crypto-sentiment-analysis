# Crypto Market Sentiment vs Trader Behavior Analysis

## Overview

This project analyzes how market sentiment (Fear vs Greed) influences trader behavior and trading performance on the Hyperliquid platform.

Using historical trading data and Bitcoin Fear/Greed sentiment data, the project explores:

- Trader profitability across different sentiment conditions
- Behavioral changes in trading activity and position sizing
- Differences between profitable and unprofitable traders
- Actionable trading strategies derived from real trading patterns

The analysis combines data cleaning, feature engineering, visualization, behavioral analysis, and clustering techniques to uncover meaningful insights from real-world crypto trading activity.

---

## Objectives

The objectives of this project are:

- Analyze whether trader performance differs between Fear and Greed market conditions
- Study behavioral changes such as:
  - Trade frequency
  - Position sizing
  - BUY vs SELL bias
- Segment traders based on activity and profitability
- Derive actionable trading strategies using sentiment-driven insights

---

## Dataset

### 1. Bitcoin Market Sentiment Dataset

Contains:
- Date
- Fear/Greed classification
- Sentiment value

### 2. Hyperliquid Historical Trader Dataset

Contains:
- Account
- Coin
- Execution price
- Position size
- Trade direction
- Closed PnL
- Timestamp
- Transaction information

> Note: The historical trader dataset is provided as a compressed `.zip` file inside the repository.

---

## Methodology

### Data Preparation

- Loaded and cleaned both datasets
- Checked for missing values and duplicates
- Converted timestamps into daily format
- Merged sentiment and trading datasets using date alignment

### Feature Engineering

Created the following metrics:

- Daily PnL per trader
- Win rate
- Trade frequency
- Average trade size
- Long/Short ratio
- Risk proxy using trade size

### Analysis Performed

- Performance comparison across Fear vs Greed
- Behavioral analysis under different sentiment conditions
- Trader segmentation:
  - Frequent vs infrequent traders
  - Winners vs losers
- Clustering traders into behavioral archetypes

---

## Key Insights

### Performance Insights

- Total PnL was higher during Greed periods (~$4.87M) compared to Fear (~$4.10M)
- Win rate was slightly higher during Fear periods (84.4% vs 82.5%)
- Extreme Greed produced the highest average PnL and highest win rate

### Behavioral Insights

- Traders were approximately **2.7x more active during Fear periods**
- Larger trade sizes were observed during Greed phases
- Traders displayed stronger BUY bias during bullish sentiment

### Trader Segmentation Insights

- Losing traders incurred significant losses during Greed due to aggressive buying behavior
- Low-frequency traders often showed higher consistency than high-frequency traders
- High-risk traders generated larger returns but traded less frequently

---

## Strategy Recommendations

### Rule 1: Avoid Aggressive Buying During Greed

- Losing traders lost approximately **-$450K during Greed periods**
- These traders executed around **66.9% BUY trades**, indicating trend-chasing behavior

**Recommendation:**
- Avoid excessive long exposure during Greed
- Reduce position size during overheated market conditions
- Avoid momentum chasing

---

### Rule 2: Extreme Greed Offers High Reward but Requires Strict Risk Control

Extreme Greed periods showed:
- Highest win rate (~89.2%)
- Highest average PnL (~$67.89 per trade)

However:
- Maximum losses reached ~$117K compared to ~$35K during Fear

**Recommendation:**
- Participate during strong bullish trends with disciplined risk management
- Use strict stop-loss mechanisms
- Avoid oversized positions

---

## Bonus Analysis — Trader Clustering

K-Means clustering identified three trader archetypes:

| Cluster | Characteristics |
|---|---|
| Cluster 0 | Low-risk, high-frequency traders |
| Cluster 1 | Medium-risk traders with larger positions |
| Cluster 2 | High-risk, low-frequency traders with very large positions |

### Key Finding

Higher trade size correlated with higher average PnL, but significantly lower trading frequency.

---

## Technologies Used

- Python
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook / VS Code

---

## Repository Structure

```plaintext
crypto-sentiment-analysis/
│
├── analysis.ipynb
├── README.md
└── data/
    ├── fear_greed_index.csv
    └── historical_data.zip
```

---

## How to Run

1. Clone the repository:

```bash
git clone https://github.com/Aaryaveersingh/crypto-sentiment-analysis.git
cd crypto-sentiment-analysis
```

2. Install dependencies:

```bash
pip install pandas matplotlib seaborn scikit-learn
```

3. Extract the historical dataset:
- Unzip `historical_data.zip` inside the `data/` folder

4. Open the notebook:
- Open `analysis.ipynb` in VS Code or Jupyter Notebook

5. Run all cells:
- Execute cells sequentially from top to bottom

---

## Conclusion

This project demonstrates that market sentiment strongly influences trader behavior and profitability.

The analysis highlights how:
- Fear drives higher trading activity and volatility
- Greed improves profitability but encourages excessive risk-taking
- Different trader groups react differently to market conditions

Overall, sentiment-aware risk management and behavioral adaptation can significantly improve trading outcomes.
