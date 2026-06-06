# E-Commerce Customer Analytics — RFM Segmentation & Clustering

Customer segmentation and revenue-opportunity analysis on the Brazilian
E-Commerce (Olist) dataset, combining **RFM scoring**, **K-Means clustering**,
SQL, and an interactive **Tableau** dashboard.

**🔗 [Live Tableau dashboard][https://public.tableau.com/app/profile/poorna.venkat.neelakantam/viz/E-CommerceCustomerAnalyticsDashboard/Dashboard1]**

---

## TL;DR

| | |
|---|---|
| **Domain** | Retail / E-Commerce |
| **Dataset** | Brazilian E-Commerce (Olist), Kaggle — 100K+ orders, 96,477 customers, 5 CSVs |
| **Stack** | Python (Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn), SQL, Tableau |
| **Methods** | RFM scoring · K-Means clustering · customer segmentation |
| **Headline result** | R$2.9M revenue-recovery opportunity identified; 12,039 at-risk customers flagged |

---

## What this demonstrates
- **Customer analytics** — RFM (Recency, Frequency, Monetary) scoring and behavioral segmentation.
- **Unsupervised ML** — K-Means clustering with proper validation (Elbow + Silhouette).
- **Data integration** — merging five relational CSVs into a single analytics-ready table.
- **BI storytelling** — translating segments into an executive Tableau dashboard.

## Approach
1. **Integrate** — merged 5 Olist CSVs (orders, customers, items, payments, reviews) into a unified table of 99,441 records / 17 features; handled datetime conversions and ~3% missing delivery dates.
2. **Score** — calculated RFM metrics for 96,477 customers (Pandas `groupby` + `qcut`), assigned quartile-based 1–4 scores, and mapped them to 10 named segments (Champions, Loyal, At Risk, Lost, etc.).
3. **Cluster** — applied K-Means (StandardScaler-normalized); used the Elbow method and Silhouette analysis to select k=3 (silhouette ≈ 0.485, expected for behavioral data).
4. **Visualize** — built a Tableau dashboard with a segment treemap, revenue-by-segment view, monthly trend, and an RFM scatter plot.

## Key findings
- **R$2.9M** revenue-recovery opportunity from churned "Lost" customers.
- **12,039** at-risk customers flagged for targeted retention.
- **6,160** Champion customers (6.4%) identified for a VIP program.
- ~40% revenue spike in November → seasonal marketing signal.
- R$15.4M total revenue analyzed.

> Figures describe what the analysis demonstrates on this public dataset.

## Repository structure
```
notebooks/
  01_data_exploration.ipynb     # loading, cleaning, merging
  02_rfm_analysis.ipynb         # RFM scoring + segmentation
  03_customer_segmentation.ipynb# K-Means clustering + validation
sql/                            # table schemas + RFM (NTILE) queries
data/ or exports/               # rfm_analysis_with_id.csv, customer_geography.csv, monthly_trend.csv
```


## Tech stack
Python (Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn) · SQL · Tableau Public

## Dataset
[Brazilian E-Commerce Public Dataset by Olist](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce) (Kaggle, public).

## Author
**Poorna Venkat Neelakantam** — [GitHub](https://github.com/poornavenkatn08) · [Tableau Public](https://public.tableau.com/app/profile/poorna.venkat.neelakantam)
