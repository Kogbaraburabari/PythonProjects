# Bank Marketing Case Study — Term Deposit Subscription Analysis

**AnalystLab Africa — Data Analytics Internship, Week 5: Business Analytics Case Study**

A data-driven analysis of a real bank marketing campaign, identifying which customer
characteristics and campaign approaches drive term deposit subscriptions, with
actionable recommendations for future campaigns.

---

## 1. Business Problem

Banks run outbound marketing campaigns to encourage customers to subscribe to term
deposits, but campaign performance varies widely across customer segments.

**Business question:** Why do some customers subscribe to term deposits while others
do not, and which customer groups are more likely to respond positively to marketing
campaigns?

Answering this allows the bank to shift from a one-size-fits-all campaign to a
targeted strategy improving conversion while reducing wasted outreach.

---

## 2. Dataset

| | |
|---|---|
| Source | [Bank Marketing Dataset — Kaggle](https://www.kaggle.com/datasets/janiobachmann/bank-marketing-dataset) |
| Rows | 11,162 customer contacts |
| Columns | 17 |
| Target variable | `deposit` — whether the customer subscribed (yes/no) |
| Missing values | 0 (some columns use `"unknown"` as a placeholder category) |
| Duplicate rows | 0 |

**Key columns:**
- **Demographics:** age, job, marital status, education
- **Financial profile:** account balance, credit default, housing loan, personal loan
- **Campaign details:** contact method, day/month of last contact, call duration, number of contacts
- **Previous campaign history:** pdays, previous, poutcome

---

## 3. Methodology

1. **Data cleaning** — checked for missing values and duplicates (none found).
   `"unknown"` categorical values were kept as a valid category rather than dropped,
   since removing them would discard up to 74.6% of rows in some columns. Created a
   `was_previously_contacted` flag from `pdays` to avoid `-1` placeholders distorting
   numeric analysis.
2. **Exploratory data analysis** — dataset overview, summary statistics, distribution
   analysis (histograms, box plots).
3. **Key driver analysis** — compared subscription rate across job, education,
   marital status, age group, previous campaign outcome, contact method, and account
   balance using bar charts, a line chart (monthly trend), and a correlation heatmap.
4. **Insight generation and recommendations** — translated statistical patterns into
   business-actionable insights.

**Tools:** Python (pandas, matplotlib, seaborn), Jupyter Notebook (VS Code)

---

## 4. Key Findings

| # | Finding |
|---|---|
| 1 | **Previous campaign success is the strongest predictor of subscription.** Customers who succeeded before subscribe again at ~91%, vs ~41% for never-contacted customers. |
| 2 | **Age shows a U-shaped relationship.** 60+ (~82%) and 18-30 (~57%) subscribe far more than working-age adults 31-50 (~41-43%). |
| 3 | **Job type matters strongly.** Students (~75%) and retirees (~65%) subscribe far more than blue-collar (~36%) or entrepreneur (~38%) customers. |
| 4 | **Contact method affects conversion.** Cellular (~54%) and telephone (~50%) contacts convert far better than an unrecorded ("unknown") method (~23%), which represents 21% of all customers. |
| 5 | **Marital status and education show moderate effects.** Single customers (~54%) convert more than married (~44%); tertiary-educated customers (~54%) convert more than primary-educated (~38-39%). |
| 6 | **Balance predicts conversion.** Subscribers hold a median balance of €733, vs €414 for non-subscribers. |
| 7 | **Campaign volume and timing may be misaligned.** May had the highest contact volume (25% of all contacts) but the lowest conversion rate (~33%). |

---

## 5. Business Insights

Subscription is driven far more by a customer's **life stage and financial
circumstances** than by campaign mechanics alone. Customers with fewer competing
financial commitments students, retirees, and single customers are consistently
more receptive, a pattern that repeats independently across age, job, and marital
status.

The single strongest driver, however, is the customer's **own history with the
bank** prior campaign success predicts future success far better than any
demographic factor, representing a low-effort, high-return re-engagement
opportunity.

Meanwhile, working-age, married, blue-collar/entrepreneur customers are the
hardest-to-convert segment, and 21% of customers are being reached through a
contact channel that isn't properly recorded converting far worse as a result.

---

## 6. Recommendations

1. **Prioritize re-engaging customers with previous campaign success** they convert at nearly double the overall rate (~91% vs ~47%).
2. **Shift marketing focus toward students, retirees, and single customers**, who consistently show the highest subscription rates.
3. **Reduce reliance on unrecorded ("unknown") contact methods** investigate the data gap and shift toward cellular/telephone contact.
4. **Reconsider campaign timing and volume**, particularly around May, where the largest contact push coincided with the weakest performance.
5. **Use account balance as a pre-screening signal** for outreach prioritization.

---

## 7. Visualizations

**Overall subscription split**
![Overall Subscription Split](charts/chart_pie.png)

**Distribution of customer age**
![Distribution of Customer Age](charts/chart_age_hist.png)

**Distribution of account balance**
![Distribution of Account Balance](charts/chart_balance_overall.png)

**Subscription rate by job type**
![Subscription Rate by Job Type](charts/chart_job.png)

**Subscription rate by education level**
![Subscription Rate by Education Level](charts/chart_education.png)

**Subscription rate by marital status**
![Subscription Rate by Marital Status](charts/chart_marital.png)

**Subscription rate by age group**
![Subscription Rate by Age Group](charts/chart_age_group.png)

**Subscription rate by previous campaign outcome**
![Subscription Rate by Previous Campaign Outcome](charts/chart_poutcome.png)

**Subscription rate by contact method**
![Subscription Rate by Contact Method](charts/chart_contact.png)

**Subscription rate by month**
![Subscription Rate by Month](charts/chart_month.png)

**Correlation heatmap of numeric variables**
![Correlation Heatmap](charts/chart_heatmap.png)

**Account balance by subscription outcome**
![Account Balance by Subscription Outcome](charts/chart_balance_box.png)

---

## 8. Repository Contents

## 9. Author

**Burabari Gift Kogbara**
AnalystLab Africa Data Analytics Internship Program — Week 5 Business Analytics
Case Study.
