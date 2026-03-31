# Azure Data Factory Incremental Load Pipeline

## Project Overview

This project demonstrates an end-to-end **incremental data loading pipeline** built using **Azure Data Factory (ADF)**. The pipeline extracts data from an **Azure SQL Database** and loads it into **Azure Data Lake Storage Gen2 (ADLS Gen2)** efficiently using incremental loading techniques.

The solution ensures:

* Efficient data movement (only new/updated records)
* Automated scheduling
* Failure monitoring with alert notifications

---

## Architecture

**Source:** Azure SQL Database
**Orchestration:** Azure Data Factory
**Destination:** Azure Data Lake Storage Gen2

**Flow:**

1. Extract incremental data from SQL using watermark logic
2. Process and copy data via ADF pipeline
3. Store data in ADLS Gen2 (structured format)
4. Trigger runs on schedule
5. Send email alerts on failure

---

## Key Features

### Incremental Data Load

* Loads only new or updated records
* Reduces processing time and cost

### Scheduled Trigger

* Pipeline runs automatically based on defined schedule
* Eliminates manual intervention

### Failure Alert System

* Configured **email alerts** using ADF monitoring
* Immediate notification on pipeline failure

### Reusable & Scalable Design

* Parameterized datasets and pipelines
* Easily extendable to multiple tables

---


## Use Cases

* Data warehousing (Bronze → Silver ingestion)
* ETL/ELT pipelines
* Near real-time reporting
* Cost-efficient large data processing

---

## Technologies Used

* Azure Data Factory (ADF)
* Azure SQL Database
* Azure Data Lake Storage Gen2
* Azure Monitor

---

## Future Enhancements

* Add support for multiple tables dynamically
* Implement CDC (Change Data Capture)
* Integrate with Azure Databricks / Synapse
* Add logging framework for audit tracking

