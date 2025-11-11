# SQL Server Lab Setup in Hyper-V
---
## 📘 Overview
This project demonstrates how to deploy a **SQL Server environment in Hyper-V** using a Windows Server 2025 virtual machine (VM). The lab covers the installation and setup of SQL Server and SQL Server Management Studio (SSMS), with the goal of creating and managing a database.
**Key Components**
- **VM1:** Windows Server 2025 (SQL Server 2022 Express)
- **SQL Server:** SQL Server 2022 Express (Database Engine)
- **SSMS:** SQL Server Management Studio (for database management)
- **Network:** Virtual Switch in Hyper-V
---
## 🧠 Learning Objectives
- Learn how to set up **SQL Server** on a virtual machine.
- Understand how to **create and manage databases** using SQL Server.
- Get hands-on with **SQL queries** to interact with data.
- Practice using **SQL Server Management Studio (SSMS)** for database management.
---
## ⚙️ Core Lab Setup
| Component | Purpose | Notes |
|------------|----------|-------|
| **Virtual Machine (VM)** | Running Windows Server 2025 | Host for SQL Server installation |
| **SQL Server 2022 Express** | Database Engine | Free version for local development |
| **SQL Server Management Studio (SSMS)** | Database Management Tool | Used to create, query, and manage databases |
| **Hyper-V** | Virtualization Platform | Simulating a server environment for SQL Server |
---
## 🧩 Key SQL Queries Demonstrated
| Query | Purpose | Result |
|-------|---------|--------|
| **Create Database** | Set up a new database | Creates a database named `CourtSystem` |
| **Create Table** | Define a table structure | Creates a `CourtCases` table for storing case data |
| **Insert Data** | Populate table with sample data | Adds records of court cases to the table |
| **Query Data** | Retrieve stored data | Fetches all rows from the `CourtCases` table |
| **Filter Open Cases** | Query specific data | Filters and shows only open cases |
---
## 🎨 Fun Step – “Data Insertion”
Before diving into queries, users insert some sample data (e.g., court cases) into the table. This helps in practicing the basic CRUD (Create, Read, Update, Delete) operations with SQL Server.
---
## 📸 Screenshots
| Image | Description |
|--------|-------------|
|<img width="461" height="158" alt="step1-createsrvvm" src="https://github.com/user-attachments/assets/c87dc7e9-3048-4263-81b2-53dec7b56555" /> | Windows Server Installation in Hyper-V |
| <img width="487" height="196" alt="step2-sqlsrv" src="https://github.com/user-attachments/assets/3e2b73a1-26aa-477f-b788-c0d1ec6d4328" />| SQL Server Installation in VM |
| <img width="916" height="368" alt="step3-ssms" src="https://github.com/user-attachments/assets/d5321bda-3ce7-4a06-bb12-516ff78a2d75" />| Install SQL Server Management Studio (SSMS) |
| <img width="481" height="511" alt="step4-connectsqlsrv" src="https://github.com/user-attachments/assets/ea5d7a44-3664-4af8-bd02-b96bcd03e817" />| Connect to SQL Server from SSMS|
| <img width="495" height="380" alt="stepx-createdb" src="https://github.com/user-attachments/assets/9a9e4628-d5d6-43a7-b2be-e4cbf204f5d0" />| Creating the `CourtSystem` database in SSMS |
| <img width="526" height="389" alt="stepx-usedb" src="https://github.com/user-attachments/assets/62fa0ede-d9fe-4317-b0ae-c5d73f799826" />| Use the `CourtSystem` database in SSMS |
| <img width="410" height="377" alt="stepx-createtable" src="https://github.com/user-attachments/assets/4869285c-919b-43b6-8763-e8ef12e692ca" />| Creating `CourtCases` table structure |
|<img width="498" height="393" alt="stepx-fakedata" src="https://github.com/user-attachments/assets/7e8fbf09-c604-4e4e-85e9-659bc9fa6a76" />| Inserting sample data into `CourtCases` table |
| <img width="892" height="866" alt="step5-querydata" src="https://github.com/user-attachments/assets/4df3f7f9-f428-4f2a-aad3-a0aa9f5fd5d0" />| Querying data from the `CourtCases` table |
| <img width="886" height="796" alt="step6-querydata" src="https://github.com/user-attachments/assets/c47ac48c-bafd-4a81-a6f6-5a84c3e71b09" />| Filtering open cases from the `CourtCases` table |
|<img width="336" height="377" alt="stepx-verify" src="https://github.com/user-attachments/assets/35f44fc0-1e07-4dd4-a9ca-eb7babdbe26c" />| Verifying `CourtSystem` database and tables in SSMS |
---
## 🧩 Technical Highlights
- Virtualized environment for SQL Server using **Hyper-V**.
- Hands-on with **SQL queries** to manage and interact with a database.
- Installation of **SQL Server 2022 Express** and **SQL Server Management Studio (SSMS)**.
- Creation and management of a simple database (`CourtSystem`) and table (`CourtCases`).
---
## 🏁 Results
| Checklist |
|--------------------------|
| ✅ SQL Server and SSMS installed on Windows Server 2025 VM |
| ✅ `CourtSystem` database and `CourtCases` table created |
| ✅ Sample data inserted and queried successfully |
| ✅ Open cases filtered and displayed |
| ✅ All resources deleted post-lab to avoid costs |
---
