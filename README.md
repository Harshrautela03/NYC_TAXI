Tech Stack
Azure Data Factory · ADLS Gen2 · Azure Databricks (PySpark) · Delta Lake · Power BI · Azure Key Vault

**Pipeline**
1.Ingestion — Data Factory pulls raw trip data into the Bronze layer (ADLS Gen2, Parquet)
2.Bronze → Silver — Databricks cleans, dedupes, and validates schema
3.Silver → Gold — Databricks aggregates into business-ready Delta tables
4.Reporting — Power BI connects directly to Gold layer
5.Security — Secrets in Key Vault, access scoped via RBAC
