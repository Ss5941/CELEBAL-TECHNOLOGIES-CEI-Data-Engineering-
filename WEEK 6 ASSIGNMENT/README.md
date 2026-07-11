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

