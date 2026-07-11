# 🛒 Smart Metadata-Driven Retail Supply Chain Pipeline

## 📌 Project Overview

RetailPulse is an end-to-end Data Engineering project developed as part of a Summer Internship Program. This project implements the Medallion Architecture (Bronze, Silver, and Gold) to process retail supply chain datasets and generate meaningful business insights.

The pipeline processes five retail datasets (Orders, Inventory, Products, Stores, and Suppliers) to identify stock shortages, analyze sales performance, and generate business KPIs.

---

# 🎯 Objectives

- Build an end-to-end Data Engineering Pipeline.
- Implement Medallion Architecture (Bronze, Silver, Gold).
- Process retail supply chain datasets.
- Clean and validate raw data.
- Generate business KPIs.
- Analyze sales and inventory performance.

---

# 🛠️ Tech Stack

- Python
- PySpark
- Spark SQL
- Databricks Community Edition
- CSV Files

---

# 📂 Datasets Used

- orders.csv
- inventory.csv
- products.csv
- stores.csv
- suppliers.csv

---

# 🥉 Bronze Layer

The Bronze Layer loads raw CSV files without modifying the original data.

### Operations Performed

- Read Orders Dataset
- Read Inventory Dataset
- Read Products Dataset
- Read Stores Dataset
- Read Suppliers Dataset

---

# 🥈 Silver Layer

The Silver Layer performs data cleaning and transformation.

### Operations Performed

- Removed Null Values
- Removed Duplicate Records
- Calculated Total Sales Value
- Added Low Stock Flag
- Prepared Clean Data for Analytics

---

# 🥇 Gold Layer

The Gold Layer generates business insights using Spark SQL.

### KPIs Generated

- Low Stock Alerts
- Daily Sales Summary
- Top Selling Products
- Store Performance Analysis

---

# 📊 Business Problems Solved

- Stock Shortages (Stockouts)
- Overstocking
- Demand Visibility
- Retail Sales Analysis
- Inventory Monitoring

---

# 🔄 Pipeline Workflow

Raw CSV Files
        ↓
Bronze Layer
        ↓
Silver Layer
        ↓
Gold Layer
        ↓
Business Insights & Reports

---

# 📈 Features

- End-to-End Data Pipeline
- Medallion Architecture
- PySpark Data Processing
- Spark SQL Analytics
- Data Cleaning
- KPI Generation
- Retail Supply Chain Analytics

---

# 📁 Project Structure

```
Final-Project/
│── final project.ipynb
│── README.md
│── data/
│   ├── orders.csv
│   ├── inventory.csv
│   ├── products.csv
│   ├── stores.csv
│   └── suppliers.csv
│
└── outputs/
```

---

# 🚀 How to Run

1. Open Databricks Community Edition.
2. Upload all datasets.
3. Import the notebook.
4. Run the notebook from the first cell to the last cell.
5. View the generated KPIs and visualizations.

---

# 📌 Results

The project successfully generates:

- Low Stock Alerts
- Daily Sales Summary
- Top Selling Products
- Store Performance Report

These outputs help businesses monitor inventory, analyze sales trends, and improve decision-making.

---

# 👨‍💻 Author

Shauryansh Chauhan .

college = MMDU.

Celebal Internship Project.

Role = - Data Engineer
