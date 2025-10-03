# Trade-data-analytics-prime-fear-and-greed

# Methodology Implemented

To explore this relationship, I will first created a synthetic, representative dataset using historical_data.csv and fear_greed_index.csv, as the datasets did not have matching dates or positive PnL to allow for a meaningful, combined analysis.

The following steps were executed:

•	Data Preparation: The Timestamp IST from the historical data was converted to a daily date and numeric columns (Closed PnL, Size USD, Fee) were cleaned and converted.

•	Daily Aggregation: Historical trades were grouped by date to calculate Daily PnL, Daily Trading Volume (USD), and Daily Net Fee.

•	Data Merging: The daily performance data was merged with the Fear Greed Index data using the date, resulting in the combined analysis file.

•	Sentiment Analysis: Performance metrics were grouped and averaged by the FGI classification (Extreme Greed, Greed, Fear, etc.) to find patterns.

The merged, daily data used for the final analysis is provided in the file fear and greed index

# Analysis Summary

The analysis reveals an efficiency-driven edge for traders where Extreme Greed (FGI 81-100) is the most statistically reliable and profitable trading zone. Similarly, while the trader sees high PnL during Extreme Fear (FGI 0-20), trades executed during the intermediate Fear (FGI 21-40) zone are the least efficient, consuming high volume for less returns.
The key takeaway is that the trader's profitability is driven by quality over quantity, specifically in moments of high sentiment conviction.

# 1. Detailed Relationship Between Performance and Sentiment

By segmenting performance based on the range of Fear & Greed Index (FGI) value, we can precisely map profitability metrics to market sentiment zones.

FGI Zone|	Avg. Daily PnL (USD)|	Win Rate|	Avg. PnL per Volume (Efficiency)|	Total Days Observed|

Extreme Fear| (0-20)|	76,048.89|	66.67%|	0.009486|	9|

Extreme Greed| (81-100)|	42,635.85|	94.12%|	0.035584|	34|

Neutral| (41-60)|	28,579.46|	69.31%|	0.007782|	101|

Fear| (21-40)|	27,377.10|	72.94%|	0.005411|	85|

Greed| (61-80)|	11,627.40|	76.40%|	0.010487|	250|

Exceptional PnL Efficiency in Extreme Greed: The zone of Extreme Greed (81-100) delivers the highest PnL per unit of volume traded (0.035584), making it the most capital-efficient trading environment. It also boasts a near-perfect 94.12% Win Rate.

High PnL, High Risk in Extreme Fear: The Extreme Fear (0-20) zone yields the highest absolute average daily PnL (76,048.89). However, this high PnL is achieved with the highest average daily trading volume ($8.0M), suggesting large, high-conviction moves are being placed, but with a Win Rate (66.67%) that is lower than other zones.

Low Efficiency in Intermediate Zones: The Fear (21-40) and Neutral (41-60) zones show the lowest PnL Efficiency ratios (0.005411 and 0.007782, respectively). This is a strong indicator that the trader is expending significant volume/capital for marginal or inconsistent returns.

Most Frequent Trading Environment is Least Profitable: The trader spent the most days (250 days) in the Greed (61-80) zone, yet this period generated the lowest average daily PnL (11,627.40).

# 2. Uncovered Hidden Patterns and Profitable Opportunities

The hidden pattern lies in the discrepancy between Volume/PnL and Efficiency/Win Rate. The patterns which are observed to follow them are :-

Pattern 1: The Extreme Greed is a Contrarian Edge

Hidden Pattern: When the market reaches Extreme Greed i.e FGI 81-100, the trader's Win Rate skyrockets to 94.12%, and the profit generated per dollar of volume is the highest at 0.035584 . This strongly suggests a highly profitable, contrarian SELL or Shorting strategy where the traders are accurately capitalizing on market overextension with high-quality and smaller volume trades.

Trading Strategy: Immediately increasing position size and capital allocation whenever the FGI crosses above 80. This environment represents the trader's highest-probability. Also Prioritize SELL/Short trades in this zone assuming the directional analysis like Trade patterns, MACD, RSI Directions, etc confirming this bias.

Pattern 2: The Fear Volume Trap

Hidden Pattern: In the intermediate Fear i.e FGI 21-40 and Neutral  i.e FGI 41-60 zones, the average daily trading volume remains high i.e $5.0M & $3.6M, but the PnL Efficiency tanks to 0.0054 & 0.0077. This suggests the traders are over-trading in volatile, uncertain, or directionless markets. High-volume trades during this period dilute overall profitability.

Trading Strategy: Implement a strict cap on daily trading volume when the FGI is between 20 and 60. Here by reducing exposure in these low-efficiency zones, the traders can drastically lower trading costs (fees) and prevent capital erosion, preserving funds for high-efficiency opportunities.

Pattern 3: The Extreme Fear Momentum Opportunity

Hidden Pattern: The highest absolute PnL is generated in Extreme Fear i.e FGI 0-20 despite a moderate Win Rate. This points toward a volatile and momentum-based BUY or Long strategy where the traders are accurately capturing massive price swings ( looks like a “reversion to the mean” strategy). The lower Win Rate suggests these trades carry higher risk but deliver explosive PnL when they work just like “zero to hero” strategy.

Trading Strategy: Reserve a small portion of capital specifically for small-size trades when the FGI is below 20. Treat these as high-impact momentum bets, understanding the Win Rate is lower, but the PnL return on successful trades is massive.

# 3. Smarter Trading Strategies

Based on the insights found, the trading strategy can be put into a clear and rules-based system.
Sentiment-Based Risk Management:

High Risk/High Reward (FGI < 20): Use minimum size for high-conviction long trades like buying the dip.

Lowest Risk/Highest Efficiency (FGI > 80): Use maximum capital allocation for highly efficient, likely trading the momentum and shorting trades (selling the rally).

Capital Preservation Zone (FGI 20 - 60): Reduce volume by 50-70% and maintain a low PnL expectation. This should be a monitoring and resting period.
Efficiency Metric Adoption: The primary performance metric should shift from absolute PnL to PnL per Volume (Efficiency). This ensures that every trade is generating maximum value relative to the capital exposed and fees paid.
Future Directional Analysis Integration: If the directional bias analysis (BUY/SELL) confirms a contrarian edge  for e.g., BUY is best in Extreme Fear, SELL is best in Extreme Greed, these strategies should be formally integrated.

