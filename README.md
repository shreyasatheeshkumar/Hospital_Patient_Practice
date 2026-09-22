#  Hospital Patient Data Analysis — SQL Project

##  Project Overview

This project focuses on analyzing **hospital patient records using SQL**.

The dataset contains patient information such as demographics, diseases, health metrics, treatment costs, admission and discharge dates, and smoking status.

The project is designed to practice SQL concepts from **basic queries to advanced analytical queries**.

---

##  Objectives

* Analyze hospital patient records using SQL
* Perform demographic analysis
* Analyze disease distribution
* Calculate treatment costs and hospital revenue
* Analyze hospital stay duration
* Perform basic health analytics
* Practice SQL aggregation and grouping
* Use string and date functions
* Practice subqueries
* Use `CASE` statements
* Use window functions such as `RANK()`

---

##  Dataset

The main table used in this project is:

### `PatientRecords`

| Column        | Description               |
| ------------- | ------------------------- |
| PatientID     | Unique patient identifier |
| PatientName   | Patient name              |
| Gender        | Patient gender            |
| Age           | Patient age               |
| City          | Patient city              |
| Disease       | Diagnosed disease         |
| BloodPressure | Blood pressure value      |
| Cholesterol   | Cholesterol level         |
| BMI           | Body Mass Index           |
| SmokingStatus | Smoking status            |
| TreatmentCost | Treatment cost            |
| AdmissionDate | Hospital admission date   |
| DischargeDate | Hospital discharge date   |

## The SQL file creates the `PatientRecords` table and inserts **200 patient records**.

##  SQL Concepts Used

### Basic SQL

* `SELECT`
* `WHERE`
* `ORDER BY`
* `LIMIT`

### Aggregate Functions

* `COUNT()`
* `SUM()`
* `AVG()`
* `MAX()`
* `MIN()`

### Grouping

* `GROUP BY`
* `HAVING`

### String Functions

* `LIKE`
* `LENGTH()`
* `UPPER()`

### Date Functions

* `DATEDIFF()`
* `YEAR()`

### Advanced SQL

* Subqueries
* `CASE`
* Window Functions
* `RANK()`
* `PARTITION BY`

---

##  Analysis Sections

### 1. Patient Demographics

Analysis includes:

* Total number of patients
* Average patient age
* Male and female patient count
* Gender percentage
* Patient distribution by city
* Average age by city

### 2. Disease Analytics

Analysis includes:

* Patient count by disease
* Disease distribution
* Heart Disease patients
* Diabetes patients
* Hypertension percentage
* Average age by disease
* Disease distribution across cities

### 3. Financial Analytics

Analysis includes:

* Total treatment revenue
* Average treatment cost
* Maximum treatment cost
* Minimum treatment cost
* Revenue by disease
* Revenue by city
* Patients above average treatment cost

### 4. Hospital Stay Analytics

Analysis includes:

* Average hospital stay
* Maximum hospital stay
* Minimum hospital stay
* Longest-stay patient
* Average stay by disease
* Average stay by city
* Patients staying more than 10 days
* Patients staying less than 5 days

### 5. Health Analytics

Analysis includes:

* Average blood pressure
* Average cholesterol
* Average BMI
* Patients with high blood pressure
* Patients with high cholesterol
* Patients with BMI above 30
* Average health metrics by disease
* Smokers vs non-smokers

---

##  Sample SQL Queries

### Find Average Treatment Cost

```sql
SELECT AVG(TreatmentCost) AS Average_Treatment_Cost
FROM PatientRecords;
```

### Count Patients by Disease

```sql
SELECT Disease, COUNT(*) AS Total_Patients
FROM PatientRecords
GROUP BY Disease;
```

### Find Total Treatment Revenue

```sql
SELECT SUM(TreatmentCost) AS Total_Revenue
FROM PatientRecords;
```

### Find Longest Hospital Stay

```sql
SELECT
    PatientName,
    AdmissionDate,
    DischargeDate,
    DATEDIFF(DischargeDate, AdmissionDate) AS Stay_Days
FROM PatientRecords
ORDER BY Stay_Days DESC
LIMIT 1;
```

### Rank Patients by Treatment Cost

```sql
SELECT
    PatientName,
    TreatmentCost,
    RANK() OVER (
        ORDER BY TreatmentCost DESC
    ) AS Cost_Rank
FROM PatientRecords;
```

## These queries are part of the SQL practice and analytics sections in the project.

##  Key Skills Demonstrated

* SQL Data Analysis
* Data Aggregation
* Data Filtering
* Healthcare Data Analysis
* KPI Analysis
* Revenue Analysis
* Patient Analytics
* Date-Based Analysis
* Subqueries
* Window Functions
* Analytical Thinking

---

##  Project Structure

```text
Hospital-Patient-SQL-Analysis/
│
├── Hospital_Patient_Practice.sql
└── README.md
```

---

##  How to Run

1. Download or clone this repository.
2. Open the `.sql` file in MySQL Workbench or any compatible SQL environment.
3. Execute the database/table creation queries.
4. Insert the patient records.
5. Run the SQL practice queries.
6. Explore the results and perform further analysis.

---

##  Project Highlights

This project demonstrates how SQL can be used to transform raw hospital patient records into meaningful analytical insights.

It covers the complete journey from:

**Patient Data → SQL Queries → KPIs → Healthcare Analysis**

---
**Areas of Interest:**
SQL | Data Analytics | Python | Machine Learning | Generative AI
