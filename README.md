# CELEBAL-TECHNOLOGIES-CEI-Data-Engineering-



## 📌 Intern Details
* **Name:** Shauryansh Chauhan 
* **Institution:** MMDU 
* **Course:** B.Tech Computer Science & Engineering
* **Role:** Data Engineer
* **Company Name:** Celebal Technologies

* # Celebal Summer Internship 2026 - Data Engineering Portfolio

This repository hosts the data engineering deliverables for Weeks 6 and 7 of the Celebal Summer Internship. The codebase transitions from core distributed big data querying with Apache Spark to structured single-node data cleaning pipelines built with Python Pandas.



---

## 📂 Project Structure & File Operations

### 📁 Week 6: Distributed Data Processing (Apache Spark)
* **`SHAURYANSH__WEEK_6_ASSIGNMENT.docx` (Core Theory)**
    * **Purpose:** Deep-dive documentation analyzing Spark's lazy computing engine architecture.
    * **Key Operations Explained:** * Distinguishes execution scopes between the **Driver Node** (orchestration and DAG building) and **Executors** (distributed computation workers).
        * Breaks down how the **Catalyst Optimizer** refructures query recipes before evaluation to prune unneeded data columns early.
        * Provides architectural comparisons between running jobs in *Client Mode* vs *Cluster Mode*.
* **`SHAURYANSH_WEEK_6_ASSIGNMENT.ipynb` (PySpark Notebook)**
    * **Purpose:** Practical notebook executing relational data transformations across distributed datasets within Databricks.
    * **Key Source Operations:** * Implements explicit schema validation using `StructType` configurations to parse file inputs safely.
        * Applies multi-conditional row filtering using PySpark `col()` configurations (e.g., extracting subset matrices matching specific regional and priority flags).
        * Demonstrates defensive data exploration commands by executing memory-capped `.show(5)` steps over system-draining `.collect()` tasks.

### 📁 Week 7: Structured Data Pipelines (Pandas)
* **`week_7_assignment.ipynb` (Data Cleaning & Feature Engineering)**
    * **Purpose:** An end-to-end Python file-processing script dedicated to validating, profiling, and parsing transactional data.
    * **Key Source Operations:**
        * **Ingestion & Encoding handling:** Safely processes raw comma-separated values using `encoding="latin1"` to eliminate corrupted character compilation breaks.
        * **Feature Engineering:** Augments the tabular matrix by synthesizing a new business intelligence metric:
            $$\text{total\_amount} = \text{Sales} \times \text{Quantity}$$
        * **Data Export Pipeline:** Concludes by serializing the memory dataframe object using `.to_csv()`, saving a cleansed, analysis-ready backup copy directly back into the system environment storage path.

---

## 🛠️ Tooling & Tech Stack
* **Languages:** Python (v3.x)
* **Big Data Framework:** Apache Spark / PySpark (Spark SQL)
* **Data Science Libraries:** Pandas, Core Python Audio/OS Toolkits
* **Work Environments:** Databricks Notebook Environment, Jupyter Notebook

---

## 🚀 Execution & Setup Notes

1.  **Distributed Notebooks (Week 6):** Import the Spark `.ipynb` file directly into your **Databricks Community Edition** cloud engine or target Spark-enabled cluster instance. Ensure your data path coordinates are pointed properly to your target distributed storage layer.
2.  **Local Pipelines (Week 7):** Ensure local packages are up to date before launching:
    ```bash
    pip install pandas jupyter
    ```
    Place your raw data files (`superstore_dataset.csv`) within the specified context directory and open via local Jupyter server workspace.
