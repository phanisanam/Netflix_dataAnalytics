
# 🎬 Netflix Data Engineering Project

## 🔹 Phase 1: Ingestion (Bronze Layer)
- Ingested raw Netflix dataset from **GitHub API** using **Azure Data Factory**.  
- Landed data in **Azure Data Lake (Bronze layer)** in JSON/CSV format.

## 🔹 Phase 2: Transformation (Silver Layer)
- Designed **parameterized modular notebooks** in Databricks to process data from Bronze → Silver.  
- Applied data cleaning:
  - Standardized column names & datatypes  
  - Removed duplicates & nulls  
  - Handled malformed records  
- Created an **automated workflow** in Databricks to trigger these notebooks for daily ingestion Using **AutoLoader**

## 🔹 Phase 3: Data Quality & Streaming with DLT
- Used **Delta Live Tables (DLT)** to enforce:
  - **Data Quality Rules** (constraints, expectations, validity checks)  
  - **Schema Enforcement**  
- Built **streaming tables** on top of Silver Delta tables to simulate real-time ingestion.  
- Performed **aggregations** (e.g., movie counts by genre, release year, ratings).  

## 🔹 Phase 4: Analytics (Gold Layer)
- Transformed curated Silver data into **business-ready Gold tables** using **DLT workflows**.  
- Aggregated and enriched data for downstream analytics.

## 🛠️ Tech Stack
- **Azure Data Factory** → Data ingestion  
- **Azure Data Lake (ADLS)** → Data storage (Bronze/Silver/Gold layers)
- **AutoLoader** - for Incremental data Loading 
- **Databricks Notebooks (PySpark)** → Data transformation  
- **Delta Lake** → Transactional storage  
- **Delta Live Tables (DLT)** → Data quality, streaming, and workflows

# 🏗️ Project Architecture

📦 netflix-data-pipeline

┣ 📂 notebooks

┃ ┣ 📜 ingest_bronze.py

┃ ┣ 📜 bronze_to_silver.py

┃ ┣ 📜 transformations_silver.py

┃ ┣ 📜 dlt_quality_pipeline.py

┃ ┗ 📜 silver_to_gold_dlt.py

┣ 📂 workflows

┃ ┣ 📜 bronze_to_silver_job.json
┃ ┗ 📜 dlt_gold_workflow.json

┣ 📜 README.md


