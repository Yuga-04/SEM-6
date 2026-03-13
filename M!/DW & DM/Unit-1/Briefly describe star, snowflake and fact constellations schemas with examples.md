<img width="577" height="251" alt="image" src="https://github.com/user-attachments/assets/ba8b08cd-74ba-41ee-9cda-ef214b17bee9" />Here is the **15-mark answer taken from your PDF notes**.

---

# Briefly Describe Star, Snowflake and Fact Constellation Schemas with Examples (15 Marks)

## 1. Star Schema

The **Star Schema** is the most commonly used data warehouse schema.
It consists of a **central fact table** connected to multiple **dimension tables**. The schema structure resembles a **star shape**, where the fact table is at the center and dimension tables surround it. 

The **fact table** contains the main quantitative data (measures) such as sales amount, quantity, or profit.
The **dimension tables** contain descriptive attributes related to the facts.

In the star schema, each dimension is represented by **only one table**, and each table contains a set of attributes. 

### Example

In a **sales data warehouse**, the fact table may store sales data while dimension tables describe the related details.

Dimensions may include:

* Time
* Item
* Location
* Branch

Example attributes for the **location dimension**:
`Location key, Street, City, State/Province, Country`. 

### Simple Diagram


<img width="577" height="368" alt="image" src="https://github.com/user-attachments/assets/39baee0f-6e18-45bb-856c-33c8483018c9" />


---

# 2. Snowflake Schema

The **Snowflake Schema** is a variation of the star schema in which **dimension tables are normalized into multiple related tables**. 

Because the dimension tables are split into additional tables, the schema structure resembles a **snowflake shape**.

This normalization reduces redundancy and improves storage efficiency, but it increases the number of joins required during queries.

### Example

In a snowflake schema:

* The **Item dimension table** can be divided into:

  * Item table
  * Supplier table

For example:

Item table attributes:

* Item key
* Item name
* Brand
* Type
* Supplier key

Supplier table attributes:

* Supplier key
* Supplier type 

Similarly, the **location dimension** may be split into **Location and City tables**.

### Diagram


<img width="577" height="338" alt="image" src="https://github.com/user-attachments/assets/2659c919-ae55-4586-82b8-844d6646718f" />


Although snowflake schema **reduces redundancy**, it is **less popular than star schema** because queries require more joins. 

---

# 3. Fact Constellation Schema (Galaxy Schema)

A **Fact Constellation Schema** contains **multiple fact tables that share dimension tables**. 

It can be viewed as a **collection of multiple star schemas** and is also called a **Galaxy Schema**.

This schema is used when multiple business processes share common dimensions.

### Example

Consider a data warehouse that includes:

* **Sales fact table**
* **Shipping fact table**

Both fact tables may share dimension tables such as:

* Time
* Item
* Location

### Diagram


<img width="577" height="251" alt="image" src="https://github.com/user-attachments/assets/82b3993e-bab9-4a5b-b53f-680d581f886c" />


In this schema, **dimension tables are shared among multiple fact tables**, allowing analysis of multiple related processes. 

---

# Conclusion

Star, Snowflake and Fact Constellation schemas are **multidimensional data models used in data warehouses**.

* **Star Schema** – Simple structure with one fact table and several dimension tables.
* **Snowflake Schema** – Normalized version of star schema with multiple related dimension tables.
* **Fact Constellation Schema** – Multiple fact tables sharing dimension tables.

These schemas help organize large volumes of data and support **efficient OLAP analysis and decision making**.

---

✅ If you want, I can also give you **the exact diagram page number from your PDF** and **show the fastest way to draw all 3 diagrams in the exam in under 30 seconds.**
