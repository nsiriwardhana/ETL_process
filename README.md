# 🎵 Music Store Data Warehouse & ETL Project (Assignment 1 – Semester 1, 2025)

This repository contains the full implementation of a **Data Warehouse and ETL solution** developed as part of Assignment 1 for the Business Intelligence course (Semester 1, 2025).

## 📌 Project Overview

The goal of this project was to design and implement a dimensional data warehouse using **SQL Server**, and perform ETL processes using **SSIS** (SQL Server Integration Services). The dataset represents a **music store's sales system**, including customer, employee, track, and invoice data.

---

## 🧩 Components

### ✅ Data Warehouse (Star Schema)
- **Fact Table:**
  - `FactSales` – sales transactions including track, customer, date, etc.
- **Dimension Tables:**
  - `DimCustomer` (SCD Type 2 applied)
  - `DimEmployee`
  - `DimTrack`
  - `DimDate`

### ✅ ETL Process (SSIS)
- **Sources:**
  - CSV and SQL database tables
- **SSIS Packages:**
  - Dimension Loads
  - Fact Table Load
  - Accumulating Fact Table Update (for transaction completion time)

---

## 🔁 SCD Type 2 Handling

The project implements **Slowly Changing Dimensions (Type 2)** on the `DimCustomer` table to maintain historical changes in customer information such as `City`, `State`, and `Country`.

---

## 📊 Fact Table Enhancements

The fact table was extended to support business analysis:
- `accm_txn_create_time` – Timestamp when the transaction was created
- `accm_txn_complete_time` – Timestamp when it was completed
- `txn_process_time_hours` – Duration in hours between creation and completion

---



---

## 🛠️ Tools Used

- **SQL Server Management Studio (SSMS)**
- **SQL Server Integration Services (SSIS)**
- **Excel / Power BI** (for OLAP visualization)
- **SQL Server Analysis Services (SSAS)**

---



## 🧠 Learning Outcome

This project demonstrates practical knowledge in:
- Dimensional modeling (Star Schema)
- ETL development using SSIS
- Handling historical data with SCD Type 2
- OLAP operations with SSAS and Excel
- Business intelligence pipeline design

---

## 📮 Author

**Nipuni Siriwardhana**   
Data Warehouse & Business Intelligence – Assignment 1  
Semester 1 – 2025
