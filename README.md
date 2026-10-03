# 🛍️ Retail Business Performance & Profitability Analysis

An end-to-end **Data Analytics project** focused on analyzing retail sales, profitability, product performance, regional performance, and inventory behavior using **Python, MySQL, and Tableau**.

The project transforms raw sales, purchase, product, and store-level data into meaningful business insights and an interactive Tableau dashboard.

---

## 📌 Project Overview

Retail businesses generate large amounts of transactional data, but raw data alone does not help management make better decisions.

The objective of this project is to analyze retail business performance and answer important questions related to:

- Revenue performance
- Product category performance
- Regional and store performance
- Profitability
- Sales trends
- Inventory movement
- Sell-through rate
- Product demand
- Inventory holding period
- Relationship between inventory and profit margin

The analysis follows a complete workflow from **data exploration and cleaning to SQL analysis, Python analysis, business reporting, and Tableau visualization**.

---

## 🎯 Project Objectives

The main objectives of this project are to:

- Analyze overall retail sales performance.
- Identify high-performing product categories.
- Compare revenue across stores and regions.
- Analyze occasion-wise and material-wise performance.
- Calculate estimated product cost and profitability.
- Analyze inventory movement and remaining stock.
- Calculate sell-through rate.
- Study monthly sales trends.
- Examine the relationship between inventory holding time and profitability.
- Build an interactive Tableau dashboard for business decision-making.

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|---|---|
| **Python** | Data cleaning, transformation and exploratory analysis |
| **Pandas** | Data manipulation and dataset merging |
| **NumPy** | Numerical operations |
| **Matplotlib** | Data visualization |
| **Seaborn** | Exploratory visualization support |
| **MySQL / SQL** | Business queries and KPI analysis |
| **Tableau** | Interactive dashboard development |
| **Jupyter Notebook** | Python analysis environment |
| **CSV** | Raw data storage |

---

## 📂 Project Structure

```text
Retail Business Analysis/
│
├── DATA/
│   ├── data_dictionary.csv
│   ├── products.csv
│   ├── purchase_data.csv
│   ├── sales_data.csv
│   └── store_regions.csv
│
├── PYTHON ANALYSIS/
│   └── 01 Data Exploration.ipynb
│
├── SQL ANALYSIS/
│   └── retail_sales_analysis.sql
│
├── TABLEAU DASHBOARD/
│   └── Retail_Business_Performance.twbx
│
├── Project Report/
│   └── 2 Page Report.pdf
│
└── Project Presentation/
    └── Retail Business Performance Presentation.pptx
```

---

# 📊 Dataset Description

The project uses multiple datasets that together describe products, purchases, sales, stores, and regions.

### 1. `sales_data.csv`

Contains retail sales transactions.

Important fields include:

- Product ID
- Order ID
- Units Sold
- Sales
- Sale Date
- Store
- Region

The dataset contains approximately **1,490 sales records**.

---

### 2. `purchase_data.csv`

Contains product purchase and inventory information.

Important fields:

- Product ID
- Unit Cost
- Unit Price
- Inbound Inventory
- Purchase Date
- Store
- Region

---

### 3. `products.csv`

Contains product-level information.

Important fields:

- Product ID
- Product Category
- Occasion
- Material
- Karigari
- Karigari Description
- Product Description

---

### 4. `store_regions.csv`

Maps stores with their respective geographical regions.

Regions include:

- North
- South
- East
- West

---

### 5. `data_dictionary.csv`

Provides definitions and descriptions of important columns used throughout the datasets.

---

# 🐍 Python Analysis

Python was used for data exploration, preparation, merging, profitability calculations, and inventory analysis.

The analysis is available in:

```text
PYTHON ANALYSIS/01 Data Exploration.ipynb
```

## Python Workflow

### 1. Data Loading

The datasets were imported using Pandas.

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
```

---

### 2. Data Exploration

The datasets were inspected using:

```python
df.head()
df.info()
df.shape
df.columns
```

This helped understand:

- Dataset size
- Column names
- Data types
- Dataset structure

---

### 3. Data Quality Checks

The analysis checks for:

- Missing values
- Duplicate records
- Incorrect data types
- Date formatting

Sale and purchase dates were converted into proper datetime formats.

---

### 4. Data Merging

Sales data was merged with product information using:

```text
Productid
```

Purchase data was aggregated at:

```text
Productid + Store + Region
```

The aggregated purchase information was then merged with sales data to create a master analytical dataset.

---

# 💰 Profitability Analysis

Estimated product cost was calculated as:

```text
Estimated Cost = Units Sold × Average Unit Cost
```

Estimated profit was calculated as:

```text
Estimated Profit = Sales − Estimated Cost
```

Profit Margin Percentage:

```text
Profit Margin % =
Estimated Profit / Sales × 100
```

These calculations allow products to be evaluated based on profitability rather than sales revenue alone.

---

# 📦 Inventory Analysis

The project also evaluates inventory performance.

## Remaining Inventory

```text
Remaining Inventory =
Inbound Inventory − Units Sold
```

---

## Sell-Through Rate

```text
Sell-Through Rate (%) =
Units Sold / Inbound Inventory × 100
```

Sell-through rate helps measure how efficiently purchased inventory is converted into sales.

---

## Average Daily Units Sold

```text
Average Daily Units Sold =
Units Sold / Sales Period Days
```

---

## Estimated Inventory Days

```text
Estimated Inventory Days =
Remaining Inventory / Average Daily Units Sold
```

This provides an estimate of how long the remaining inventory could last based on historical sales velocity.

---

# 🔎 SQL Analysis

The SQL analysis is available in:

```text
SQL ANALYSIS/retail_sales_analysis.sql
```

MySQL queries were used to perform structured business analysis.

The SQL analysis includes:

- Table structure validation
- Record count
- Data preview
- NULL value detection
- Duplicate analysis
- Date range analysis
- Numerical data validation
- Revenue analysis
- Units sold analysis
- Profitability analysis
- Category performance
- Occasion performance
- Region performance
- Store performance
- Product-level performance
- Monthly sales trends
- Material performance

---

## 📈 Important SQL Business Questions

The SQL analysis answers questions such as:

- Which product category generates the highest revenue?
- Which occasion generates the highest revenue?
- Which region performs best?
- Which store generates the most revenue?
- Which product generates the highest revenue?
- Which material generates the highest revenue?
- Which year generated the highest revenue?
- Which month generated the highest revenue?
- Which category and occasion combination performs best?
- Which region-category combination generates the most revenue?
- Which store-category combination performs best?
- Which store and occasion combination generates the most revenue?

---

# 📊 Tableau Dashboard

An interactive Tableau dashboard was developed to communicate the final results visually.

Dashboard file:

```text
TABLEAU DASHBOARD/Retail_Business_Performance.twbx
```

The dashboard contains analysis of:

- Total Revenue
- Units Sold
- Sales Records
- Profit
- Profit Margin
- Product Categories
- Regions
- Stores
- Occasions
- Monthly Revenue Trends
- Inventory Performance
- Product Performance

The dashboard allows users to quickly identify important business trends and compare performance across different dimensions.

---

# 📌 Key Business Insights

The complete analysis generated several important findings.

### 💵 Revenue

Approximately:

```text
₹668.12 Million
```

of retail revenue was analyzed.

---

### 📦 Units Sold

Approximately:

```text
19,029 Units
```

were sold across the analyzed transactions.

---

### 🧾 Sales Records

The sales dataset contains approximately:

```text
1,490 Records
```

---

### 👗 Product Category Performance

**Lehanga** generated the highest category revenue in the category analysis, making it one of the major contributors to overall business performance.

---

### 📦 Inventory vs Profitability

The correlation between:

```text
Estimated Inventory Days
```

and

```text
Profit Margin Percentage
```

was approximately:

```text
0.06
```

This represents a **very weak positive linear relationship**.

Therefore, inventory holding time alone does not strongly explain profitability in this dataset.

---

### 📈 Sell-Through Rate

Many Product–Store combinations achieved very high or even **100% sell-through rates**.

However, their profit margins varied significantly.

This indicates that:

```text
High Sales Volume ≠ High Profitability
```

Cost structure and product pricing must also be considered.

---

### ⚠️ Negative Profit Margins

Some Product–Store combinations generated negative estimated profit margins despite strong inventory movement.

Possible factors include:

- High purchasing cost
- Low selling price
- Pricing decisions
- Product-level cost structure

---

# 💡 Business Recommendations

Based on the analysis, businesses should evaluate products using multiple metrics instead of relying only on revenue.

### Recommended approach:

- Monitor **profit margin and revenue together**.
- Track inventory aging regularly.
- Identify products with strong demand and healthy margins.
- Review products with high sell-through but low profitability.
- Optimize purchasing decisions using historical demand.
- Review pricing strategies for products with negative margins.
- Compare product performance across regions and stores.
- Reduce unnecessary inventory accumulation.
- Use dashboards for continuous KPI monitoring.

---

# 📉 Important Analytical Finding

One of the major conclusions from the analysis is:

> Strong inventory movement does not automatically mean strong profitability.

Products may sell quickly while still producing low or negative margins due to high procurement costs or inappropriate pricing.

Therefore, management should consider:

```text
Demand + Revenue + Cost + Profit Margin + Inventory
```

together when making business decisions.

---

# 🔄 Project Workflow

```text
Raw Retail Data
       ↓
Data Exploration
       ↓
Data Cleaning
       ↓
Data Transformation
       ↓
Dataset Merging
       ↓
Profitability Calculations
       ↓
Inventory Analysis
       ↓
SQL Business Analysis
       ↓
Python Validation
       ↓
Tableau Dashboard
       ↓
Business Insights
       ↓
Recommendations
```

---

# 🚀 How to Run the Project

## Python Analysis

### Step 1

Clone or download the repository.

### Step 2

Install the required Python libraries:

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

### Step 3

Open Jupyter Notebook:

```bash
jupyter notebook
```

### Step 4

Open:

```text
PYTHON ANALYSIS/01 Data Exploration.ipynb
```

### Step 5

Update the CSV file paths in the notebook according to your local project directory before running the cells.

---

# 🗄️ Running the SQL Analysis

1. Open MySQL Workbench.
2. Create or select the retail analysis database.
3. Import the prepared retail analytical data.
4. Create/use the `retail_sales_master` table.
5. Open:

```text
SQL ANALYSIS/retail_sales_analysis.sql
```

6. Execute the queries sequentially.

---

# 📊 Opening the Tableau Dashboard

Install **Tableau Desktop** or another compatible Tableau application.

Open:

```text
TABLEAU DASHBOARD/Retail_Business_Performance.twbx
```

to explore the dashboard.

---

# 📑 Additional Project Deliverables

The repository also contains a final project report:

```text
Project Report/2 Page Report.pdf
```

and a presentation:

```text
Project Presentation/Retail Business Performance Presentation.pptx
```

These provide an executive-level overview of the methodology, results, insights, and recommendations.

---

# 🎓 Skills Demonstrated

This project demonstrates practical knowledge of:

- Data Analytics
- Exploratory Data Analysis
- Data Cleaning
- Data Transformation
- Data Validation
- Data Modeling
- SQL
- MySQL
- Python
- Pandas
- NumPy
- Matplotlib
- Tableau
- KPI Analysis
- Profitability Analysis
- Inventory Analysis
- Business Intelligence
- Dashboard Development
- Data Visualization
- Business Problem Solving
- Insight Generation

---

# ✅ Conclusion

This project demonstrates a complete **Retail Business Analytics workflow** using Python, SQL, and Tableau.

The analysis shows how transactional data can be converted into actionable business insights by combining revenue, profitability, product demand, regional performance, and inventory metrics.

One of the most important findings is that **high sales or fast inventory movement does not necessarily guarantee profitability**. Businesses should therefore evaluate sales performance alongside product cost, pricing, profit margin, and inventory efficiency.

The final dashboard provides management with an easy way to monitor business KPIs and support better data-driven decisions.

---
