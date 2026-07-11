
### 📁 Week 7: Structured Data Pipelines (Pandas)
* **`week_7_assignment.ipynb` (Data Cleaning & Feature Engineering)**
    * **Purpose:** An end-to-end Python file-processing script dedicated to validating, profiling, and parsing transactional data.
    * **Key Source Operations:**
        * **Ingestion & Encoding handling:** Safely processes raw comma-separated values using `encoding="latin1"` to eliminate corrupted character compilation breaks.
        * **Feature Engineering:** Augments the tabular matrix by synthesizing a new business intelligence metric:
            
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
