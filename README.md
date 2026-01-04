🛍️ GCP Retailer Data Engineering Project
📌 Overview

GCP-RETAILER_PROJECT is an end-to-end data engineering pipeline built on Google Cloud Platform (GCP).
It ingests data from multiple sources (MySQL & API), processes it using Dataproc (PySpark), stores it in Google Cloud Storage (GCS), and transforms it into analytics-ready tables in BigQuery using a Bronze–Silver layered architecture orchestrated by Apache Airflow (Cloud Composer).

This project demonstrates real-world data engineering practices including incremental loads, SCD handling, schema evolution, orchestration, and cloud-native design.

🏗️ Architecture

MySQL / API Sources
        |
        v
Dataproc (PySpark Jobs)
        |
        v
GCS Landing Layer (Parquet / JSON)
        |
        v
BigQuery Bronze (External Tables)
        |
        v
BigQuery Silver (Cleaned, SCD, Analytics Ready)
        |
        v
Analytics / Reporting

🧰 Tech Stack

| Category        | Tools                           |
| --------------- | ------------------------------- |
| Cloud Platform  | Google Cloud Platform (GCP)     |
| Storage         | Google Cloud Storage (GCS)      |
| Processing      | Dataproc (PySpark)              |
| Orchestration   | Apache Airflow (Cloud Composer) |
| Data Warehouse  | BigQuery                        |
| Source Systems  | MySQL, REST API                 |
| CI/CD           | Cloud Build                     |
| Version Control | Git & GitHub                    |

📂 Project Structure
GCP-RETAILER_PROJECT
│
├── data
│   ├── Ingestion
│   │   ├── retailerMysqlToLanding.py
│   │   ├── supplierMysqlToLanding.py
│   │   └── customerReviews_API.py
│   │
│   ├── Configs
│   │   ├── retailer_config.csv
│   │   └── supplier_config.csv
│   │
│   ├── BO
│   │   ├── bronzeTable.sql
│   │   ├── silverTable.sql
│   │   └── goldTable.sql
│   │
│   └── DBs
│       ├── retailerdb.sql
│       └── supplierdb.sql
│
├── workflows
│   ├── pyspark_dag.py
│   └── bq_dag.py
│
├── utils
│   └── helper utilities
│
├── cloudbuild.yaml
├── .gitignore
└── README.md


👨‍💻 Author

Krish
Data Engineer | GCP | BigQuery | PySpark | Airflow

📎 GitHub: https://github.com/krishh24997


⭐ If you like this project

Give it a ⭐ and feel free to fork or contribute!


