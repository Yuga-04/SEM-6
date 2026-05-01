# Explain in Detail about the FP-Growth Algorithm with Suitable Example

## Introduction

The **FP-Growth (Frequent Pattern Growth) Algorithm** is an efficient method used in **Association Rule Mining** to discover frequent itemsets from large transactional databases.

Unlike the Apriori algorithm, FP-Growth does not generate candidate itemsets repeatedly. Instead, it compresses the database into a compact structure called an **FP-Tree (Frequent Pattern Tree)** and mines the frequent patterns directly from the tree. 

FP-Growth uses a **divide-and-conquer strategy**, making it faster and more efficient than Apriori for large datasets.

---

# Definition of FP-Growth Algorithm

The FP-Growth algorithm:

* Compresses the database into an FP-tree.
* Stores important association information in compact form.
* Mines frequent patterns without candidate generation. 

---

# Need for FP-Growth Algorithm

Apriori algorithm has some disadvantages:

* Requires multiple database scans.
* Generates huge candidate itemsets.
* High computational cost for large databases.

To overcome these problems, FP-Growth was introduced.

---

# Features of FP-Growth Algorithm

1. Avoids candidate generation.
2. Uses compressed FP-tree structure.
3. Requires fewer database scans.
4. Faster than Apriori for large databases.
5. Efficient for dense datasets.

---

# Basic Concepts

## Frequent Pattern

A frequent pattern is a set of items that appears frequently in the transaction database.

Example:

```text id="9a2j7n"
{Milk, Bread}
```

If this combination appears many times, it becomes a frequent itemset.

---

# FP-Tree (Frequent Pattern Tree)

An FP-tree is a compact tree structure used to store transaction information.

It contains:

* Root node labeled as “null”
* Item nodes
* Support counts
* Links between similar items

---

# Steps in FP-Growth Algorithm

The FP-Growth algorithm works in two major phases:

1. Construction of FP-tree
2. Mining frequent patterns from FP-tree

---

# Algorithm Procedure

## Step 1: Scan Database

Scan the transaction database and find support count of each item.

Remove infrequent items whose support is less than minimum support.

---

## Step 2: Sort Frequent Items

Arrange frequent items in descending order of support count.

This ordered list is called:

```text id="u89h4g"
L
```

---

## Step 3: Construct FP-Tree

* Create root node labeled “null”.
* Insert transactions into the tree according to ordered frequent items.
* Shared prefixes use common branches.
* Increase count values for repeated paths.

---

## Step 4: Mine Frequent Patterns

* Construct conditional pattern bases.
* Build conditional FP-trees.
* Generate frequent itemsets recursively.

---

# Suitable Example

Consider the following transaction database.

| Transaction ID | Items          |
| -------------- | -------------- |
| T100           | I1, I2, I5     |
| T200           | I2, I4         |
| T300           | I2, I3         |
| T400           | I1, I2, I4     |
| T500           | I1, I3         |
| T600           | I2, I3         |
| T700           | I1, I3         |
| T800           | I1, I2, I3, I5 |
| T900           | I1, I2, I3     |

Assume:

```text id="g6y5jt"
Minimum Support Count = 2
```

---

# Step 1: Count Item Supports

| Item | Support Count |
| ---- | ------------- |
| I1   | 6             |
| I2   | 7             |
| I3   | 6             |
| I4   | 2             |
| I5   | 2             |

All items satisfy minimum support.

---

# Step 2: Sort Items in Descending Order

The frequent item list becomes:

```text id="i1k9u2"
L = {I2:7, I1:6, I3:6, I4:2, I5:2}
```

---

# Step 3: Construct FP-Tree

## First Transaction

Transaction:

```text id="u7g5ja"
T100 = {I1, I2, I5}
```

According to L order:

```text id="m6x2kd"
{I2, I1, I5}
```

Create branch:

```text id="7bw1xk"
null
 └── I2:1
      └── I1:1
           └── I5:1
```

---

## Second Transaction

Transaction:

```text id="8g3s1a"
T200 = {I2, I4}
```

Branch becomes:

```text id="d9u2hz"
null
 └── I2:2
      ├── I1:1
      │    └── I5:1
      └── I4:1
```

The count of I2 increases because prefix is shared.

---

## Continue for All Transactions

After inserting all transactions, the FP-tree is constructed.

The tree stores compressed transaction information efficiently.

---

# Mining Frequent Patterns

Frequent patterns are generated starting from the least frequent item.

---

# Conditional Pattern Base

## For Item I5

I5 appears in two branches:

```text id="u1f4wa"
<I2, I1, I5:1>
<I2, I1, I3, I5:1>
```

Prefix paths:

```text id="h4m2zs"
<I2, I1:1>
<I2, I1, I3:1>
```

These form the conditional pattern base for I5.

---

# Conditional FP-Tree for I5

The conditional FP-tree becomes:

```text id="6xq8op"
<I2:2, I1:2>
```

Generated frequent patterns:

```text id="jy9q1k"
{I2, I5:2}
{I1, I5:2}
{I2, I1, I5:2}
```

---

# Mining for I4

Conditional pattern base:

```text id="u4q7pl"
{I2, I1:1}
{I2:1}
```

Conditional FP-tree:

```text id="4n7jqa"
<I2:2>
```

Generated pattern:

```text id="wh8n2v"
{I2, I4:2}
```

---

# Mining for I3

Conditional pattern base:

```text id="5s8kdw"
{I2, I1:2}
{I2:2}
{I1:2}
```

Generated frequent patterns:

```text id="fc4j0v"
{I2, I3:4}
{I1, I3:4}
{I2, I1, I3:2}
```

---

# Advantages of FP-Growth Algorithm

1. Faster than Apriori.
2. No candidate generation.
3. Requires only two database scans.
4. Efficient memory usage due to compressed FP-tree.
5. Suitable for large databases.

---

# Disadvantages of FP-Growth Algorithm

1. FP-tree construction may become complex.
2. Difficult to implement compared to Apriori.
3. FP-tree may become large for sparse datasets.

---

# Applications of FP-Growth Algorithm

* Market Basket Analysis
* Recommendation Systems
* Web Usage Mining
* Medical Diagnosis
* Fraud Detection
* Customer Purchase Analysis

---

# Comparison Between Apriori and FP-Growth

| Apriori                      | FP-Growth                 |
| ---------------------------- | ------------------------- |
| Generates candidate itemsets | No candidate generation   |
| Multiple database scans      | Only two scans            |
| Slower for large datasets    | Faster for large datasets |
| High computation cost        | Efficient computation     |
| Uses join and prune          | Uses FP-tree              |

---

# Conclusion

The FP-Growth algorithm is an efficient frequent pattern mining technique that overcomes the limitations of the Apriori algorithm. It uses a compact FP-tree structure and mines frequent patterns without candidate generation. Due to its speed and efficiency, FP-Growth is widely used in association rule mining and market basket analysis. 
