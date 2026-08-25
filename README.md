
Banking Customer Churn Analysis (SQL + Python)

End-to-end churn analysis on a banking dataset — pulling data from a SQLite database with SQL, cleaning and merging it with pandas, engineering a churn flag, and visualizing churn drivers with matplotlib and seaborn.

📌 Project Overview

This project analyzes customer, account, card, and transaction data from a banking SQLite database to understand churn behavior and its relationship with key variables such as card type, account balance, and credit score.

Key steps covered:

Connecting to a SQLite database and querying tables with SQL
Cleaning and transforming data with pandas (renaming columns, fixing dtypes, handling missing values)
Merging multiple tables (accounts, transactions, cards, customers)
Feature engineering a churn flag based on card expiration date
Calculating churn rate, revenue at risk, and correlations (churn vs. balance, churn vs. credit score)
Visualizing churn trends over time and by card type
Building a correlation heatmap and pairplot
Encoding and preparing data for further analysis

🛠️ Tech Stack
Python: pandas, numpy
Database: SQLite (via sqlite3)
Visualization: matplotlib, seaborn
Environment: Jupyter Notebook

📂 Repository Structure
├── sql_python_project.ipynb   # Main analysis notebook
├── README.md                  # Project documentation
└── data/                      # (not included — see Data section below)
📊 Dataset

The project uses a banking dataset (bank_sqlite.db) with the following tables:

accounts — account-level details (balance, open date, account type)
customers — customer details (credit score, etc.)
cards — card details (card type, expiration date)
transactions — transaction-level records (amount, date, merchant)
merchants / branches — supporting reference tables

🔑 Key Analysis
Churn Rate: overall percentage of churned cards/accounts
Churn by Card Type: which card types churn more
Revenue at Risk: share of total transaction revenue tied to churned accounts
Correlation Analysis: churn vs. transaction amount, balance, and credit score
Churn Trend Over Time: monthly churn pattern
Multivariate View: catplot/facet grid across account type, card type, and credit score

🚀 How to Run
Clone the repository:
bash
   git clone https://github.com/<your-username>/<repo-name>.git
   cd <repo-name>
Install dependencies:
bash
   pip install pandas numpy matplotlib seaborn jupyter
Place the SQLite database file (bank_sqlite.db) in the path referenced in the notebook, or update the sqlite3.connect(...) path in the first few cells to match your local setup.
Launch Jupyter and run the notebook:
bash jupyter notebook sql_python_project.ipynb
   
📈 Sample Visualizations
Churn trend line chart (monthly)
Churn rate bar chart by card type
Correlation heatmap (seaborn + matplotlib)
Pairplot of numeric features
Catplot: churn by account type, card type, and credit score

📝 Future Improvements
Automate the SQL → pandas pipeline into reusable functions/scripts
Add a proper churn prediction model (e.g. logistic regression / random forest) on top of the current EDA
Parameterize the database path via a config file instead of a hardcoded local path
