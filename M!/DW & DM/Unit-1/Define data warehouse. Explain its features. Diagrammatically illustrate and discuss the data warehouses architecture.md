Here is the **15-mark answer strictly from your PDF** with the **diagram reference page**.

---

# Define Data Warehouse. Explain its Features. Diagrammatically Illustrate and Discuss the Data Warehouse Architecture. (15 Marks)

## 1. Definition of Data Warehouse

A **Data Warehouse** is defined as a **subject-oriented, integrated, time-variant and non-volatile collection of data that supports management’s decision-making process.** 

Data warehousing refers to the **process of constructing and using data warehouses** to store and analyze large volumes of data collected from different sources. 

---

# 2. Features (Characteristics) of Data Warehouse

### 1. Subject-Oriented

A data warehouse is organized around **major subjects of the organization**, such as customer, supplier, product and sales.
It focuses on modeling and analysis of data for decision making rather than daily operations. 

### 2. Integrated

Data in the warehouse is collected from **multiple heterogeneous sources** such as relational databases, flat files and transaction systems.
Before loading into the warehouse, data is cleaned and transformed into a **consistent format**. 

### 3. Time-Variant

A data warehouse stores **historical data over a long period of time** (usually 5–10 years).
This helps in identifying **trends, patterns and forecasting future decisions**. 

### 4. Non-Volatile

Once the data is stored in the warehouse, it is **not frequently updated or deleted**.
The data is mainly used for **analysis and reporting**, not for transaction processing. 

---

# 3. Data Warehouse Architecture

A **Data Warehouse Architecture** describes the structure and components used to collect, store and analyze data.

The commonly used architecture is the **Three-Tier Data Warehouse Architecture**.

---

## Diagram: Three-Tier Data Warehouse Architecture



<img width="577" height="368" alt="image" src="https://github.com/user-attachments/assets/c6242408-4ef5-4796-87ba-971676628b78" />



---

# 4. Components of Data Warehouse Architecture

## 1. Bottom Tier

The **bottom tier** consists of the **data warehouse database server**, usually a relational database system.

Back-end tools are used to:

* Extract data from operational databases
* Clean and transform the data
* Load the data into the warehouse

Gateways such as **ODBC, OLEDB and JDBC** help client programs communicate with the database.

This tier also contains the **Metadata Repository**, which stores information about the warehouse data. 

---

## 2. Middle Tier

The **middle tier** contains the **OLAP Server**, which provides multidimensional analysis.

It can be implemented using:

* **ROLAP (Relational OLAP)** – Uses relational database systems.
* **MOLAP (Multidimensional OLAP)** – Uses multidimensional cube storage. 

The OLAP server performs operations such as:

* Aggregation
* Query processing
* Data analysis

---

## 3. Top Tier

The **top tier** is the **front-end layer** used by users.

It includes:

* Query tools
* Reporting tools
* Data analysis tools
* Data mining tools

These tools allow managers and analysts to **analyze data and support decision making**. 

---

# Conclusion

A **Data Warehouse** is an important system used for storing and analyzing large volumes of historical data.
Its **subject-oriented, integrated, time-variant and non-volatile characteristics** make it suitable for decision support systems.
The **three-tier architecture** helps efficiently manage data storage, processing and analysis.

---

✅ If you want, I can also give you the **exact exam-ready diagram your professor expects (very simple hand-draw version)** so you can **reproduce it quickly in the exam and score full marks.**
