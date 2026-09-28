
# Azure Global Supply Chain Data Platform

An end-to-end data engineering project demonstrating **Incremental Data Loading** and **Modular PySpark Architecture**. Built on Azure Databricks and orchestrated by Azure Data Factory, this project focuses on pipeline efficiency, DRY (Don't Repeat Yourself) code principles, and runtime optimization.

---

## 🎯 Key Technical Implementations

- **Reusable PySpark Modules:** Centralized ingestion, transformation, and validation logic into utility modules (`00_utils`) to promote code reusability and maintainability across the data platform.
- **Watermark-Based Incremental Loading:** Engineered a robust incremental load pattern using a control table to track high-water marks (timestamps), ensuring only new or updated supply chain records are extracted from source systems.
- **Adaptive Query Execution (AQE):** Leveraged Databricks Serverless AQE to dynamically optimize data enrichment joins, automatically handling potential data skew and coalescing partitions at runtime.
- **SIT / ETL Testing:** Implemented automated System Integration Testing (SIT), enforcing schema validation on ingestion and performing exact Source-to-Target count checks between Bronze and Silver layers to guarantee zero data loss.
- **Automated Orchestration:** Used Azure Data Factory to orchestrate Databricks Workflows, handling task dependencies across the Medallion architecture.

---

## 🛠 Tech Stack

| Category | Technology |
|---|---|
| Cloud & Compute | Azure Databricks (Serverless), PySpark |
| Storage | Azure Data Lake Storage Gen2 (ADLS Gen2), Delta Lake |
| Orchestration | Azure Data Factory, Databricks Workflows |
| Architecture | Medallion (Bronze/Silver), Watermarking, Modular Code |

---

## 📸 Pipeline Proofs of Execution

### ADF Orchestration Success
![ADF Run](proofs/1_adf_successful_run.png)

### Databricks Workflow & Task Dependencies
![Databricks Workflow](proofs/2_databricks_workflow.png)

### Incremental Load Logic (Skipping when no new data exists)
![Incremental Logic](proofs/3_incremental_skip_proof.png)

### SIT Count Check (Bronze vs Silver)
![SIT Check](proofs/4_sit_count_check_proof.png)

---

## 👤 Author
**Nitesh Choudhary**
Azure Data Engineer
[LinkedIn](#) | [Email](mailto:nitesh.choudhary@example.com)
