<img width="1467" height="1107" alt="image" src="https://github.com/user-attachments/assets/b17400f8-a108-444b-a845-ba36e4e4d535" /><img width="1613" height="216" alt="image" src="https://github.com/user-attachments/assets/ef7b2a44-f169-4005-9d92-d114de2d8754" /># SQL-TO-ADLS-INGESTION
An ETL/ELT framework using Azure Data Factory to migrate on-premise SQL Server relational data into ADLS Gen2. Includes Self-Hosted Integration Runtime (SHIR) configurations, parameterized pipelines for full/incremental loads, and Parquet file conversion.

**=========Project Overview===========**
* Modern organizations generate large volumes of operational data in on-premise systems. To enable scalable analytics and reporting, this data must be efficiently migrated to the cloud.

* This project demonstrates an end-to-end data engineering pipeline that extracts data from an On-Premise SQL Server, processes it using Azure Data Factory, and stores it in Azure Data Lake Storage Gen2. The pipeline implements a metadata-driven incremental loading strategy using a watermark table, ensuring that only new or updated records are processed.

**=========Project Architecture=======**
<img width="851" height="531" alt="image" src="https://github.com/user-attachments/assets/0a942fcd-f317-4a08-882a-904e3c54cf0b" />

**=========Data Warehouse Model========**
* Star Schema used for analytics
* Dimension Tables: DimCustomer, DimProduct, DimDate, DimRegion, DimStore etc.,,,
* Fact Tables: FactSales, FactOrders, FactPayments, FactReturns etc.,,
* Optimized for reporting and BI queries

**==========Data Warehouse Configuration======**
<img width="806" height="542" alt="image" src="https://github.com/user-attachments/assets/69c57930-3314-4f0f-9b8d-b0d6cdc998ea" />

**=========ADF Pipeline Logic=========**
* Lookup activity retrieves table metadata
* ForEach loop processes tables dynamically
* Condition checks if new records exist
* Copy activity loads data to ADLS





