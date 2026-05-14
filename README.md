# Smart Claims Automation Platform

An end-to-end **Databricks Lakehouse** solution that automates car insurance claims processing by unifying data sources, applying AI-driven damage assessment, and enforcing business rules.

## 🚀 Overview
This project implements a **Medallion Architecture** (Bronze → Silver → Gold) to ingest and process data from SQL Server, Kinesis streams, and S3. It features a **Computer Vision model** to classify accident severity, a **rules engine** for automated approvals, and a custom **Databricks App** for customer submission and admin review.

## 🏗️ Architecture Highlights
- **Ingestion:** Lakeflow Connect (CDC from SQL Server), AutoLoader (S3 images), and Kinesis streaming (telematics).
- **Processing:** Declarative Pipelines with built-in data quality checks and schema evolution.
- **Machine Learning:** Fine-tuned ResNet model (MLflow) for image classification; deployed via Real-time Serving.
- **Consumption:** Databricks Apps (Streamlit + Lakebase for low latency), SQL Dashboards, and Genie (Natural Language Querying).

## 🔑 Key Features
- **Automated Claims Review:** Cross-references ML predictions, policy limits, and telematics speed to auto-approve or flag claims.
- **Unified Data Lake:** Single source of truth for customers, policies, claims, and telematics.
- **Real-time & Batch:** Seamless handling of streaming telematics and batch image processing.
- **Interactive Portal:** Customer-facing claim submission and Admin dashboard for investigation.

## 🛠️ Tech Stack
- **Core:** Databricks, Unity Catalog, Delta Lake
- **Ingestion:** Lakeflow Connect, AutoLoader, Kinesis
- **ML:** MLflow, PyTorch, Hugging Face, Model Serving
- **App:** Databricks Apps, Lakebase (PostgreSQL), Streamlit
- **Languages:** Python, SQL

## 📂 Project Structure
```text
├── ingestion/          # Lakeflow pipelines for SQL, Kinesis, S3
├── transformation/     # Bronze → Silver → Gold logic & data quality
├── ml/                 # Image classification training & MLflow tracking
├── rules/              # Business logic for claim approval
└── app/                # Databricks App code (Streamlit)
```

## 🚦 Getting Started
1. **Ingest Data:** Run Lakeflow pipelines to load raw data into the Bronze layer.
2. **Transform:** Execute Declarative Pipelines to clean data and build Gold tables.
3. **Train Model:** Run the ML notebook to fine-tune and register the damage classifier.
4. **Deploy:** Launch the Databricks App and connect the Model Serving endpoint.
5. **Analyze:** Use Genie or BI Dashboards to explore claims insights.

---
*Built with the latest Databricks Lakehouse functionalities for scalable, AI-driven data solutions.*
