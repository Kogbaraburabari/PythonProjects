# AAPL Historical Stock Analysis | Python

## Project Overview

This project presents an end-to-end time-series analysis of historical Apple Inc. (AAPL) stock data using Python.

The analysis examines long-term price performance, daily returns, volatility, trading activity, drawdowns, recovery periods, and historical monthly seasonality.

The objective was not simply to visualize stock prices, but to evaluate historical performance and downside risk from multiple analytical perspectives and translate the results into clear, evidence-based insights.

---

## Business Questions

The analysis was designed to answer the following questions:

1. How has AAPL's price performed over the historical period?
2. How volatile has the stock been over time?
3. What have been the largest historical drawdowns?
4. How long did major drawdown periods and recoveries take?
5. What does the distribution of daily returns reveal about downside risk?
6. Is trading volume associated with daily return movements?
7. Are larger price movements associated with higher trading activity?
8. Are there noticeable differences in historical returns across calendar months?
9. What does the combination of returns, volatility, and drawdowns reveal about AAPL's historical risk profile?

---

## Dataset

The dataset contains historical AAPL stock market observations covering:

**12 December 1980 – 10 August 2026**

Final analytical dataset:

- **11,506 rows**
- **17 columns**

Key variables include:

- Date
- Open
- High
- Low
- Close
- Adjusted Close
- Volume
- Daily Return
- Intraday Range
- Intraday Range %
- Daily Price Change
- 20-Day Moving Average
- 20-Day Rolling Volatility
- Volume Change %
- Running Peak
- Drawdown
- Zero Volume Flag

---

## Analysis Performed

### 1. Price Performance

Examined AAPL's historical adjusted closing price to understand the long-term price trajectory and major periods of market decline.

### 2. Daily Returns

Calculated daily percentage returns to evaluate short-term price movements and identify extreme positive and negative trading days.

### 3. Rolling Volatility

Calculated 20-day rolling volatility to identify periods when short-term market risk increased substantially.

### 4. Drawdown Analysis

Measured declines from historical running peaks to identify the magnitude and duration of historical downside periods.

### 5. Recovery Analysis

Analysed major drawdown episodes to determine how long AAPL took to recover from significant declines.

### 6. Return Distribution

Examined the distribution of daily returns and calculated skewness to understand the shape and downside characteristics of return behaviour.

### 7. Trading Volume Analysis

Compared trading volume with both daily returns and absolute daily returns to distinguish between return direction and return magnitude.

### 8. Annual Performance

Calculated annual returns to examine year-to-year variation in historical performance.

### 9. Monthly Seasonality

Compared average historical returns across calendar months to identify differences in historical monthly performance.

---

## Key Findings

### Long-Term Price Growth

AAPL experienced substantial long-term price appreciation across the historical period, although the overall upward trajectory was interrupted by several major drawdown periods.

### Significant Downside Risk

The maximum historical drawdown was approximately **81.80%**, demonstrating that substantial declines from previous peaks occurred during the observed period.

### Volatility Varied Over Time

20-day rolling volatility showed periods of substantially elevated market risk.

The highest observed 20-day volatility was approximately **12.89%**.

### Extreme Daily Movements

Most daily returns were concentrated around zero, while a smaller number of observations produced exceptionally large movements.

- Largest positive daily return: approximately **33.23%**
- Largest negative daily return: approximately **-51.87%**

### Negative Skewness

Daily returns had a skewness of approximately **-0.36**, indicating a somewhat heavier or longer negative tail relative to the positive side.

### Trading Volume and Return Magnitude

The Pearson correlation between trading volume and daily return was approximately **0.001**, indicating almost no linear relationship between trading volume and return direction.

However, the correlation between trading volume and absolute daily return was approximately **0.384**, suggesting that higher trading activity was more associated with larger price movements regardless of direction.

### Historical Monthly Performance

Historical monthly performance varied across calendar months.

October recorded the highest average monthly return at approximately **6.33%**, while September recorded the lowest at approximately **-3.90%**.

August also showed relatively strong historical average performance at approximately **5.24%**.

These are historical observations and should not be interpreted as reliable predictions of future performance.

### Drawdown Recovery

Several historical drawdown episodes lasted months or years before the stock returned to previous peak levels, demonstrating that the magnitude of a decline alone does not fully describe downside risk.

---

## Visualizations

The project includes visualizations covering:

- Adjusted closing price over time
- Drawdown over time
- Annual returns
- Volume vs daily return
- Highest volatility periods
- 20-day rolling volatility
- Daily return distribution

---

## Project Outputs

### Analytical Dataset

`AAPL_analytical_dataset.csv`

The final analytical dataset containing the engineered variables used throughout the analysis.

### Analytical Tables

The project includes:

- Annual returns
- Monthly seasonality
- Top 10 positive returns
- Top 10 negative returns
- Top 10 volatility observations
- Top 10 drawdown episodes
- Drawdown summary
- Recovery summary

### Insight Summary

A concise analytical summary is included in the project outputs, highlighting the major findings and conclusions from the analysis.

---

## Tools & Technologies

- **Python**
- **Pandas**
- **NumPy**
- **Matplotlib**
- **Seaborn**
- **Jupyter Notebook**

---

## Analytical Approach

The project followed a structured analytical workflow:

**Data → Validation → Feature Engineering → Exploratory Analysis → Risk Analysis → Visualization → Insight Generation → Output**

The analysis separates historical observations from interpretation and avoids treating historical patterns as guaranteed future outcomes.

---

## Limitations

This analysis is based on historical market data and describes past behaviour.

Historical return patterns, volatility, seasonality, and volume relationships do not guarantee future performance.

The analysis also focuses primarily on market-price and trading-activity variables and does not incorporate fundamental company metrics, macroeconomic variables, valuation measures, dividends, or broader portfolio considerations.

Therefore, the findings should be interpreted as historical market analysis rather than investment advice or a predictive trading model.

---

## Project Context

This project was completed as part of the **AnalystLab Africa Data Analytics Internship** and demonstrates practical application of Python-based data analysis, time-series analysis, statistical reasoning, visualization, and analytical storytelling.
