# Explain the Data Mining Functionalities in Detail (15 Marks)

## Introduction

**Data mining functionalities** define the kinds of patterns or knowledge that can be discovered from large databases. These functionalities specify the type of analysis that can be performed in a data mining task. 

Data mining tasks are generally classified into two categories:

1. **Descriptive mining tasks** – describe general properties of data.
2. **Predictive mining tasks** – perform predictions using existing data. 

---

# 1. Concept/Class Description

Concept description describes the **general characteristics of data belonging to a particular class**.

It includes two forms:

## a) Data Characterization

Data characterization summarizes the **general characteristics or features of a target class of data**. 

The data related to the target class are collected using database queries and then summarized.

Example:
Analyzing characteristics of software products whose sales increased by 10% in the last year.

The results can be presented using:

* Tables
* Charts
* Data cubes
* Characteristic rules. 

---

## b) Data Discrimination

Data discrimination compares the **general features of a target class with those of other contrasting classes**. 

Example:
Comparing the characteristics of software products whose sales increased with those whose sales decreased.

The results are often represented using **discriminant rules**.

---

# 2. Mining Frequent Patterns, Associations and Correlations

Frequent patterns are **patterns that occur frequently in a dataset**. 

These include:

* Frequent itemsets
* Sequential patterns
* Structured patterns

Association rules reveal relationships among data items.

Example:

```
buys(X, “computer”) → buys(X, “software”)
```

This rule indicates that customers who buy computers are also likely to buy software.

Association rules are evaluated using measures such as:

* **Support**
* **Confidence**. 

---

# 3. Classification

Classification is the process of **finding a model that can predict the class label of objects whose class is unknown**. 

The model is built using **training data**, where class labels are known.

Common classification techniques include:

* Decision trees
* Neural networks
* Rule-based classifiers

📄 Diagram reference: **Decision tree classification – Page 43 (Figure 1.10)**.

Example:
Classifying emails as **spam or non-spam**.

---

# 4. Prediction

Prediction is used to **predict continuous numeric values** rather than class labels. 

Regression analysis is commonly used for prediction.

Example:

* Predicting **future sales revenue**
* Forecasting **stock market prices**.

---

# 5. Clustering

Clustering groups data objects into clusters such that:

* Objects in the **same cluster are highly similar**.
* Objects in **different clusters are dissimilar**. 

Unlike classification, clustering does **not require predefined class labels**.

Example:
Grouping customers based on their purchasing behavior.

📄 Diagram reference: **Cluster diagram – Page 47 (Figure 1.11)**.

---

# 6. Outlier Analysis

Outliers are **data objects that deviate significantly from the normal behavior of data**. 

Outlier detection is useful in applications such as:

* Fraud detection
* Intrusion detection
* Fault detection.

Example:
Identifying unusual credit card transactions.

---

# 7. Evolution Analysis

Evolution analysis studies **patterns and trends in data over time**. 

It includes:

* Time-series analysis
* Sequential pattern mining
* Periodicity analysis

Example:
Analyzing **stock market trends** or **seasonal sales patterns**.

---

# Conclusion

Data mining functionalities enable the discovery of useful patterns and knowledge from large datasets. Important functionalities include **concept description, association analysis, classification, prediction, clustering, outlier detection and evolution analysis**. These techniques help organizations analyze data and support effective decision making. 

---
