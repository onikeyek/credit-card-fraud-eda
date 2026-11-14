# Credit Card Fraud Patterns and Transaction Behaviour
### An Exploratory Data Analysis (EDA)

## 📌 Project Overview

This project explores credit card transaction data to understand spending patterns and identify characteristics associated with fraudulent transactions.

Using Exploratory Data Analysis (EDA), the project investigates relationships between transaction amounts, merchant categories, and transaction times to identify patterns that may support fraud risk assessment and business decision-making.

The analysis is exploratory rather than predictive. It focuses on uncovering patterns, interpreting findings, and translating data into meaningful business insights.

## 🎯 Project Objectives

The main objectives of this analysis are to:

- Understand transaction spending patterns and distributions.
- Examine differences between fraudulent and legitimate transactions.
- Identify merchant categories with varying fraud rates.
- Investigate how fraud rates change across different hours and periods.
- Explore transaction behaviour and its potential implications for fraud monitoring.

## 📂 Dataset

- **Source:** [Kaggle – Fraud Detection Dataset](https://www.kaggle.com/datasets/kartik2112/fraud-detection) by Kartik Shenoy.
- **Period:** January 2019 – June 2020.
- **Total records:** 1,296,675 transactions.
- **Original dataset dimensions:** 1,296,675 rows and 23 columns.
- **Sample used for analysis:** 200,000 transactions.

### Key Variables

| Variable | Description |
|---|---|
| `amt` | Transaction amount |
| `category` | Merchant category |
| `trans_date_trans_time` | Transaction timestamp |
| `is_fraud` | Fraud indicator (0 = legitimate, 1 = fraudulent) |
| `merchant` | Merchant name |
| `trans_num` | Transaction identifier |

A random sample of 200,000 transactions was selected using a fixed random seed (`42`) to make exploratory analysis and visualization more efficient and reproducible.

## 🛠️ Tools and Technologies

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib

## 🔍 Analytical Approach

The analysis followed a structured EDA process:

1. **Data Loading and Exploration:** Loaded the transaction dataset and examined its structure, dimensions, data types, and summary statistics.

2. **Data Quality Assessment:** Inspected missing values and duplicate records to understand potential data quality issues.

3. **Data Cleaning:** Prepared the dataset for analysis, including handling relevant data quality issues and converting date columns into datetime format.

4. **Sampling:** Selected a reproducible random sample of 200,000 transactions for efficient analysis.

5. **Feature Engineering:** Extracted time-based features, including month, year, hour, and day of the week.

6. **Univariate Analysis:** Examined transaction amount distributions, transaction categories, fraud frequency, and outliers.

7. **Bivariate Analysis:** Investigated relationships between fraud status, transaction amounts, merchant categories, and time.

8. **Advanced Temporal Analysis:** Examined transaction volumes and fraud rates by hour and year, including a comparison of late-night fraud patterns across 2019 and 2020.

## 📊 Key Findings and Insights

### 1. Transaction Amount Distribution

Transaction amounts are right-skewed, with most transactions involving relatively small amounts and a smaller number of high-value transactions.

Fraudulent transactions tend to have higher typical transaction amounts than legitimate transactions. However, some of the largest transactions are legitimate, indicating that transaction amount alone is not a reliable indicator of fraud.

### 2. Fraud Distribution

Fraudulent transactions represent a small proportion of the overall dataset, highlighting the class imbalance commonly found in transaction fraud data.

### 3. Fraud Rates by Merchant Category

Fraud rates vary across merchant categories. Some categories show higher fraud exposure than others, suggesting that category-specific monitoring may be useful when assessing transaction risk.

### 4. Transaction Behaviour Over Time

Transaction volumes and total transaction amounts vary across the observed period. Monthly analysis also reveals changes in transaction activity and fraud rates.

### 5. Fraud Rate by Hour of Day

The hourly analysis reveals noticeable differences in fraud rates throughout the day.

The highest fraud rates in the 200,000-transaction sample occur at:

| Hour | Fraud Rate |
|---|---:|
| 22:00 | 2.86% |
| 23:00 | 3.02% |

Elevated fraud rates are also observed between midnight and 03:00, ranging from approximately 1.35% to 1.62%.

In comparison, most daytime hours record fraud rates below 0.20%.

### 6. Late-Night Fraud Comparison: 2019 vs 2020

A further investigation examined whether the elevated late-night fraud rates were consistent across the two years.

| Year | Hour | Total Transactions | Fraud Cases | Fraud Rate |
|---|---:|---:|---:|---:|
| 2019 | 22:00 | 7,385 | 206 | 2.79% |
| 2019 | 23:00 | 7,375 | 220 | 2.98% |
| 2020 | 22:00 | 3,023 | 92 | 3.04% |
| 2020 | 23:00 | 2,943 | 92 | 3.13% |

The comparison shows that elevated fraud rates at 22:00 and 23:00 were observed in both years. The rates were slightly higher in 2020.

This suggests that the late-night pattern was not limited to one year. However, the comparison should be interpreted cautiously because the 2020 dataset covers only January to June.

## 💡 Business Recommendations

Based on the observed patterns, the following recommendations are proposed:

- Consider combining transaction amount, merchant category, and time-related signals when assessing fraud risk.
- Introduce category-specific monitoring based on observed differences in fraud rates.
- Consider additional monitoring during late-night and early-morning hours, particularly between 22:00 and 03:00.
- Review fraud monitoring strategies as transaction patterns change over time.
- Avoid relying on transaction amount or time alone when assessing potentially fraudulent activity.

## ⚠️ Limitations

- The analysis is exploratory and does not establish causal relationships.
- A random sample of 200,000 transactions was used for analysis rather than the entire dataset.
- The 2020 data covers only part of the calendar year, limiting direct year-to-year comparisons.
- External economic and demographic datasets were not incorporated.
- No predictive modelling or fraud detection system was developed.
- The observed patterns should not be interpreted as proof of fraudulent behaviour in individual transactions.

## 📝 Conclusion

This project demonstrates how exploratory data analysis can reveal meaningful patterns in credit card transaction behaviour.

The analysis identified differences in transaction amounts, merchant categories, and fraud rates across different times of the day. In particular, the late-night analysis revealed consistently elevated fraud rates at 22:00 and 23:00 across both observed years.

These findings demonstrate the potential value of transaction-level analysis in supporting fraud risk assessment and informing business monitoring strategies.

## 👩‍💻 Author

**Naimot Yekini**
