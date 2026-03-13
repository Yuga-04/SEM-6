# Explain with Three-Tier Architecture Diagram and Give the Steps for Design and Construction of Data Warehouse (15 Marks)

## 1. Three-Tier Data Warehouse Architecture

A **Data Warehouse Architecture** defines the structure used to collect, store, and analyze data from different sources.
The commonly used architecture is the **Three-Tier Architecture**, which consists of:

1. Bottom Tier
2. Middle Tier
3. Top Tier 

---

## Diagram: Three-Tier Data Warehouse Architecture

```
                Top Tier
        --------------------------
        Query Tools
        Reporting Tools
        Data Mining Tools
        Analysis Tools
        --------------------------

                Middle Tier
        --------------------------
              OLAP Server
        (ROLAP / MOLAP Server)
        --------------------------

                Bottom Tier
        -----------------------------------------
        Data Warehouse Database Server
        ETL Tools (Extract, Transform, Load)
        Operational Databases / External Sources
        Metadata Repository
        -----------------------------------------
```

This architecture separates **data storage, processing and user interaction** into different layers.

---

# 2. Components of Three-Tier Architecture

## 1. Bottom Tier

The **bottom tier** is the **data warehouse database server**, which stores the warehouse data in a relational database system. 

Back-end tools and utilities are used to populate the warehouse. These tools perform:

* Data extraction
* Data cleaning
* Data transformation
* Data loading
* Data refresh

Data is extracted from **operational databases or external sources** using gateways such as:

* ODBC
* OLEDB
* JDBC

This tier also contains the **metadata repository**, which stores information about the structure and contents of the data warehouse. 

---

## 2. Middle Tier

The **middle tier** is the **OLAP server**, which provides multidimensional analysis of data. 

The OLAP server can be implemented using:

* **ROLAP (Relational OLAP)** – Uses relational databases to store data.
* **MOLAP (Multidimensional OLAP)** – Uses multidimensional cube structures for faster analysis.

This layer processes queries and performs data aggregation.

---

## 3. Top Tier

The **top tier** is the **front-end client layer** used by users to interact with the data warehouse. 

It includes tools such as:

* Query tools
* Reporting tools
* Data analysis tools
* Data mining tools

Managers, analysts and executives use these tools for **decision making and business analysis**.

---

# 3. Steps for Design and Construction of Data Warehouse

The design and construction of a data warehouse involve several important steps.

### 1. Define Business Requirements

Identify the **business objectives, users and information requirements** for decision making.

### 2. Design the Data Model

Create a **multidimensional data model** such as:

* Star schema
* Snowflake schema
* Fact constellation schema

### 3. Data Extraction

Collect data from **multiple heterogeneous sources** such as operational databases, files and external systems.

### 4. Data Cleaning

Detect errors and inconsistencies in data and **correct them to improve data quality**.

### 5. Data Transformation

Convert data into a **common format suitable for the warehouse**.

### 6. Data Loading

Load the transformed data into the **data warehouse database**.

### 7. Data Refresh

Update the warehouse periodically to **maintain current and historical data**.

### 8. Metadata Management

Store information about **data sources, transformations, schemas and data lineage** in the metadata repository.

---

# Conclusion

The **Three-Tier Data Warehouse Architecture** separates the system into **data storage, processing and user access layers**.
By following systematic steps such as **data extraction, cleaning, transformation and loading**, organizations can successfully design and construct a data warehouse to support effective decision making.

---
