# AAPL Historical Stock Analysis

## 📊 Project Overview

This project presents a comprehensive analysis of historical Apple Inc. (AAPL) stock data using Python.

The analysis goes beyond basic price exploration to examine long-term price performance, daily returns, volatility, trading activity, drawdowns, recovery periods, and historical monthly seasonality.

The project was completed as part of the **AnalystLab Africa Data Analytics Internship — Week 6: Advanced Python for Data Analysis**.

---

## 🎯 Project Objective

The objective of this analysis was to understand AAPL's historical market behaviour and identify meaningful patterns in:

- Long-term price performance
- Daily returns
- Market volatility
- Trading volume
- Extreme price movements
- Historical drawdowns
- Drawdown recovery periods
- Monthly seasonality
- Downside risk

The analysis focuses on historical evidence and is intended for analytical and educational purposes rather than investment advice or future price prediction.

---

## 📁 Dataset

The final analytical dataset contains:

- **11,506 observations**
- **17 analytical variables**
- **Date range:** December 12, 1980 – August 10, 2026

The final dataset includes:

| Variable | Description |
|---|---|
| Date | Trading date |
| Adj Close | Adjusted closing price |
| Close | Closing price |
| High | Highest price during the trading day |
| Low | Lowest price during the trading day |
| Open | Opening price |
| Volume | Trading volume |
| Zero_Volume_Flag | Indicator for zero-volume observations |
| Daily_Return | Daily percentage return |
| Intraday_Range | Difference between daily high and low |
| Intraday_Range_Pct | Intraday range relative to price |
| Daily_Price_Change | Daily change in closing price |
| MA_20 | 20-day moving average |
| Volatility_20 | 20-day rolling volatility |
| Volume_Change_Pct | Percentage change in trading volume |
| Running_Peak | Historical running peak |
| Drawdown | Decline from the historical running peak |

---

## 🛠️ Tools & Technologies

- **Python**
- **Pandas**
- **NumPy**
- **Matplotlib**
- **Jupyter Notebook**
- **Git**
- **GitHub**

Python was used for data cleaning, transformation, feature engineering, statistical analysis, time-series analysis, and visualization.

---

# 🔍 Analytical Workflow

## 1. Data Loading & Exploration

The historical AAPL dataset was loaded into Python and examined to understand its structure and quality.

Initial exploration included:

- Dataset dimensions
- Column names
- Data types
- Date range
- Missing values
- Duplicate observations
- Numerical characteristics
- Data-quality issues

---

## 2. Data Cleaning & Preparation

The dataset was validated and prepared for time-series analysis.

The workflow maintained separation between the original dataset and the final analytical dataset to preserve data integrity and reproducibility.

---

## 3. Feature Engineering

Additional analytical variables were created to support deeper analysis of price behaviour and market risk.

Key engineered features included:

- Daily returns
- Daily price changes
- Intraday trading range
- Intraday range percentage
- 20-day moving average
- 20-day rolling volatility
- Volume percentage change
- Running historical peak
- Drawdown from historical peak

---

## 4. Return Analysis

Daily returns were analysed to understand the distribution and magnitude of AAPL's historical price movements.

The analysis examined:

- Daily return distribution
- Largest positive returns
- Largest negative returns
- Return skewness
- Annual returns
- Monthly returns

---

## 5. Volatility Analysis

A 20-day rolling volatility measure was used to examine how market risk changed over time.

The analysis identified:

- Periods of elevated volatility
- Highest-volatility trading days
- Changes in volatility over time
- Relationship between trading volume and return magnitude

---

## 6. Drawdown & Recovery Analysis

Historical drawdowns were analysed by measuring declines from previous running peaks.

The analysis identified:

- Drawdown start dates
- Drawdown end dates
- Maximum drawdowns
- Drawdown trough dates
- Trading-day duration
- Calendar-day duration
- Recovery dates
- Recovery duration
- Ongoing drawdown periods

This allowed downside risk to be evaluated using both the **magnitude** and **duration** of declines.

---

## 7. Seasonality Analysis

Historical monthly performance was analysed by calendar month.

The analysis compared:

- Average monthly returns
- Monthly performance variation
- Strongest historical months
- Weakest historical months

These results represent historical observations and should not be interpreted as reliable predictions of future performance.

---

# 📌 Key Findings

### Long-Term Price Growth

AAPL's adjusted closing price increased substantially over the historical period, although the long-term upward trend was interrupted by several major drawdown periods.

### Significant Downside Risk

The maximum historical drawdown was approximately **81.80%**, demonstrating that substantial declines from previous peaks occurred during the observed period.

### Volatility Varied Considerably

The 20-day rolling volatility showed periods of substantially elevated market risk.

The highest observed 20-day volatility was approximately **12.89%**.

### Extreme Daily Movements Were Relatively Uncommon

Most daily returns were concentrated around zero, while a smaller number of observations produced exceptionally large positive or negative movements.

The largest observed:

- **Positive daily return:** approximately **33.23%**
- **Negative daily return:** approximately **-51.87%**

### Negative Skewness

Daily returns had a skewness of approximately **-0.36**, indicating that the distribution contained a somewhat heavier negative tail relative to the positive side.

### Trading Volume and Return Direction

The Pearson correlation between trading volume and daily return was approximately **0.001**.

This indicates almost no linear relationship between trading volume and the direction of daily returns.

However, the correlation between trading volume and absolute daily return was approximately **0.384**.

This suggests that higher trading activity was more associated with the **magnitude of price movements** than with whether the movement was positive or negative.

### Historical Monthly Performance Varied

Historical average monthly returns differed across calendar months.

- **October:** approximately **6.33%**
- **August:** approximately **5.24%**
- **September:** approximately **-3.90%**

These figures describe historical behaviour within the dataset and do not establish a dependable seasonal trading strategy.

### Major Drawdowns Required Extended Recovery Periods

Several historical drawdowns lasted months or years before the stock recovered to its previous peak.

This demonstrates the importance of evaluating both the magnitude of a decline and the time required for recovery.

---

# 📈 Visualizations

The project includes the following visualizations:

1. **Drawdown Over Time**
2. **Annual Return by Year**
3. **Trading Volume vs Daily Return**
4. **Top 10 Highest-Volatility Days**
5. **20-Day Rolling Volatility Over Time**
6. **Daily Return Distribution**
7. **Adjusted Close on Logarithmic Scale**

These visualizations provide complementary perspectives on AAPL's historical price behaviour, return distribution, volatility, trading activity, and downside risk.

---

# 📋 Analytical Outputs

The analysis produced the following analytical tables:

- `annual_returns.csv`
- `monthly_seasonality.csv`
- `top_10_positive_returns.csv`
- `top_10_negative_returns.csv`
- `top_10_volatility.csv`
- `top_10_drawdowns.csv`
- `drawdown_summary.csv`
- `recovery_summary.csv`

The final analytical dataset is:

- `AAPL_analytical_dataset.csv`

---

# 📂 Project Structure

```text
AAPL-Advanced-Python-Stock-Analysis/
│
├── README.md
│
├── notebooks/
│   └── AAPL_Advanced_Python_Analysis.ipynb
│
├── data/
│   ├── raw/
│   └── processed/
│       └── AAPL_analytical_dataset.csv
│
├── analysis_output/
│   ├── tables/
│   │   ├── annual_returns.csv
│   │   ├── monthly_seasonality.csv
│   │   ├── top_10_positive_returns.csv
│   │   ├── top_10_negative_returns.csv
│   │   ├── top_10_volatility.csv
│   │   ├── top_10_drawdowns.csv
│   │   ├── drawdown_summary.csv
│   │   └── recovery_summary.csv
│   │
│   └── visualizations/
│       ├── 01_drawdown_over_time.png
│       ├── 02_annual_return_by_year.png
│       ├── 03_volume_vs_daily_return.png
│       ├── 04_top_10_highest_volatility_days.png
│       ├── 05_20_day_rolling_volatility_over_time.png
│       ├── 06_daily_return_distribution.png
│       └── 07_adjusted_close_log_scale.png
│
├── reports/
│   └── AAPL_Week6_Insight_Summary.docx
│
├── requirements.txt
│
└── .gitignore
