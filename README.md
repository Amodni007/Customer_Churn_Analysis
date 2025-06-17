#  Customer Churn Analysis Project : Using Excel, SQL, and Python
This project explores customer churn behavior using a telecom dataset. The aim is to understand why customers leave and help businesses reduce churn. It combines Excel, SQL, and Python for a complete data analysis workflow.

## 📊 Tools Used
- **Excel**: Cleaning, PivotTables, Charts
- **SQL (SQLite)**: Query-based analysis
- **Python (Pandas, Seaborn, Sklearn)**: Visuals, heatmaps, modeling

  ## 🔍 Key Business Insights
- 📉 Month-to-month contracts have the **highest churn rate**
- 💳 Customers paying via **electronic check** churn more
- 📈 Customers with **longer tenure** are more likely to stay
- 📊 Features like **Tech Support**, **Internet Service**, and **Contract Type** are strong churn predictors

##  Excel Work : Data Cleaning + Basic EDA

- **Data Cleaning**:
  - Removed empty rows and duplicate entries
  - Fixed column formats (e.g., `TotalCharges` as numeric)
  - Saved clean versions in `.xlsx` and `.csv`

- **Exploratory Data Analysis (EDA)**:
  - Created PivotTables:
    - Churn by Gender
    - Churn by Contract Type
    - Churn by Payment Method
  - Added conditional formatting and grouped tenure

- **Data Visualization**:
  - Bar and pie charts to show churn trends
  - All charts moved to a `Charts` sheet in Excel

---

##  SQL Analysis : Querying the Cleaned Data

 Tool Used: [DB Browser for SQLite](https://sqlitebrowser.org/)

- **Imported the clean dataset** into a SQLite database as a table `telco_customers`
- **Explored data structure** using:
  ```sql
  SELECT * FROM telco_customers LIMIT 10;
  PRAGMA table_info(telco_customers);


 ## Python – Visualization + Optional Modeling
 Tool Used: Jupyter Notebook
 - **Data Loading and Inspection**:
  - Loaded cleaned CSV with `pandas`
  - Used `df.info()`, `df.describe()`, and null checks

- **Data Exploration**:
  - Analyzed churn percentages
  - Created crosstabs: Gender vs Churn, Contract vs Churn

- **Data Visualization** (with `matplotlib` & `seaborn`):
  - Count plots for churn by contract/payment method
  - Tenure distribution histogram
  - Correlation heatmap to identify relationships

- **(Optional) Logistic Regression Model**:
  - Built a basic model with `sklearn` to predict churn
  - Used `MonthlyCharges` and `Tenure` as predictors
  - Evaluated accuracy on a test set

- Saved analysis in: `churn_analysis.ipynb`



