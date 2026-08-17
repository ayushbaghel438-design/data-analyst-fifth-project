# data-analyst-fifth-project
# Task 5 – Exploratory Data Analysis (EDA)
**DataX Labs | Data Analyst Internship**

## 📌 Objective
Extract insights using visual and statistical exploration on an e-commerce customer & transaction dataset.

## 🛠️ Tools Used
- Python 3
- Pandas
- Matplotlib
- Seaborn
- Jupyter Notebook

## 📂 Repository Structure
```
Task5_EDA/
├── data/
│   └── ecommerce_customer_data.csv     # Synthetic dataset (1000 rows x 12 cols)
├── notebook/
│   └── Task5_EDA.ipynb                 # Full EDA notebook (executed, with outputs)
├── images/                             # Exported chart images used in the PDF report
│   ├── histograms.png
│   ├── boxplots.png
│   ├── categorical_counts.png
│   ├── scatterplots.png
│   ├── pairplot.png
│   ├── heatmap.png
│   └── spend_by_category.png
├── report/
│   └── Task5_EDA_Report.pdf            # Polished PDF report of findings
└── README.md
```

## 🔍 What Was Done
1. **Initial inspection** — `.info()`, `.describe()`, `.value_counts()` on all columns.
2. **Light cleaning** — imputed the ~2% missing values in `AnnualIncome` and `Rating` with the median.
3. **Univariate analysis** — histograms for distribution shape/skew, boxplots for outlier detection.
4. **Categorical analysis** — value counts for `Gender`, `City`, `ProductCategory` visualized as bar charts.
5. **Bivariate analysis** — scatterplots (Age vs SpendingScore, Income vs SpendingScore, Price vs Quantity).
6. **Multivariate analysis** — `sns.pairplot()` and `sns.heatmap()` correlation matrix.
7. **Category deep-dive** — spend distribution by product category.
8. **Findings & recommendation** — written observations after every visual, plus a summary section.

## 📊 Key Findings
- Dataset is largely clean; only `AnnualIncome` and `Rating` had minor (~2%) missing values.
- `AnnualIncome`, `Price`, and `TotalSpend` are right-skewed with a handful of genuine high-value outliers.
- Electronics and Fashion lead in order volume; Electronics drives the highest revenue per order.
- `AnnualIncome` and `SpendingScore` show a moderate **negative** correlation (r ≈ -0.50) — spending isn't purely income-driven.
- Most numeric features are weakly correlated with each other → low multicollinearity risk for modeling.
- **Recommendation:** Segment customers using SpendingScore + ProductCategory affinity + recency (RFM-style / K-Means), not income alone.

## ▶️ How to Run
```bash
pip install pandas numpy matplotlib seaborn jupyter
jupyter notebook notebook/Task5_EDA.ipynb
```

## 📎 Deliverables
- ✅ Jupyter Notebook (`notebook/Task5_EDA.ipynb`)
- ✅ PDF Report of findings (`report/Task5_EDA_Report.pdf`)

---
*Submitted as part of the Data Analyst Internship at DataX Labs.*

