# Trader-Sentiment-Analysis
# Trader Performance vs Market Sentiment Analysis. Data Science Assignment

## Objective

The objective of this analysis is to examine how Bitcoin market sentiment 
(Fear vs Greed) impacts trader behavior and performance on Hyperliquid.

The aim to identify whether traders change their trading patterns based on market sentiment and whether profitability differs during Fear and Greed periods.The goal is to derive actionable trading insights from sentiment-driven behavior.

## Dataset Description

Two datasets were used:

1. Fear/Greed Index Dataset
   - Columns: timestamp, value, classification, date
   - Represents daily Bitcoin market sentiment.

2. Historical Trader Dataset
   - Includes trade-level data such as:
     Account, Coin, Execution Price, Size USD,
     Side, Closed PnL, Fee, Timestamp IST, etc.
   - Represents individual trade behavior and performance.
  
## Methodology

The analysis was performed in the following stages:

   1. Data Cleaning
   - Checked for missing values and duplicates.
   - Converted timestamps to datetime format.
   - Extracted daily date for alignment.

   2. Data Alignment
   - Merged trader data with sentiment data at daily level.

   3. Feature Engineering
   - Daily PnL per trader
   - Win rate per account
   - Trade frequency per day
   - Average trade size (Size USD)
   - Long/Short ratio
   - Trader segmentation (High size, Frequent, Consistent winners)

   4. Sentiment-Based Comparison
   - Compared performance metrics between Fear and Greed days.
   - Analyzed behavioral shifts across sentiment regimes.

## Key Insights

1. Performance Differences Across Sentiment

Average PnL and win rate show noticeable variation between Fear and Greed days. 
Greed days tend to have slightly higher average profitability, while Fear days 
exhibit higher volatility in returns.

2. Increased Volatility During Fear

Standard deviation of PnL is significantly higher during Fear periods, 
indicating elevated uncertainty and risk exposure.

3. Behavioral Shift in Trade Activity

Trade frequency and average trade size increase during Greed days, 
suggesting traders are more confident and aggressive in bullish sentiment.

4. Long/Short Bias

Greed days show a stronger long bias, whereas Fear days demonstrate 
a relatively balanced or increased short activity.

5. Segment-Level Differences

High trade-size traders experience larger drawdowns during Fear days.
Frequent traders perform better in momentum-driven (Greed) environments.
Consistent winners maintain relatively stable performance across sentiment regimes.

## Strategy Recommendations

1. Position Size Adjustment During Fear

Reduce trade size by 30–50% during Fear days, especially for high-size traders.
This may help reduce drawdowns during volatile sentiment periods.

2. Selective Aggression During Greed

Increase trade frequency during Greed days, but only for consistent winners.
Momentum environments favor disciplined traders.

3. Sentiment-Aligned Bias

Adopt a long bias during Greed regimes and reduce directional exposure during Fear periods.

4. Risk Management Overlay

Introduce volatility filters that reduce exposure when daily PnL variance exceeds a threshold.


## How to Run

1. Install dependencies:
pip install -r requirements.txt

2. Open:
trader_analysis.ipynb

## Conclusion

This analysis demonstrates that market sentiment significantly influences trader behavior and performance.

Fear periods are characterized by higher volatility and larger drawdowns,
while Greed periods encourage higher activity and improved average returns.

Incorporating sentiment-aware adjustments into trading strategies 
can potentially improve risk-adjusted performance.

## Summary

This project analyzes the relationship between Bitcoin market sentiment 
(Fear/Greed Index) and trader behavior on Hyperliquid.

The findings suggest that:

- Fear periods are associated with higher volatility.
- Greed periods show higher trading activity and improved average returns.
- High-size traders are more exposed to sentiment-driven risk.

Actionable strategies include reducing exposure during Fear and increasing 
selective participation during Greed.
