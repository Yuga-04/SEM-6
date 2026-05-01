Here is the **15-mark answer from your PDF notes** with **diagram page numbers**.

---

# Describe in Brief About Various Schemas in Multidimensional Data Model (15 Marks)

## Introduction

In a **data warehouse**, the **multidimensional data model** is used to organize data for analytical processing.
The most commonly used schemas in this model are:

1. Star Schema
2. Snowflake Schema
3. Fact Constellation Schema (Galaxy Schema) 

These schemas organize the relationship between **fact tables and dimension tables** to support efficient OLAP analysis.

---

# 1. Star Schema

The **Star Schema** is the most commonly used schema in data warehouse design.
It consists of a **large central fact table** that contains the main data and several **dimension tables** connected to it. The structure resembles a **star**, with dimension tables arranged around the central fact table. 

The **fact table** stores numerical measures such as sales amount, quantity, or profit.
The **dimension tables** store descriptive attributes related to the facts.

Each dimension is represented by **one table containing a set of attributes**. 

### Example

A **sales data warehouse** may contain:

Fact Table:

* Sales (sales amount, quantity)

Dimension Tables:

* Time
* Item
* Location
* Branch

### Simple Diagram

```
           Time
            |
Location — Sales Fact — Item
            |
          Branch
```

📄 **Diagram page in PDF:** Around **Page 6** (Star Schema figure).

---

# 2. Snowflake Schema

The **Snowflake Schema** is a variation of the star schema where **dimension tables are normalized into multiple related tables**. 

Because the dimension tables are divided into additional tables, the schema structure resembles a **snowflake**.

This normalization reduces **data redundancy** and saves storage space, but it increases the number of **joins required for queries**, which may reduce performance.

### Example

In the snowflake schema:

The **Item dimension** may be divided into:

Item Table

* Item key
* Item name
* Brand
* Type
* Supplier key

Supplier Table

* Supplier key
* Supplier type

Similarly, the **Location dimension** can be divided into **Location and City tables**. 

### Diagram

```
            Supplier
               |
Time      Item Table
   \         |
    \      Sales Fact
     \       |
      \   Location
           |
          City
```

📄 **Diagram page in PDF:** Around **Page 7**.

---

# 3. Fact Constellation Schema (Galaxy Schema)

A **Fact Constellation Schema** consists of **multiple fact tables that share dimension tables**.
It can be viewed as a **collection of star schemas** and is also called a **Galaxy Schema**. 

This schema is used when multiple business processes need to be analyzed together.

### Example

A data warehouse may contain:

Fact Tables:

* Sales
* Shipping

Both fact tables may share dimension tables such as:

* Time
* Item
* Location

### Diagram

```
           Time
            |
Item — Sales Fact — Location
            |
       Shipping Fact
```

📄 **Diagram page in PDF:** Around **Page 8**.

---

# Conclusion

The **multidimensional data model** uses schemas such as **Star, Snowflake and Fact Constellation** to organize warehouse data efficiently.

* **Star Schema** – Simple structure with one fact table and multiple dimension tables.
* **Snowflake Schema** – Normalized version of star schema.
* **Fact Constellation Schema** – Multiple fact tables sharing dimension tables.

These schemas help support **efficient OLAP analysis and decision making in data warehouses**. 

---

✅ If you want, I can also show you **the 3 diagrams exactly like in your PDF (almost identical to what teachers expect in exams)** so you can **draw them perfectly and score full marks.** 📊✍️
