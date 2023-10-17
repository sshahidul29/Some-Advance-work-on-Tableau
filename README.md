## Overview

This project aims to empower our Educational Institute client with data-driven insights and decision-making capabilities by providing a robust data infrastructure and actionable analytics. It involves integrating, cleaning, and structuring data, and creating the analytical model for informed decision-making.

## Enterprise Data Warehouse was built in MSSQL Server using SSMS

- Performed business requirement gathering, documentation and profiling of available data.
- Collaborated with the project team to identify and document source-to-target mapping. 
- Created Bus Matrix (composition of Business process, Granularity, Facts, Fact Tables, and Dimensions).
- Designed and implemented Enterprise Data Warehouse (EDW) using Ralph Kimball’s Dimensional Modelling Approach.
- Created and configured Staging, EDW, and Control Framework databases on MS SQL Server. 

  ![Tableau]()  
Figure 1: Class Attendance Star Schema

## ETL Pipeline was built in Visual Studio using SSIS

- The project aimed to create an ETL (Extract, Transform, Load) pipeline for data extraction, transformation, and loading into SQL Server Databases from the OLEDB source.
- Wrote ETL packages to extract, transform and load data from the OLTP database to Staging and staging to EDW Databases.
- Created a metric table for an audit of Source Count, and Destination Count Staging database, and Pre, Current, Post, Type1, and Type2 Counts for EDW using the Control framework database.
- Scheduled and monitored SQL Server Agent jobs to run ETL SSIS packages to move data.

  
   ![Class Attendance](https://github.com/sshahidul29/Building-an-Analytic-Environment-for-Class-Attendance-Management-Systems/blob/main/Figures/ClassETL3.PNG) 

 Figure 2: Control-flow diagram for ETL Pipeline

   ![Class Attendance](https://github.com/sshahidul29/Building-an-Analytic-Environment-for-Class-Attendance-Management-Systems/blob/main/Figures/ClassETL1.PNG) 

 Figure 3: Data-flow diagram of ETL Pipeline for Student dimension

  ![Class Attendance](https://github.com/sshahidul29/Building-an-Analytic-Environment-for-Class-Attendance-Management-Systems/blob/main/Figures/ClassETL2.PNG) 

Figure 4: Data-flow diagram for Incremental load of ETL Pipeline for FactClassAttendance

 ![Class Attendance](https://github.com/sshahidul29/Building-an-Analytic-Environment-for-Class-Attendance-Management-Systems/blob/main/Figures/ClassETL4.PNG) 

Figure 5: Control-flow diagram for ETL Pipeline to automate the system through SQL Server Agent
