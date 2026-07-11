# Shauryansh_week_4-assignment
WEEK 4 ASSIGNMENT ( Azure Cloud Fundamentals and Data Pipeline Implementation using ADF )
# Azure Cloud Fundamentals and Data Pipeline Implementation using ADF

## 👤 Student Information
* **Name:** Shauryansh chauhan
* **Course:** B.Tech Computer Science & Engineering
* **Roll No:** 11232836
* **Institution:** MMDU
* **Program:** Celebal Summer Internship 2026 (Week 4 Assignment)

---

## 🚀 Project Objective
The objective of this project is to understand core Azure cloud concepts and construct an end-to-end data validation and orchestration pipeline using **Azure Storage Accounts** and **Azure Data Factory (ADF)**. The pipeline checks for the existence of an incoming dataset and securely copies it over to a target destination container upon successful validation.

---

## 🏗️ Pipeline Architecture & Workflow
1. **Source Storage:** A flat CSV file uploaded into an Azure Blob Storage container (`input-data`).
2. **Metadata Validation:** ADF uses a `Get Metadata` activity to verify the presence of the source file.
3. **Secure Execution:** Authentication is entirely handled securely via a `System Assigned Managed Identity` using RBAC permissions (`Storage Blob Data Contributor`).
4. **Data Ingestion:** Upon a successful metadata verification check, a `Copy Data` activity routes the dataset directly into a destination container (`output-data`).

---

## 🛠️ Step-by-Step Implementation Details

### Phase 1: Foundation & Storage Setup
* **Resource Group Created:** `rg-data-pipeline-lab` (Region: `East US`)
* **Storage Account Provisioned:** `storagepipelinelab2026`
* **Blob Containers Configured:**
  * `input-data` (Contains the raw source CSV)
  * `output-data` (Target landing directory)

### Phase 2: Security & Identity Access Management (IAM)
* Configured Role-Based Access Control (RBAC) on the storage account.
* Assigned the **Storage Blob Data Contributor** role to the Azure Data Factory instances' System Assigned Managed Identity to eliminate hardcoded credentials or connection strings.

### Phase 3: Azure Data Factory (ADF) Setup
* Provisioned an ADF instance named `adf-pipeline-lab`.
* Explored and utilized core ADF components:
  * **Author Tab:** Canvas for compiling data components.
  * **Monitor Tab:** Interface for managing and viewing execution logs.
  * **Manage Tab:** Interface for building linked infrastructure.

### Phase 4: Linked Services & Datasets
* **Linked Service:** Created `LS_AzureBlobStorage` using Managed Identity authentication.
* **Datasets:**
  * Source Dataset: `DS_Input_CSV` pointing towards `input-data/`
  * Destination Dataset: `DS_Output_CSV` pointing towards `output-data/`

### Phase 5: Pipeline Orchestration & Architecture
* Created pipeline `PL_EndToEnd_Data_Copy`.
* **Get Metadata Activity:** Linked to `DS_Input_CSV` configuration checking parameters for `Item name` and `Exists`.
* **Copy Data Activity:** Connected sequentially downstream of the Metadata activity via a **Success Dependency (Green box)**. Source mapped to `DS_Input_CSV` and Sink mapped to `DS_Output_CSV`.

---

## 📊 Execution & Verification Results
* The orchestration was executed using the **Debug** trigger workflow inside ADF Studio.
* **Get Metadata** ran successfully, establishing that the file exists.
* **Copy Data** fired sequentially afterward, transferring the CSV data streams.
* Final deployment checks inside the Azure Portal confirmed the dynamic arrival of the data inside the `output-data` container.

## 📄 License
This project is completed as part of academic internship work and is open for educational evaluation.
