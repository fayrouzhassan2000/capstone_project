# Late Delivery Prediction – Olist E-commerce Dataset

##  Team Members

| Name | Phone | Email | ID |
|---|---|---|---|
| Fayrouz Hassan Mahmoud Mohamed | 01558162250 | fairouzhassan2000@gmail.com | 23011125 |
| Kirollos Nader Naguib Youssef | 01206997713 | kirellos.farag.20@gmail.com | 23011425 |
| Fady Anter Abdel-Shahid Nan | 01202804250 | fadyanter2005@gmail.com | 23011404 |
| Fares Hassan Abdelsalam Ragab | 01289961996 | areschamp2003@gmail.com | 23011408 |
| Kareem Younes Abdelaziz Ibrahim | 01278278142 | kyabdelaziz95@gmail.com | 2401244390 |

##  Project Idea

This project uses the **Olist** dataset — a comprehensive Brazilian e-commerce dataset covering orders, customers, products, pricing, payments, reviews, sellers, and delivery information — to analyze and **predict late deliveries**.

The notebook covers the full data science pipeline:
- **Data Loading**: pulling multiple relational tables (customers, products, sellers, orders, order items, payments, reviews, translations) from a PostgreSQL database (Neon).
- **Data Cleaning**: fixing column names, data types, categorical inconsistencies, and validating/handling inconsistent dates.
- **Feature Engineering & Merging**: building a full dataset and engineering features such as order season, weekday, customer/seller aggregates, and defining the target variable `is_late`.
- **Exploratory Data Analysis (EDA)**: outlier analysis, target distribution (highly imbalanced ~92% on-time vs ~8% late), correlation heatmap, time-based trends, category/state-level payment and delay analysis.
- **ML Pipeline**: data splitting, encoding (including frequency encoding for high-cardinality `customer_city`), feature scaling, handling class imbalance (Oversampling, Undersampling, SMOTE), hyperparameter tuning, and evaluating an **XGBoost Classifier** (Confusion Matrix, ROC-AUC, Feature Importance).
- **Business Insights & Recommendations**: translating model findings (e.g., seasonal concentration of delays in Autumn/Summer, high-delay months like March) into actionable operational recommendations, along with study limitations.

##  How to Run

1. Clone/download the project and open `Capstone_Model_2__Analysis.ipynb` in Jupyter Notebook / JupyterLab / VS Code.
2. Place the `.env` file (containing the `NEON_DATABASE_URL` database connection string) in the same folder as the notebook — it will be loaded automatically.
3. Install the required libraries (see below).
4. Run the notebook cells sequentially from top to bottom.

##  Requirements / Libraries

- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `plotly`
- `sqlalchemy`
- `psycopg2`
- `python-dotenv`
- `scikit-learn`
- `imbalanced-learn` (imblearn)
- `xgboost`
- `joblib`

Install them with:
```bash
pip install pandas numpy matplotlib seaborn plotly sqlalchemy psycopg2-binary python-dotenv scikit-learn imbalanced-learn xgboost joblib
```
