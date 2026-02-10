# Credit Card Fraud Patterns and Customer Behavior  
## An Exploratory Data Analysis (EDA)

📌 Project Introduction
This project performs Exploratory Data Analysis (EDA) on a large credit card transaction dataset to understand customer spending behavior and identify patterns associated with fraudulent transactions. The analysis focuses on uncovering trends, relationships, and temporal patterns that can support fraud risk assessment and decision-making.

The project is exploratory, not predictive, and emphasizes clear insights, responsible interpretation, and business relevance.

## Objective of the Analysis

The objective of this analysis is to explore credit card transaction data in order to:
- Understand customer spending behavior
- Identify patterns associated with fraudulent transactions
- Examine how fraud risk varies by transaction amount, category, and time

This study is exploratory in nature and focuses on identifying trends and relationships rather than building predictive models.

## Scope and Assumptions

- The analysis focuses on exploratory data analysis (EDA) techniques.
- No predictive modeling or causal inference is performed.
- Economic effects are discussed only in the context of observed temporal patterns.
- External economic or demographic datasets are not incorporated.

## 📂 Dataset

- Type: Credit card transaction records
- Time period: 2019–2020
- Size: ~1.3 million transactions

# Key variables:
* amt – transaction amount
* category – merchant category
* trans_date_trans_time – transaction timestamp
* is_fraud – fraud indicator (0 = non-fraud, 1 = fraud)
  
** ⚠️ Note: Due to dataset size, a representative sample was used for visualization to ensure efficient analysis while preserving overall patterns.**

## 🔧 Tools & Technologies

    Python
    Jupyter Notebook
    Libraries: pandas, numpy, matplotlib


## Analytical Approach (Process Summary)

The analysis followed a structured exploratory data analysis (EDA) process:
1. Data preparation: Cleaned and validated transaction data, handled missing values, and engineered time-based features.
2. Univariate analysis: Examined individual variables such as transaction amounts, categories, and fraud frequency.
3. Bivariate analysis: Explored relationships between fraud status and transaction amount, category, and time.
4. Advanced temporal analysis: Investigated hourly patterns and year-to-year changes to capture behavioral and economic context.
This approach ensures insights are data-driven, interpretable, and relevant to business decision-making.


## Key Insights

- Fraudulent transactions are rare but tend to involve higher typical amounts than legitimate transactions.
- Extremely high transaction values are usually legitimate, indicating that amount alone is not a reliable fraud indicator.
- Fraud risk varies significantly by transaction category, with higher exposure in certain online and miscellaneous categories.
- Fraud activity shows time-based patterns, with relatively higher risk during low-activity hours.
- Despite lower transaction volume in 2020, the fraud rate increased, suggesting heightened risk during periods of economic disruption.

## 💡Recommendations

- Apply multi-factor fraud scoring combining amount, category, and time-of-day signals.
- Use category-specific monitoring to reduce false positives.
- Increase vigilance during late-night and early-morning hours.
- Adapt fraud monitoring strategies during periods of economic or behavioral change.

## ⚠️ Limitations

- The analysis is exploratory and does not establish causal relationships.
- No external economic or demographic datasets were used.
- Results are intended to inform understanding, not to serve as a deployed fraud detection system.

** Author: 
Naimot Yekini 
