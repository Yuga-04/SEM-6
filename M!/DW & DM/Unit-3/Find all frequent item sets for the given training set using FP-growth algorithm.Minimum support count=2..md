<img width="725" height="304" alt="image" src="https://github.com/user-attachments/assets/f64ae59c-7863-44ee-8bce-6e1eb4ef0bea" />
# Find All Frequent Item Sets Using FP-Growth Algorithm

## Minimum Support Count = 2

---

# Given Transaction Database

| Transaction ID | Items                 |
| -------------- | --------------------- |
| T1             | Pen, Notebook, Eraser |
| T2             | Pen, Notebook         |
| T3             | Notebook, Eraser      |
| T4             | Pen, Marker           |
| T5             | Pen, Notebook, Eraser |

---

# Step 1: Find Support Count of Each Item

Count the occurrence of each item in all transactions.

| Item     | Support Count |
| -------- | ------------- |
| Pen      | 4             |
| Notebook | 4             |
| Eraser   | 3             |
| Marker   | 1             |

Minimum Support Count:

```text id="1ikj2s"
Min_Sup = 2
```

Remove infrequent items.

Since Marker has support count 1, it is removed.

---

# Frequent 1-Itemsets

```text id="8i4ksn"
L<sub>1</sub> =
{
{Pen},
{Notebook},
{Eraser}
}
```

---

# Step 2: Arrange Items in Descending Order of Support

Order frequent items according to support count.

```text id="v7s1qd"
Pen = 4
Notebook = 4
Eraser = 3
```

Ordered list:

```text id="4m5j3a"
L = {Pen, Notebook, Eraser}
```

---

# Step 3: Construct FP-Tree

Create root node:

```text id="1h4g7m"
NULL
```

---

# Insert Transaction T1

Transaction:

```text id="f8w2ka"
{Pen, Notebook, Eraser}
```

FP-Tree:

```text id="9p2sjd"
NULL
 └── Pen:1
      └── Notebook:1
           └── Eraser:1
```

---

# Insert Transaction T2

Transaction:

```text id="n7x5de"
{Pen, Notebook}
```

Common prefix exists.

Increase counts.

```text id="4g2kqm"
NULL
 └── Pen:2
      └── Notebook:2
           └── Eraser:1
```

---

# Insert Transaction T3

Transaction:

```text id="1s8vna"
{Notebook, Eraser}
```

New branch created.

```text id="k3d9wo"
NULL
 ├── Pen:2
 │     └── Notebook:2
 │            └── Eraser:1
 │
 └── Notebook:1
        └── Eraser:1
```

---

# Insert Transaction T4

Transaction:

```text id="x5q2nr"
{Pen}
```

Increase Pen count.

```text id="7g3mfp"
NULL
 ├── Pen:3
 │     └── Notebook:2
 │            └── Eraser:1
 │
 └── Notebook:1
        └── Eraser:1
```

---

# Insert Transaction T5

Transaction:

```text id="m6k1zp"
{Pen, Notebook, Eraser}
```

Increase counts along common path.

Final FP-Tree:

```text id="5v8qtn"
NULL
 ├── Pen:4
 │     └── Notebook:3
 │            └── Eraser:2
 │
 └── Notebook:1
        └── Eraser:1
```

---

# Step 4: Mine Frequent Patterns

Mining starts from least frequent item.

---

# Conditional Pattern Base for Eraser

Eraser appears in:

1.

```text id="4x2wje"
Pen → Notebook → Eraser : 2
```

2.

```text id="9q7kdm"
Notebook → Eraser : 1
```

Conditional Pattern Base:

```text id="r5k8av"
{
{Pen, Notebook : 2},
{Notebook : 1}
}
```

---

# Frequent Patterns with Eraser

| Frequent Pattern        | Support Count |
| ----------------------- | ------------- |
| {Eraser}                | 3             |
| {Notebook, Eraser}      | 3             |
| {Pen, Eraser}           | 2             |
| {Pen, Notebook, Eraser} | 2             |

---

# Conditional Pattern Base for Notebook

Notebook appears in:

```text id="7n4qsd"
Pen → Notebook : 3
Notebook : 1
```

Conditional Pattern Base:

```text id="2j8wfa"
{
{Pen : 3}
}
```

---

# Frequent Patterns with Notebook

| Frequent Pattern | Support Count |
| ---------------- | ------------- |
| {Notebook}       | 4             |
| {Pen, Notebook}  | 3             |

---

# Conditional Pattern Base for Pen

Pen appears alone with count 4.

Frequent Pattern:

| Frequent Pattern | Support Count |
| ---------------- | ------------- |
| {Pen}            | 4             |

---

# Final Frequent Itemsets

## Frequent 1-Itemsets

| Itemset    | Support Count |
| ---------- | ------------- |
| {Pen}      | 4             |
| {Notebook} | 4             |
| {Eraser}   | 3             |

---

## Frequent 2-Itemsets

| Itemset            | Support Count |
| ------------------ | ------------- |
| {Pen, Notebook}    | 3             |
| {Notebook, Eraser} | 3             |
| {Pen, Eraser}      | 2             |

---

## Frequent 3-Itemsets

| Itemset                 | Support Count |
| ----------------------- | ------------- |
| {Pen, Notebook, Eraser} | 2             |

---

# All Frequent Itemsets

```text id="2m7xqa"
{
{Pen},
{Notebook},
{Eraser},
{Pen, Notebook},
{Notebook, Eraser},
{Pen, Eraser},
{Pen, Notebook, Eraser}
}
```

---

# Conclusion

Using the FP-Growth algorithm, the transaction database is compressed into an FP-tree and frequent itemsets are mined without candidate generation. With minimum support count 2, the frequent itemsets obtained are:

```text id="6w3jke"
{Pen},
{Notebook},
{Eraser},
{Pen, Notebook},
{Notebook, Eraser},
{Pen, Eraser},
{Pen, Notebook, Eraser}
```

The FP-Growth algorithm efficiently discovers frequent patterns with fewer database scans and better performance compared to Apriori.
