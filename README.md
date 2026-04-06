# AdventureWorks-Azure-ETL-Project
Build a complete Azure ETL pipeline: extract on-prem SQL Server data, transform with Databricks, model in Synapse, and create dashboards in Power BI.

# End-to-End Data Engineering Pipeline using Azure & Databricks

## 📌 Overview
I have created this project and published it on my YouTube Channel : www.youtube.com/@DataToCrunch .

<img width="1921" height="1078" alt="image" src="https://github.com/user-attachments/assets/a9facbc5-4358-42d4-b3be-a531ff007d8c" />

This project demonstrates a real-world, production-style data pipeline built using **Azure services** and **Databricks**, based on the **AdventureWorks2019 SQL Server database**.  

<img width="1918" height="1068" alt="image" src="https://github.com/user-attachments/assets/0e06231d-e253-4067-b273-566d28260637" />


The pipeline simulates enterprise ingestion patterns by sourcing data from an on-prem SQL Server, moving it to Azure, and processing it through a **Medallion Architecture**, culminating in interactive **Power BI dashboards**.

---

## 🏗️ Architecture

On-Prem SQL Server → Azure Data Factory → ADLS (Bronze) → Databricks (Silver & Gold) → Azure Synapse Analytics → Power BI

<img width="1657" height="1154" alt="image" src="https://github.com/user-attachments/assets/4430c52b-a5b4-444f-8f01-e66966aae611" />


---

## ⚙️ Tech Stack

- SQL Server 2019 + SSMS  
- Azure Data Factory (ADF)  
- Azure Data Lake Storage Gen2 (ADLS)  
- Azure Key Vault  
- Azure Databricks (PySpark)  
- Delta Lake  
- Azure Synapse Analytics  
- Power BI  

---

## 🔄 Pipeline Flow

### 🔹 Data Source
- Dataset: AdventureWorks2019 (SQL Server sample database)  
- Hosted on-prem or local SQL Server

### 🔹 Ingestion (ADF)
- ADF pipelines connect to on-prem SQL Server via **Self-hosted Integration Runtime**  
- Dynamically copies multiple tables  
- Stores raw data in ADLS **Bronze layer**

<img width="2167" height="1014" alt="image" src="https://github.com/user-attachments/assets/69ced15d-5d56-4e24-bf91-b9440a23cf89" />


### 🔹 Bronze Layer
- Raw, unprocessed data  
- Stored in **Delta format**  
- Append-only ingestion

### 🔹 Silver Layer
- Data cleaning and transformation in **Databricks**  
- Deduplication and schema enforcement

### 🔹 Gold Layer
- Business-level aggregations  
- Analytics-ready datasets  
- Exposed via **Synapse Views & External Tables**

### 🔹 Visualization
- Power BI dashboards connected to Gold layer for reporting

---

## 🚀 Key Features

- End-to-end **Azure-based ETL pipeline**  
- Secure connection from on-prem SQL to cloud (ADF + Integration Runtime)  
- Medallion architecture (Bronze, Silver, Gold)  
- Delta Lake MERGE operations for upserts  
- Modular, scalable, production-ready design

---

## ▶️ How to Run
- Restore & explore the AdventureWorks2019 SQL Server database
- Connect ADF to on-prem SQL using Self-hosted Integration Runtime
- Use Azure Data Factory to dynamically copy multiple tables
- Store data in ADLS Gen2 using the Bronze, Silver, Gold layers
- Use Azure Key Vault for secure secret management
- Transform data using Azure Databricks
- Views & External Tables creation using Azure Synapse Analytics
- Create stunning dashboards in Power BI

---

## 🎥 YouTube Walkthrough
https://youtu.be/XYQU5ZMuMuE?si=cnu81JOI8gi_puK_

---

## 📌 Dataset 
https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbmM0SmtudFg1RUZ0RG8ya0F2S0xyMzM1Z0tTZ3xBQ3Jtc0ttU0VkY0VBNU5Ha3F2N0lBVDNFeFRIUXhJMW94cGZzOWRnN2gtY1BpaDZmUWQ2RGluemJaT1p6cWRtaHpSTDF0Y3pEdXhEQzVLTGlGazdwM2dra2dSZlBCVFN1UGtXT2NWV1lDb1JFRlRNclBaMkk5bw&q=https%3A%2F%2Flearn.microsoft.com%2Fen-us%2Fsql%2Fsamples%2Fadventureworks-install-configure%3Fview%3Dsql-server-ver16%26tabs%3Dssms&v=XYQU5ZMuMuE
