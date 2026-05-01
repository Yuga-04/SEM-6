# Why is Outlier Mining Important? Explain Statistical-Based, Distance-Based and Deviation-Based Outlier Detection Approaches

## Introduction

Outlier mining is an important data mining task used to identify data objects that are significantly different from the remaining data objects. These abnormal objects are called **outliers**. 

Outliers may represent:

* Fraudulent activities
* Abnormal behavior
* Errors
* Rare events
* Important hidden patterns

Hence, detecting outliers is very useful in many real-world applications.

---

# Importance of Outlier Mining

Outlier mining is important because many exceptional data objects contain valuable information rather than simple noise. 

## Applications of Outlier Mining

### 1. Fraud Detection

Outlier mining helps identify unusual credit card transactions or banking activities that may indicate fraud.

### 2. Network Security

It detects abnormal network traffic and intrusion attempts.

### 3. Medical Analysis

It helps identify unusual medical responses or rare diseases.

### 4. Telecommunication Monitoring

Unusual call patterns can indicate misuse or illegal activities.

### 5. Customized Marketing

It identifies customers with extremely high or low spending behavior.

### 6. Crime Detection

It helps monitor suspicious activities in electronic commerce and security systems.



---

# Approaches to Outlier Detection

The major approaches are:

1. Statistical-Based Outlier Detection
2. Distance-Based Outlier Detection
3. Deviation-Based Outlier Detection

---

# 1. Statistical-Based Outlier Detection

## Definition

The statistical distribution-based approach assumes that the data follows a known probability distribution such as:

* Normal distribution
* Poisson distribution

Objects that deviate significantly from the expected distribution are treated as outliers. 

---

## Working Principle

* A statistical model is created for the data.
* Parameters such as mean and variance are calculated.
* A discordancy test is performed to identify abnormal values.

Two hypotheses are considered:

### Working Hypothesis (H)

All data objects belong to the same distribution.

### Alternative Hypothesis

Some objects belong to a different distribution and are treated as outliers.



---

## Types of Alternative Distributions

### 1. Inherent Alternative Distribution

All objects belong to another distribution model.

### 2. Mixture Alternative Distribution

Some values come from a different population.

### 3. Slippage Alternative Distribution

Most objects belong to the original distribution while a few values are shifted.

---

## Example

Consider the marks:

40, 42, 43, 45, 41, 95

The value **95** is far away from the mean and is treated as an outlier.

---

## Advantages

* Mathematically strong
* Effective for normally distributed data

## Disadvantages

* Requires knowledge of data distribution
* Difficult for complex datasets

---

# 2. Distance-Based Outlier Detection

## Definition

An object is considered an outlier if most other objects are located far away from it. 

This approach does not depend on any statistical distribution.

---

## Working Principle

For each object:

* Distance from neighboring objects is calculated.
* If fewer neighboring objects exist within a specified distance, the object becomes an outlier.

An object is a distance-based outlier if at least a fraction of the objects lie farther than a specified minimum distance from it. 

---

## Algorithms Used

### 1. Index-Based Algorithm

Uses indexing structures like R-trees and k-d trees.

### 2. Nested-Loop Algorithm

Compares objects using memory-efficient processing.

### 3. Cell-Based Algorithm

Partitions data into cells for faster processing.

---

## Example

Consider points:

(2,3), (3,4), (2,4), (3,3), (25,30)

The point **(25,30)** is far away from all other points and becomes an outlier.

---

## Advantages

* No need for statistical assumptions
* Suitable for multidimensional data

## Disadvantages

* Computationally expensive
* Performance decreases with high dimensions

---

# 3. Deviation-Based Outlier Detection

## Definition

Deviation-based outlier detection identifies objects that deviate from the normal characteristics of a dataset. 

Instead of using statistical tests or distance measures, it focuses on detecting deviations from patterns.

---

## Working Principle

* A normal behavior pattern is identified.
* Objects that do not fit the pattern are considered outliers.

---

## Techniques Used

### 1. Sequential Exception Technique

Objects are sequentially compared to identify deviations.

### 2. OLAP Data Cube Technique

Uses multidimensional analysis to identify abnormal patterns.

---

## Important Terms

### Exception Set

Smallest subset whose removal reduces dissimilarity.

### Dissimilarity Function

Measures how different objects are from one another.

### Cardinality Function

Counts the number of objects.

### Smoothing Factor

Measures reduction in dissimilarity after removing subsets.



---

## Example

Suppose most employees log in between 9 AM and 10 AM.

If one employee regularly logs in at 3 AM, the behavior deviates from the normal pattern and is considered an outlier.

---

# Comparison of Approaches

| Approach          | Basis                    | Advantage                        | Limitation                      |
| ----------------- | ------------------------ | -------------------------------- | ------------------------------- |
| Statistical-Based | Probability distribution | Accurate for known distributions | Requires distribution knowledge |
| Distance-Based    | Distance between objects | Simple and flexible              | Expensive for large data        |
| Deviation-Based   | Pattern deviation        | Detects behavioral anomalies     | Difficult pattern modeling      |

---

# Conclusion

Outlier mining is an essential data mining process used to detect abnormal and exceptional data objects. It is widely used in fraud detection, medical diagnosis, security monitoring, and business intelligence. Statistical-based, distance-based, and deviation-based approaches provide different methods for identifying outliers depending on the nature of the dataset and application requirements. 
